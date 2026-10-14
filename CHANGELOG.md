# Changelog

All notable changes to Talkflow. Versions follow [Semantic Versioning](https://semver.org).

## 1.2.1 — 2026-10-14

- **The subtitle bar follows your screen.** By default it turns dark over a dark window, such as a code editor, and light over a light page, so it never stands out as a bright window (or a reflection in glasses). It switches smoothly, only when the background really changes. *Settings → Bar colours* has Auto, Light and Dark. Talkflow checks a tiny, shrunken view of the screen behind the bar on your PC; nothing is saved or sent.
- **Easier-to-read cyan text** in light mode.

## 1.2.0 — 2026-10-13

- **Interview rounds.** In your profile you can add an interview process (company, role and, if you like, the job description). Each round is kept as a short, editable brief: what was asked, what you said, what you promised and what is still open. A round can come from a listening session (it joins the process in use when you press Stop), from a conversation in the Inbox, or from your own notes. Later answers draw on the briefs of the rounds you switch on and on the job description, never on full transcripts. The Live view shows which process is in use.
- **Solve from screen.** Press **Ctrl+Alt+Shift+S**, or **Screen** in Live, to send one screenshot of a coding task to your AI provider. It captures the screen under your mouse, or a window you pick in Settings even when other windows cover it. The answer gives the approach, complexity and edge cases, hints first and the code when you ask for it. Follow-ups reuse the same screenshot (show the code, explain, optimise, another language), and **Review my code** captures your own code. Talkflow's windows stay out of the shot, and screenshots are not saved.
- **Answers that stick to your profile.** What your profile says comes before generic advice and is never contradicted. Methods and figures stay with the employer they belong to, and answers no longer make up numbers. A question that was cut off gets a short holding reply, and technical terms the speech recognition misheard are understood from context.
- **Speech not meant for you is skipped.** Talkflow no longer answers TV, ads, speeches or side talk. It shows a quiet **Answer anyway** line instead, and skipped lines are not saved. Typed questions and screenshots are always answered.
- **Better question detection.** A line cut off mid-sentence waits a few seconds and is joined with the next one. A question that follows a reaction in the same line, such as "Great. Now explain RAG.", is now detected.
- **Try again** on answers that failed.
- **Update notices.** Talkflow checks a small file published by Zehnix at start and every six hours, and uses it only if Zehnix's signature on it is valid. It tells you when a new version is out and can show a short notice; an update prompt never interrupts listening. Nothing about you is sent.
- **Optional usage statistics and error reports.** Talkflow asks once, in setup or after this update, and both are off unless you tick them. They never include what anyone said, your questions and answers, your profile, screenshots or keys. *Settings → Privacy* has both switches, an example of what's sent, and **Delete data sent so far**. The [privacy policy](PRIVACY.md) lists exactly what is sent and how long it is kept.
- **Keyboard shortcuts and tips in Settings.** Every shortcut in one list, short tips, and where to find the log. **Ctrl+K** jumps to the question box, and **Esc** closes dialogs.
- **Copy conversation text.** You can now select and copy the conversation in Live and in the Inbox.

## 1.1.1 — 2026-10-12

- **Talkflow ships compiled.** The app's code is installed only in compiled form; it runs exactly as before.
- **New licence.** From this version Talkflow is under the Talkflow licence: free to download and use, for personal and commercial work; copying, modifying, reverse engineering and redistributing it are not allowed. Copies of 1.0.0 and 1.1.0 keep the MIT licence they were released with.

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
