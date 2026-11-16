# ClipFinder v1.4.0.7

## New: download only part of a video
No more downloading a whole 10-hour VOD for one moment. In **Downloader → Download links** there is a new **✂ ONLY PART** row:

- **Start / End** - type the times (`8:03:02`, `03:02`, `29000` or `8h3m2s`). Every link in the list downloads just that part.
- **Links with a time in them** start there by themselves: Kick `?t=28982`, YouTube `&t=90` or `?t=1h2m3s`, Twitch `?t=2h10m5s`.
- **No end?** It grabs the length in **"No end? grab"** (10 minutes unless you change it), so pasting a Kick link with `?t=` is enough.
- **A different part per link**: write it after the link, e.g. `https://kick.com/...  8:03:00-8:10:00`.
- The file name says which part it is, e.g. `... [8h03m02s-8h13m02s] - ClipFinder.mp4`, so parts never overwrite each other.

Only the needed part is downloaded: one minute out of a 10-hour Kick VOD took about 5 seconds.

Leave Start / End empty and use links without a time to download whole videos like before. Clip Finder's own link box and the channel browser still download the whole video.

## Fixed
- **Kick VODs were saved as "<code> - master.m3u8 - ClipFinder.mp4".** They are now named "<channel> - <title> - ClipFinder.mp4" again.

## Upgrading
Update from inside the app (banner or Settings → Update Center), or download `ClipFinder-Setup.exe` below.

---

*Built by [@MarsScumbags](https://x.com/MarsScumbags)*
