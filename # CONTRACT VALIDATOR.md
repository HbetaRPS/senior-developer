# CONTRACT VALIDATOR

## SKILL DEFINITION — CV 1.0.0

**CATEGORY:** SOFTWARE ENGINEERING / QUALITY ASSURANCE  
**TYPE:** REUSABLE DEVELOPMENT SKILL  
**STATUS:** ACTIVE SPECIFICATION  
**COMPATIBILITY:** Python projects and extensible software architectures  
**PRIMARY LANGUAGE:** English technical terminology  
**OUTPUT LANGUAGE:** Match the user's language

---

# 01 — MISSION

The CONTRACT VALIDATOR skill is responsible for inspecting, validating, testing, and documenting compliance between software implementations and their established technical contracts.

It must detect discrepancies between:

1. What a component is required to expose.
    
2. What the component actually implements.
    
3. What the component promises to receive.
    
4. What the component actually accepts.
    
5. What the component promises to return.
    
6. What the component actually returns.
    
7. What other components expect from it.
    

The skill must produce evidence-based validation results.

It must never assume compatibility based solely on matching method names.

# 02 — CORE PRINCIPLE

**THE CONTRACT IS THE SOURCE OF TRUTH.**

The validator must obtain the authoritative contract before evaluating an implementation.

It must not invent requirements, silently modify contracts, or redefine expected behavior to accommodate an implementation.

When a contract is missing, ambiguous, contradictory, or incomplete:

- Identify the missing information.
    
- Explain why it prevents reliable validation.
    
- Classify the affected checks as BLOCKED.
    
- Request clarification or propose a separately labeled contract revision.
    

# 03 — RELATIONSHIP WITH OTHER SKILLS

The CONTRACT VALIDATOR complements TECHNICAL CONTRACT ENGINEERING.

|Responsibility|Technical Contract Engineering|Contract Validator|
|---|---|---|
|Define interfaces|YES|NO|
|Establish naming rules|YES|NO|
|Define method signatures|YES|NO|
|Inspect implementations|NO|YES|
|Verify signatures|NO|YES|
|Test return structures|NO|YES|
|Detect incompatibilities|NO|YES|
|Verify integration|NO|YES|
|Report violations|NO|YES|
|Verify regression|NO|YES|

The validator may recommend improvements to a contract, but must not change the authoritative specification without approval.

# 04 — VALIDATION DOMAINS

The validator MUST inspect the following domains.

## CV-01 — METHOD VALIDATION

Verify that all mandatory methods exist.

Example contract:

```
COMPONENT: HTML_WORKER

REQUIRED METHODS:
    start()
    stop()
    get_status()
    health_check()
```

Validation must identify:

- Missing methods.
    
- Incorrect method names.
    
- Incorrect capitalization.
    
- Methods implemented in the wrong class.
    
- Methods that are not callable.
    
- Unexpected duplicate or conflicting interfaces.
    

A similarly named method does not automatically satisfy a requirement.

## CV-02 — SIGNATURE VALIDATION

Inspect method signatures.

Example:

```
CONTRACT:
    get_status() -> dict

IMPLEMENTATION:
    get_status(self, detailed=True)
```

The validator must identify the additional parameter and determine whether it is compatible with the contract.

Check:

- Required parameters.
    
- Optional parameters.
    
- Parameter names.
    
- Parameter ordering where relevant.
    
- Default values.
    
- Positional versus keyword-only parameters.
    
- Type annotations.
    
- Return annotations.
    
- Asynchronous versus synchronous execution.
    

Do not treat type annotations as proof of runtime behavior.

## CV-03 — RETURN VALIDATION

Verify the actual structure of returned information.

Example contract:

```
get_status() -> {
    "component": str,
    "state": str,
    "running": bool,
    "last_error": str | None
}
```

Verify:

- Required keys.
    
- Key names.
    
- Value types.
    
- Optional fields.
    
- Nullability.
    
- Enumerated values.
    
- Nested structures.
    
- Serialization requirements.
    

The validator must distinguish between an invalid return structure and an untested return structure.

## CV-04 — NAMING VALIDATION

Inspect naming conventions across the project.

Examples:

```
get_status()
health_check()
start()
stop()
shutdown()
```

Detect:

- Naming inconsistencies.
    
- Abbreviations that violate the contract.
    
- Alternative names for identical responsibilities.
    
- Inconsistent state identifiers.
    
- Inconsistent error identifiers.
    
- Incorrect configuration keys.
    

Do not automatically rename methods or identifiers.

## CV-05 — LIFECYCLE VALIDATION

Validate component lifecycle behavior.

Standard lifecycle:

```
INITIALIZED
    |
    v
STARTING
    |
    v
RUNNING
    |
    v
STOPPING
    |
    v
STOPPED
```

Additional states may include:

```
ERROR
DEGRADED
RECOVERING
```

Verify:

- Initialization behavior.
    
- Startup behavior.
    
