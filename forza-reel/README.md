# FORZA.REEL — Forza Horizon 6 Photography Gallery

## Adding Photos

1. Drop your screenshot into the `images/` folder
2. Open `photos.json` and add an entry:

```json
{
  "src": "images/your-photo.jpg",
  "car": "Car Name",
  "cat": "supercar",
  "meta": "Location · Time of Day"
}
```

That's it. The gallery updates automatically.

### Categories (`cat` field)
Use any of these — filters are built automatically from whatever you use:
- `supercar`
- `hypercar`
- `classic`
- `rally`
- `drift`
- `muscle`
- Or make up your own — new categories appear as filter buttons automatically.

### Photo order
Photos appear in the order they are listed in `photos.json`.
The **first 3 entries** are shown in the hero section at the top.

---

## Deploying to Netlify (Recommended — Free)

The easiest way to get your gallery online:

1. Go to [netlify.com](https://netlify.com) and create a free account
2. From your dashboard, click **"Add new site"** → **"Deploy manually"**
3. Drag your entire `forza-reel` folder onto the Netlify drop zone
4. Done — Netlify gives you a live URL instantly (e.g. `random-name.netlify.app`)

To update the site later (new photos, edited JSON):
- Go back to your Netlify site dashboard
- Click **Deploys** → drag the updated folder again

To get a custom URL like `forza-reel.netlify.app`:
- Go to **Site configuration** → **Change site name**

---

## Deploying to GitHub Pages (Free, version controlled)

1. Create a free account at [github.com](https://github.com)
2. Click **New repository**, name it `forza-reel`, set it to Public
3. Upload all your files (index.html, photos.json, images/ folder)
4. Go to **Settings** → **Pages** → Source: `main` branch → `/root`
5. Your site will be live at `yourusername.github.io/forza-reel`

Adding new photos later: upload the new image + update photos.json via the GitHub website.

---

## Viewing Locally (for testing before deploying)

You can't open index.html directly in a browser (photos.json won't load due to browser security).
Instead, run a simple local server:

**If you have Python installed:**
```
cd forza-reel
python3 -m http.server
```
Then open: http://localhost:8000

**If you have Node.js installed:**
```
npx serve forza-reel
```

---

## File Structure

```
forza-reel/
├── index.html       ← The gallery (don't need to edit this)
├── photos.json      ← Your photo list (edit this to add photos)
├── README.md        ← This file
└── images/
    ├── photo1.jpg
    ├── photo2.jpg
    └── ...
```
