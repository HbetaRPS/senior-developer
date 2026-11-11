# SKILL MARKDOWN FORMATTING STANDARD

# VERSION 1.0.0

## 1. PURPOSE

Define a universal structure and formatting convention for all SKILL.md files.

Every skill must be:

- Predictably structured.
    
- Easy to interpret.
    
- Independently understandable.
    
- Operationally precise.
    
- Consistent in terminology.
    
- Free from unnecessary repetition.
    

## 2. FILE NAMING

Canonical filename:

SKILL.md

Directory naming:

skill-name/  
SKILL.md  
references/  
examples/  
scripts/

Rules:

- Use lowercase directory names.
    
- Separate words with hyphens.
    
- Use SKILL.md as the main instruction file.
    
- Use supporting files only when necessary.
    
- Avoid duplicate instructions across files.
    

## 3. METADATA STANDARD

When the skill platform requires YAML frontmatter, use:

---

Rules:

- Use a stable skill identifier.
    
- Use a concise, operational description.
    
- Do not include unnecessary metadata.
    
- Do not add frontmatter when the target platform does not support or require it.
    

## 4. DOCUMENT HIERARCHY

Use this exact default section sequence:

# SKILL NAME

# VERSION X.X.X

## 1. PURPOSE

## 2. SCOPE

## 3. ACTIVATION CONDITIONS

## 4. CORE PRINCIPLES

## 5. INPUT REQUIREMENTS

## 6. EXECUTION WORKFLOW

## 7. OPERATIONAL RULES

## 8. OUTPUT STANDARD

## 9. EXCEPTIONS AND CONFLICTS

## 10. VALIDATION CHECKLIST

## 11. EXAMPLES

## 12. FINAL DIRECTIVE

Only include sections that are relevant to the skill.

Do not create empty sections.

## 5. HEADING CONVENTIONS

Use:

- H1 (#) for the skill title.
    
- H2 (##) for primary sections.
    
- H3 (###) for subsections.
    
- H4 (####) only for necessary nested details.
    

Rules:

- Number primary sections sequentially.
    
- Use descriptive uppercase section titles.
    
- Maintain consistent heading depth.
    
- Never use headings merely for decoration.
    

## 6. WRITING CONVENTIONS

Use:

- Direct instructions.
    
- Imperative language.
    
- Short, precise paragraphs.
    
- Consistent terminology.
    
- Explicit conditions.
    
- Explicit expected behavior.
    

Preferred:

ALWAYS:  
Perform the required validation before delivery.

NEVER:  
Claim that validation succeeded without executing it.

AVOID:  
Vague instructions such as "make it better" or "handle appropriately."

## 7. RULE CLASSIFICATION

Use consistent rule terminology:

MUST:  
Mandatory behavior.

MUST NOT:  
Prohibited behavior.

SHOULD:  
Strong recommendation.

SHOULD NOT:  
Discouraged behavior.

MAY:  
Optional behavior.

Use these terms consistently throughout the document.

## 8. LISTS AND PROCEDURES

Use numbered lists for:

- Execution sequences.
    
- Workflows.
    
- Ordered procedures.
    
- Priority hierarchies.
    

Use bullet lists for:

- Independent requirements.
    
- Characteristics.
    
- Alternatives.
    
- Examples.
    

Use nested lists only when necessary.

## 9. CODE AND TECHNICAL REFERENCES

All code examples must:

- Use the correct language identifier.
    
- Follow that language's conventions.
    
- Be syntactically coherent.
    
- Use consistent naming.
    
- Avoid unexplained placeholders.
    

Use fenced code blocks with language identifiers.

Example:

```
def main():
    return 0


if __name__ == "__main__":
    raise SystemExit(main())
```

Keep technical identifiers unchanged.

## 10. SKILL RESPONSIBILITY

Each skill must have a clearly defined responsibility.

A skill SHOULD specify:

- What it does.
    
- When it activates.
    
- What information it requires.
    
- What operations it performs.
    
- What it must not do.
    
- What it produces.
    
- How completion is validated.
    

Avoid combining unrelated responsibilities into one skill.

## 11. EXECUTION WORKFLOW

When applicable, define an explicit workflow:

1. IDENTIFY
    
2. INSPECT
    
3. ANALYZE
    
4. EXECUTE
    
5. VALIDATE
    
6. DELIVER
    

Each stage must specify its expected result when the sequence is operationally significant.

## 12. OUTPUT CONTRACT

Define the expected output format.

Examples:

- Complete source code.
    
- Structured analysis.
    
- Markdown documentation.
    
- Validation report.
    
- File deliverables.
    
- Extracted objectives.
    

Do not leave output expectations implicit when they materially affect the result.

## 13. DEPENDENCIES AND REFERENCES

Document external requirements only when applicable.

Use:

- references/ for detailed reference material.
    
- examples/ for illustrative examples.
    
- scripts/ for executable supporting utilities.
    

The main SKILL.md must remain understandable without requiring the reader to inspect every supporting file.

## 14. VALIDATION CHECKLIST

Before delivering a skill, verify:

[ ] Correct filename.  
[ ] Correct skill identifier.  
[ ] Metadata compatible with the target platform.  
[ ] Clear purpose.  
[ ] Defined activation conditions.  
[ ] Defined scope.  
[ ] Consistent terminology.  
[ ] Sequential heading hierarchy.  
[ ] Explicit operational instructions.  
[ ] Defined output expectations.  
[ ] No contradictory instructions.  
[ ] No unnecessary duplication.  
[ ] Examples consistent with the rules.

## 15. FINAL DIRECTIVE

ONE SKILL = ONE CLEAR RESPONSIBILITY.

STRUCTURE BEFORE COMPLEXITY.

INSTRUCTIONS BEFORE EXPLANATIONS.

CONSISTENCY BEFORE NOVELTY.

Every skill must follow this standard unless the target platform imposes a specific structural requirement.

END OF STANDARD.