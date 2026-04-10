# draftCGTS2026
CGTS 2026

## Codex in VS Code

This workspace is configured to run Codex through WSL on Windows, which is the supported path for agent mode.

If Codex still fails to start, check that WSL is installed, accessible from your Windows account, and that VS Code can open the folder with the Remote WSL extension enabled.

### Troubleshooting "Unable to attach to browser"
1. **Use File Mode**: For static development without a web server, select the **"Open index.html (Edge)"** configuration in the Run & Debug sidebar.
2. **Close Existing Edge Instances**: If Edge is already running, the debugger might fail to take control. Try closing all Edge windows and launching again.
3. **Manual Attach**: To use the "Attach to Edge" config, you must first start Edge from a Windows terminal with debugging enabled:
   `msedge.exe --remote-debugging-port=9222`
4. **WSL Networking**: If you are using a local server (like port 8080), ensure the server is actually running in your WSL terminal before hitting F5.
