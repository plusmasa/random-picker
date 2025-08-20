# Random Picker

A fun single‑file random picker with physics, SVG art, confetti, and sound. Pick a random person from a list using one of three modes:

- Bowl (Physics): bouncing avatar balls in a bowl
- Popcorn: kernels pop out of a tapered bucket
- Wheel: a spin‑the‑wheel with avatars on slices

No build step required — just open `index.html` in a modern browser.

## Features

- Three modes: Bowl, Popcorn, Wheel
- Add names with unique circular avatars (masked from `AvatarLibrary/` images)
- Shake strength control (disabled in Wheel mode)
- Pick Next selects a winner; Continue or Undo as needed
- Winner popup says “You’re up!” and triggers a confetti celebration (beige/green palette)
- Per‑mode sounds: rattle (Bowl), popcorn (Popcorn), spin (Wheel)
- Background music with Play/Pause and Mute buttons
- Mode‑specific backgrounds:
	- Bowl: `bkgd.jpg`
	- Popcorn: `bkgdCity2.jpg`
	- Wheel: `bkgdSeats.jpg`
- Single file app — HTML/CSS/JS contained in `index.html` using Matter.js via CDN

## Quick start

Option 1 — open directly:
- Double‑click `index.html` (works in most browsers)

Option 2 — serve locally (recommended for consistent asset loading):
- Python 3: `python3 -m http.server 8000` then open http://localhost:8000/
- Node (if you have `npx`): `npx serve -p 8000` then open http://localhost:8000/

## Usage

1. Enter a name and click Add (repeat to build your roster)
2. Choose a Mode: Bowl, Popcorn, or Wheel
3. Optional: Adjust Shake strength (not used in Wheel)
4. Press Shake (disabled in Wheel) or go straight to Pick next
5. When the winner appears, use Continue to keep going, or Undo to put them back
6. Clear all resets the roster; Reset resets the scene
7. Use the Play/Pause button for background music and the Mute button to mute all sounds

Notes
- Wheel mode disables Shake; press Pick next to spin the wheel
- Keyboard shortcuts are intentionally disabled to avoid accidental actions while typing

## Project structure

- `index.html` — App UI, styling, and logic
	- Bowl and Popcorn physics with Matter.js (CDN)
	- Popcorn bucket and Wheel rendered as SVG overlays
	- Confetti rendered on a canvas behind the winner popup
	- Per‑mode audio SFX and simple background music control
- `AvatarLibrary/` — Source avatar images (masked into circles at runtime)
- `Icons/` — UI icons (SVG)
- `Sounds/` — `bgMus.mp3`, `rattle.mp3`, `popcorn.mp3`, `spin.mp3`
- Backgrounds: `bkgd.jpg`, `bkgdCity2.jpg`, `bkgdSeats.jpg`

## Development

- No build tools; edit `index.html` directly
- Matter.js 0.20.0 via CDN
- SVG art layers are recreated on engine reset to avoid disappearing visuals
- Wheel mode uses SVG + easing animation to land on a random winner

## Deploy (GitHub Pages)

Because this is static, you can host it with GitHub Pages:
1. Push the repo to GitHub (done)
2. In the repo: Settings → Pages
3. Source: Deploy from a branch
4. Branch: `master` and Folder: `/ (root)`
5. Save — your site will be available at `https://<your-username>.github.io/random-picker/`

## License

No license specified. If you plan to distribute, consider adding a LICENSE file.

