# ClipFinder v1.4.0.2

A fix for Microsoft Defender quarantining ClipFinder.

## Fixed
- **Microsoft Defender flagged `ClipFinder.exe` as "Settings Modifier" (potentially unwanted) and quarantined it** together with the Start Menu and Desktop shortcuts. The culprit was the small launcher EXE (a PyInstaller one-file program whose only job was to start the app). That kind of unsigned, self-extracting EXE is a common false-positive target.
- The launcher EXE is gone. The shortcuts now start the bundled Python (`python\pythonw.exe`, digitally signed by the Python Software Foundation) with `clipfinder.py` directly. The app itself did not change.
- Installing over an older version removes the old `clipfinder.exe` and recreates the shortcuts.

## AI providers and downloads (checked against the live services, November 2026)
- **OpenRouter:** 5 of the 7 free models ClipFinder used have been removed by OpenRouter (DeepSeek V4 Flash, Nemotron 3 Super, Nex N2.5 Pro / Mini, Qwen 3.8 27B). They are replaced by free models that are live today: **Nemotron 3 Ultra** (clip finding), **Nemotron 3.5 Super VL** (images), **Nemotron 3.5 Lightning** (quick jobs) and **Gemma 4 26B**, next to Gemma 4 31B and the free router.
- **Gemini:** `gemini-2.5-flash` is retired by Google (from December 1, 2026 its requests are redirected to 3.5 Flash-Lite), so it is replaced by **Gemini 3.6 Flash**. If you had 2.5 Flash selected, ClipFinder switches to the default model.
- **Kick downloads:** the app now accepts curl-cffi 0.17, the version the current yt-dlp installs (it used to hold it back at 0.16).
- **YouTube downloads:** the portable Node.js the app downloads is now 24.22.2 (24.22.1 was a security release).
- Groq, Kick and Twitch were checked and needed no changes.

## Upgrading
If Defender already quarantined ClipFinder, **download and run `ClipFinder-Setup.exe`** from this release. The in-app updater only replaces `clipfinder.py`, so it cannot bring back the shortcuts Defender removed. Your settings, API keys, models and clips are kept.

Do not restore the quarantined `ClipFinder.exe` from Defender: it is no longer used.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
