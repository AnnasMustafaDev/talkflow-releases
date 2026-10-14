# Talkflow privacy policy

Talkflow has no account. Usage statistics and error reports are optional and off unless you say yes (section 5). Your audio never leaves your PC: speech recognition runs locally.

Talkflow uses the network only in the cases below. You start the first three yourself; the update check (4) runs on its own and sends nothing about you; reports (5) are sent only if you turned them on.

## 1. Answers, summaries and the key test — to the AI provider you chose

Talkflow talks to the provider you picked in Settings (OpenAI, Anthropic (Claude) or Google (Gemini)) with your own API key. What it sends depends on the action:

| You… | Talkflow sends |
|---|---|
| get an answer (a question was detected in the meeting, or you typed one) | the question; the last few lines heard in the meeting, **as text**, never audio; up to your last five questions and answers since you last pressed Start (each Start begins a fresh conversation); your profile text; your answer-length and tone settings; and, if you picked an interview process, its job-description excerpt and the briefs of the rounds you switched on |
| press **Summary** | up to your last five questions and answers since you last pressed Start and your profile text |
| press **Screen** or Ctrl+Alt+Shift+S (Solve from screen), or a follow-up button on that answer | one screenshot of the screen under your mouse, or of the window you picked in Settings, shrunk to at most 2000 pixels wide; plus the same context as an answer. Follow-ups send that screenshot again; Review my code takes a new one. Nothing is captured until you press it, and screenshots are not saved |
| press **Test** in Settings | a fixed test prompt only |
| add a round to an interview process (when you press Stop with a process picked, attach a conversation, or add notes) | once, that round's conversation (the questions and Talkflow's suggested answers) or your notes, so the provider writes a short brief; Talkflow keeps only the brief |

The "lines heard in the meeting" are what **other participants** said. If you use Talkflow in a meeting, it is your responsibility to tell the other participants that you use live transcription and an AI assistant, and to follow the rules of the meeting, interview or test you are in.

That provider's terms and privacy policy apply to this data: [OpenAI](https://openai.com/policies/privacy-policy/) · [Anthropic](https://www.anthropic.com/legal/privacy) · [Google](https://policies.google.com/privacy).

**To opt out:** don't add an API key. Talkflow then sends nothing to any AI provider. It can still transcribe locally, but it can't write answers.

## 2. Speech models — downloaded from Hugging Face

