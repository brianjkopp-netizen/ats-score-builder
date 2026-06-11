# ATS Score Builder

A reusable, portable skill that tailors any resume to any job description to clear an **80%+ ATS
match** (measured by any ATS keyword-match checker). It works as a Claude Skill, and the same
checklist works on its own as a manual process with any AI assistant or by hand.

It encodes a method refined across dozens of real applications: one that took resumes from the 50s
into the 90s on ATS keyword scans, and turned ATS rejections into recruiter screens.

---

## What it is

Applicant Tracking Systems (ATS) reject most resumes before a human ever reads them, usually for
reasons that have nothing to do with the candidate's qualifications. They reject on two things:

1. **Parseability** — whether the software can cleanly read your file (tables, graphics, odd bullets,
   and non-standard dates quietly break this).
2. **Keyword match** — whether your resume contains the job description's exact phrases, scored as
   literal string matching. "Agile" does not satisfy "Agile software development." "AI" does not
   satisfy "Artificial Intelligence."

ATS Score Builder is a 15-step checklist plus formatting standards that fix both. It does **not**
write a resume for you from nothing, and it never invents experience. It surfaces the real
qualifications you already have in the exact language the ATS is scoring.

## What it does

- Extracts the keywords a specific job description scores hardest (the ones appearing 2+ times, plus
  implicit skills the responsibilities imply).
- Flags the gap between what your resume says and what the JD wants, in exact-match terms.
- Enforces the acronym rule: every key term appears in both its acronym and spelled-out form.
- Weaves required soft skills into your summary instead of burying them in a list.
- Applies a high-impact **ALL-CAPS bullet-label** technique that raises keyword density while making
  the resume easier for a human recruiter to scan.
- Fixes the silent formatting killers: bold overuse, non-standard bullets, "&" and pipe characters,
  long-form dates, and over-long paragraphs.
- Includes scope-gap framing for applying one level above your current title.
- Gates on a sign-off step so you never fabricate a qualification you do not hold.

## What it deliberately does not do

It will not invent experience, skills, titles, or metrics. An honest 80%+ resume gets a **real**
candidate past the filter and in front of a human, which is the only thing the score is for. A resume
gamed with skills you do not have wastes everyone's time at the interview.

---

## What's in this package

```
ats-score-builder/
├── SKILL.md                          # The skill itself: the 15-step checklist + formatting standards
├── README.md                         # This file
├── LICENSE                           # MIT
├── templates/
│   └── resume_template.md            # Blank ATS-safe resume structure to build from
└── examples/
    ├── sample_job_description.md     # A realistic JD to practice against
    ├── before_resume.md              # A strong-but-untailored resume (scores low)
    ├── keyword_audit.md              # The worked audit connecting before to after
    └── after_resume.md               # The same resume after the skill (scores high)
```

Read the three example files in order — before, audit, after — to see exactly what the method changes
and why. Nothing in the "after" resume is fabricated; every change is wording or formatting.

---

## How to use it

### Option A — As a Claude Skill (recommended)

Claude Skills are folders containing a `SKILL.md` with YAML frontmatter. To use this one:

1. **Download** this repository (Code → Download ZIP, or `git clone`).
2. **Install the skill** wherever your Claude environment loads skills from. In Claude Code or the
   Claude apps that support skills, place the `ats-score-builder/` folder in your skills directory.
   Claude reads the `name` and `description` in `SKILL.md` and triggers the skill automatically when
   you ask it to tailor or score a resume.
3. **Use it.** Paste a job description and your current resume and say something like *"Tailor my
   resume to this job and get me past the ATS."* The skill runs the keyword audit first, shows you
   matched and unmatched keywords, waits for your sign-off, then builds the tailored version.

If your environment does not auto-load skills, you can paste the contents of `SKILL.md` into the
conversation as instructions and it works the same way.

### Option B — As a manual checklist (no special tooling)

The method is tool-agnostic. Open `SKILL.md`, work through the 15 steps against your resume and a
specific job posting, and apply the formatting standards. Use `templates/resume_template.md` as your
starting structure and the `examples/` files as your reference.

### Verifying the score

Run the finished resume through an ATS keyword-match checker (several free and paid options exist;
DOCX scans more reliably than PDF). Record any missed Hard Skills and Soft Skills,
add those exact strings, and rescan.

- **Target: 80%+ minimum, 90%+ for high-priority roles.**
- A near-100% score is achievable but optional; for senior roles, the high 80s to low 90s can read
  more naturally to an experienced reviewer. That is a judgment call, not a rule.

---

## The 15 steps at a glance

1. Extract JD phrases appearing 2+ times, plus implicit skills; flag proprietary terms to exclude.
2. Verify exact-match wording, not synonyms.
3. Include both acronym and spelled-out forms of every key term.
4. Weave required soft skills into the summary prose.
5. Put the exact target job title in the tagline.
6. Put city and state in the contact line.
7. Keep paragraphs under ~40 words.
8. Bold only company names and job titles.
9. Use standard round bullets only.
10. Replace "&" with "and"; keep pipes out of the body.
11. Use consistent MM/YYYY dates.
12. Lead each bullet with an ALL-CAPS exact-JD-phrase label.
13. Frame scope when applying above your current title.
14. Sign off on the keyword list before writing — never fabricate.
15. Scan, record red-X items, iterate to the target score.

Full detail and rationale for each step is in `SKILL.md`.

---

## Contributing

Issues and pull requests welcome, especially additional worked before/after examples in different
fields (the bundled example is product management; nursing, software engineering, finance, and trades
examples would all be useful).

## License

MIT — see `LICENSE`. Use it, fork it, adapt it. Attribution appreciated but not required.

## A note on intent

This method helps qualified people get read. It is for getting your **real** experience past an
automated filter, not for gaming your way into a role you are not equipped for. Used honestly, it
levels a playing field that formatting and keyword quirks have tilted against good candidates.
