# The Declaration of Independence: Analysis and Reflection

Students **choose one** of four ways to complete this assignment. All three ask for the same thinking, and students turn in one file on Google Classroom.

| Option | What it is | Students submit |
|---|---|---|
| 1. 3D game, two looks (`blocky-3d/`, `storybook-third-person/`) | Explore Philadelphia in 3D, climb parkour trials, talk to the people involved. Block-world and storybook (Wind Waker style) both use a camera behind the player. Same story and assignment in each. Needs WebGL. | Essay (Word document) from the game |
| 2. Pixel-art game (`pixel-art/`) | A walkable, top-down Philadelphia. Runs on almost any device, including phones. | Essay (Word document) from the game |
| 3. Written assignment (`text-assignment/`) | The Word document: watch the video overview, read the primary source, and write the analysis and reflection. | The completed document |

Students start at the landing page, `index.html`. It explains the three options, what each one asks for, how to choose, and how to turn the work in.

## Keyboard-only play

Every game can be played without a mouse. In dialogue: arrow keys (or W A S D) move between answers, highlighted phrases, charges and buttons; E, Z or Enter selects; number keys jump to an answer; in the charge list, typing a number such as 14 jumps to that charge, and PgUp/PgDn skip five; End jumps to the buttons; Ctrl+Enter saves what you are writing. Esc opens the satchel, where Left/Right (or 1 to 6) switch tabs and Up/Down move into the page. Closing the satchel returns you to where you were.

## What every option asks for

1. **Analysis of the Preamble**: its core values and how it justifies independence.
2. **Analysis of 3 to 5 charges** against King George III, chosen by the student from the Declaration’s list of 27: how each is addressed in our society today, or how the colonists’ experience influenced it.
3. **Reflection (1 to 2 paragraphs)** on whether the Declaration is, or isn’t, a reflection of American values, with quotes, the core values and how they show up today (especially in the legal system), and the contradictions with the society of its time or ours.

In the games the same writing happens inside the story: a Preamble note (30+ words), a short explanation for each charge the student chooses (10+ words, at least three charges), and a final reflection (100+ words). Before a student chooses, the committee that drafted the Declaration reads all 27 charges aloud (a dramatized reading, labeled as such, using the Declaration’s own words), and the charge scrolls stay sealed until that reading has been heard. Earlier, at the start of the Preamble section, the game gives a quick summary of the Bill of Rights, which stays available in the satchel under the Bill of Rights tab (along with the later amendments the game cites). At each charge scroll the game shows the full list of 27 charges in the National Archives wording, and the student picks the one they want to explain. A charge can only be chosen once. Every charge comes with colonial background and a three-choice card challenge about how today’s law answers it, and the answer choices appear in a different order each time. Three analyzed charges move the story forward. Five earns a special bonus (the “Scholar of the Charges” card and 500 points), and that distinction appears in a box at the top of the student’s essay PDF. The essay PDF lists the charges in the order the student chose them. At the end the game builds an essay PDF from those answers: the student’s name and date, a title, the Preamble analysis, each charge with its quoted text and the student’s explanation, and the reflection, with a one-line game record and completion code at the bottom. The games let a student analyze up to seven charges (one per scroll). Only three are required.

## Folder layout

```
index.html                  student-facing landing page (choose one of three options)
blocky-3d/                  Option 1, the 3D game
pixel-art/                  Option 2, the pixel-art game
text-assignment/            Option 3, the Word document
lib/                        three.js r128 and jsPDF 2.5.1, bundled so the games work if a CDN is blocked (jsPDF is no longer used; the essay is a Word document the game builds itself)
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
- **The essay Word document (.docx).** It unlocks only after the final reflection. It is formatted like an essay (Times 12 point, 1.5 line spacing, indented paragraphs, real Word headings, a running head with the student’s name and page number) and is built in the browser and saved with a normal download. The completion code at the bottom is computed from the student’s work, so you can see it matches the writing in the file. It is not a security feature.
- **Special characters.** The Word document keeps accented letters, emoji and other scripts as typed. The game’s "Copy case file" option is still available as plain text.
- **Platforming.** In the 3D game, Esc then **Play** has a Platforming assist switch that lets a student read the charge scrolls from the ground.
- **Sources.** Quotes in the games are real and labeled primary or retrospective. The map is stylized, and the narration is the game’s own. The games were created by Claude with prompting and iteration.
- **Fonts and libraries.** The games request two fonts from Google Fonts and fall back to system fonts if blocked. three.js and jsPDF are MIT licensed and included in `lib/`. The game text uses public-domain historical documents, plus one short excerpt from Dr. King’s 1963 speech.

## The graphic novel journal (`journal/`)

An illustrated, page-turning version of the same story, for students who would rather read, draw conclusions, and build something than play a game. It reuses the games' narration, primary-source quotes, legal-lens notes, check questions, the "mark the ledger" exercises, and the same writing prompts, so students do the same thinking in a different format.

* **Read:** the story is told in five parts (June 1776 through the Hall of Echoes). Panels are drawn in code in an ink-and-halftone style, with a portrait of the speaker.
* **Collect:** students clip quotes, lens notes, and dated clippings to a scrapbook and earn the same stamps as the games' cards.
* **Write:** the Preamble analysis, three to five charges chosen from the 27 and explained, and the final reflection. Minimum word counts match the games, and examining five charges earns the Scholar of the Charges distinction.
* **Assemble:** at the end of each part the student edits a newspaper front page: a headline they write, a picture they choose, and pinned clippings. These are bound into a printable book.
* **Turn in:** the Word essay (identical in layout to the games' essay) unlocks when the final reflection is saved. The book can also be printed or saved as a PDF from the browser.

Notes: progress saves in the student's browser, and headlines and journal text are not checked beyond word counts. The illustrations are stylized, and the narration is the game's own (no invented quotations are attributed to historical figures).

## Screenshots

The `screenshots/` folder holds JPEG screenshots of each version, with a small gallery page (`screenshots/index.html`) linked from the landing page. They are useful for showing students the options before they choose, or for a class presentation. The 3D screenshots are bird's-eye views.
