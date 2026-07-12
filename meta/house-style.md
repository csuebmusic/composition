# house style

Canonical conventions for the composition lessons hub. This file is authoritative. When it disagrees with something said in conversation, defer to the file and flag the discrepancy so we can reconcile it. A convention lives in conversation until it stabilizes, then gets promoted here.

Canonical files:

- `meta/house-style.md` (this file)
- `meta/references.md` (the uploaded reference set and how to use it)

## scope: two layers

Everything produced here belongs to one of two layers, set by audience.

Student-facing and public-facing output is the airtight layer: student handouts, score-study guides, analytical prompts, worked examples, feedback a student reads, and anything published or shared beyond us (the repo README, the live site, Canvas announcements). The style rules below hold here without exception, and process stays off the page: no verification, reasoning, or judgment calls in anything a student or the public reads.

The between-us layer is our working exchanges and the instructor-facing side of any work: planning notes, this file and the other `meta/` files, commit messages, and the colleague-level breakdown on a graded item. Process belongs here. Report reasoning, verification, and judgment calls in this layer, and strip them from anything that goes out.

## register

Register is set per material, not fixed for the project. Each piece is written to one of these levels.

Lower-division undergraduate: composers early in their training who read notation and know the fundamentals, but are new to writing their own music. Warm, clear, and scaffolded. Define specialized terms the first time they appear and build vocabulary deliberately. Assume they can read a score, not that they know advanced theory or orchestration.

Upper-division undergraduate: developing composers with theory and analysis behind them. More analytical, less glossed. Assume fluency with common-practice harmony and basic formal analysis, and introduce orchestration and notation practice as craft to be refined rather than concepts met for the first time.

Graduate: emerging professional composers. Rigorous and precise, written to them as peers. Assume analytical and technical fluency and the vocabulary of the field, and where an advanced or contested idea matters, situate it the way one composer would for another.

Internal and planning material (for us): practical and concrete. Where students get stuck, at each level, and what to do about it.

Connect technical work to creative outcomes: orchestration, notation, and analysis are in service of what the student is trying to write, so tie the craft back to the music wherever it is relevant.

## style

These are the profile's communication rules. They govern the mechanical style layer in all student-facing and public-facing output. They are register-neutral and hold at every level. Apply the right register and these rules together: the right register, written clean.

1. Always write in prose. Use bullet points only for genuine lists (parameters, steps, discrete items), never for content that reads naturally as sentences.
2. Never use em dashes. Use a colon to introduce or define, a period to split contrasting ideas, parentheses for an aside, a comma when the clause attaches smoothly. En dashes are fine in number ranges and typographic compounds.
3. Do not stack negatives into a "no X, no Y, only Z" beat. Restate positively, naming what a thing is or does. A single negative is fine when the negation is the point.
4. Cut hedging filler ("it's worth noting that," "essentially," "basically," "in some sense"). Commit or cut.
5. Do not write announcement or justification sentences that describe what the next sentence will deliver, or what the previous sentence just delivered. Name the point directly, then stop. After naming a strength or a result, do not add a sentence restating why it matters.
6. State the point about a thing directly and leave your process out. Say what a source is or does ("the Kooijman article is your sharpest source"), not that you verified it, that it "is real," "checks out," or "is confirmed." The exception is a result the reader must act on: a source that cannot be verified or looks fabricated, or a specific error to fix (wrong pages, date, attribution).
7. Keep headings minimal and never in title case.

Register holds everywhere: clear, direct, and grounded in specific examples, favoring constructive and actionable guidance over purely evaluative comment, with goals and expectations transparent while leaving room for exploration.

## visual language

Student-facing materials are HTML built on the project's stylesheet, `assets/style.css`. Specs, READMEs, and internal notes are Markdown.

Colors are referenced through named CSS variables, never hardcoded hex in component CSS. The locked core palette:

```
--bg          #f7f7f4    soft near-white paper
--bg-alt      #ecece7    lifted panel: callouts, figures, tables
--ink         #1d2127    cool near-black, body text
--ink-soft    #4c515a    secondary text
--ink-faint   #838994    captions, footer, grid labels
--rule        #d2d1cb    panel borders, axes
--rule-soft   #e6e5e0    faint grid, section rules
--accent      #345b7d    steel blue, marks and links
--accent-soft #23415c    darker steel, emphasis on the page
--warn-bg     #f2ede3    caution panel
--warn-ink    #6b4a22
--serif       Courier Prime    mono-first: both names hold one face
--mono        Courier Prime
```

The palette shares its custom-property names with the other csuebmusic repos, so diagrams and widgets port between repos and re-skin themselves. Composition is mono-first: `--serif` and `--mono` both resolve to Courier Prime, its own identity apart from the sans-body audio repos. A ported widget that leaned on a sans body, or on caps for contrast, reads flatter here, so weight, size, and color carry the hierarchy instead. Typography is Courier Prime throughout, loaded from Google Fonts in the stylesheet.

Pages are self-contained and browser-only: viewable with no build step and no external runtime dependency.

Analytical and pedagogical diagrams (form, texture, register and orchestration maps, process) are hand-authored inline SVG in the house style. The SVG is written inline in the HTML, since CSS variables resolve only when the SVG is embedded, not when it is loaded through `<img src>`.

Notation is treated as given. Music is not engraved here. Score examples arrive as images or external files that you or the student supply, and materials reference and analyze them rather than typesetting them. `figure.score` carries a supplied score image.

Domain-specific diagram color families (instrument families for orchestration and register maps, section colors for form diagrams, voice colors for texture and process diagrams) are added to the stylesheet when the first diagram that needs them lands, the way the audio repos grew their meter and cable families.

## feedback

This is a lessons hub with no formal rubric. Feedback ties to the goal of the lesson and to the student's developing craft: what the piece is trying to do, what is working, and the next concrete move. Keep it constructive and actionable rather than purely evaluative, and pitch it to the student's level.

## references

Uploaded texts are authoritative. Search them first before answering a conceptual or pedagogical question, and prefer them over general knowledge. Where the set has no source for a topic, flag the gap and offer to draft a handout or find suitable material rather than filling it in. The set and its topic map are in `meta/references.md`.

## git workflow

Commit directly to `main` using this project's token. One logical change per commit, with a descriptive multi-line message, and push after each commit so the work can be pulled locally. For destructive or wide-reaching operations (reorganizations, mass renames, deletions), describe the plan first and wait for confirmation before executing.

## repository layout

The structure lands as materials do rather than being imposed up front. The starting skeleton:

```
composition/
├── README.md              overview
├── index.html             the hub landing page
├── score-studies/         close-reading guides for specific scores and passages
├── orchestration/         orchestration lessons and handouts
├── notation/              notation lessons and handouts
├── tools/                 interactive analytical and pedagogical HTML
├── assets/                the repo's own style.css, score images, audio
└── meta/                  conventions files, ours only
```

## before drafting

Before a substantial deliverable, confirm the level (lower-division, upper-division, or graduate), the area (composition, orchestration, notation, or a tool), whether it is student-facing or for planning, and any length or format constraint. For short requests, infer and proceed.