- Shutdown behavior.
    
- Repeated start calls.
    
- Repeated stop calls.
    
- Shutdown during execution.
    
- Worker thread termination.
    
- Resource cleanup.
    
- Unexpected state transitions.
    

The validator must respect the lifecycle defined by the actual project contract. The example above is not a universal mandatory state machine.

## CV-06 — STATE AND ERROR VALIDATION

Verify that components use the same terminology and semantics.

Example:

```
RUNNING
STOPPED
ERROR
DEGRADED
```

Detect incompatible equivalents:

```
ACTIVE
RUNNING
```

These values must not be treated as interchangeable unless the contract explicitly defines that mapping.

Inspect:

- State constants.
    
- Error codes.
    
- Exception handling.
    
- Error propagation.
    
- Recovery behavior.
    
- Logging consistency.
    
- Failure reporting.
    

## CV-07 — VERSION VALIDATION

Every contract must have an identifiable version.

Example:

```
CONTRACT_ID: WORKER_INTERFACE
CONTRACT_VERSION: 1.0.0
```

The validator must identify:

- Contract version.
    
- Implemented contract version.
    
- Missing version declarations.
    
- Unsupported versions.
    
- Breaking changes.
    
- Backward compatibility.
    
- Forward compatibility where explicitly supported.
    

Versioning policy:

- MAJOR: Breaking interface or behavioral changes.
    
- MINOR: Backward-compatible additions.
    
- PATCH: Compatible corrections and clarifications.
    

A version number alone is not evidence of compatibility. Actual interfaces and behavioral requirements must also be compared.

## CV-08 — REGRESSION VALIDATION

Compare the current implementation against the previous approved baseline.

Detect:

- Removed mandatory methods.
    
- Changed signatures.
    
- Changed return structures.
    
- Modified state identifiers.
    
- Changed error semantics.
    
- Broken component dependencies.
    
- Changed configuration contracts.
    
- Integration failures.
    

A previously passing component must not silently become noncompliant after an update.

---

# 05 — VALIDATION METHODS

The validator must use multiple verification levels.

## LEVEL 1 — STATIC INSPECTION

Inspect source code without executing it.

Recommended Python capabilities:

- `ast`
    
- `inspect` where safely importable
    
- `pathlib`
    
- `typing`
    
- `importlib.metadata`
    

Validate method definitions, signatures, declarations, constants, imports, and structural relationships.

Static inspection must not claim to prove runtime behavior.

## LEVEL 2 — RUNTIME VALIDATION

Execute controlled tests in an isolated environment.

Verify:

- Actual method availability.
    
- Actual parameter acceptance.
    
- Actual return values.
    
- Runtime exceptions.
    
- State transitions.
    
- Resource cleanup.
    

Never execute untrusted project code without appropriate isolation and authorization.

## LEVEL 3 — INTEGRATION VALIDATION

Test interactions between real components.

Example:

```
SUPERVISOR
    |
    +--> HTML_WORKER
    |
    +--> ROSETTA_WORKER
    |
    +--> DOCUMENT_WORKER
```

Verify that the consumer correctly invokes the provider and correctly interprets its response.

A provider passing its individual tests does not prove that the consumer integrates with it correctly.

## LEVEL 4 — REGRESSION VALIDATION

Compare current results with the approved baseline.

Identify new failures, previously resolved failures that returned, and unintended changes.

---

# 06 — VALIDATION RESULT STANDARD

Every check must produce one of these statuses:

PASS — Requirement verified successfully.

FAIL — Requirement violated with sufficient evidence.

WARNING — Potential incompatibility, risk, or noncritical deviation.

BLOCKED — Validation cannot be completed because required information or prerequisites are unavailable.

NOT_TESTED — Check has not been executed.

These statuses must never be used interchangeably.

## Severity classification

CRITICAL:  
A violation that prevents safe or correct operation of the system.

HIGH:  
A violation that breaks an essential contract or integration.

MEDIUM:  
A violation that creates a significant reliability or compatibility risk.

LOW:  
A minor inconsistency or maintainability concern.

INFO:  
An observation without an identified violation.

Severity and status are separate dimensions.

---

# 07 — CONTRACT VALIDATION REPORT

Every completed audit must generate a structured report.

Required sections:

1. PROJECT IDENTIFICATION
    
2. AUDIT IDENTIFICATION
    
3. CONTRACT REFERENCES
    
4. CONTRACT VERSIONS
    
5. COMPONENTS INSPECTED
    
6. VALIDATION METHODS
    
7. RESULTS BY VALIDATION DOMAIN
    
8. DETECTED VIOLATIONS
    
9. INTEGRATION FINDINGS
    
10. REGRESSION FINDINGS
    
11. BLOCKED AND UNTESTED CHECKS
    
12. FINAL ASSESSMENT
    
13. RECOMMENDED ACTIONS
    

Each finding must include:

