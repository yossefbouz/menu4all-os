# Menu4All OS

Le site de l'équipe Menu4All : **qui a décidé quoi, quand, où en est chaque client, et comment on se paie.**

En ligne : https://menu4all-os.vercel.app

| Page | Ce qu'on y trouve |
|---|---|
| [`index.html`](index.html) — **Tableau de bord** | Clients (un état, un responsable), équipe, journal des décisions filtrable, questions à trancher, les 4 règles. |
| [`deux-secteurs.html`](deux-secteurs.html) — **Plan deux secteurs** | L'organisation Web / Marketing, les parts de chaque contrat, un **simulateur** (qui touche quoi sur un montant donné), les offres marketing, les 7 règles, qui fait quoi cette semaine. |
| [`presentation-deux-secteurs.html`](presentation-deux-secteurs.html) — **Présentation d'équipe** | 15 slides pour la réunion de validation et l'onboarding des nouveaux (flèches du clavier pour naviguer). |

Les sources en texte, à côté :

- [`DECISIONS.md`](DECISIONS.md) — une ligne par décision depuis le 14/07/2026, datée, signée, avec la preuve. Dernière : D-029 (deux secteurs, **proposée**).
- [`CLIENTS.md`](CLIENTS.md) — un état et un responsable par établissement.
- [`TEAM.md`](TEAM.md) — qui fait quoi (six personnes depuis le 14/09/2026).
- [`REMUNERATION.md`](REMUNERATION.md) — le modèle de rémunération par parts, les règles, trois exemples chiffrés.
- [`PLAN-2026-09-DEUX-SECTEURS.md`](PLAN-2026-09-DEUX-SECTEURS.md) — le plan complet.

Site statique, aucun build : Vercel sert les fichiers tels quels.

## Les 4 règles

1. **Une décision non écrite n'existe pas.** Une ligne dans `DECISIONS.md` le jour même : date, décision, qui, pourquoi, preuve.
2. **Un client, un état, un responsable.**
3. **On signe.** Youssef, Haroun, Bayram, Idriss, Aziz, Drago, le client par son nom.
4. **La preuve vit dans le dépôt** (commit, doc, ou une phrase qui dit « WhatsApp du 12/09 »).

## Mettre à jour

1. Modifier le `.md` concerné dans le dépôt privé (`menu4all-deck/ops/`).
2. Reporter le changement dans les tableaux `CLIENTS` / `D` en bas de `index.html`, ou dans `deux-secteurs.html` si c'est le modèle de rémunération qui change.
3. Recopier ici (les numéros de téléphone des clients sont retirés au passage), `git commit` + `git push` → Vercel redéploie.

> Version publique : les numéros de téléphone des clients ont été retirés ; ils restent dans le dépôt privé.
