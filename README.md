# NEBULA SIEGE

A 3D omnidirectional space defense game built with Electron, Vanilla JS, Three.js, and the Web Audio API. The project is packaged so the GitHub Release ZIP can be extracted and launched like a normal Windows game folder.

## What It Demonstrates

- Cinematic post-processing bloom using Three.js `EffectComposer`
- Procedural audio synthesized entirely in the browser
- Object-pooled particle effects for explosions and trails
- Clean OOP architecture with separate game systems
- Real 3D spatial gameplay with pointer lock and quaternion camera control

## Project Files

- `index.html` - The complete game, UI, and logic in one file
- `main.js` - Electron main process entrypoint
- `preload.js` - Reserved preload hook for future native features
- `README.md` - Project overview and release instructions
- `LICENSE` - MIT license
- `.gitignore` - Editor and OS ignores
- `package.json` - Minimal static-server metadata

## Controls

- Click - Start game and lock the pointer
- Mouse - Aim the fighter
- Left mouse button - Fire twin cannons
- `W A S D` - Thrust in local space
- `Space` - Ascend
- `Shift` or `Ctrl` - Descend
- `Esc` - Pause by releasing pointer lock
- `R` - Restart after game over

## How To Run

### Option 1: Run the Desktop App

After installing dependencies, launch the Electron app:

```bash
npm start
```

### Option 2: Open Directly

Extract the GitHub Release ZIP and open `index.html` in a modern browser.

### Option 3: Local Server

If you want to use the included `package.json` script:

```bash
npm run web
```

That serves the folder on port `8080`.

## Notes For Releases

- Keep the release ZIP limited to the files above plus Electron dependencies in `node_modules` if you are distributing a development build.
- For the final GitHub Release, use `npm run dist` to generate the Windows installer and portable build under `release/`.
- The game depends on Three.js CDN imports, so the browser needs network access the first time it loads.
- High score data is stored locally with `localStorage`.

## License

MIT. See [LICENSE](LICENSE).
