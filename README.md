Commander Token Board
A fast, mobile‑friendly, installable web app for tracking creature tokens, counters, and battlefield state in Magic: The Gathering — optimized for Commander gameplay.
This project is built as a lightweight PWA (Progressive Web App), meaning it works offline, installs to your phone like a native app, and loads instantly.

✨ Features
Token Creation
- Create tokens using:
- Preset tokens (Angel, Zombie, Goblin, Treasure, etc.)
- Custom tokens (name, color, P/T, image)
- Upload session‑only images (never stored permanently)
- Add multiple tokens at once (quantity field)
- Optional Haste checkbox:
- Haste tokens enter without summoning sickness
- Non‑haste tokens enter with summoning sickness

🎨 Visual Design
- Tokens use a 5×7 card ratio for a clean, MTG‑like appearance
- Auto‑colored borders based on token color identity
- Optional token art (user‑uploaded)
- Auto‑adjusting text and layout for mobile and desktop

🧮 Counters System
Each token supports:
- +1/+1 counters
- –1/–1 counters
- Buttons to add or remove each type
- Effective P/T automatically recalculated:
effectivePower = basePower + plusCounters - minusCounters
effectiveToughness = baseToughness + plusCounters - minusCounters


Counters persist across taps, turns, and reloads.

⚔️ Battlefield Interactions
Tap / Untap
- Tap a token by clicking it
- Tokens with summoning sickness cannot tap
- Haste tokens can tap immediately
Remove Tokens
- Right‑click (desktop) removes one copy
- Long‑press (mobile) removes one copy
- If quantity reaches zero, the token disappears
Next Turn
- Clears summoning sickness from all tokens
Clear All
- Removes all tokens and session images

📦 Preset Token Library
Includes a curated, alphabetized list of common MTG tokens:
- Angels, Demons, Dragons
- Goblins, Soldiers, Spirits
- Eldrazi Spawn/Scions
- Treasures, Clues, Food
- And many more
Each preset auto‑fills:
- Name
- Color
- Power/Toughness
Preset fields are locked to prevent accidental edits.

🔍 Searchable Preset Picker
- Filter presets instantly by typing
- Click a preset to auto‑fill the token form
- Uses fallback icons (letter‑based) for a clean, consistent UI

📱 PWA Support
The app is fully installable on mobile and desktop.
Includes:
- manifest.json
- service-worker.js
- Offline caching
- Home‑screen icon support
- iOS‑specific meta tags for full‑screen mode
On iPhone
Install via: Share → Add to Home Screen

🗂️ Storage Behavior
- Tokens are saved in localStorage
- Uploaded images are stored in memory only (session‑only)
- Refreshing the page keeps tokens but clears images
- Clearing tokens resets everything

🚀 Tech Stack
- HTML5
- CSS3
- Vanilla JavaScript
- Progressive Web App (PWA)
- No frameworks, no dependencies, no build step

📄 License
This project is free to use, modify, and expand for personal or playgroup use.
