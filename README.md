# The Declaration of Independence: Analysis and Reflection

Students **choose one** of three ways to complete this assignment. All three ask for the same thinking, and students turn in one file on Google Classroom.

| Option | What it is | Students submit |
|---|---|---|
| 1. 3D block-world game (`blocky-3d/`) | Explore a block-built Philadelphia, climb parkour trials, talk to the people involved. Needs WebGL. | PDF certificate from the game |
| 2. Pixel-art game (`pixel-art/`) | A walkable, top-down Philadelphia. Runs on almost any device, including phones. | PDF certificate from the game |
| 3. Written assignment (`text-assignment/`) | The Word document: watch the video overview, read the primary source, and write the analysis and reflection. | The completed document |

Students start at the landing page, `index.html`. It explains the three options, what each one asks for, how to choose, and how to turn the work in.

## What every option asks for

1. **Analysis of the Preamble**: its core values and how it justifies independence.
2. **Analysis of 3 to 5 charges** against King George III: how each is addressed in our society today, or how the colonists’ experience influenced it.
3. **Reflection (1 to 2 paragraphs)** on whether the Declaration is, or isn’t, a reflection of American values, with quotes, the core values and how they show up today (especially in the legal system), and the contradictions with the society of its time or ours.

In the games the same writing happens inside the story: a Preamble note (30+ words), a short explanation for each charge (10+ words, at least three charges), and a final reflection (100+ words). The completion certificate gathers all of it into one PDF, along with the contradiction ledger and the evidence cards the student collected. The games let a student examine more than five charges. Only three are required.

## Folder layout

```
index.html                  student-facing landing page (choose one of three options)
blocky-3d/                  Option 1, the 3D game
pixel-art/                  Option 2, the pixel-art game
text-assignment/            Option 3, the Word document
lib/                        three.js r128 and jsPDF 2.5.1, bundled so the games work if a CDN is blocked
.nojekyll                   tells GitHub Pages to serve files as they are
```

## The written option

The landing page links to `text-assignment/Primary Source_ Decleration of Independence.docx`. Because the filename has spaces, the link is written with `%20`. If you rename the file (for example to `Declaration-Assignment.docx`), open `index.html`, find the Option 3 card, and update the `href` to match. Filenames are case-sensitive on GitHub Pages.

A browser downloads a `.docx` instead of showing it. Students open it in Word or Google Docs. In Google Classroom you can also attach the same Word document to the assignment with **Make a copy for each student**, so students type directly into their own copy.

## Hosting on GitHub Pages

The site is served from the `main` branch, root folder (**Settings → Pages → Deploy from a branch → `main` / `(root)`**). The student link is:

`https://law-justice.github.io/Decleration-of-Independence.io/`

The games are at `/blocky-3d/` and `/pixel-art/` under that address. After you change files on GitHub, give Pages a minute or two to update, and refresh with Ctrl+Shift+R (or Cmd+Shift+R) if you still see the old version.

To test locally, run `python3 -m http.server 8000` in the repository folder and visit `http://localhost:8000/`.

## Notes for teachers

- **Saving.** Each game stores progress in the student’s own browser (localStorage), separately per game. It is not shared between devices, and nothing is sent to a server.
- **The certificate.** It unlocks only after the final reflection. It is a landscape certificate page followed by the formatted submission pages, built in the browser and saved with a normal download. It includes a verification code computed from the student’s work, so you can see it matches the writing in the file. It is not a security feature.
- **Special characters.** Emoji and non-Latin scripts in a student’s writing are dropped or shown as "?" in the PDF. The game’s "Copy case file" option keeps everything as plain text.
- **Platforming.** In the 3D game, Esc then **Play** has a Platforming assist switch that lets a student read the charge scrolls from the ground.
- **Sources.** Quotes in the games are real and labeled primary or retrospective. The map is stylized, and the narration is the game’s own. The games were created by Claude with prompting and iteration.
- **Fonts and libraries.** The games request two fonts from Google Fonts and fall back to system fonts if blocked. three.js and jsPDF are MIT licensed and included in `lib/`. The game text uses public-domain historical documents, plus one short excerpt from Dr. King’s 1963 speech.
