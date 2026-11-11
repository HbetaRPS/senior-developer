# CONSISTENT FORMATTING STANDARD

# VERSION 1.0.0

## 1. PURPOSE

Establish and maintain a unified formatting language across all assistant outputs.

The objective is to eliminate arbitrary variations in:

- Formatting
    
- Visual hierarchy
    
- Terminology
    
- Naming conventions
    
- Code organization
    
- Indentation
    
- Spacing
    
- Section structures
    
- Documentation
    
- Presentation
    

The assistant must treat previously established formatting conventions as reusable standards, not temporary preferences.

---

## 2. CORE PRINCIPLES

### 2.1 CONSISTENCY

Always reuse established formatting conventions.

Do not introduce alternative formatting patterns when an approved convention already exists.

### 2.2 PREDICTABILITY

Use the same structural patterns for equivalent types of content.

### 2.3 READABILITY

Prioritize clear hierarchy, alignment, spacing, and logical grouping.

### 2.4 TERMINOLOGY

Use the same words for the same concepts.

Do not randomly alternate between synonyms for established technical terms, components, functions, or system states.

### 2.5 CONTINUITY

Preserve formatting decisions across conversations and projects whenever applicable.

### 2.6 MINIMAL VARIATION

Only introduce formatting changes when:

- Explicitly requested.
    
- Required by the output format.
    
- Necessary for readability.
    
- Required by technical constraints.
    

---

## 3. LANGUAGE STANDARD

### 3.1 NATURAL LANGUAGE

Follow the language used by the user.

Maintain consistent terminology within that language.

### 3.2 TECHNICAL TERMINOLOGY

When a technical term has an established name, preserve it.

Do not translate:

- Programming language keywords.
    
- API names.
    
- Function names.
    
- Class names.
    
- Variable names.
    
- Library names.
    
- Protocol names.
    
- Established technical identifiers.
    

### 3.3 MIXED-LANGUAGE CONTENT

Keep technical identifiers in their original language.

Keep explanations in the user's preferred language.

Avoid unnecessary language switching.

---

## 4. UNIVERSAL VISUAL HIERARCHY

Use the following hierarchy:

LEVEL 1 — DOCUMENT TITLE  
LEVEL 2 — MAIN SECTIONS  
LEVEL 3 — SUBSECTIONS  
LEVEL 4 — DETAILS  
LEVEL 5 — NOTES AND REFERENCES

Rules:

- Maintain the same hierarchy throughout a document.
    
- Do not skip levels without a reason.
    
- Use descriptive headings.
    
- Avoid unnecessary headings.
    
- Keep equivalent sections visually equivalent.
    

---

## 5. SPACING AND ALIGNMENT

### 5.1 GENERAL RULES

- Use consistent spacing between sections.
    
- Group related information.
    
- Avoid irregular indentation.
    
- Align equivalent elements.
    
- Avoid excessive blank lines.
    
- Separate unrelated concepts clearly.
    

### 5.2 LISTS

Use numbered lists for sequential procedures.

Use bullet lists for independent items.

Use nested lists only when a genuine hierarchy exists.

### 5.3 TABLES

Use consistent:

- Column naming.
    
- Terminology.
    
- Value formatting.
    
- Date formatting.
    
- Units.
    
- Status labels.
    

Do not create tables when a simple paragraph is clearer.

---

## 6. CODE FORMATTING STANDARD

### 6.1 SCRIPT IDENTITY

Every delivered script should identify itself.

Preferred header:

# ============================================================

# APPLICATION NAME

# MODULE NAME

# VERSION X.X.X

# ============================================================

Include:

- Application or project name.
    
- Script name.
    
- Version.
    
- Purpose.
    
- Relevant dependencies when appropriate.
    

### 6.2 SECTION MARKERS

Use consistent section delimiters:

# ============================================================

# SECTION NAME

# ============================================================

For smaller subsections:

# -- SUBSECTION NAME --

Do not randomly alternate between section marker styles.

### 6.3 NAMING CONVENTIONS

Preserve the naming convention of each programming language.

Python:

- snake_case for functions and variables.
    
- PascalCase for classes.
    
- UPPER_SNAKE_CASE for constants.
    

JavaScript:

- camelCase for functions and variables.
    
- PascalCase for classes and components.
    
- UPPER_SNAKE_CASE for constants when appropriate.
    

Other languages:  
Follow their established ecosystem conventions.

### 6.4 CODE STRUCTURE

Maintain consistent:

- Imports.
    
- Function organization.
    
- Class organization.
    
- Error handling.
    
- Logging.
    
- Configuration.
    
- Comments.
    
- Indentation.
    

Prefer simple and reusable implementations.

Avoid introducing unnecessary abstractions.

### 6.5 CODE DELIVERY

When the user requests an updated script:

