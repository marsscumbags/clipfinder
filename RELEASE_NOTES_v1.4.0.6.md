# ClipFinder v1.4.0.6

## Fixed
- **Transcription failed** with "open() got an unexpected keyword argument 'metadata_errors'" (Censor, Transcript, Clip Finder and Post Studio whenever faster-whisper was used). The installer since 1.4.0.3 shipped a newer audio library (PyAV 19) that faster-whisper does not support yet. It is now pinned to a working version, ClipFinder switches an installed PyAV 19 back by itself at start-up, and works around it until then. The installer build now really decodes audio before it is released, so this cannot ship again.
- **"'NoneType' object has no attribute 'write'"** when a component showed a progress bar (for example the openai-whisper model download). ClipFinder runs without a console window, and that output now goes nowhere instead of crashing.
- The automatic repair of components could not change the version of protected packages (such as PyAV). Fixed.

## Changed
- **ClipFinder no longer picks an output folder for you.** On every tab (Clip Finder, Auto Edit, Transcript, Downloader, Thumbnails, Studio, Censor, Music Removal) an empty output box shows a yellow **⚠ Pick a folder** tag, and starting a job without a folder asks you where to save. Nothing is saved to your Downloads folder or next to the source video unless you choose it. Folders you already picked stay as they are.

## Upgrading
Update from inside the app (banner or Settings → Update Center), or download `ClipFinder-Setup.exe` below.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
