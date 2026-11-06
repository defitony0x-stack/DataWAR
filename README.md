# DATA WAR 0.13

Static browser game (three.js r128 from cdnjs). No build step.

Files
- index.html  the game
- models/     GLB models, loaded by relative path
- vercel.json cache headers for models
- package.json  start script for Railway (serve)

Deploy on Vercel: import the repo, Framework Preset "Other", leave build and output blank.
Deploy on Railway: new project from the repo, it runs "npm start".
