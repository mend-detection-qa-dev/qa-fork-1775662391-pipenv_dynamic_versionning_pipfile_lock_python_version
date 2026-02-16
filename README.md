# Pipenv Test Case 5: Pipfile.lock with python_version

## What This Tests
Tests detection of Python version from Pipfile.lock when Pipfile has no requires section, using `python_version` field.

## Expected
3.10 found through PipfileLockPythonVersion

## Files
- `Pipfile` - No requires section
- `Pipfile.lock` - Contains `"python_version": "3.10"` in _meta.requires

## Expected Behavior
Your version detection tool should detect **Python 3.10** from Pipfile.lock.

## Priority
This is the **fourth priority** detection method for Pipenv projects (after .python-version, .tool-versions, and Pipfile).

## Note
Pipfile.lock is checked when Pipfile doesn't specify a Python version requirement.
