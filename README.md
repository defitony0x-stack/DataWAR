# DATA WAR 0.19

Static browser game (three.js r128 from cdnjs). No build step.

Files
- index.html  the game
- models/     GLB models, loaded by relative path
- vercel.json cache headers for models
- package.json  start script for Railway (serve)

Deploy on Vercel: import the repo, Framework Preset "Other", leave build and output blank.
Deploy on Railway: new project from the repo, it runs "npm start".

0.19 changes
- Allies can now be hurt and killed. Each has 70 HP; enemy bolts hit them, they scream when hit (voice cue, throttled) and scream again when they go down, then fall (Death animation where the model has one) and are removed after about 14 seconds. The marker over their head goes green to red with health, they leave the minimap when dead, and Kade reports "NAME is down!".
- Enemies now shoot the nearest visible ally as well as you, face them and slow down while engaging them. Enemy movement is otherwise unchanged (that is the next fix).

0.18 changes
- Allies rewritten. Each ally has its own AI and no longer follows or depends on the player: they spawn in the hall, patrol assigned posts (west / east) while it is quiet, and when hostiles appear they head out through the gate, flank on their own side, pick firing positions about 10-17 m from the target, reposition every few seconds, and shoot with distance-based accuracy (misses show as tracers). They path around walls and crates through the doors and the gate, detect when they are stuck, and keep clear of each other and the player.

0.17 changes
- All sounds replaced with the supplied Mixkit / Pixabay set. Ambience = civil war battle + gun fight bed with distant bombs, looped seamlessly. Gunshots, enemy fire and hit tick are cut from the 8-bit gun files. Hurt = effort grunt, kill = battle scream, ally callouts = battle shouts (female variants pitched up). Wave start = drums of war call, boss entrance = creature scream + massive explosion, boss fight adds the battle drums track.
- Kept from before (nothing in the new set matches): reload and footsteps.
- Old files are in sounds/old/ and are not loaded.

0.16 changes
- Intro video sound is on by default; the SOUND ON/OFF button is gone. If a browser blocks autoplay with sound, the intro starts silent and the sound comes on at the first tap, click or key press.
- Audio engine: ambience no longer ducked by gunfire (own limiter, bypasses master compressor) and louder; sounds are no longer dropped while the audio context is waking; audio preloads silently on the first menu tap; failed samples are retried; ally callouts are louder and more frequent.

0.15 changes
- Removed VX-7 Carbine, Needle SMG and Rail-9 Marksman (their models rendered as flat bars). The armory now only lists weapons whose model loaded.
- Allies walk instead of running and keep formation with a gentle catch-up.
- New cinematic battle ambience (layered loop) and overlapping ally voice callouts.
- Saved loadouts from 0.14 reset once, because weapon slots changed.
