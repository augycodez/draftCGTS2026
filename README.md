# draftCGTS2026
CGTS 2026

## Codex in VS Code

This workspace is configured to run Codex through WSL on Windows, which is the supported path for agent mode.

If Codex still fails to start, check that WSL is installed, accessible from your Windows account, and that VS Code can open the folder with the Remote WSL extension enabled.

### Troubleshooting "Unable to attach to browser"
1. **Use Server Mode (Recommended for WSL)**: Run `python3 -m http.server 8080` in your WSL terminal, then use the **"Launch Edge"** configuration.
2. **File Mode Limitations**: **"Open index.html (Edge)"** may fail in WSL because Windows Edge often cannot resolve internal Linux file paths.
3. **Clean Session (Fixes Attach Errors)**: We now use `"userDataDir": false` in `launch.json`. This forces a clean, temporary browser profile, which prevents "Unable to attach" errors caused by existing profile locks.
4. **Final Check**: If problems persist, ensure all Edge processes are killed via Task Manager (Ctrl+Shift+Esc) before starting the debugger.
