# The Infinite Rugby League Stadium

Single self-contained HTML file (`index.html`). No backend, no external APIs, no build step, no npm, no bundler. Every feature ships inside this one file.

## Hard rules
- NEVER split this into multiple files.
- NEVER add npm, webpack, vite, or any build tool.
- NEVER add external API calls or fetch requests to third-party services.
- NEVER remove or restructure existing working features without being asked.
- All changes are surgical edits to index.html.

## After every change
- Confirm the file is valid HTML: opening and closing tags balanced.
- Confirm the embedded JavaScript has no syntax errors.
- Confirm you have not introduced any duplicate function names.
- If you changed anything in the persistence layer (saveState/loadState/saveHistory/loadHistory), confirm the save key names have not changed unless asked.

## Project context
- localStorage key `infinite_stadium_v2` stores the bracket and match state.
- localStorage key `infinite_stadium_history_v1` stores the permanent records layer (separate from the bracket — the RESET button must never touch it).
- `buildPool()` is deterministic — no Math.random(). Team-year entries must be identical on every page load so the records layer can track dynasties.
- The match engine is in `fireEvent()`. The golden point branch is separate and correct — do not touch it unless asked.
- Web Speech API uses a fixed voice picked by `loadVoice()`. A voice selector exists in the footer.
