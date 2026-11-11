---

# CONSISTENT LANGUAGE & SYNTAX

## CANONICAL LANGUAGE ENFORCEMENT SKILL

### 1. PRIMARY OBJECTIVE

Ensure that all generated content, documentation, scripts, code, interfaces, and technical communications maintain consistent language and syntax.

The objective is not simply to write correctly.

The objective is to establish a canonical language standard and consistently reuse it.

Once a convention has been established, do not introduce unnecessary alternatives.

### 2. CORE PRINCIPLES

**2.1 — Terminology Consistency**

- Use the same word for the same concept.
    
- Do not alternate between synonyms without a semantic reason.
    
- Preserve established technical terminology.
    
- Do not rename established components, variables, classes, methods, or modules arbitrarily.
    
- Reuse the user's existing vocabulary when it is technically correct.
    
- Maintain consistent terminology across documentation, logs, UI labels, and source code.
    

**2.2 — Language Consistency**

- Detect the language selected for the current task.
    
- Maintain that language throughout the deliverable.
    
- Do not randomly switch between English and Spanish.
    
- Preserve technical terms in their original language when appropriate.
    
- Maintain consistent spelling, grammar, capitalization, and punctuation.
    
- Use one language convention consistently within the same document or interface.
    

**2.3 — Syntax Consistency**

- Use established grammatical and structural patterns.
    
- Maintain consistent sentence construction.
    
- Maintain consistent formatting and punctuation.
    
- Avoid unnecessary stylistic variations.
    
- Follow the existing project's syntax conventions whenever available.
    

### 3. PROGRAMMING LANGUAGE ENFORCEMENT

Programming languages must be treated independently.

Never assume that conventions from one programming language should be transferred directly to another.

For each programming language:

1. Identify the language and version.
    
2. Identify the established project conventions.
    
3. Identify existing naming conventions.
    
4. Identify established functions, methods, classes, and APIs.
    
5. Reuse existing implementation patterns whenever appropriate.
    
6. Introduce new patterns only when technically necessary.
    

#### 3.1 — Python

Canonical defaults:

- Variables: `snake_case`
    
- Functions: `snake_case`
    
- Classes: `PascalCase`
    
- Constants: `UPPER_SNAKE_CASE`
    
- Modules: `snake_case.py`
    
- Private members: `_leading_underscore`
    
- Imports: Standard library, third-party, local modules.
    
- Prefer dependency injection over unnecessary global dependencies.
    
- Prefer explicit resource management and predictable error handling.
    

Example:

```
def process_email(email_record):
    received_at = email_record.received_at
    return received_at


class EmailProcessor:
    def process_email(self, email_record):
        return process_email(email_record)
```

Do not alternate between `process_email`, `handle_email`, and `execute_email` when they represent the same operation without a meaningful distinction.

#### 3.2 — Java

Canonical defaults:

- Variables: `camelCase`
    
- Methods: `camelCase`
    
- Classes: `PascalCase`
    
- Interfaces: `PascalCase`
    
- Constants: `UPPER_SNAKE_CASE`
    
- Packages: lowercase
    
- Use established Java APIs and project conventions.
    
- Maintain consistent method signatures and exception handling.
    

Example:

```
public class EmailProcessor {

    public EmailRecord processEmail(EmailRecord emailRecord) {
        return emailRecord;
    }
}
```

Do not arbitrarily alternate between `processEmail()`, `handleEmail()`, and `executeEmail()` for identical responsibilities.

#### 3.3 — Other Programming Languages

Apply the equivalent canonical conventions for:

- JavaScript / TypeScript
    
- C / C++
    
- C#
    
- SQL
    
- PowerShell
    
- HTML / CSS
    
- JSON
    
- Other languages encountered.
    

Always prioritize the language's official conventions and the project's existing standards.

### 4. CANONICAL FUNCTION POLICY

Functions and methods must have stable responsibilities and names.

Before creating a function:

1. Check whether an equivalent function already exists.
    
2. Check its established name.
    
3. Check its parameters and return type.
    
4. Check its error-handling behavior.
    
5. Reuse it when appropriate.
    

Never create duplicate functions simply because another name sounds better.

Never change an established function signature without a technical justification.

When a change is necessary, identify its impact on existing callers.

### 5. CANONICAL TERMINOLOGY REGISTRY

Maintain an internal terminology registry for every substantial project.

Example:

|Concept|Canonical term|Avoid|
|---|---|---|
|Email processing|Email Processor|Mail Handler|
|Background execution|Worker|Runner|
|Application coordination|Supervisor|Controller|
|Error recording|Error Logger|Failure Writer|
|Configuration|Config|Settings / Preferences interchangeably|
|Database record|Record|Entry / Item interchangeably|

The registry must distinguish concepts that genuinely have different meanings.

Do not force different concepts into the same terminology.

### 6. PROJECT CONSISTENCY

When working with an existing project:

- Treat existing working conventions as the primary reference.
    
- Preserve module names and public interfaces.
    
- Preserve established architectural vocabulary.
    
- Reuse existing functions and utilities.
    
- Maintain consistent logging terminology.
    
- Maintain consistent UI labels.
    
- Maintain consistent configuration keys.
    
- Avoid introducing new naming systems unnecessarily.
    

When a project already has an established standard, do not create a competing standard.

### 7. CHANGE CONTROL

Any deviation from established conventions must have a reason.

Classify deviations as:

- NECESSARY: Required for correctness or compatibility.
    
- IMPROVEMENT: A demonstrable improvement to maintainability or clarity.
    
- COMPATIBILITY: Required by an external API or language specification.
    
- LEGACY: Preserved to avoid breaking existing integrations.
    

Never silently introduce a new convention.

### 8. CONSISTENCY VALIDATION

Before delivering an artifact, perform a consistency review.

Check:

**LANGUAGE**

- Is the language consistent?
    
- Are technical terms used consistently?
    
- Are there unnecessary language switches?
    

**TERMINOLOGY**

- Are identical concepts named identically?
    
- Are established project terms preserved?
    
- Are synonyms introducing ambiguity?
    

**PROGRAMMING**

- Are naming conventions consistent?
    
- Are equivalent operations using established functions?
    
- Are APIs and method signatures consistent?
    
- Are duplicate implementations unnecessary?
    

**STRUCTURE**

- Are headers, comments, logs, and sections consistent?
    
- Is formatting uniform?
    
- Are UI labels following the same terminology?
    

### 9. PRIORITY HIERARCHY

When standards conflict, follow this order:

1. Language and programming language specifications.
    
2. Existing project contracts and public interfaces.
    
3. Explicit user-defined conventions.
    
4. Established project terminology and patterns.
    
5. Official language and framework conventions.
    
6. This skill's canonical defaults.
    
7. Personal stylistic preferences.
    

Never sacrifice correctness merely to preserve superficial consistency.

### 10. FINAL ENFORCEMENT RULE

CONSISTENCY IS A REQUIREMENT, NOT A SUGGESTION.

Do not change terminology, syntax, function names, naming conventions, or communication patterns simply to create variety.

Use established conventions repeatedly.

Introduce variation only when there is a meaningful semantic, technical, compatibility, or readability reason.

The final output must feel as though it was written by one consistent author, following one coherent language standard and one coherent technical vocabulary.