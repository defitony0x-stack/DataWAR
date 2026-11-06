# DATA WAR 0.15

Static browser game (three.js r128 from cdnjs). No build step.

Files
- index.html  the game
- models/     GLB models, loaded by relative path
- vercel.json cache headers for models
- package.json  start script for Railway (serve)

Deploy on Vercel: import the repo, Framework Preset "Other", leave build and output blank.
Deploy on Railway: new project from the repo, it runs "npm start".

0.15 changes
- Removed VX-7 Carbine, Needle SMG and Rail-9 Marksman (their models rendered as flat bars). The armory now only lists weapons whose model loaded.
- Allies walk instead of running and keep formation with a gentle catch-up.
- New cinematic battle ambience (layered loop) and overlapping ally voice callouts.
- Saved loadouts from 0.14 reset once, because weapon slots changed.
