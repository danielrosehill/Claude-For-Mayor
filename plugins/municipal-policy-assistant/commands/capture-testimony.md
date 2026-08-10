---
description: Clean a raw dictated testimony into a dated, redacted testimony file (stage 1 of the pipeline)
argument-hint: <path to raw file in testimonies-raw/, or paste the raw text>
---

Process a raw first-person testimony about living in the city into a publishable record. Follow the `municipal-policy-methodology` skill's rules throughout.

Input: $ARGUMENTS — either a path to a raw file (typically in `testimonies-raw/`, which is gitignored) or the raw text pasted directly.

## Steps

1. **Read the raw material.** If it's an audio file, transcribe it first (a transcription MCP tool may be available; otherwise ask the user for a transcript).
2. **Clean it**:
   - Remove disfluencies ("um", false starts, repeated words) and dictation artifacts (mis-transcribed terms — e.g. "arnona" rendered as "our nona"; garbled street and neighbourhood names, which dictation gets wrong constantly and which matter here).
   - Preserve the first-person voice, tone, and **every factual claim exactly as stated**. Cleaning never adds claims, softens them, strengthens them, or changes numbers. If a passage is ambiguous, keep the ambiguity or ask.
   - Organize into sections with headings if the account is long.
3. **Redact**: remove or generalize full names of private individuals, exact addresses, and identifying details of third parties. Public figures, municipal officials acting in their role, and institutions stay named.
   - Municipal testimony de-anonymises easily: a street, a building, a school and a date together identify a household. **Generalise to the neighbourhood by default.** Where the specific location is the substance of the account, keep it but flag it in your report so the user can confirm.
4. **Write the file** to `testimonies/YYYY-MM-DD-<policy-area>.md` (today's date unless the user specifies when the account was given), with this frontmatter:
   ```yaml
   ---
   title: <short title>
   date: YYYY-MM-DD
   policy-area: <kebab-case-area>
   status: cleaned
   source: <one line describing the raw source and where it is retained privately>
   ---
   ```
5. **Update the index table** in `testimonies/index.md`.
6. **Create or update the policy-area tracker** at `policy/<area>/index.md` with the pipeline stage table (see an existing area for the format, or `policy/index.md` if this is the first) and mark stage 1 complete. Add the area to the tables in `policy/index.md`, `tasks.md`, `README.md` and the `planks` array in `site/src/pages/index.astro` — all five are kept in step, per `CLAUDE.md`.
7. **Extract research hooks**, into two separate lists in the tracker's "Scope notes" section:
   - **Facts to establish** — every claim needing quantification or legal verification at the research stage.
   - **Attributions to test** — every point where the account assumes a particular body is responsible. These go straight to `/map-powers`, and they are frequently wrong in an interesting way. Do not correct them in the testimony; the testimony records what the resident believed, and the gap between that and the powers map is itself a finding.

Never commit anything from `testimonies-raw/`. Confirm the raw file is covered by `.gitignore` before committing.
