BACKGROUND MUSIC — HOW TO ADD IT LATER
======================================

Music is intentionally not included yet. Until it is configured, the
invitation plays nothing, shows no music button and makes no audio requests.

To enable it:

1. Put the music file into this folder and name it:

       assets/music.mp3

   (MP3 is the safest choice for iPhone Safari and WhatsApp's in-app browser.
   Keep it small — about 2–4 MB, 128 kbps is plenty.)

2. Open index.html and, in the WEDDING configuration at the top, change

       music: {
         src: '',

   to

       music: {
         src: './assets/music.mp3',

   Keep the leading "./" — the relative path is what makes it work both when
   opening the file locally and later on GitHub Pages (/Wedding-E-Z/).

3. That's it. Playback starts when the guest taps the wax seal (browsers only
   allow sound after a tap), and a round play/pause button appears in the
   bottom-right corner. The music pauses automatically when the guest leaves
   the tab and resumes when they return. Adjust loudness with music.volume.

Only use music you have the right to use.
