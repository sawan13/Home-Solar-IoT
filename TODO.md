# Nav Tab Active Bottom Border Update Plan

## Approved Plan Steps (Breakdown):

1. **✅ Understanding Complete**: Analyzed all .nav-tab CSS across 7 HTML files via read_file + search_files.

2. **Update base .nav-tab style in ALL files**: Add `border-bottom: 2px solid transparent; transition: border-bottom-color 0.3s ease;` for smooth underline.

3. **Edit index.html** (unique border-color rule):
   ```
   OLD: .nav-tab:hover, .nav-tab.active { background:var(--panel2); color:var(--text);border-color: var(--sun2); }
   NEW: .nav-tab:hover { background:var(--panel2); color:var(--text); } .nav-tab.active { color:var(--text); border-bottom: 3px solid var(--sun2); }
   ```

4. **Edit devices.html, users.html**:
   ```
   OLD: .nav-tab:hover, .nav-tab.active { background:var(--panel2); color:var(--text); }
   NEW: .nav-tab:hover { background:var(--panel2); color:var(--text); } .nav-tab.active { color:var(--text); border-bottom: 3px solid var(--sun2); }
   ```

5. **Edit analytics.html, settings.html, setup.html, powerflow_light.html** (similar background rules).

6. **Test**: Open index.html/devices.html in browser, verify active underline in var(--sun2).

7. **Cleanup**: Update TODO.md as [COMPLETED], attempt_completion.

**Progress: Step 1/7 complete. Next: Base style updates.**

