Bounce Tales - Browser Edition
==============================

WHAT'S INSIDE
-------------
bounce-tales.html   The whole game in one file (J2ME emulator + game, ~600 KB).
                    No install, no Node.js, no internet needed.

PLAY (Windows/Mac/Linux)
------------------------
1. Unzip.
2. Double-click bounce-tales.html. It opens in your browser.
3. Click once (unlocks audio), then play.

CONTROLS
--------
Arrows / WASD   Move
Enter / Space   OK / Jump
Q / E           Soft keys
0-9 * #         Phone keys
R               Restart

HOST ON VERCEL (or any static host)
-----------------------------------
You no longer need the old Node.js project. The single HTML file is the
complete app - it is pure static content.

Easiest: go to vercel.com/new, drag the folder that contains this HTML
(rename bounce-tales.html to index.html first if you want it served at "/"),
and deploy. Or run `npx vercel` in that folder and accept the defaults.
Netlify / GitHub Pages work the same way.
