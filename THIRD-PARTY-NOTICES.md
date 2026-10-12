# Third-party notices

Talkflow is MIT-licensed (see `LICENSE`). The installer bundles the components below, each under its own licence. Licence texts ship with the installer: most Python packages carry theirs in `runtime\Lib\site-packages\<package>.dist-info\` (ONNX Runtime in `runtime\Lib\site-packages\onnxruntime\`), and the rest are in the `licenses\` folder next to this file.

## Runtime

| Component | Licence | Licence text |
|---|---|---|
| CPython 3.12 (embeddable distribution) | Python Software Foundation License | `runtime\LICENSE.txt` |
| Microsoft Visual C++ runtime (`vcruntime140*.dll`, `msvcp140*.dll`, next to `python.exe`) | Microsoft Visual C++ Redistributable licence (distributable code) | [Microsoft's terms](https://visualstudio.microsoft.com/license-terms/) |
| faster-whisper | MIT | dist-info |
| ↳ Silero VAD model (`silero_vad_v6.onnx`) | MIT | `licenses\Silero-VAD.txt` |
| CTranslate2 | MIT | `licenses\CTranslate2.txt` |
| ↳ Intel oneMKL (statically linked into `ctranslate2.dll`) and Intel OpenMP runtime (`libiomp5md.dll`) | Intel proprietary licence, redistributable runtime | `licenses\Intel-OpenMP-and-oneMKL.txt` |
| ↳ NVIDIA CUDA runtime and GPU kernels (statically linked into `ctranslate2.dll`) | NVIDIA CUDA EULA (redistributable) | `licenses\NVIDIA-CUDA-EULA.txt` |
| ↳ oneDNN, Thrust/CUB (statically linked into `ctranslate2.dll`) | Apache-2.0 | `licenses\Apache-2.0.txt` |
| ↳ spdlog (statically linked into `ctranslate2.dll`) | MIT | `licenses\spdlog.txt` |
| ONNX Runtime | MIT (with its own third-party notices) | `onnxruntime\LICENSE`, `onnxruntime\ThirdPartyNotices.txt` |
| NumPy | BSD-3-Clause AND 0BSD AND MIT AND Zlib AND CC0-1.0; bundled OpenBLAS/LAPACK BSD-3-Clause; bundled GCC runtime GPL-3.0-or-later WITH GCC-exception-3.1 | dist-info |
| PyAudioWPatch | Apache-2.0 | dist-info |
| ↳ PyAudio (the code PyAudioWPatch is based on) | MIT | `licenses\PyAudio.txt` |
| ↳ PortAudio (statically linked) | MIT-style PortAudio licence | `licenses\PortAudio.txt` |
| pywebview | BSD-3-Clause | dist-info |
| ↳ Microsoft WebView2 SDK (`Microsoft.Web.WebView2.*.dll`, `WebView2Loader.dll`) | Microsoft WebView2 SDK licence (BSD-3-Clause style) | `licenses\WebView2-SDK.txt` |
| pythonnet, clr_loader, bottle | MIT | dist-info |
| proxy_tools | MIT | `licenses\proxy_tools.txt` |
| tokenizers, flatbuffers | Apache-2.0 | `licenses\Apache-2.0.txt` |
| huggingface_hub, hf-xet | Apache-2.0 | dist-info |
| anthropic | MIT | dist-info |
| openai, google-genai, google-auth | Apache-2.0 | dist-info |
| httpx, httpcore, websockets | BSD-3-Clause | dist-info |
| pydantic, pydantic-core, PyYAML, jiter, annotated-types, typing-inspection | MIT | dist-info |
| requests, cryptography, tenacity | Apache-2.0 (cryptography: Apache-2.0 OR BSD-3-Clause) | dist-info |
| certifi | MPL-2.0 | dist-info |
| tqdm | MPL-2.0 AND MIT | dist-info |
| protobuf | BSD-3-Clause | dist-info |
| pip (used only by the optional GPU add-on) | MIT | dist-info |
| other small dependencies | see their `.dist-info` folders | dist-info |

**Not bundled on purpose:**
- **PyAV / FFmpeg.** faster-whisper imports it but uses it only to decode audio *files*. Talkflow passes raw audio, so the installer leaves PyAV and its FFmpeg libraries out.
- **CTranslate2's separate NVIDIA cuDNN library.** Only GPU speech needs it, and the optional GPU add-on installs NVIDIA's own copy. A CPU-only install contains no separate NVIDIA libraries, though `ctranslate2.dll` itself links NVIDIA's CUDA runtime statically (see above).

## Interface

| Component | Licence | Licence text |
|---|---|---|
| Bricolage Grotesque, Hanken Grotesk, JetBrains Mono (fonts) | SIL Open Font License 1.1 | `app\src\ui\web\fonts\OFL-*.txt` |
| Lucide icons (portions from Feather) | ISC (Feather portions: MIT) | `licenses\Lucide.txt` |

The Chrome extension bundles the same fonts and icons, and carries their licence texts in its own `licenses/` folder.

## Downloaded later, not bundled

| Component | When | Licence |
|---|---|---|
| Whisper speech models (OpenAI) in CTranslate2 format | first start, or *Download* in Settings | MIT |
| NVIDIA cuBLAS, cuDNN and NVRTC | only if you tick the GPU add-on in the installer | NVIDIA software licence, accepted by installing the `nvidia-*` packages; their licence texts are installed with them in `{app}\gpu` |
