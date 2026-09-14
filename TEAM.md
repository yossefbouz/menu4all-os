# Menu4All — L'équipe et ce que chacun a livré

*Mis à jour le 13/09/2026. Les chiffres de commits viennent de `git log` (dépôt principal + dépôt `caprice`).*

## Vue d'ensemble

| Personne | Rôle | Depuis | Identité git |
|---|---|---|---|
| **Youssef Bouzgarrou** | Co-fondateur — produit, développement, analyse business, décks et rapports | Juillet 2026 | `youssef` (61 commits ici + 3 dans `caprice`) |
| **Haroun Rhim (Kafteji)** | Co-fondateur — développement | Août 2026 | `Kaftej1` (7 commits ici) · `Haroun Rhim <harounkafteji@gmail.com>` (4 commits dans `caprice`) |
| **Bayram** | Négociateur — prospection terrain et négociation avec les établissements | Août 2026 | — (pas de commits, travail terrain) |
| **Idriss** | Négociateur — prospection terrain et négociation avec les établissements | Août 2026 | — (pas de commits, travail terrain) |
| **Aziz** | Secteur Marketing (contenus, réseaux sociaux) — *rôle exact à confirmer* | Septembre 2026 | — |
| **Drago** *(prénom à confirmer)* | Secteur Marketing (contenus, réseaux sociaux) — *rôle exact à confirmer* | Septembre 2026 | — |
| Claude (Opus 5 / Sonnet 5 / Fable 5.1) | Assistant de développement en binôme, co-auteur des commits | Juillet 2026 | `Co-Authored-By` dans les messages de commit |

### Organisation proposée le 14/09/2026 (D-029, à valider)

| Secteur | Membres | Responsable proposé |
|---|---|---|
| **Web** — sites, cartes, QR, espace gérant, modules, maintenance | Youssef, Bayram, Haroun | Youssef |
| **Marketing** — réseaux sociaux, contenus, shooting, campagnes | Haroun, Idriss, Aziz, Drago | Haroun |

Tout membre peut apporter et signer un client dans les deux secteurs. Rémunération par parts : voir [REMUNERATION.md](REMUNERATION.md) ; plan complet : [PLAN-2026-09-DEUX-SECTEURS.md](PLAN-2026-09-DEUX-SECTEURS.md).

Compte partagé de l'entreprise : `youssefbouzgarrouyb1@gmail.com` (GitHub `youssefbouzgarrouyb1-droid`, Vercel, Supabase). Règle du 08/08/2026 : cette identité sert **uniquement** à Menu4All.

---

## Youssef — ce qu'il a livré

