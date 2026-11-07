# ClipFinder v1.4.0.2

A fix for Microsoft Defender quarantining ClipFinder.

## Fixed
- **Microsoft Defender flagged `ClipFinder.exe` as "Settings Modifier" (potentially unwanted) and quarantined it** together with the Start Menu and Desktop shortcuts. The culprit was the small launcher EXE (a PyInstaller one-file program whose only job was to start the app). That kind of unsigned, self-extracting EXE is a common false-positive target.
- The launcher EXE is gone. The shortcuts now start the bundled Python (`python\pythonw.exe`, digitally signed by the Python Software Foundation) with `clipfinder.py` directly. The app itself did not change.
- Installing over an older version removes the old `clipfinder.exe` and recreates the shortcuts.

## Upgrading
If Defender already quarantined ClipFinder, **download and run `ClipFinder-Setup.exe`** from this release. The in-app updater only replaces `clipfinder.py`, so it cannot bring back the shortcuts Defender removed. Your settings, API keys, models and clips are kept.

Do not restore the quarantined `ClipFinder.exe` from Defender: it is no longer used.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
