# SCRIPT FORMATTING STANDARD

# VERSION 1.0.0

## 1. PURPOSE

Establish a consistent formatting and structural language for all executable scripts.

The objective is to ensure:

- Readability.
    
- Predictable organization.
    
- Consistent naming.
    
- Maintainability.
    
- Clear execution flow.
    
- Reliable debugging.
    
- Reusable components.
    
- Consistent delivery.
    

## 2. FILE NAMING

Use descriptive filenames.

Preferred convention:

application_component.py

Examples:

RESA_PIPELINE_CORE.py  
RESA_SUPERVISOR.py  
RESA_GUI.py  
EMAIL_EXTRACTOR.py

Rules:

- Preserve established project naming conventions.
    
- Avoid ambiguous filenames.
    
- Avoid unnecessary abbreviations.
    
- Use version numbers in headers, not automatically in filenames.
    
- Do not rename existing files without authorization.
    

## 3. SCRIPT IDENTITY HEADER

Every script must identify itself.

Canonical Python header:

# ============================================================

# GASPAR OS

# APPLICATION NAME

# MODULE NAME

# VERSION 1.0.0

#   

# PURPOSE:

# Brief description of the script.

#   

# REQUIREMENTS:

# Python 3.10+

# ============================================================

Rules:

- Include the application or project name.
    
- Include the module name.
    
- Include the version.
    
- Describe the purpose.
    
- Identify important runtime requirements.
    
- Keep the header concise.
    

Do not add unnecessary metadata or YAML frontmatter.

## 4. SECTION MARKERS

Use two standardized section delimiters.

### 4.1 PRIMARY SECTION

# === SECTION NAME ===

Example:

# === IMPORTS ===

# === CONFIGURATION ===

# === LOGGING ===

# === CORE FUNCTIONS ===

# === MAIN EXECUTION ===

### 4.2 SUBSECTION

# -- SUBSECTION NAME --

Example:

# -- PATH RESOLUTION --

# -- VALIDATION --

# -- ERROR HANDLING --

Rules:

- Use uppercase section names.
    
- Keep section names descriptive.
    
- Use the same delimiter convention throughout the script.
    
- Avoid excessive section fragmentation.
    

## 5. PYTHON STRUCTURE

Use this default order:

1. SCRIPT IDENTITY HEADER
    
2. IMPORTS
    
3. CONSTANTS
    
4. CONFIGURATION
    
5. PATH RESOLUTION
    
6. LOGGING
    
7. DATA STRUCTURES
    
8. CORE FUNCTIONS
    
9. SERVICE OR CLASS DEFINITIONS
    
10. APPLICATION INITIALIZATION
    
11. MAIN EXECUTION
    

Only include applicable sections.

Do not introduce unnecessary classes or layers.

## 6. NAMING CONVENTIONS

Python:

- Functions: snake_case
    
- Variables: snake_case
    
- Classes: PascalCase
    
- Constants: UPPER_SNAKE_CASE
    
- Modules: lowercase_with_underscores
    

Examples:

def process_email():  
pass

class EmailProcessor:  
pass

MAX_RETRIES = 5

Preserve existing public identifiers unless a change is explicitly required.

For other programming languages, follow their established ecosystem conventions.

## 7. FUNCTION STANDARD

Every function must have:

- One clear responsibility.
    
- A descriptive name.
    
- Explicit parameters.
    
- Predictable return behavior.
    
- Appropriate error handling.
    

Prefer:

def validate_email(email):  
if not email:  
return False

```
return True
```

Avoid:

- Excessively long functions.
    
- Unnecessary nested conditionals.
    
- Repeated logic.
    
- Hidden dependencies.
    
- Unexplained side effects.
    
- Generic names such as process_data() when a precise name is available.
    

Use dependency injection when it simplifies testing, reuse, or integration.

Do not introduce abstractions without a functional reason.

## 8. INDENTATION AND SPACING

Python:

- Four spaces per indentation level.
    
- Never mix tabs and spaces.
    
- Two blank lines between top-level functions and classes.
    
- One blank line between related logical blocks.
    
- Consistent multiline argument alignment.
    

Maintain consistent formatting across the entire file.

## 9. IMPORT STANDARD

Organize imports in this order:

1. Standard library.
    
2. Third-party libraries.
    
3. Internal project modules.
    

Example:

import os  
import sys  
import logging  
from pathlib import Path

import customtkinter as ctk

from RESA_PIPELINE_CORE import RESAPipeline

Rules:

- Remove unused imports.
    
- Avoid unnecessary wildcard imports.
    
- Avoid circular dependencies.
    
- Do not import optional dependencies unnecessarily.
    

## 10. CONFIGURATION AND PATHS

Prefer:

- Centralized configuration.
    
- pathlib.Path for filesystem operations.
    
- Relative paths where appropriate.
    
- Explicit configuration defaults.
    
- Environment-independent path resolution.
    

Avoid:

- Duplicated path definitions.
    
- Unnecessary hardcoded user directories.
    
- Configuration values scattered across functions.
    
- Destructive operations without validation.
    

## 11. LOGGING STANDARD

Use consistent logging.

Canonical format:

[YYYY-MM-DD HH:MM] [COMPONENT] [LEVEL] MESSAGE

