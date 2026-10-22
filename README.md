# The Committee of Five

A history and law game about writing the Declaration of Independence. Two versions, as plain static files. No server, build step, or account is needed.

```
index.html          landing page with links to both versions
blocky-3d/          the 3D block-world platformer (needs WebGL)
pixel-art/          the top-down pixel-art world (works on almost any device)
lib/                three.js r128 and jsPDF 2.5.1, bundled so the games work on networks that block CDNs
.nojekyll           tells GitHub Pages to serve the files as they are
```

## Host it on GitHub Pages

1. Create a new public repository on GitHub (for example `committee-of-five`).
2. Upload everything in this folder to the repository root, keeping the folder structure. On github.com choose **Add file → Upload files** and drag the contents in. `index.html` should sit at the top level, not inside another folder.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the `main` branch and the `/ (root)` folder, and save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io/committee-of-five/`. Share that link. The two games are at `/blocky-3d/` and `/pixel-art/`.

To use your account’s main site (`https://YOUR-USERNAME.github.io/`) instead, name the repository `YOUR-USERNAME.github.io`.

## Test it on your own computer first

Opening `index.html` by double-clicking can block some features. Serve the folder instead:

```
cd committee-of-five
python3 -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Things to know

- **Saving progress.** Each student’s progress is stored in their own browser (localStorage) on their own device, per game. Clearing site data or switching devices starts over. Nothing is sent anywhere.
- **Certificate.** After the final reflection, the Case file tab in the satchel offers a PDF certificate with all of the student’s writing. It is built in the browser and saved with a normal download. Students attach it to the Google Classroom assignment.
- **Fonts.** The games ask Google Fonts for two typefaces. If that is blocked they fall back to system fonts and still work.
- **3D version.** It needs WebGL. If the platforming is too hard for a student, the **Play** tab in the satchel has a Platforming assist switch that lets them read the charge scrolls from the ground.
- **Licenses.** three.js and jsPDF are MIT licensed. The game text uses public-domain historical documents, plus one short excerpt from Dr. King’s 1963 speech.
