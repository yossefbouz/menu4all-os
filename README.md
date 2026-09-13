# Menu4All OS

Le système d'exploitation de l'équipe Menu4All : **qui a décidé quoi, quand, et où en est chaque client.**

- **Le tableau visuel** : [`index.html`](index.html) — clients, équipe, journal des décisions (filtrable par auteur), questions à trancher, règles.
- [`DECISIONS.md`](DECISIONS.md) — une ligne par décision depuis le 14/07/2026, datée, signée, avec la preuve.
- [`CLIENTS.md`](CLIENTS.md) — un état et un responsable par établissement.
- [`TEAM.md`](TEAM.md) — qui fait quoi.

Site statique, aucun build : Vercel sert `index.html` tel quel.

## Les 4 règles

1. **Une décision non écrite n'existe pas.** Une ligne dans `DECISIONS.md` le jour même : date, décision, qui, pourquoi, preuve.
2. **Un client, un état, un responsable.**
3. **On signe.** Youssef, Haroun, Bayram, Idriss, le client par son nom.
4. **La preuve vit dans le dépôt** (commit, doc, ou une phrase qui dit « WhatsApp du 12/09 »).

## Mettre à jour

1. Modifier le `.md` concerné.
2. Reporter le changement dans les tableaux `CLIENTS` / `D` en bas de `index.html`.
3. `git commit` + `git push` → Vercel redéploie.

> Version publique : les numéros de téléphone des clients ont été retirés ; ils restent dans le dépôt privé `menu4all-deck` (`ops/`).