**Cap Grill (juillet → septembre 2026)** — responsable du client de bout en bout.
- 26/07 : paquet client complet (vitrine + carte trilingue FR/EN/AR, offre 1 500 DT) — `cf1794b`
- 31/07 : vraie carte transcrite depuis les photos des ardoises (12 sections, ~100 plats), 16 photos Instagram, QR + cartes de table — `09fe9af`, `2b01ebe`
- 05/08 : **Loop 1 Gold** — commande à table, espace gérant, 6 langues, 30 QR, backend commutable Supabase/local — `8478454`
- 06/08 : base Supabase en production, modèle de sécurité RLS — `38d4551`, `9a65880`
- 12/08 : Loops 3 à 6 — fiche table, saisie serveur, réservations, CRUD complet, 13/13 tests prod, guide serveurs — `e654a5d` → `0b5b81a`
- 18–19/08 : couche motion GSAP, logo officiel, 17 visuels — `b615cf3`, `6c08f78`
- 21–23/08 : Loop 7–8 — journal du service, carte du jour (prix & ruptures), graphiques SVG maison, dashboard mobile — `521d84f`, `a645400`
- 24/08 : Loop 9 — compte service (deux niveaux d'accès), **menu consultatif (commande client désactivée)** — `1de58ea`, `e0097d3`
- 27/08 : Loop 10 — 60 tables, réservations visibles sur le plan, transfert de table — `2995bf9`
- 03–04/09 : **capgrill.org** (Cloudflare DNS → Vercel), référencement ouvert, Search Console — `3cbf7a9`
- 07–08/09 : mise en production (audit réel de la base, sauvegarde, script GO-LIVE), recette complète avant démo — `9e27ac4`, `f5d2318`

**Caprice (septembre 2026)** — le **module de stock**.
- 05/09 : espace inventaire complet (registre, mouvements, projection 14 jours, suggestions de commande), refonte admin, présentation client 16 slides — `9eef760`, `089fd98`
- 06/09 : diagnostic du login admin cassé en prod (variables d'environnement Vercel manquantes) — `a93b796`

**Pilotage & vente**
- 14/07 : concept de base réutilisable (un code, un JSON par client) — `menu4all-prototype-loop-prompt.md`
- 17/07 : premier paquet d'acquisition (Nostraliva) + décks Menu4All — `caec030`
- 05/08 : **Master plan** (5 clients, 3 catégories, packs officiels, 6 loops) + dossier partenaire Word — `8d9012f`, `92fb6c6`
- 05–07/08 : présentation client Cap Grill FR + EN, détail du prix 1 500 DT, page hébergement — `306ceb1` → `90b3007`
- 21/08 : rapport hébergement (le gratuit tient ×30, clause commerciale Vercel) — `3367a1f`
- 02–03/09 : proposition ART (FR + EN), nouvelle grille tarifaire — `clients/art/`
- 07/09 : prototype de démonstration MANEKEN (système glacier : site, commandes, factures, stock, tournées) — `new client/maneken/`

## Haroun — ce qu'il a livré

**Cap Grill**
- 10/08 : **Loop 2** — plan de salle (30 tables, statut dérivé des commandes, « Libérer la table »), compte `admin@capgrill.tn` créé dans Supabase, correction du bug `hidden`/`display` qui bloquait le panier et l'écran de connexion — `96e5804`, `8d92986`
- 13/08 : support de formation du personnel (15 slides) ; correction des 6 décks qui ne défilaient plus sur certains Chrome (scroll-snap + smooth) — `691f0da`, `da103db`, `994bf41`, `33dbb63`
- 20/08 : support de formation en PDF + CSS d'impression — `7afcd9a`

**Caprice** — le **menu digital** (dépôt séparé `youssefbouzgarrouyb1-droid/caprice`).
- 03/09 : site menu public FR/EN/AR avec photos par catégorie, connexion admin + éditeur de prix sur Supabase, fonctions Vercel, serveur local SQLite — `cd80966`
- 03/09 : connexion du dépôt à Vercel, redéploiements, correction du crash `/api/admin/login` en prod — `f5c930e`, `eb5b01b`, `e4d9a80`

## Bayram et Idriss — ce qu'ils ont fait

Prospection et négociation sur le terrain, sans trace git ; à consigner par eux dans `DECISIONS.md` au fil de l'eau.

**Leur approche :** ils vont voir le gérant directement, identifient la catégorie de l'établissement (touristique / local premium / café d'études) et la douleur du quotidien, puis passent la main à Youssef et Haroun pour une démo sur le menu réel du client. Cinq à six établissements approchés à ce jour : Cap Grill, Caprice, Art+, Bistrot+, et les petits tickets (Fares, Captain). *Qui a mené quel rendez-vous : à préciser par eux.*

| Établissement | Contact obtenu | Résultat connu au 14/09 |
|---|---|---|
| Cap Grill | Si Slim | Signé (Gold 1 500 DT) — livré |
| Caprice | *(à compléter)* | Accord — menu + stock construits, prêt à livrer |
| Art+ (Flashback+ et R+) | Amine Dababi | Contact pris, proposition préparée, **négociation pas encore menée** |
| Bistrot+ | *(à compléter)* | Identifié, **négociation pas encore menée** |
| Fares | (tél. dans le dépôt privé) | Identifié (design seul, 300 DT) |
| Captain | Fraj Chrif | Identifié (QR hors-ligne), RDV prévu début août |
| Kavos Café | *(à compléter)* | Nom seulement |

## Cap Grill : un travail à deux

Youssef et Haroun ont développé Cap Grill **côte à côte** : Youssef a porté l'architecture, la carte, le backend et les loops 1, 3–10 ; Haroun a livré le plan de salle (loop 2), le compte gérant, la formation du personnel et les correctifs d'affichage transversaux. Cap Grill est **marqué LIVRÉ** le 13/09/2026 (en ligne sur capgrill.org depuis le 03/09, recette de production passée le 08/09).
