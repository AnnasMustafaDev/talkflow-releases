# Talkflow privacy policy

Talkflow has no account, no analytics and no telemetry of its own. Your audio never leaves your PC: speech recognition runs locally.

Talkflow sends data over the network only in the cases below, and you start each one yourself.

## 1. Answers, summaries and the key test — to the AI provider you chose

Talkflow talks to the provider you picked in Settings (OpenAI, Anthropic (Claude) or Google (Gemini)) with your own API key. What it sends depends on the action:

| You… | Talkflow sends |
|---|---|
| get an answer (a question was detected in the meeting, or you typed one) | the question; the last few lines heard in the meeting, **as text**, never audio; up to your last five questions and answers since you last pressed Start (each Start begins a fresh conversation); your profile text; your answer-length and tone settings |
| press **Summary** | up to your last five questions and answers since you last pressed Start and your profile text |
| press **Test** in Settings | a fixed test prompt only |

The "lines heard in the meeting" are what **other participants** said. If you use Talkflow in a meeting, it is your responsibility to tell the other participants that you use live transcription and an AI assistant, and to follow the rules of the meeting, interview or test you are in.

That provider's terms and privacy policy apply to this data: [OpenAI](https://openai.com/policies/privacy-policy/) · [Anthropic](https://www.anthropic.com/legal/privacy) · [Google](https://policies.google.com/privacy).

**To opt out:** don't add an API key. Talkflow then sends nothing to any AI provider. It can still transcribe locally, but it can't write answers.

## 2. Speech models — downloaded from Hugging Face

Talkflow contacts [Hugging Face](https://huggingface.co) only to **download** a speech-recognition model: the first time you start listening with a model you don't have yet, or when you press **Download** in *Settings → This PC & speech models*. Downloaded models load offline after that. The download sends no personal data beyond what any download sends, such as your IP address. Talkflow never sends a Hugging Face token, even if another program saved one on your PC, and turns Hugging Face telemetry off.

## 3. GPU add-on (optional) — downloaded from PyPI

If you tick **GPU speech recognition** in the installer, it downloads NVIDIA's CUDA libraries (cuBLAS, cuDNN and NVRTC, under NVIDIA's licence) from [PyPI](https://pypi.org). This happens once, during setup.

## Bundled components

ONNX Runtime, which Talkflow uses to detect when someone speaks, can log telemetry events through Windows. Talkflow turns off ONNX Runtime's optional telemetry when it loads it; Windows may still record a minimal start-up event, subject to your Windows diagnostic-data setting. Nothing else in Talkflow phones home.

## What stays on your PC

| What | Where |
|---|---|
| Settings, and your API keys encrypted with Windows DPAPI | `%APPDATA%\Talkflow` |
| Conversations and summaries | `Documents\Talkflow` (change it in Settings). If your Documents folder syncs to OneDrive, these sync too. |
| Log file, and the window's browser cache (WebView2) | `%LOCALAPPDATA%\Talkflow` |
| Speech models | `%USERPROFILE%\.cache\huggingface\hub` (shared with other apps that use Hugging Face) |
| Download logs and temporary download data (from Hugging Face's downloader) | `%USERPROFILE%\.cache\huggingface\xet` |
| Browser cache from earlier Talkflow builds | `%APPDATA%\pywebview` (safe to delete) |

- To stop saving conversations, turn off **Save conversations** in Settings.
- To delete old ones automatically, use **Delete after**.
- Uninstalling Talkflow keeps your data. Delete the folders above to remove it.

## Contact

Questions about privacy: [open an issue](https://github.com/Zehnix/talkflow-releases/issues).
