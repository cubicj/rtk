# Codex CLI Hooks

> Part of [`hooks/`](../README.md) — see also [`src/hooks/`](../../src/hooks/README.md) for installation code

## Specifics

- Programmatic PreToolUse hook: `rtk hook codex` reads the hook payload from stdin and rewrites Bash commands to their `rtk` equivalents via `updatedInput`
- `rtk init --codex` registers the hook in `hooks.json` (`$CODEX_HOME/hooks.json` when set, otherwise `~/.codex/hooks.json`)
- The hook entry carries both `command` (POSIX) and `commandWindows` (`rtk.exe`) so one config works across platforms
- `rtk-awareness.md` is the legacy prompt-level guidance document, no longer installed by `rtk init --codex`
