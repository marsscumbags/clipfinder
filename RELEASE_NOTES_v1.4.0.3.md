# ClipFinder v1.4.0.3

Fixes for transcripts that repeat themselves and for component installs that failed or broke things.

## Fixed
- **Transcripts no longer get stuck repeating a phrase** ("that's it, that's it, that's it, ..." or the same line over and over). The GPU engine (whisper.cpp) no longer feeds earlier text back into itself, which is what started the loops. Any loop that still slips through, in any engine, is cut down to two copies. Normal speech like "no no no no" or "alright, alright, alright" is left alone. This applies to the Transcript tab, Post Studio, Clip Finder and Censor.
- **Installing OpenCV from Settings broke numpy.** OpenCV was shown as missing even though it was installed, because the check looked for the wrong package name. Clicking Install then tried to install a second copy while ClipFinder was running, failed with "Access is denied", and left numpy half-deleted, so transcription stopped working. The check now finds the OpenCV that ships with ClipFinder. Install buttons now download and test the package first, then switch it on when you restart ClipFinder.
- **Half-installed packages repair themselves.** At start-up ClipFinder now checks that the required packages are complete and reinstalls any that are missing files. If your numpy was damaged by the problem above, it is fixed the first time you start this version.
- **The openai-whisper fallback could not be installed** ("Cannot import 'setuptools.build_meta'"). It is now built correctly with the bundled Python.
- **Downloading a faster-whisper model could fail** with "[WinError 1314] A required privilege is not held by the client". Models are now saved as normal files.

## Changed
- **The Editor tab is switched off for now.** It is hidden, along with the "Edit" button in the channel browser.
- **New: Settings → What is what.** A short guide to the tabs, AI providers, transcription engines, Whisper models and components.

## Upgrading
Update from inside the app (banner or Settings → Update Center), or download `ClipFinder-Setup.exe` below.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
