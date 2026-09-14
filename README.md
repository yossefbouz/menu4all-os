# Menu4All Team

The Menu4All team site: **what's next, what happened, who does what, and how we get paid.**

Live: https://menu4all-os.vercel.app

| Page | What's on it |
|---|---|
| [`index.html`](index.html) — **Team page** | Calendar first (two meetings a week, Tunisia time), news feed, tasks filterable by person with the share each one earns, the pay model, every decision so far, client states, open questions, the team. |
| [`plan.html`](plan.html) — **Two-sector plan** | The Web / Marketing organisation, the shares of every contract, a **simulator** (who gets what on any amount), the marketing offers, the seven rules, this week's tasks. |
| [`presentation.html`](presentation.html) — **Team presentation** | 15 slides for the validation meeting and onboarding (arrow keys to navigate). French version: [`presentation-fr.html`](presentation-fr.html). |

Text sources, kept in French in the private repo and copied here:

- [`DECISIONS.md`](DECISIONS.md) — one line per decision since 14 July 2026, dated, signed, with proof. Latest: D-030.
- [`CLIENTS.md`](CLIENTS.md) — one state and one owner per venue.
- [`TEAM.md`](TEAM.md) — who does what (six people since 14 Sept 2026).
- [`REMUNERATION.md`](REMUNERATION.md) — the pay model by shares, the rules, three worked examples.
- [`PLAN-2026-09-DEUX-SECTEURS.md`](PLAN-2026-09-DEUX-SECTEURS.md) — the full plan.

Static site, no build: Vercel serves the files as they are.

## The four rules

1. **A decision that isn't written down doesn't exist.** One line in `DECISIONS.md` the same day: date, decision, who, why, proof.
2. **One client, one state, one owner.**
3. **We sign.** Youssef, Haroun, Bayram, Idriss, Aziz, Drago, the client by name.
4. **Proof lives in the repo** (a commit, a doc, or one sentence saying "WhatsApp of 12 Sept").

## Updating

1. Edit the source in the private repo (`menu4all-deck/ops/`): the `.md` files, and `menu4all-os.html` (this site's index), `deux-secteurs.html` (plan), the two decks.
2. Run the build script: it renames to the public file names, rewrites links, and removes client phone numbers.
3. `git commit` + `git push`, then `vercel --prod --yes` from this folder: the Vercel project is linked through the CLI, **a push alone does not redeploy**.

> Public version: client phone numbers are removed; they stay in the private repo.
