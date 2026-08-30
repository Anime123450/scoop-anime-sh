# scoop-anime-sh

A [Scoop](https://scoop.sh) bucket for **[anime-sh](https://github.com/Anime123450/anime-sh)** —
the terminal-native anime client.

```powershell
scoop bucket add anime-sh https://github.com/Anime123450/scoop-anime-sh
scoop install anime-sh
```

That installs a single self-contained executable — no Python needed.

## You also want mpv

anime-sh plays through [mpv](https://mpv.io), and downloads through ffmpeg.
Neither is bundled: mpv is GPL, so shipping the binary inside a release would
carry source-offer obligations that declaring a dependency does not.

```powershell
scoop install mpv        # needed to play anything
scoop install ffmpeg     # only for `anime download`
```

Then `anime doctor` will confirm everything was found, and name the exact
command for anything that was not.

## Updating

```powershell
scoop update anime-sh
```

The manifest carries `checkver` and `autoupdate`, so the bucket follows new
[releases](https://github.com/Anime123450/anime-sh/releases) of anime-sh
without needing to be edited.