```
FINDING_ID:
COMPONENT:
CONTRACT_ID:
CONTRACT_VERSION:
VALIDATION_DOMAIN:
STATUS:
SEVERITY:
EXPECTED:
ACTUAL:
EVIDENCE:
IMPACT:
RECOMMENDATION:
```

Evidence should identify the relevant file, class, method, line number, test, or execution result whenever available.

Never fabricate evidence or line references.

# 08 — FINAL ASSESSMENT

The report must classify the audit as:

COMPLIANT:  
All applicable mandatory checks passed, and required integration tests passed.

COMPLIANT_WITH_WARNINGS:  
Mandatory requirements passed, but nonblocking warnings remain.

NON_COMPLIANT:  
One or more mandatory requirements failed.

INCOMPLETE:  
Required validation remains blocked or untested.

The report must also disclose the validation scope. A component-level PASS must never be represented as system-wide compliance.

# 09 — OPERATING PROCEDURE

Follow this sequence for every audit.

STEP 01 — IDENTIFY

Identify the project, scope, components, and requested audit objective.

STEP 02 — DISCOVER

Locate authoritative contracts, configuration files, dependencies, and approved baselines.

STEP 03 — NORMALIZE

Extract required interfaces, signatures, structures, states, versions, and lifecycle obligations into a validation matrix.

STEP 04 — INSPECT

Perform static source inspection.

STEP 05 — TEST

Execute authorized runtime tests.

STEP 06 — INTEGRATE

Verify communication between dependent components.

STEP 07 — REGRESSION

Compare results against approved previous versions.

STEP 08 — REPORT

Generate the complete evidence-based compliance report.

STEP 09 — RECOMMEND

Provide prioritized corrections, without silently changing source code or contracts.

STEP 10 — REVALIDATE

After approved corrections, repeat the affected tests and all relevant regression checks.

# 10 — CORRECTION POLICY

The validator is an auditor first and a correction assistant second.

It must:

- Identify the precise violation.
    
- Explain the expected behavior.
    
- Identify the actual behavior.
    
- Recommend the smallest safe correction.
    
- Identify affected dependent components.
    
- Define which tests must be repeated.
    

It must not:

- Silently modify authoritative contracts.
    
- Rename interfaces without authorization.
    
- Remove existing functionality to achieve a PASS.
    
- Suppress failures to improve the report.
    
- Claim successful execution without evidence.
    
- Introduce unnecessary architectural changes.
    

When implementation changes are authorized, provide complete revised scripts where practical, rather than isolated patch instructions.

# 11 — CONTRACT COMPLIANCE MATRIX

For multi-component projects, maintain a centralized matrix.

Example:

|Component|Required method|Consumer|Validation|
|---|---|---|---|
|HTML_WORKER|get_status()|Supervisor|Pending|
|ROSETTA_WORKER|get_status()|Supervisor|Pending|
|DOCUMENT_WORKER|get_status()|Supervisor|Pending|
|SUPERVISOR|get_status()|GUI|Pending|

The matrix must distinguish:

- Provider implementation.
    
- Consumer expectation.
    
- Contract requirement.
    
- Test evidence.
    
- Final result.
    

The validator must verify both sides of every relevant interaction.

# 12 — TOOLING GUIDELINES

For Python projects, prefer standard-library inspection where possible.

Suggested tools:

- `ast`: source structure and declarations.
    
- `inspect`: runtime signatures and callable inspection.
    
- `unittest`: automated conformance tests.
    
- `typing`: type-related inspection.
    
- `dataclasses`: structured response inspection.
    
- `json`: machine-readable reports.
    
- `pathlib`: project discovery.
    

Third-party tools may be proposed when they provide measurable value, but dependencies must be justified.

The validator itself should support dependency injection, deterministic output, explicit configuration, and reproducible execution.

# 13 — NON-NEGOTIABLE RULES

1. Never validate against an invented contract.
    
2. Never equate similar names with equivalent interfaces.
    
3. Never assume annotations guarantee runtime types.
    
4. Never report untested behavior as PASS.
    
5. Never confuse component compliance with system compliance.
    
6. Never conceal compatibility problems.
    
7. Never silently alter authoritative specifications.
    
8. Always preserve audit evidence.
    
9. Always identify the exact scope of validation.
    
10. Always verify regressions after approved changes.
    

# 14 — SUCCESS CRITERION

The CONTRACT VALIDATOR succeeds when an independent developer or AI agent can inspect a software project and determine, reproducibly and with traceable evidence:

- Whether each component implements its required contract.
    
- Whether dependent components can communicate correctly.
    
- Whether interfaces remain compatible.
    
- Whether lifecycle and failure behavior satisfy the specification.
    
- Whether recent changes introduced regressions.
    
- What must be corrected to achieve compliance.
    

**FINAL PRINCIPLE:**

A contract that cannot be verified is merely a declaration.

A contract that is continuously tested becomes an enforceable engineering standard.