# ClipFinder v1.4.0.5

## Fixed
- **openai-whisper could not be installed** ("downloaded but does not import: No module named 'torch'"). It now installs together with everything it needs: PyTorch (if you do not have it yet), numba, tiktoken and the other small helpers. Before, it was installed on its own and its check ran before PyTorch was ready.

openai-whisper is only the last-resort transcription engine. Most people never need it: whisper.cpp (graphics card) and faster-whisper (comes with the installer) are faster.

## Upgrading
Update from inside the app (banner or Settings → Update Center), or download `ClipFinder-Setup.exe` below. Then click Install next to openai-whisper in Settings → Update Center again if you want it.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
