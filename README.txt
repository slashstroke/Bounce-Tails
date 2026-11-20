Bounce Tales - Browser Edition (build 2026-11-20b)
==================================================

WHAT'S INSIDE
-------------
bounce-tales.html   The whole game in one file (J2ME emulator + game, ~600 KB).
                    No install, no Node.js, no internet needed.

PLAY (Windows/Mac/Linux)
------------------------
1. Unzip.
2. Double-click bounce-tales.html. It opens in your browser.
3. Click once (unlocks audio), then play.

You can verify you are on this build: the hint line at the bottom of the
page ends with "build 2026-11-20b". If it does not, you opened an older
downloaded copy - delete it and use this zip.

Music: the game plays the original .mid files from the JAR through a
Web-Audio synthesizer (MIDI is parsed and rendered live, nothing is
converted). The synth follows the original game's sound: soft plucked
acoustic bass, per-channel volume balance and pitch bends from the files,
and a drum kit modeled on the phone's built-in GM percussion (the JAR
ships no drum samples - on the original device these notes were rendered
by the phone's wavetable kit): swept-sine kick, body+noise snare, soft
non-tonal metallic ride (the level song's quiet vel-54 timekeeper), noise
wash crashes, toms, bongos and the percussion clicks the songs actually
use - kick 36, ride 51/59, snare 38/40, crash 49/57, chinese 52, bongo 60,
high-Q 27 and metronome 33, exactly as found in the 8 songs. Nothing
sustains between beats, so there is no drone or hum. Playback runs on the
audio thread, so it never stutters even under heavy load.

DISPLAY
-------
The game fills your screen. On start it picks the internal resolution whose
aspect ratio matches your window: on a 1920x1080 monitor it runs 640x360
(3x integer scale) and fills the screen edge to edge, windowed AND
fullscreen, no black bars. Resizing, monitor switches, phone rotation and
entering fullscreen all re-fit automatically. An old saved size whose shape
does not match your current screen is ignored and re-fitted, so a stale
pick can never letterbox the game again.

[  /  ]          Cycle screen resolutions manually
                 320x240 (classic landscape) - 240x320 (classic portrait)
                 480x360 - 640x480 - 800x600 (4:3)
                 640x360 - 960x540 (16:9) - 800x480 (5:3) - 360x640 (portrait)
                 (a manual choice is remembered while it matches your screen)

You can also force a mode with a URL parameter: bounce-tales.html?res=640x360

F               Enter / exit fullscreen (or double-click the game)
Fullscreen uses your whole monitor; Esc also exits.

CONTROLS (directions)
---------------------
W / ArrowUp      UP    - jump
A / ArrowLeft    LEFT  - move left
D / ArrowRight   RIGHT - move right
S / ArrowDown    DOWN  - roll / duck
Space / Enter    OK / confirm (also Fire; numpad Enter and numpad 5 work)
Q / E            Soft keys (F1 / F2 also work)
0-9 * #          Phone keys (top row or numpad)
R                Restart
F                Fullscreen
[ / ]            Change screen resolution

All keys are resolved by physical key position AND key name, so any keyboard
layout (incl. non-US) works, holding several keys at once works, and holding
keys while the window loses focus cannot leave them stuck.

HOST ON VERCEL (or any static host)
-----------------------------------
You no longer need the old Node.js project. The single HTML file is the
complete app - it is pure static content.

Easiest: go to vercel.com/new, drag the folder that contains this HTML
(rename bounce-tales.html to index.html first if you want it served at "/"),
and deploy. Or run `npx vercel` in that folder and accept the defaults.
Netlify / GitHub Pages work the same way.