Recommended levels:

DEBUG  
INFO  
WARNING  
ERROR  
CRITICAL

Example:

[2026-11-11 14:30:00] [EMAIL_WORKER] [INFO] WORKER STARTED

Rules:

- Identify the script or component.
    
- Record meaningful state transitions.
    
- Record exceptions with traceback when appropriate.
    
- Avoid duplicate log handlers.
    
- Do not silently suppress errors.
    
- Never log passwords, credentials, or sensitive tokens.
    

## 12. ERROR HANDLING

Handle errors at the appropriate operational boundary.

Rules:

- Catch specific exceptions whenever possible.
    
- Preserve traceback information.
    
- Include contextual information.
    
- Distinguish recoverable from fatal failures.
    
- Avoid empty except blocks.
    
- Avoid reporting success after failure.
    
- Preserve the original exception when re-raising.
    

## 13. MAIN EXECUTION

Use an explicit entry point.

Canonical Python pattern:

def main():  
return 0

if **name** == "**main**":  
raise SystemExit(main())

Rules:

- Avoid executing application operations during module import.
    
- Initialize resources in a controlled sequence.
    
- Close resources appropriately.
    
- Support graceful shutdown where applicable.
    

For GUI applications, initialize the root window before creating dependent fonts or widgets.

## 14. SCRIPT SIZE AND COMPLEXITY

Prefer:

- Small, focused modules.
    
- Reusable functions.
    
- Explicit dependencies.
    
- Minimal duplication.
    
- Clear execution flow.
    

For GASPAR OS projects, aim for fewer than 600 lines per script when reasonably possible.

This is a guideline, not a reason to split a simple implementation into unnecessary files.

Do not optimize line count at the expense of correctness or readability.

## 15. DEPENDENCY MANAGEMENT

Document dependencies.

Prefer:

- Standard library when sufficient.
    
- Explicit package requirements.
    
- Compatible package versions.
    
- Reproducible installation instructions.
    
- PowerShell commands for Windows environments.
    

Avoid unnecessary administrative privileges.

## 16. WINDOWS COMPATIBILITY

For Windows-oriented scripts:

- Use pathlib for paths.
    
- Handle Windows path conventions.
    
- Avoid assuming the current working directory.
    
- Use subprocess safely.
    
- Quote paths correctly in shell instructions.
    
- Avoid unnecessary administrator privileges.
    
- Preserve compatibility with the declared Python version.
    

When giving file recovery guidance, mention Windows Properties → Previous Versions early when relevant.

## 17. GUI STANDARD

When developing GASPAR OS interfaces:

- Use CustomTkinter where established.
    
- Follow GASPAR OS Visual Identity Standard.
    
- Preserve established typography.
    
- Preserve light/dark appearance conventions.
    
- Use consistent spacing and alignment.
    
- Keep UI logic separated from reusable business logic where practical.
    

Do not introduce an alternative visual identity without authorization.

## 18. CODE DELIVERY STANDARD

When delivering scripts:

1. Provide the complete requested implementation.
    
2. Identify the filename and version.
    
3. Preserve existing functionality.
    
4. Describe significant changes.
    
5. Identify dependencies.
    
6. Report validation performed.
    
7. Identify untested operations.
    
8. Provide execution instructions when necessary.
    

Never provide fragmented patch instructions when the user requested a complete updated script.

## 19. VALIDATION STANDARD

Perform the following checks when the environment permits.

### STATIC VALIDATION

- Syntax compilation.
    
- Import verification.
    
- Reference verification.
    
- Function and class consistency.
    
- Configuration verification.
    

### COMPATIBILITY VALIDATION

- Python version compatibility.
    
- Package API compatibility.
    
- Function signatures.
    
- Operating system compatibility.
    

### RUNTIME VALIDATION

- Initialization.
    
- Resource acquisition.
    
- Connections.
    
- Main operations.
    
- Shutdown.
    

### DELIVERY ASSURANCE

Distinguish clearly between:

VERIFIED:  
Test executed and passed.

FAILED:  
Test executed and failed.

PENDING:  
Test not executed.

NOT APPLICABLE:  
Test does not apply.

Never claim runtime validation based solely on syntax compilation.

## 20. SELF-CONSISTENCY CHECKLIST

[ ] Script identity header.  
[ ] Correct version.  
[ ] Consistent section markers.  
[ ] Correct naming conventions.  
[ ] Organized imports.  
[ ] Consistent indentation.  
[ ] No unnecessary duplication.  
[ ] Explicit dependencies.  
[ ] Centralized configuration.  
[ ] Appropriate logging.  
[ ] Appropriate exception handling.  
[ ] Controlled initialization.  
[ ] Resource cleanup.  
[ ] Compatibility verified where possible.  
[ ] Complete implementation delivered.  
[ ] Validation status accurately reported.

## 21. FINAL DIRECTIVE

IDENTITY BEFORE IMPLEMENTATION.

STRUCTURE BEFORE COMPLEXITY.

REUSE BEFORE DUPLICATION.

EXPLICIT BEHAVIOR BEFORE HIDDEN SIDE EFFECTS.

VALIDATION BEFORE DELIVERY.

Every script must follow this standard while respecting the conventions and requirements of its programming language and project.

END OF STANDARD.