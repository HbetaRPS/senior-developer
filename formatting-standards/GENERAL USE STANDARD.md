# GENERAL USE STANDARD

# VERSION 1.0.0

## 1. PURPOSE

Establish a simple, universal standard for organizing, identifying, documenting, validating, and delivering work.

This standard applies to:

- Scripts and software.
    
- Skills and instructions.
    
- User interfaces.
    
- Documentation.
    
- Reports and technical deliverables.
    
- Applications and project components.
    

Its purpose is to maintain consistency, clarity, reliability, and continuity across all projects.

## 2. NAMING & NOMENCLATURE

Maintain consistent and descriptive names across all project components.

Rules:

- Use clear, meaningful identifiers.
    
- Preserve established project terminology.
    
- Avoid unnecessary abbreviations.
    
- Avoid multiple names for the same concept.
    
- Keep filenames, modules, functions, classes, and components logically related.
    
- Preserve existing naming conventions unless a change is necessary.
    

## 3. STRUCTURE & ORGANIZATION

Organize every deliverable according to its function.

Rules:

- Separate unrelated responsibilities.
    
- Group related components.
    
- Avoid unnecessary complexity.
    
- Reuse existing structures when appropriate.
    
- Keep dependencies explicit.
    
- Maintain predictable organization.
    
- Avoid unnecessary duplication.
    

## 4. UI & DESIGN

Maintain a consistent visual and interaction identity.

Rules:

- Reuse established design systems.
    
- Maintain consistent typography, colors, spacing, and alignment.
    
- Use predictable component behavior.
    
- Keep visual hierarchy clear.
    
- Maintain consistent interaction states.
    
- Preserve existing interface conventions.
    

Do not introduce a new visual identity without authorization.

## 5. DOCUMENTATION

Document information necessary to understand, operate, maintain, and troubleshoot a deliverable.

When applicable, identify:

- Purpose.
    
- Requirements.
    
- Dependencies.
    
- Configuration.
    
- Execution instructions.
    
- Component responsibilities.
    
- Limitations.
    
- Known issues.
    

Keep documentation accurate and synchronized with the implementation.

Avoid documenting behavior that has not been verified.

## 6. LOGGING & ERROR HANDLING

Make important operations observable and failures diagnosable.

Rules:

- Use consistent logging levels.
    
- Identify the component generating each event.
    
- Record important execution stages.
    
- Capture relevant error context.
    
- Preserve traceback information when appropriate.
    
- Distinguish warnings from failures.
    
- Avoid silently suppressing exceptions.
    
- Never report success after a failed operation.
    
- Never expose credentials or sensitive information in logs.
    

Use appropriate recovery and retry mechanisms when applicable.

## 7. VALIDATION & QUALITY CONTROL

Validate deliverables before declaring them complete.

Apply relevant checks according to the type of work:

- Structural integrity.
    
- Naming consistency.
    
- Dependency compatibility.
    
- Configuration correctness.
    
- Syntax and reference validity.
    
- Functional behavior.
    
- Runtime behavior.
    
- Error handling.
    
- Output integrity.
    

Do not perform irrelevant validation merely to satisfy a checklist.

Only report tests that were actually executed.

## 8. DELIVERY STANDARD

Deliver complete, usable, and clearly identified results.

Every delivery should establish, when applicable:

- What was produced.
    
- Which version was delivered.
    
- What changed.
    
- What was verified.
    
- What remains pending.
    
- What limitations exist.
    
- How to use or execute the result.
    

Prefer complete deliverables over fragmented instructions when a complete implementation is requested.

Never claim that an operation, modification, or test succeeded without confirmation.

## 9. CONTINUITY & REUSE

Preserve established project decisions and conventions.

Rules:

- Reuse approved components and structures.
    
- Preserve compatible existing functionality.
    
- Avoid unnecessary redesigns.
    
- Avoid unnecessary renaming.
    
- Maintain compatibility with existing project architecture.
    
- Introduce changes only when they provide a clear benefit or are explicitly requested.
    

When changing an established convention, identify the reason and scope of the change.

## 10. PRIORITY & EXCEPTIONS

Apply the following priority:

1. Explicit instructions in the current request.
    
2. User-approved project standards.
    
3. Existing project architecture and conventions.
    
4. Specialized formatting and implementation standards.
    
5. GENERAL USE STANDARD defaults.
    

A specialized standard takes precedence over a general rule within its specific domain.

Do not force a convention when technical requirements make it unsuitable.

## 11. FINAL QUALITY CHECK

Before delivering substantial work, verify:

[ ] Correct naming and identification.  
[ ] Logical organization.  
[ ] Consistent visual identity where applicable.  
[ ] Sufficient documentation.  
[ ] Appropriate logging and error handling.  
[ ] Relevant validation performed.  
[ ] Complete and accurate delivery.  
[ ] Existing conventions preserved.  
[ ] Limitations and pending work identified.  
[ ] No unsupported claims of success.

## 12. FINAL DIRECTIVE

CONSISTENCY ACROSS PROJECTS.

CLARITY IN EVERY COMPONENT.

REUSE BEFORE DUPLICATION.

VALIDATION BEFORE DELIVERY.

PRESERVE ESTABLISHED CONVENTIONS.

Apply this standard to all general-purpose work unless a more specific instruction or specialized standard takes precedence.

END OF STANDARD.