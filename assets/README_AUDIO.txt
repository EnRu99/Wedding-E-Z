BACKGROUND MUSIC
================

File:   assets/music.mp3
Source: "The One, But It's That Instrumental Loop Everyone's Obsessed With.mp3"
        (renamed so the URL has no spaces or special characters)

How it behaves
- Nothing plays when the page opens.
- Music starts when the guest taps the E & Z wax seal (browsers only allow
  sound after a tap) and fades in over a few seconds on desktop and Android.
- It loops. A round play/pause button appears in the bottom-right corner after
  the envelope has opened.
- It pauses when the guest leaves the tab and resumes when they come back.
- If playback is blocked or the file is missing, the invitation still works
  normally.

Volume
The file was made 6 dB quieter with the lossless MP3Gain method (only the
frames' gain fields change; nothing is re-encoded). This matters for iPhones,
where websites cannot set the volume at all. On desktop and Android,
music.volume in the WEDDING config (index.html) sets the level, 0.8 by default.

Replacing the music
Put the new file at assets/music.mp3, or change music.src in the WEDDING
config. Keep the relative "./" path so it works locally and on GitHub Pages.
Set src: '' to switch the music off completely.

Only use music you have the right to use, especially on a public website.