Talkflow contacts [Hugging Face](https://huggingface.co) only to **download** a speech-recognition model: the first time you start listening with a model you don't have yet, or when you press **Download** in *Settings → This PC & speech models*. Downloaded models load offline after that. The download sends no personal data beyond what any download sends, such as your IP address. Talkflow never sends a Hugging Face token, even if another program saved one on your PC, and turns Hugging Face telemetry off.

## 3. GPU add-on (optional) — downloaded from PyPI

If you tick **GPU speech recognition** in the installer, it downloads NVIDIA's CUDA libraries (cuBLAS, cuDNN and NVRTC, under NVIDIA's licence) from [PyPI](https://pypi.org). This happens once, during setup.

## 4. Update check — a small file from GitHub

At start and every six hours, Talkflow downloads a small settings file published by Zehnix (`policy.json` and its signature, from Zehnix's public `talkflow-releases` repository on GitHub). It says whether a newer version exists and can carry a short notice. Talkflow only uses the file if Zehnix's signature on it is valid. Nothing about you is sent: it's a plain download, so GitHub sees your IP address as with any download.

## 5. Usage statistics and error reports — optional, to Zehnix

Talkflow asks once (in setup, or after an update) whether to send these. Both are **off unless you tick them**, and you can change either at any time in *Settings → Privacy*.

| If you turn on… | Talkflow sends to zehnix.co |
|---|---|
| **Usage statistics** | a random install ID (made on your first yes, not linked to your name or email); the Talkflow and Windows versions; your Windows display language; your device class (GPU model, RAM, CPU threads); when Talkflow starts or is updated; for each listening session the minutes, the number of answers, the median time to the first word, whether it listened to the speakers or a Chrome tab, the AI provider and model, and the speech engine; and which features you use (Solve from screen, interview briefs, summary, invisible mode, Talkflow for Chrome) |
| **Error reports** | the same install ID and versions; the step that failed, the error type and message, and the technical trace, with your Windows user name and home folder removed |

**Never sent this way:** what anyone said, your questions and answers, summaries, your profile, interview processes and briefs, job descriptions, screenshots, API keys, the launch password, or file and folder names.

On the server, Zehnix derives your country and city from the connection. The IP address itself is kept 30 days for abuse and fraud checks, then deleted. Usage events are kept 13 months and error reports 90 days. *Settings → Privacy → Delete data sent so far* deletes everything sent under your install ID and turns both reports off. *What's sent* shows an example report. Reports wait on your PC (at most 1 MB) while you're offline.

## Talkflow for Chrome (optional extension, not in the Chrome Web Store yet)

The extension doesn't talk to any server, including Talkflow's. It works only with the Talkflow app on the same PC:

- **Audio of one tab, when you ask.** Clicking the Talkflow icon (or pressing Alt+Shift+T) on a tab lets the extension hear that tab's audio, and Chrome marks the tab while it does. The audio goes from Chrome straight to the Talkflow app on your PC (Chrome's native messaging, then a local connection protected by a random key stored in your Windows profile). It is never sent anywhere else. In the app it is handled exactly like speaker audio: transcribed locally, never stored. Listening stops when you press Stop, close the tab, or close Chrome.
- **What the side panel shows** (the lines heard, questions and answers) comes from the app and isn't stored by the extension. Typed questions go to the app, which handles them as in section 1.
- **No page access.** The extension can't read or change web pages, and has no access to your browsing history, cookies or other tabs. Its permissions: `tabCapture` (the tab's audio), `activeTab` (the name and address of the tab you clicked, shown in the panel), `offscreen` (to process the audio), `sidePanel` and `nativeMessaging` (to reach the app).

## Bundled components

ONNX Runtime, which Talkflow uses to detect when someone speaks, can log telemetry events through Windows. Talkflow turns off ONNX Runtime's optional telemetry when it loads it; Windows may still record a minimal start-up event, subject to your Windows diagnostic-data setting. Apart from the optional reports in section 5, nothing else in Talkflow phones home.

## What stays on your PC

| What | Where |
|---|---|
| Settings, your API keys encrypted with Windows DPAPI, the key that lets the Chrome extension's bridge connect (`bridge.key`), the cached update-check file, and reports waiting to be sent (`telemetry-queue.jsonl`, only if you turned reports on) | `%APPDATA%\Talkflow` |
| Conversations, summaries, interview processes and round briefs | `Documents\Talkflow` (change it in Settings). If your Documents folder syncs to OneDrive, these sync too. |
| Log file, and the window's browser cache (WebView2) | `%LOCALAPPDATA%\Talkflow` |
| Speech models | `%USERPROFILE%\.cache\huggingface\hub` (shared with other apps that use Hugging Face) |
| Download logs and temporary download data (from Hugging Face's downloader) | `%USERPROFILE%\.cache\huggingface\xet` |
| Browser cache from earlier Talkflow builds | `%APPDATA%\pywebview` (safe to delete) |

- **Subtitle bar colours.** With *Bar colours* on Auto (the default), the bar looks at a tiny, shrunken view (48 × 27 pixels) of the screen behind it every 1.5 seconds to pick a light or dark look. It is used on the spot, never saved and never sent. Choose Light or Dark to turn this off.
- To stop saving conversations, turn off **Save conversations** in Settings.
- To delete old ones automatically, use **Delete after**.
- Uninstalling Talkflow keeps your data. Delete the folders above to remove it.

## Contact

Questions about privacy: [open an issue](https://github.com/Zehnix/talkflow-releases/issues).
