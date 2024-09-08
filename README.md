# `qmlformat` pre-commit hook
This repository aims to create a simple pre-commit hook to automatically run the `qmlformat` tool.

## Usage
```yaml
repos:
- repo: https://github.com/MBugdol/QmlFormatHook
  rev: 0.1
  hooks:
    - id: qmlformat
```

## Requirements
This project requires that `qmlformat` can be found on the current session's `PATH`. This is due to the fact that there is no `qmlformat` repository available, and I cannot install it alongside the hook.

## Current state
Currently this hook is implemented as a `system` hook, calling `qmlformat` directly. There are plans for converting it to a python script.

## Future plans
- make this repository a mirror of `qmlformat` when/if it becomes available
- convert the bare-bones `system` hook to a `python` one and force the `-i` parameter
- add error message explaining need to add `qmlformat` to `PATH` environment variable