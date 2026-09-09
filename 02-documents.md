# Module 2 — Documents

Skills that create, read, and edit real office files.

## Skills covered

| Skill | Handles | Trigger it by saying… |
|-------|---------|-----------------------|
| `docx` | Word documents (`.docx`, `.dotx`) | "Word doc", "letter", "memo as a .docx" |
| `pdf`  | PDF files | "make a PDF", "merge these PDFs", "extract text from this pdf" |
| `pptx` | PowerPoint (`.pptx`, `.potx`) | "PowerPoint", "slide deck as .pptx" |
| `xlsx` | Spreadsheets (`.xlsx`, `.csv`, …) | "spreadsheet", "clean this CSV", "add a column and total it" |

## When each one fires

The rule of thumb: **name the file format and the skill triggers.** These skills are for
when the deliverable *is the file* — something you'll download, email, or print.

- Say "Word document" or ".docx" → `docx`
- Say "PDF" or point at a `.pdf` → `pdf`
- Say "PowerPoint" or ".pptx" → `pptx`
- Say "spreadsheet", ".xlsx", or point at a ".csv" → `xlsx`

> **Nuance:** If you ask for a "report" or "slides" *without* naming a format, Claude may
> prefer a live Artifact or a connected document tool instead of a file. If you want an
> actual Office file, say so.

## Worked examples

**Word:**
> **You:** draft a one-page project kickoff memo as a .docx, with a title, three sections, and today's date

Claude uses `docx`, produces a formatted `.docx`, and hands you the file.

**PDF (manipulation, not just creation):**
> **You:** merge `intro.pdf` and `appendix.pdf` into one file, appendix last

Claude uses `pdf` to combine them. The `pdf` skill also does splitting, rotating,
watermarking, form-filling, and OCR on scanned PDFs.

**PowerPoint:**
> **You:** turn the outline in `pitch.md` into a 6-slide .pptx

Claude uses `pptx`. It can also *read* an existing deck — e.g. "pull all the text out of
`deck.pptx`" triggers it even though you're extracting, not creating.

**Spreadsheet:**
> **You:** this CSV has headers on row 3 and junk rows — clean it into a proper xlsx with a total row

Claude uses `xlsx` to restructure and compute.

## Common mistakes

- **Asking for "slides" and getting an Artifact instead of a file.** Say ".pptx" if you
  need the file.
- **Expecting the `pdf` skill for a Google Doc.** These skills are for the named file
  types only.
- **Huge spreadsheets:** describe the transformation clearly (which column, what formula)
  — the skill computes real formulas, so precision helps.

## Try it

1. Create a scratch `notes.md` with a few bullet points.
2. Ask for it three ways and watch which skill triggers each time:
   - "…as a Word doc"
   - "…as a PDF"
   - "…as a PowerPoint"
3. Then make a small CSV and ask Claude to "add a column that sums the others as an xlsx."

Next: [Module 3 — Artifacts & Design](03-artifacts-and-design.md)
