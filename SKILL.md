---
name: ats-score-builder
description: >
  Use this skill whenever someone wants to build, rewrite, or score a resume against a specific job
  description to pass an Applicant Tracking System (ATS) and clear an 80%+ keyword match. Triggers
  include: "tailor my resume to this job", "score my resume against the JD", "run an ATS check",
  "ATS prep", "help me get past the ATS", "why isn't my resume getting responses", or any request
  pairing a resume with a job posting. Also trigger when someone pastes a job description and asks "how
  do I match up" or "rewrite this for the role" — treat that as an ATS tailoring request. Run the
  keyword audit first, every time, before writing any resume content.
---

# ATS Score Builder

A reusable method for tailoring any resume to any job description to clear an 80%+ ATS match
(measured by any ATS keyword-match checker). This is a keyword-and-formatting discipline, not a
content-invention exercise. Never fabricate experience, skills, titles, or metrics the candidate does
not actually hold. The goal is to surface real qualifications in the exact language the ATS scores.

The checklist runs **before** writing. Tailoring after the fact produces lower scores and weaker resumes.

Bundled references in this skill folder:
- `examples/sample_job_description.md` — a realistic JD to practice the audit against
- `examples/before_resume.md` — a strong-but-untailored resume (scores low)
- `examples/after_resume.md` — the same resume after applying this skill (scores high)
- `examples/keyword_audit.md` — the worked Step 1–3 audit that connects the two
- `templates/resume_template.md` — a blank ATS-safe structure to build from

---

## How ATS scoring works (the model to keep in mind)

An ATS scores a resume on two axes:

1. **Searchability / parseability** — can the system read the file, find the job title, location,
   dates, and section headers? Formatting failures (tables, graphics, odd bullets, special characters,
   non-standard dates) silently drop the score here even when the content is strong.
2. **Keyword match** — does the resume contain the skills, tools, and phrases from the JD, in the exact
   forms the JD uses? This is literal string matching, not semantic understanding. "Agile" does not
   satisfy "Agile software development." "AI" does not satisfy "Artificial Intelligence."

Most resumes lose points on both axes for fixable reasons. This skill closes both.

---

## Workflow — always run in this order

### Step 1 — Phrase extraction (from the JD)

- Extract every skill, tool, certification, title, and responsibility phrase that appears **2 or more
  times** in the JD. Repetition signals what the employer is scoring hardest.
