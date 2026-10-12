# Changelog

All notable changes to Talkflow. Versions follow [Semantic Versioning](https://semver.org).

## 1.1.0 — 2026-10-12

- **Floating bar: dragging works on scaled displays.** On 125 % and 150 % screens the bar jumped into a corner and blinked when you dragged it. It now follows the cursor smoothly, keeps part of itself on screen so you can always grab it, comes back if it ended up off-screen, and a double-click on its top strip puts it back at the top centre.
- **Ready for Talkflow for Chrome.** The installer sets up the local connection the upcoming Chrome extension uses to listen to one meeting tab and show answers in Chrome's side panel (for Chrome and Edge, removed on uninstall). The extension itself comes to the Chrome Web Store later. While it listens to a tab, the main window says which one.
- Published by Zehnix: the installer's publisher, support and update links point to Zehnix.

## 1.0.0 — 2026-10-09

The first public release.

- **Live answers in your voice** from your speakers' audio or a typed question, streamed word by word, with tones (confident, concise, warm, technical, STAR) and short or detailed length.
- **Local speech recognition** with Whisper models, from tiny to large-v3. Talkflow detects your PC (GPU, RAM, CPU) and picks the best model that runs live.
- **Speech models manager** in Settings: fit for your PC, download with live progress, remove, open the model folder.
- **OpenAI, Claude or Gemini** with your own key, encrypted with Windows DPAPI.
- **Floating answer bar** with a live audio meter; movable, resizable and closable.
- **Inbox** of past meetings with search, meeting summaries, and automatic deletion after 7, 30 or 90 days.
- **Activity dashboard**: questions answered, time to first word, questions over time.
- **Frost and Graphite modes** with Signal Cyan or Ember accents.
- **Opt-in invisible mode** (off by default), an optional launch password, and a responsible-use acknowledgement in the first-run setup.
- **Windows installer**: per-user without admin rights or for all users, English and German, an optional GPU add-on for NVIDIA cards, and clean upgrades and uninstalls that keep your data.
