# txnkzy.github.io

## Homerow Piano

A nine-key piano trainer in a single file (`index.html`). There's no build step and no backend; the only external files are two Google Fonts.

- **Keys:** `A S D F G H J K L` play C4 D4 E4 F4 G4 A4 B4 C5 D5. No other keyboard keys play notes. `Space` plays or pauses.
- **Modes:** Free play, Listen (auto-playing falling notes) and Learn (the song waits until you press the right key).
- **Songs:** 13 public-domain melodies in three difficulty levels, each arranged to fit the nine keys. Songs that had to be changed are labelled "Simplified", and a tooltip explains what changed.
- **Import audio:** drop in an MP3, WAV or M4A you have the rights to use. It's transcribed in the browser (YIN pitch detection), fitted onto the home row, and saved on your device. Nothing is uploaded.

Key colours show which finger plays each key: pinky, ring, middle, index, and "index reach" for G and H.

### Run it

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 5178
```

### Performance check

- Add `#perf` to the URL to show a frame-rate meter.
- Add `#stress` to also load a 1,600-note stress-test song.
