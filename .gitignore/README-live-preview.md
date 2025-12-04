# Live preview — open to the side (quick guide)

Short and practical ways to get a live, reload-on-save preview of your HTML to the side in VS Code.

Options (recommended):

1) Microsoft Live Preview (best in-editor experience)

- Install the "Live Preview" extension (look for "Live Preview" by Microsoft in Extensions).
- Open your `flexbox.html` file.
- Open the Command Palette (Ctrl+Shift+P) and run: "Live Preview: Show Preview".
- With the preview open, use the editor split button (or press Ctrl+\) and drag the preview tab to the right to show it side-by-side with the editor. The preview updates automatically on save.

2) Live Server + Browser Preview (external server, in-editor browser window)

- Install these extensions (search/install in Extensions view):
  - Live Server (by Ritwick Dey)
  - Browser Preview (by auchenberg)
- Right-click `flexbox.html` → "Open with Live Server"; Live Server will start a local URL (e.g., http://127.0.0.1:5500).
- Open Command Palette (Ctrl+Shift+P) → "Browser Preview: Open Preview" and paste the local URL. Place the Browser Preview panel to the right — it acts like a browser inside VS Code and auto-refreshes.

3) Quick local server (no extension) — opens external browser

- Using PowerShell from the project folder:

```powershell
# Python 3 built-in server (runs on port 5500)
python -m http.server 5500

# Or use Node (if you have http-server installed)
npx http-server -p 5500
```

- Open http://localhost:5500/flexbox.html in your browser and snap the browser window to the right side of your screen (Windows Snap) to view side-by-side with VS Code.

Tips
- Use Ctrl+S to save and trigger a live reload.
- If the extension provides a toolbar button in the editor, look for a preview icon — right-click the preview tab title to move it to the side.
- If you want me to set up an in-workspace task or install extensions for you automatically, tell me which option you prefer and I'll add the config.

Quick workspace shortcut and task
- Shortcut: press Ctrl+Alt+L to start Live Server and open the in-editor Simple Browser preview for this workspace (configured via the "multi-command" extension).
- Task: open the Command Palette (Ctrl+Shift+P) and run "Tasks: Run Task" → "Start Python http.server (5500)" — this starts a simple local server if you prefer not to use Live Server.
