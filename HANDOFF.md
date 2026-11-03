# Parakeet Software — session handoff

One-paragraph context + every live link, so a new chat can pick up the whole build.
Paste the "Context for a new chat" block below into a fresh session to continue.

## Live links (GitHub Pages — branch `v2-oct-18-2026`)

| What | URL |
|---|---|
| **Policy console (hub — start here)** | https://clinical-trials.github.io/Parakeet/ |
| New Mexico app (Medical Psilocybin Act / SB219) | https://clinical-trials.github.io/Parakeet/app.html |
| Colorado app (Prop 122 / 1 CCR 213-1) | https://clinical-trials.github.io/Parakeet/app-co.html |
| UNM IRB forms (PDFs) | https://clinical-trials.github.io/Parakeet/forms/ |

- **Repo:** `github.com/clinical-trials/Parakeet` — **served branch: `v2-oct-18-2026`** (NOT `main`). Push only to v2; `.nojekyll` at root.
- Local checkout: `/Users/lgm/Parakeet/`
- Explainer video (local, not in git): `/Users/lgm/Parakeet/brag-output/brag.mp4`

## Context for a new chat (paste this)

> I'm building **Parakeet Software**, a psilocybin compliance/govtech platform for **New Mexico** (Medical Psilocybin Act, SB219 / 7.35.2–7.35.3 NMAC; DOH; producer/clinician/approved-setting) and **Colorado** (Prop 122 / Natural Medicine Health Act / 1 CCR 213-1; Dept. of Revenue Natural Medicine Division for businesses, DORA for facilitators), with Oregon shown for comparison. It's static single-file HTML/vanilla-JS SPAs served from GitHub Pages at `github.com/clinical-trials/Parakeet`, **branch `v2-oct-18-2026`** (push only there; `.nojekyll` at root). Local checkout `/Users/lgm/Parakeet/`: `index.html` (console hub), `app.html` (NM), `app-co.html` (CO). Live hub: https://clinical-trials.github.io/Parakeet/
>
> Key design rules: compliance-forward and text-first (no fake/animated hero art); large, user-friendly type; statutory terminology only (if a term isn't in the statute, don't use it); patient-first, "human not clinical" language; "not legal advice" removed site-wide; honest/no-fabrication (verify every PMID against PubMed before putting it on the site; prefer primary sources). Roles via RBAC; drafts saved to localStorage with try/catch.
>
> Most recent work — the **Colorado research arm** (Regulator → 🔬 Research in app-co.html): naturalistic research questions CO could answer today (inventory-only caveat); an **IRB arm routing to CU Anschutz COMIRB** (303-724-1055, comirb@ucdenver.edu, Fitzsimons Bldg 500 / MS F490, Aurora CO 80045; Mon 12–1 office hours) **and CDPHE**; and **four real, verified CU Anschutz psilocybin studies** shown across the research spectrum — Hutchison 25-0291 (naturalistic), Fischer 22-1207/NCT05398484 (double-blind RCT), Fischer 23-1455/NCT06430541 (interventional), and Fischer 25-2070 (dose-escalation in older adults, **flagged higher-risk**) — plus a Stacy Fischer, MD investigator profile with 5 PubMed-verified publications. An NM dataset/research-question card pair is on the NM research tab.

## Build path so far (what exists)

- **Console (`index.html`)**: state-aware hub linking NM/CO/OR; events roster; corrected fund amounts (SB219 §14: $1M each + $2M DOH ops) and §8 board composition.
- **New Mexico (`app.html`)**: outcomes visualization; compliance monitor; DOH site-visit inspection; lab-initiated batch **recall** (lab initiates, batch pulled from supply chain immediately, DOH notified — no added admin steps when patient safety is involved); calendar-only view; application **wizard** generalized to all license types with pop-up reg references + acknowledgements + regs quiz; save-in-progress drafts; GRT deduction connection (NMSA §7-9-73.2); **UNM IRB** research integration (consent elements, 4 downloadable attributed IRB PDFs, event-report layer, study-protocol builder); top search bar + always-on adverse-event + recall buttons; two-way secure messaging (DOH↔licensees, either side initiates); patient-first home; dataset research-question cards.
- **Colorado (`app-co.html`)**: 5 license-type application wizards with statutory acknowledgements + rule pop-ups; licensing/renewals; requirements/bulletins promulgation; inventory/chain-of-custody + COA (Total Psilocin); compliance monitor; verified healing-center directory; dev-reference regulator contact banner; **research arm** (above).
- **Outreach** (`outreach/`, local only — not published): 3 draft regulator intro emails.
- **Explainer video** (`brag-output/`, local only): 25s Colorado launch video (open-source music/SFX, app UI recreated, honest disclaimer).

## Guardrails to carry forward

- Push ONLY to `v2-oct-18-2026`; verify live via curl polling after push.
- Verify every PMID/NCT/protocol against PubMed / ClinicalTrials.gov / the official page before it goes on the live site.
- Keep `outreach/` and `brag-output/` **out of git** (draft outreach + large video).
- Real-person media/data stays private; investigator profiles use only public professional info.
