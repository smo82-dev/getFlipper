Flipper interactive demo v19 — a single self-contained index.html (no build step).

Fixes in v19
- Provider buttons now remove their Flipper on the second click. The page wrote messages to
  two elements (#feedback, #appstatus) that no longer existed; each write threw an error and
  stopped the button handler before the screen and button were updated.
- Every Flipper shows its real allowance faces: Grok weekly, Kimi monthly, Copilot monthly +
  chat. Claude's weekly is used up, so its 5-hour face shows 0% "weekly cap", as the app does.
- Phone layout: the "Add or remove Flippers" panel was squashed to 42px wide, hiding buttons.
- Auto-hide waits 10 seconds, as its message says (it was 3).
- The "Still interested?" prompt waits until the visitor pauses instead of interrupting a drag.
- "Get Windows companion" opens the getFlipper Releases page.
- Ferris wheel: the stack spaces itself to fit the window, so all six Flippers stay inside
  the browser (and the desktop), at any screen size. The simulated browser is also larger.

Hosting on Cloudflare Pages: connect the repo (or upload this folder), no build command,
output directory = this folder. _headers adds basic security headers.
