# Random Picker — Bowl Mode (Single File)

A fun, single-file HTML picker that uses physics to randomly select a person from a bowl of bouncing avatars.

## Run
- Open `index.html` directly in your browser, or
- Serve the folder locally and visit `http://localhost:5500/index.html` (any static server is fine).

## Use
- Add names in the top bar and click Add.
- Click Shake to agitate the bowl.
- Click Pick next to select someone; the winner pops out and is removed from the bowl.
- Undo restores the last picked person back into the bowl.

## Notes
- Light beige theme (#FAF3ED) with calm, natural accents.
- Avatars are masked to round circles; crisp high-res is used for the winner popup.
- Matter.js via CDN. No build step; everything is in `index.html`.
 - Background: If `bkgd.jpg` is present in this folder, it will show behind the bowl at ~20% opacity. If it's missing, a subtle built-in gradient fallback is used so the scene still feels alive. Replace with your own image by dropping a `bkgd.jpg` next to `index.html`.

## Deploy
- GitHub Pages: push this folder and enable Pages on the repo.
- Netlify: drag-and-drop the folder into Netlify Drop.
- Any static host works.

## Git quickstart
```bash
# Initialize (if not already)
 git init -b main

# Ignore common local files
 echo -e ".DS_Store\n.vscode/\n.playwright-mcp/\nnode_modules/\n.venv/\n.env/" > .gitignore

# Commit
 git add .
 git commit -m "Initial commit: single-file Random Picker"
```