- Surface **implicit** skills the responsibilities imply but never name (e.g., "owns the design
  handoff" implies "wireframes," "mockups," "prototyping").
- Flag **proprietary or internal program names** (e.g., a company's internal platform codename). Do
  NOT force these into the resume. ATS systems do not score proprietary terms as required keywords, and
  inserting them looks artificial.
- Build two lists: **matched** (already in the resume) and **unmatched** (gaps to address).

### Step 2 — Exact-match verification

The ATS matches strings literally. Confirm each extracted phrase appears **verbatim**, not as a synonym.

| Resume says | JD wants | Result |
|---|---|---|
| "continuous optimization" | "continuous improvement" | Miss |
| "Agile" | "Agile software development" | Miss |
| "customer-focused" | "customer focus" | Miss (hyphenation differs) |
| "led teams" | "cross-functional collaboration" | Miss |

A shorter form does not cover a longer form, and vice versa. Match the JD's exact wording, including
hyphenation and word order.

### Step 3 — Acronym rule (both forms required)

Every acronym in the JD must appear in **both** the acronym and the spelled-out form, at least once each:

- AI **and** "Artificial Intelligence"
- ROI **and** "Return on Investment"
- KPI / KPIs **and** "Key Performance Indicators"
- SDLC **and** "Software Development Lifecycle"
- SaaS, API, CRM, B2B, etc. — same rule, plus their expansions

A common clean way to satisfy both: first use spells it out with the acronym in parentheses, e.g.
"Artificial Intelligence (AI)," then later uses can run the acronym alone.

### Step 4 — Soft skills woven into prose

- Soft skills that appear **2 or more times** in the JD must be woven into the **summary/profile as
  natural language**, not parked only in a skills list. Many ATS configs and human reviewers weight
  in-context usage over a bare list.
- High-frequency trap words to always check: collaboration, accountability, communication, ownership,
  adaptability, continuous improvement, stakeholder management, influence.
- Missing soft skills in the summary is one of the most common reasons a score stalls below 80%.

### Step 5 — Job title match

- The **exact job title string** from the posting must appear in the resume tagline — the line directly
  under the candidate's name. Use the verbatim string, not an approximation.
- Tagline placement reliably satisfies the ATS Job Title Match check; burying it only in the summary
  often does not.
- If the current/most-recent title differs from the target, the tagline is where you bridge that gap
  (see Step 13).

### Step 6 — Contact line

- City and state (and country if applying internationally) must appear in the contact line. ATS uses
  location for candidate matching and geo-filtered searches.
- Include a professional email, phone, and LinkedIn URL on the same header block.

### Step 7 — Paragraph length

- No paragraph block longer than ~40 words. ATS parsers and recruiters both skim.
- Role intro lines: two sentences maximum, each under ~30 words.
- If a summary runs long, split it into two or three discrete short blocks. This alone has lifted
  flagged scores.

### Step 8 — Bold styling discipline

- Reserve bold for **company names and job titles only**.
- No bold on bullet labels, no bold in prose paragraphs or the summary.
- ATS scanners frequently flag "too much bold styling" as a formatting error. Use ALL-CAPS labels
  (Step 12) for emphasis instead — they read as emphasis to a human without tripping the bold flag.

### Step 9 — Bullet characters

- Use **standard round bullets** throughout. No hyphens, asterisks, arrows, checkmarks, or decorative
  glyphs as bullet markers.
- Non-standard bullet characters cause parse failures that silently drop content from the scan.

### Step 10 — Special characters

- Use commas, not pipes (|), inside skills lists.
- Replace "&" with "and" in competency lines and taglines. The ampersand commonly triggers a special-
  character warning.
- A pipe in the contact/header line is usually tolerated, but avoid pipes elsewhere in body content.
- Avoid em dashes; use commas, colons, periods, or restructured sentences.

### Step 11 — Date formatting

- Use MM/YYYY throughout, e.g. `01/2022 – 01/2026`.
- Avoid long-form month names ("January 2022") and year-only ranges ("2022–2026"). Inconsistent or
  non-standard date formats reliably drop the Searchability score.
- Keep one date format across the entire document.

### Step 12 — ALL-CAPS bullet-label strategy (highest-impact technique)

This is the single most effective move for raising keyword density without harming readability.

- Lead each experience bullet with the **exact JD keyword phrase in ALL CAPS**, followed by a colon,
  then the achievement.
- Example: `ARTIFICIAL INTELLIGENCE AND DIGITAL TRANSFORMATION: Led the rollout of an AI governance
  framework across four product teams, cutting review cycle time by 30 percent.`
- Use the verbatim JD phrase in the label, not a paraphrase.
- Benefit is double: it raises ATS keyword match AND gives a human reviewer a scannable left-margin
  index of exactly the competencies they posted for.
- Do not bold these labels — the ALL-CAPS treatment carries the emphasis.

### Step 13 — Scope/level gap framing (when the title is below target)

When the candidate's current title sits below the target level (e.g., Director applying for VP):

- Address it directly in the summary. Do NOT write "functioning as a VP" — that phrasing announces the
  gap instead of closing it.
- Use the pattern: `"Most recent role carried [Exact Target Title] scope:"` followed by four concrete
  scope signals:
  1. Portfolio / budget dollar size
  2. Executive or board-level accountability
  3. Team or organization span
  4. Governance or P&L ownership
- Let the metrics close the gap. The statement simply gives the reader permission to read the rest of
  the resume at the target level.

### Step 14 — Pre-build sign-off gate

Before writing any resume content, present back to the user:

1. The **matched** keyword list (already covered).
2. The **unmatched** keyword list, separating **genuine, addressable gaps** (real experience not yet
   surfaced) from **non-addressable gaps** (skills the candidate does not hold) and **proprietary
   terms** (ignore).
3. Get explicit confirmation before proceeding. Never invent experience to close a non-addressable gap.

This gate prevents both wasted rewrites and dishonest resumes.

### Step 15 — Scan, verify, iterate

- Build v1, then scan it with an ATS keyword-match checker (DOCX scans more reliably than PDF).
- Record every red-X item from the Hard Skills and Soft Skills tables — those are the exact strings to
  add in v2.
- **Target: 80%+ minimum; 90%+ for high-priority roles.**
- A near-perfect 100% is achievable but optional. Some experienced reviewers read a 100% keyword match
  as gamed; for senior roles, landing in the high 80s/low 90s can read more natural. Treat this as a
  per-role judgment call, not a rule.
- Do not recommend submission below the 80% floor.

---

## Formatting standards (apply on every build)

| Element | Standard |
|---|---|
| Font | One clean sans-serif (Arial or Calibri), black text, left-aligned |
| Layout | Single column. No tables, text boxes, headers/footers, images, or columns — they break ATS parsing |
| Section headers | Standard, literal names: "Experience," "Education," "Skills," "Certifications" |
| Skills section | Comma-separated prose or a simple comma list. No tables, no pipes |
| Dates | MM/YYYY, consistent throughout |
| Bullets | Standard round bullets only |
| Bold | Company names and job titles only |
| Special characters | "and" not "&"; no em dashes; no decorative glyphs |
| File format | Submit DOCX unless the posting requires PDF; DOCX parses most reliably |

---

## Quick pre-build checklist (final gate before writing)

- [ ] JD keywords (2+ occurrences) extracted; matched vs. unmatched lists built
- [ ] Implicit skills surfaced; proprietary terms flagged and excluded
- [ ] Both acronym and spelled-out forms present for every key term
- [ ] Soft skills woven into the summary prose, not only listed
- [ ] Exact job title in the tagline, verbatim
- [ ] City/state in the contact line
- [ ] No paragraph over ~40 words
- [ ] Bold limited to company names and job titles
- [ ] Standard round bullets only
- [ ] "&" replaced with "and"; pipes confined to the header
- [ ] Dates in consistent MM/YYYY format
- [ ] ALL-CAPS bullet labels using exact JD phrases
- [ ] Scope-gap framing in the summary if the title is below target
- [ ] Sign-off gate completed with the user before writing
- [ ] No fabricated experience, skills, titles, or metrics anywhere

---

## Core principle

The ATS rewards literal keyword matching and clean parsing. This skill makes a candidate's **real**
qualifications legible to that system in the JD's own language. It never invents qualifications. An 80%+
score gets a real resume past the filter and in front of a human — which is the only thing the score is
for.
