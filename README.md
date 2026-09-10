# IAM Quest — a 21-day Identity & Access Management concepts handbook

An interactive, self-contained study handbook that teaches Identity and Access
Management (IAM) from zero — built to prepare for an IT Enterprise Security
internship in Identity & Access Management.

It's a single HTML file: 21 days of concepts across three weeks, plus a Day 0
orientation and a 20-question final exam. Everything runs in the browser with no
build step, no dependencies, and no internet connection required.

## Live version

If GitHub Pages is enabled for this repo (see below), the handbook is available at:

```
https://<your-username>.github.io/<repo-name>/IAM-Concepts-Handbook.html
```

## What's inside

- **Day 0 — Orientation:** the two questions IAM exists to answer, and a map of the whole field.
- **Week 1 — Foundations (Days 1–7):** Active Directory; DNS/ports/time; certificates; Kerberos; SAML; OAuth; a consolidation day.
- **Week 2 — Modern & Governance (Days 8–14):** OIDC & JWTs; provisioning & SCIM; MFA & passkeys; Zero Trust; IGA lifecycle; IGA certification & SoD; a consolidation day.
- **Week 3 — Privileged & Cloud (Days 15–21):** PAM; secrets management; cloud identity (AWS/Entra); non-human identities & CIEM; AppSec scanning; identity as a data problem; a capstone.
- **Final Exam:** 20 questions across all three weeks, auto-graded, with a per-week breakdown and a full answer scheme.

Each day has plain-language explanations, custom diagrams, "mental model" and
"watch for" callouts, an interactive quiz with instant feedback, and a
self-check with revealable model answers.

## Progress tracking

Progress is saved automatically in your browser (via `localStorage`):

- Days you mark complete stay ticked between visits.
- The XP bar and level in the sidebar reflect how far you've got.
- Your final-exam score is remembered.

Because it uses browser storage, progress is per-browser and per-device — it
won't sync across machines, and clearing your browser data will reset it.

## Running it

Just open `IAM-Concepts-Handbook.html` in any modern browser — double-click the
file, or serve the folder with any static server. No installation needed.

## Hosting it yourself on GitHub Pages

1. Push this repo to GitHub (see `SETUP.md` for the exact commands).
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Choose the `main` branch and the `/ (root)` folder, then **Save**.
4. Wait a minute, then visit the URL shown at the top of the Pages settings.

## Repository layout

```
.
├── IAM-Concepts-Handbook.html   # the handbook (open this)
├── README.md                    # this file
├── SETUP.md                     # step-by-step git + Pages instructions
└── LICENSE                      # license for your own write-ups
```

## Credits & scope

This is a personal study aid built to accompany a separate hands-on lab manual.
It focuses on concepts and mental models, not click-by-click lab steps. Content
is original study material; verify anything security-critical against primary
sources (Microsoft Learn, IDPro, OWASP, NIST) before relying on it at work.
