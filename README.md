# RYVEX

**An auto-DJ and a manual DJ deck in one Windows app.** Point it at your music and it plays a set by itself, mixing songs with beat-matched transitions. Or take the decks yourself, with stems, effects, a sampler and a radio stream built in.

> Ryvex is a one-person project, built and tested on Windows. If something is wrong, see **Getting help** at the bottom.

---

## Download

**[Download the latest version](https://github.com/kiingprints/RYVEX-Releases/releases/latest)**, then under **Assets** choose `Ryvex-Setup-x.y.z.exe`. Run it, pick an install folder, and finish.

- Windows 10 or 11, 64-bit.
- Your music, mixes, settings and cue points are stored in your user folder, not the install folder, so updating or reinstalling never touches them.
- **Windows may say "unknown publisher" or show a SmartScreen warning.** The installer is not code-signed yet. Choose **More info > Run anyway**. Each release also has a `.sha256` file if you want to check the download yourself.

### Updating
Ryvex checks for new versions by itself. You can also use **Settings > About > Check for updates**. It shows a progress window while it downloads, verifies the file, and installs. Nothing installs without you pressing the button.

---

## First five minutes

1. **Add your music.** In the left panel press **+ Add** and pick a folder. Ryvex scans and analyzes every song (tempo, key, energy, beat grid). A bar fills along each row while it works. You can start right away; songs are ready as they finish.
2. **Press AUTO-DJ.** It builds a set from your library, starting with a song of middling energy, and picks each next song to fit the last one: close tempo, matching key, similar energy. Songs you liked are picked more often.
3. **Take over any time.** Touch a deck and the Auto-DJ pauses. Press AUTO-DJ again and it carries on from the song that is playing.

**Want to start with a specific song?** Load it on a deck (right-click a song > *Load to deck*) and press AUTO-DJ. It plays that song first and builds behind it. Or right-click > *Start Auto-DJ from this song*.

---

## What it does

### Auto-DJ
- Beat-matched, phrase-aligned transitions: blends, bass swaps, filter moves, echo-outs, drops, and short scratches where nobody is singing.
- Build-up and hit sounds on drops (risers, swells, snare rolls, impacts, sub drops). Drop your own sound files in an FX folder to use them too.
- **Set queue tab:** drag songs to reorder, Delete to remove, **Undo** (button or Ctrl+Z) to put things back, double-click to play a song next. Right-click a song in the Library > **Play next** puts it at the top without interrupting anything, and the songs after it are re-ordered to fit.
- Keeps itself stocked, never repeats the same song back to back, and can keep the same artist apart and avoid songs played in the last few hours.
- Remembers the running set. If the app closes unexpectedly, it offers to carry on where it left off.

### Manual mixing
- 2 decks, or 4 with the deck toggle. Scrolling waveforms with beat grid, hot cues, loops, loop roll, beat jump, sync and key lock.
- **Stems:** split any song into vocals, drums, bass and melody and mute or echo each one. Runs on your graphics card if it can (AMD, Nvidia or Intel via DirectML), otherwise on the processor.
- **STEM / KEY pads:** echo the vocals or drums alone, or shift a song's key from -2 to +3 semitones.
- **Library hints:** green rows fit the song that is playing, and a column tells you why (for example "key +1, tempo +2%").
- Fix a wrong tempo or beat grid: half or double time, an exact BPM, or **tap it** along with the song.

### Sampler
Eight pads. Cut a loop from a deck, load a file, or press **AUTO CHOPS** to fill all eight from the song that is playing: kick, snare, drum bar, vocal chop, vocal bar, bass hit, melody and a full bar (needs that song's stems).

### Microphone
A mic bar with ducking (the music dips when you talk) and **Voice FX**: Off, Echo or Reverb.

### Radio and streaming
- Stream your mix to a **SHOUTcast** or **Icecast** server (**Broadcast** button). Track titles update on every transition, and the ON AIR button shows how many people are listening.
- A now-playing text file for your stream overlay, jingles played every N songs, an optional **clean-air** mode that leaves out explicit songs, and "restart when the set ends" so the stream never goes quiet.
- **Song requests:** open a small web page that listeners can use to request songs (More > Song requests).
- **More > Export tracklist** saves what played, with times, ready for a video or stream description.

### Extras
- **Set planner** and saved **mixes** (generated groups of songs that mix well).
- **Song notes:** start a song at a chosen bar, keep it in until a chosen bar, or add a reminder.
- **Find missing songs** (More menu) relinks songs you moved or renamed and keeps their likes, notes and cue points.
- A MIDI controller can be connected (More > MIDI controller). Render a set to a WAV file from the More menu.
- Themes, a compact layout for small screens, and a second song list beside the Library: drag a folder into it.

---

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| Space | Play or pause |
| N | Mix to the next song now |
| 1 2 3 4 | Play or pause deck A, B, C, D |
| Q W E R | Cue deck A, B, C, D (hold to preview) |
| A S D F | Sync deck A, B, C, D |
| T | Mic on or off |
| / | Jump to the song search box |
| Ctrl+Z | Undo a queue change |

The full list is under **More > Keyboard shortcuts**. Shortcuts are ignored while you are typing in a box.

---

## Where your things are

Everything personal lives in `C:\Users\<you>\.autodj`: settings, likes, notes, cue points, saved mixes, the analysis cache, sampler pads and the error log. Open it from **Settings > About > Open data folder**. Uninstalling Ryvex does not delete it.

---

## Good to know

- **Your music, your rights.** Ryvex plays files you already have. It does not download or stream music from other services. If you broadcast publicly, you are responsible for having the licenses your country requires for that.
- **Stems take a moment** the first time a song is separated; the result is kept so the next time is instant. The first time you use stems, Ryvex downloads its stem model once (a large file, so you need an internet connection). Without it, Ryvex falls back to a simpler, lower-quality split.
- **Key shift** only works on a deck you play by hand, because it adds a tiny delay that would throw off the Auto-DJ's timing. Pressing it on an Auto-DJ deck takes that deck over.
- This is a young project. Some newer parts (stem and key pads, jingles, auto chops, the transition sounds) have had the least real-world use.

---

## Getting help

Something broken, confusing, or missing? Open an **Issue** on this repository and include:

1. Your Ryvex version (Settings > About).
2. What you did, and what you expected.
3. A screenshot, if it is about how something looks.
4. The file `error.log` from **Settings > About > Open data folder** (open it in Notepad and attach it or paste the last few lines).

Thank you for trying Ryvex.
