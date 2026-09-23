# txnkzy.github.io

## Homerow Piano

A nine-key piano trainer in a single file (`index.html`, about 1.5 MB). There's no build step and no backend. The piano recordings are embedded in the file, and the only external files are two Google Fonts.

- **Keys:** `A S D F G H J K L` are nine fixed finger positions. Each song retunes them to its own notes, in its own key and range. Für Elise gets C4 E4 G♯4 A4 B4 C5 D5 D♯5 E5; Minuet in G gets its F♯s. Keys tuned to a sharp or flat are drawn dark, like black keys. No other keyboard keys play notes, and `Space` plays or pauses.
- **Fitting songs to nine keys:** if a song uses more than nine different notes, the least-used ones fold into their nearest neighbour. If it uses fewer, the spare keys continue its scale, so every key still plays in tune in Free play.
- **Sound:** a real recorded grand piano (Salamander Grand Piano, a Yamaha C5), sampled every minor third. Each note is corrected to exact equal temperament at A4 = 440 Hz. Songs are played with a soft, normal or lively touch, and a softer touch also sounds darker, as on a real piano. There's a volume slider next to the mute button, and it remembers your setting.
- **Modes:** Free play, Listen (auto-playing falling notes) and Learn (the song waits until you press the right key).
- **Songs:** 13 public-domain melodies in three difficulty levels. Each is labelled "As written", "Simplified" or "Excerpt", and a tooltip explains what changed and how the keys are tuned.
- **Import audio:** drop in an MP3, WAV or M4A you have the rights to use. It's transcribed in the browser (YIN pitch detection) at the pitch it was recorded, the keys are tuned to it, and it's saved on your device. Nothing is uploaded.

Key colours show which finger plays each key: pinky, ring, middle, index, and "index reach" for G and H.

### Credits

Piano samples: [Salamander Grand Piano V3](https://archive.org/details/SalamanderGrandPianoV3) by Alexander Holm, licensed [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). The MP3 encodes come from [Tone.js](https://tonejs.github.io/audio/salamander/). They're re-pitched in the browser and otherwise unmodified.

### Run it

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 5178
```

### Performance check

- Add `#perf` to the URL to show a frame-rate meter.
- Add `#stress` to also load a 1,600-note stress-test song.