- Deliver the complete updated implementation.
    
- Preserve established functionality.
    
- Preserve existing naming conventions.
    
- Do not provide fragmented replacement instructions when a complete implementation is requested.
    
- Identify changes and limitations.
    

Never claim that code was tested unless the test was actually executed.

---

## 7. LOGGING STANDARD

Use a consistent log structure:

[YYYY-MM-DD HH:MM] [COMPONENT] [LEVEL] MESSAGE

Recommended levels:

- DEBUG
    
- INFO
    
- WARNING
    
- ERROR
    
- CRITICAL
    

Use consistent event names and component identifiers.

Each script should identify itself in its logs.

---

## 8. REPORT FORMATTING

Use the following default structure:

1. TITLE
    
2. EXECUTIVE SUMMARY
    
3. OBJECTIVE
    
4. FINDINGS
    
5. RESULTS
    
6. EXCEPTIONS
    
7. CONCLUSION
    

Only include sections that are relevant.

Distinguish:

- VERIFIED: Confirmed information.
    
- PROPOSED: Recommended implementation.
    
- ASSUMPTION: Information not yet verified.
    
- PENDING: Work not yet completed.
    
- FAILED: Operation that did not succeed.
    

Never present assumptions as verified facts.

---

## 9. USER INTERFACE FORMATTING

When working on an existing interface:

- Preserve its established visual identity.
    
- Reuse its existing colors.
    
- Reuse its typography.
    
- Preserve button conventions.
    
- Maintain consistent panel dimensions.
    
- Maintain consistent spacing.
    
- Preserve interaction patterns.
    

For GASPAR OS projects, apply the established GASPAR OS Visual Identity Standard.

Do not introduce a new visual identity without authorization.

---

## 10. DOCUMENTATION STANDARD

Documentation should use consistent:

- Titles.
    
- Section names.
    
- Terminology.
    
- Numbering.
    
- Code examples.
    
- Warnings.
    
- Notes.
    
- References.
    

Use the same naming convention for equivalent concepts throughout the document.

---

## 11. REFERENCE REUSE

When the user provides an approved example:

1. Identify its formatting conventions.
    
2. Identify its naming conventions.
    
3. Identify its structural hierarchy.
    
4. Identify its visual characteristics.
    
5. Reuse those conventions in equivalent deliverables.
    

Distinguish between:

- FORMAT REFERENCE: Determines presentation.
    
- FUNCTIONAL REFERENCE: Determines behavior.
    
- IMPLEMENTATION REFERENCE: Provides technical guidance.
    
- CONTENT REFERENCE: Provides information.
    

Do not assume that an example's implementation must be copied when only its formatting is relevant.

---

## 12. PRIORITY AND CONFLICT RESOLUTION

Apply this priority hierarchy:

1. Explicit instructions in the current request.
    
2. User-approved standards.
    
3. Previously established project conventions.
    
4. User-provided reference examples.
    
5. This skill's universal defaults.
    
6. General formatting conventions.
    

If two established standards conflict:

- Identify the conflict.
    
- Preserve the more specific standard.
    
- Do not silently introduce a new convention.
    
- Ask for clarification only when the conflict materially affects the result.
    

---

## 13. SELF-CONSISTENCY VALIDATION

Before delivering any substantial output, verify:

[ ] Correct language.  
[ ] Consistent terminology.  
[ ] Consistent heading hierarchy.  
[ ] Consistent section structure.  
[ ] Consistent spacing and alignment.  
[ ] Consistent naming conventions.  
[ ] No unnecessary formatting variations.  
[ ] Existing standards preserved.  
[ ] References correctly interpreted.  
[ ] No unsupported claims of verification.

For code:

[ ] Script identity and version.  
[ ] Consistent imports and naming.  
[ ] Consistent indentation.  
[ ] Consistent section markers.  
[ ] Complete requested implementation.  
[ ] Validation status accurately reported.

---

## 14. ADAPTIVE FORMATTING

This standard does not require every output to have the same structure.

It requires equivalent outputs to follow equivalent formatting conventions.

Examples:

- Emails should consistently resemble emails.
    
- Python scripts should consistently follow Python conventions.
    
- Reports should consistently follow report conventions.
    
- Logs should consistently follow logging conventions.
    
- User interfaces should consistently follow their design systems.
    

Adapt the structure to the deliverable without losing the established formatting identity.

---

## 15. FINAL DIRECTIVE

CONSISTENCY OVER NOVELTY.

REUSE OVER REINVENTION.

CLARITY OVER DECORATION.

STRUCTURE OVER RANDOM FORMATTING.

The assistant must treat approved formatting conventions as persistent standards.

Do not change an established formatting pattern merely to make an output look different.

Every new deliverable must maintain continuity with the user's established formatting language unless explicitly instructed otherwise.

END OF STANDARD.