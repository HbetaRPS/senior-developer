---

# ANALYSIS

## 1. PURPOSE

Establish a consistent analytical methodology for understanding a subject, identifying its actual objectives, examining available evidence, evaluating its current state, and producing reliable conclusions.

Analysis must establish **what is happening, what is intended, what is missing, and what needs to be achieved** before determining how to achieve it.

## 2. CORE PRINCIPLES

1. OBJECTIVE FIRST — Identify the intended outcome before examining implementation choices.
    
2. EVIDENCE BASED — Ground conclusions in available evidence.
    
3. IMPLEMENTATION INDEPENDENT — Do not confuse the existing implementation with the intended objective.
    
4. TRACEABILITY — Connect conclusions to their supporting evidence.
    
5. COMPLETENESS — Examine relevant dependencies, interactions, and failure conditions.
    
6. CONSISTENCY — Use established terminology, standards, and definitions.
    
7. TRANSPARENCY — Distinguish verified facts from assumptions and unknowns.
    
8. ACTIONABILITY — Produce conclusions that support informed decisions.
    

## 3. ANALYSIS PROCESS

### 3.1 SUBJECT IDENTIFICATION

Determine:

- What is being analyzed?
    
- What is its purpose?
    
- What context is relevant?
    
- What information is available?
    
- What is outside the scope?
    

### 3.2 OBJECTIVE EXTRACTION

Identify:

- Original user objective.
    
- Intended deliverables.
    
- Expected behavior.
    
- Desired results.
    
- Explicit requirements.
    
- Implied requirements.
    
- Constraints and exclusions.
    

Do not assume that the existing implementation accurately represents the original objective.

### 3.3 REQUIREMENT DECOMPOSITION

Organize requirements into:

- FUNCTIONAL — What must happen?
    
- OPERATIONAL — Under what conditions must it work?
    
- TECHNICAL — What constraints must be respected?
    
- STRUCTURAL — What components or relationships are necessary?
    
- QUALITY — What standards must the result satisfy?
    
- DELIVERY — What must actually be delivered?
    

### 3.4 EVIDENCE EXAMINATION

Inspect relevant evidence, including:

- Source files and scripts.
    
- Configuration files.
    
- Logs and execution traces.
    
- Documentation.
    
- Data structures.
    
- Dependencies.
    
- Existing workflows.
    
- Previous decisions.
    

Classify findings:

- VERIFIED — Directly supported by evidence.
    
- INFERRED — Supported by evidence but not explicitly confirmed.
    
- ASSUMED — Used provisionally without sufficient verification.
    
- UNKNOWN — Requires additional information.
    

### 3.5 CURRENT STATE ANALYSIS

Determine:

- What currently works?
    
- What does not work?
    
- What is partially implemented?
    
- What is missing?
    
- What is duplicated?
    
- What is unnecessarily complex?
    
- What dependencies exist?
    
- What constraints affect the result?
    

### 3.6 ROOT CAUSE ANALYSIS

When investigating problems:

1. Identify observable symptoms.
    
2. Locate the affected components.
    
3. Trace relevant execution paths.
    
4. Identify dependencies and interactions.
    
5. Determine the earliest demonstrable failure.
    
6. Separate root causes from secondary symptoms.
    
7. Identify contributing conditions.
    
8. Establish evidence supporting each conclusion.
    

Never declare a root cause solely from a plausible explanation.

### 3.7 OPTIONS EVALUATION

When alternatives exist, compare them using relevant criteria:

- Functional suitability.
    
- Complexity.
    
- Reliability.
    
- Compatibility.
    
- Maintainability.
    
- Performance.
    
- Dependencies.
    
- Operational risks.
    
- Implementation effort.
    

Distinguish objectively superior alternatives from subjective preferences.

### 3.8 RISK AND GAP IDENTIFICATION

Identify:

- Missing requirements.
    
- Unsupported assumptions.
    
- Technical limitations.
    
- Failure scenarios.
    
- Compatibility risks.
    
- Security considerations.
    
- Operational risks.
    
- Unverified dependencies.
    
- Differences between intended and current behavior.
    

### 3.9 VALIDATION CRITERIA

Define how conclusions or proposed solutions can be verified.

Validation criteria must be:

- Specific.
    
- Observable.
    
- Relevant to the original objective.
    
- Reproducible where possible.
    
- Independent of unsupported assumptions.
    

### 3.10 CONCLUSION

Produce a decision-ready conclusion containing:

- Main findings.
    
- Supporting evidence.
    
- Identified causes or gaps.
    
- Relevant risks.
    
- Available alternatives.
    
- Recommended direction, when justified.
    
- Remaining unknowns.
    
- Next actions.
    

## 4. ANALYSIS OUTPUT STANDARD

Use the following structure when appropriate:

1. OBJECTIVE — What must be achieved?
    
2. SCOPE — What is being examined?
    
3. REQUIREMENTS — What conditions must be satisfied?
    
4. EVIDENCE — What information supports the analysis?
    
5. CURRENT STATE — What exists today?
    
6. FINDINGS — What was discovered?
    
7. ROOT CAUSES — What explains the identified problems?
    
8. GAPS — What is missing?
    
9. RISKS — What could compromise the outcome?
    
10. OPTIONS — What alternatives exist?
    
11. RECOMMENDATION — What direction is justified?
    
12. VALIDATION — How will success be demonstrated?
    

Omit sections that are irrelevant rather than filling them with unnecessary content.

## 5. ANALYTICAL BOUNDARIES

ANALYSIS must not:

- Begin implementation without authorization.
    
- Replace the user's objective with a preferred technical solution.
    
- Assume missing requirements.
    
- Invent evidence.
    
- Confuse symptoms with causes.
    
- Recommend unnecessary architectural complexity.
    
- Treat successful initialization as proof of functional success.
    
- Claim testing or validation that was not performed.
    
- Introduce unrelated improvements into the scope.
    

When information is insufficient, identify the limitation and request only the information necessary to proceed.

## 6. RELATIONSHIP WITH OTHER SKILLS

ANALYSIS establishes the findings and reasoning that other skills may use.

- OBJECTIVE EXTRACTION — Determines intended outcomes and deliverables.
    
- CONSISTENT LANGUAGE & SYNTAX — Maintains terminology and language consistency.
    
- GENERAL USE STANDARD — Establishes common quality and operational conventions.
    
- DOCUMENTATION STANDARD — Governs documentation structure.
    
- VALIDATION & DELIVERY STANDARD — Governs verification and delivery.
    
- LOGGING & ERROR HANDLING STANDARD — Governs operational observability and error management.
    

ANALYSIS does not replace these standards.

## 7. FINAL RULE

**Understand before changing. Verify before concluding. Establish the objective before choosing the implementation.**

The quality of an analysis is determined by the accuracy, traceability, and usefulness of its conclusions — not by its length or complexity.