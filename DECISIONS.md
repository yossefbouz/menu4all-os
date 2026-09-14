# Menu4All — Journal des décisions

*Une ligne par décision, du premier jour à aujourd'hui. Reconstitué le 13/09/2026 depuis les commits, les rapports et les décks ; à partir de maintenant, on l'alimente le jour même.*
*Format : voir [README.md](README.md). Les hashs renvoient au dépôt principal sauf mention « caprice ».*

---

## Juillet 2026 — fondations

### D-001 — 2026-07-14 — Un seul code, un JSON par client
**Décision :** Menu4All Base = un code réutilisable ; onboarder un client = un dossier de JSON (marque, menu, config) + assets, sans toucher au code. Mobile-first, multilingue (AR/FR/EN/DE/IT, RTL), QR brandé, zéro dépendance CDN.
**Qui :** Youssef. **Pourquoi :** vendre vite à plusieurs établissements sans refaire un site à chaque fois.
**Preuve :** `menu4all-prototype-loop-prompt.md`.

### D-002 — 2026-07-17 — Le pattern « paquet d'acquisition » par client
**Décision :** chaque prospect reçoit un dossier `clients/<slug>/` : recherche (chaque fait marqué OBSERVED/ASSUMED), `brand.json`, `menu-vision.json`, déck de pitch, plan de vente, handoff. Premier exemplaire : Nostraliva. Grille de lancement : 690 / 1 190 / 1 890 DT par an, échéancier **40 % signature · 30 % après essai 7 jours · 30 % sur 3 mois**.
**Qui :** Youssef. **Preuve :** `caec030`, `clients/nostraliva/docs/HANDOFF.md`.

### D-003 — 2026-07-26 — Cap Grill : offre 1 500 DT en une fois, site sans framework
**Décision :** offre unique 1 500 DT (site vitrine + carte trilingue + QR + mise en ligne), même échéancier 40/30/30. Techniquement : HTML/CSS/JS pur, aucun build, tout le contenu dans `js/data.js`.
**Qui :** Youssef. **Pourquoi :** un restaurant gastronomique sans aucune présence web ; simplicité = déployable et modifiable par n'importe qui.
**Preuve :** `cf1794b`, `clients/resto-cap-grill/docs/OFFER-1500.md`.

### D-004 — 2026-07-27 — Règles techniques transversales
**Décision :** jamais de classes CSS `ad-*` (les bloqueurs de pub cachent les éléments — préfixe `mg-`) ; site en `noindex` tant que le patron n'a pas validé ; page 404 brandée.
**Qui :** Youssef. **Preuve :** `4aa4af3`, README racine « Gotchas ».

### D-005 — 2026-07-31 — Aucun prix inventé : la carte réelle fait foi
**Décision :** les prix publiés sont ceux transcrits des 4 photos des ardoises fournies par le patron ; les quelques lignes incertaines sont marquées `(?)` et doivent être validées par Si Slim avant facturation. Photos : uniquement celles de l'Instagram du restaurant.
**Qui :** Youssef (photos : Si Slim). **Pourquoi :** les estimations sous-évaluaient la carte de 15 à 90 %.
**Preuve :** `09fe9af`, `docs/CARTE-REELLE-2026-07-31.md`.

---

## Août 2026 — le plan, puis Cap Grill Gold

### D-006 — 2026-08-04 — Master plan approuvé : 5 clients, 3 catégories, packs officiels
**Décision :** segmentation A touristique / B local premium / C café d'études ; packs **Bronze 800 · Silver 1 000 · Gold 1 500 · Diamond 6 000 DT** en une fois (ou 79 / 99 / 139 / 549 DT par mois) ; **Design seul 300 DT** ; **Maintenance 50–100 DT par 2 mois**. Ordre d'exécution : Cap Grill → Fares → Bistrot+ → Flashback+/R+ → Captain.
**Qui :** Youssef (approbation). **Preuve :** `8d9012f`, `MASTER-PLAN-2026-08.md` §5, `Menu4All-Dossier-Partenaire-Aout-2026.docx`.

### D-007 — 2026-08-05 — Cap Grill Loop 1 : Supabase comme backend, 6 langues, WiFi par QR
**Décision :** backend Supabase (gratuit) avec bascule automatique en prototype localStorage si non configuré ; 6 langues (la 6ᵉ offerte en geste commercial) ; 2 QR par table (menu + WiFi) ; canal WhatsApp en secours pour les commandes.
**Qui :** Youssef. **Preuve :** `8478454`, HANDOFF « Loop 1 ».

### D-008 — 2026-08-06 — Modèle de sécurité : clés publiques + RLS
**Décision :** l'URL et la clé « publishable » vivent dans le code du site (publiques par nature) ; la protection vient des policies RLS : un visiteur ne peut qu'**insérer** une commande/réservation, rien lire. La clé `service_role` n'apparaît jamais dans le dépôt. Corollaire découvert : jamais de `.select()` après un insert client.
**Qui :** Youssef. **Preuve :** `38d4551`, `9a65880`, README racine « Security model ».

### D-009 — 2026-08-07 — L'hébergement se vend comme un service payant
**Décision :** l'hébergement est présenté au client comme une prestation professionnelle (page « Vercel Pro », 99 DT/an réels — pas 2,75 DT/mois) ; **abonnement 50 DT/mois à partir de la 2ᵉ année** ; le prix 1 500 DT est détaillé en 6 lignes dans le déck ; version anglaise du déck conservée à côté de la française pour Si Slim.
**Qui :** Youssef. **Preuve :** `144d033`, `4d364d6`, `fb52ff6`, `90b3007`.

### D-010 — 2026-08-08 — Règle des comptes : une identité Menu4All, rien d'autre
**Décision :** `youssefbouzgarrouyb1@gmail.com` (GitHub `youssefbouzgarrouyb1-droid`, Vercel, Supabase) sert **uniquement** à Menu4All et est partagé par les deux fondateurs ; tout le reste sur les comptes personnels. Chaque machine doit committer avec l'email Menu4All, sinon Vercel ne construit pas.
**Qui :** Youssef. **Preuve :** `358a671`, README racine « Accounts — the golden rule ».
> ⚠️ Écart constaté : le domaine capgrill.org (03/09) et la Search Console sont sur le compte **personnel** `youssefbouzgarrouyb@gmail.com` — à régulariser ou à documenter comme exception.

### D-011 — 2026-08-10 — Plan de salle : le gérant libère la table à la main
**Décision :** une table redevient « libre » **uniquement** quand la caisse clique « Libérer la table » — aucun automatisme. Compte gérant `admin@capgrill.tn` créé (Auto Confirm). Règle CSS : tout élément togglé par `hidden` reçoit `.x[hidden]{display:none}`.
**Qui :** Haroun. **Preuve :** `96e5804`, `8d92986`, HANDOFF « Loop 2 ».

### D-012 — 2026-08-12 — Le staff crée ; une commande envoyée ne se modifie pas
**Décision :** les serveurs saisissent commandes et réservations depuis l'espace gérant ; « modifier » une commande = nouvelle commande sur la même table (addition cumulée), erreur = annuler + refaire. Réservation prise par téléphone = née « confirmée ». Le compte partagé Menu4All devient second admin (`sql/0003`). Plats au poids : jamais commandables en ligne (pesée cuisine).
**Qui :** Youssef. **Preuve :** `6ebb7e3`, `e654a5d` → `0b5b81a`, `docs/RAPPORT-TESTS-2026-08-12.md` (13/13).

### D-013 — 2026-08-13 — Formation du personnel en déck, et les décks sans `scroll-behavior: smooth`
**Décision :** un support de formation de 15 slides (~20 min, finit par une mise en pratique) devient un livrable standard ; règle technique pour tous les décks : jamais `smooth` avec `scroll-snap mandatory`.
**Qui :** Haroun. **Preuve :** `691f0da`, `da103db`, `33dbb63`.

### D-014 — 2026-08-21 — La carte de référence reste dans le code ; la base ne stocke que les exceptions
**Décision :** `js/data.js` = carte de référence (noms, photos, traductions, prix normaux) ; la table `menu_overrides` ne contient que les prix du jour et les ruptures, supprimés dès qu'on « remet à la carte ». Journal du service = relecture des commandes servies, aucune donnée nouvelle. Espace gérant refait pour le téléphone (barre d'onglets en bas).
**Qui :** Youssef. **Preuve :** `521d84f`, HANDOFF « Loop 7 ».

### D-015 — 2026-08-21 — Hébergement gratuit assumé pour l'instant ; choix reporté à la remise officielle
**Décision :** le gratuit (Vercel Hobby + Supabase Free) tient ×30 clients ; le vrai risque est la clause « usage non commercial » de Vercel Hobby. À la remise officielle : **Cloudflare Pages (0 DT, commercial autorisé) ou un seul Vercel Pro pour tout le portefeuille** — décision business **encore ouverte**. Supabase : ping hebdomadaire anti-pause + export CSV avant toute fermeture longue.
**Qui :** Youssef (recommandation). **Preuve :** `3367a1f`, `docs/RAPPORT-HEBERGEMENT-2026-08.md`.

### D-016 — 2026-08-23 — Graphiques dessinés à la main, jamais deux échelles
**Décision :** graphiques du journal en SVG maison (rien à télécharger en salle) ; une seule échelle Y par graphe, étiquettes sélectives, jumeau tabulaire pour l'accessibilité. Base de production remplie de données de démo pour la présentation au patron (194 commandes).
**Qui :** Youssef. **Preuve :** `a645400`, `docs/DEMO-2026-08-23.md`.

### D-017 — 2026-08-24 — Deux niveaux d'accès, et la commande client désactivée
**Décision (demande du gérant) :** compte `service@capgrill.tn` pour la salle : commandes, plan, réservations — **sans** Journal ni La Carte. Barrière dure en SQL sur la carte (`is_main_admin`), Journal masqué par l'interface seulement (choix assumé et documenté). Et : **`selfOrdering: false`** — le QR ouvre une carte consultative, les commandes passent par les serveurs ; réactivable en un déploiement.
**Qui :** Si Slim (demande), Youssef (mise en œuvre). **Preuve :** `1de58ea`, `e0097d3`, `sql/0006_staff_service.sql`.

### D-018 — 2026-08-27 — 60 tables, réservations visibles, transfert de table
**Décision (demandes du gérant) :** le restaurant compte 60 tables (et non 30) ; toute réservation non annulée du jour s'affiche sur la tuile de sa table quel que soit l'état ; transfert de table sans recréer la commande.
**Qui :** Si Slim (demande), Youssef. **Preuve :** `2995bf9`, `sql/0007_tables_60.sql`.

---

## Septembre 2026 — mise en ligne, Caprice, nouveaux prospects

### D-019 — 2026-09-02 — Proposition ART avec une NOUVELLE grille tarifaire
**Décision :** le déck ART affiche **Bronze 1 000 · Silver 1 300 · Gold 2 000 · Diamond 7 500 DT**, design seul **400 DT**, maintenance **100 DT/mois**, hébergement et QR inclus — au-dessus de la grille officielle d'août (D-006).
**Qui :** Youssef. **Preuve :** `clients/art/ART-Menu4All-Presentation-FR.html`.
> ❓ **À trancher :** laquelle des deux grilles est officielle à partir de septembre ? (Le master plan, le dossier partenaire et le déck Menu4All disent encore 800/1 000/1 500/6 000.)

### D-020 — 2026-09-03 — capgrill.org, et le site devient visible sur Google avant la validation des prix
**Décision :** domaine capgrill.org acheté chez Cloudflare, DNS « DNS only » vers Vercel, `www` et `capgrill.vercel.app` redirigés en 308 (les QR imprimés continuent de marcher). Référencement **ouvert** (`noindex` retiré, sitemap, Schema.org) à la demande de Youssef « le plus joignable possible » — **avant** la validation des prix par le patron, en connaissance de cause.
**Qui :** Youssef. **Preuve :** `3cbf7a9`, HANDOFF « Domaine officiel ».

### D-021 — 2026-09-03 — Caprice : dépôt séparé, architecture différente de Cap Grill
**Décision :** Caprice vit dans son propre dépôt (`youssefbouzgarrouyb1-droid/caprice`) et son propre projet Vercel ; l'admin passe par des **fonctions serveur** (login mot de passe haché + JWT, Supabase avec la clé service côté serveur) et non par RLS + auth Supabase comme Cap Grill. Menu public FR/EN/AR par catégories avec photos.
**Qui :** Haroun. **Preuve :** caprice `cd80966`, `e4d9a80`.
> Conséquence à assumer : deux architectures à maintenir. À décider un jour : laquelle devient le standard pour les prochains clients.

### D-022 — 2026-09-05 — Répartition Caprice : Haroun le menu, Youssef le stock
**Décision :** Youssef prend le module de gestion de stock (modèle de réapprovisionnement transparent et déterministe : position de stock, point de commande, dates de danger/rupture, suggestion de commande ; « historique insuffisant » plutôt qu'une fausse précision). Un modèle probabiliste ne viendra qu'après 8–12 semaines de données réelles.
**Qui :** Youssef (avec Haroun). **Preuve :** caprice `9eef760`, `INVENTORY_PLAN.md`, `site/presentation.html` (16 slides).

### D-023 — 2026-09-06 — Les 5 variables d'environnement Caprice sont obligatoires sur Vercel
**Décision :** le login admin de prod ne peut fonctionner sans `ADMIN_PASSWORD_HASH` (+ 4 autres) posées dans Vercel ; le hash se génère en une ligne, le mot de passe en clair n'est écrit nulle part.
**Qui :** Youssef. **Preuve :** caprice `a93b796`, `server/.env.example`.

### D-024 — 2026-09-07 — Cap Grill passe en production : audit réel, sauvegarde, suppression à la main
**Décision :** on relève l'état **réel** de la base avant d'agir (235 commandes = tests et démo, aucun vrai service) ; sauvegarde dans un schéma `backup` ; le bloc `delete` de `sql/GO-LIVE-2026-09-07.sql` est lancé **à la main par Youssef** (l'assistant n'exécute jamais de suppression) ; message de livraison rédigé, à envoyer **après** le nettoyage. Prototype MANEKEN (système glacier) construit le même jour.
**Qui :** Youssef. **Preuve :** `9e27ac4`, `c2c3204`, `docs/MESSAGE-CLIENT-MISE-EN-PRODUCTION.md`.

### D-025 — 2026-09-08 — Recette de production avant démo : « prêt »
**Décision :** tout le public est testé sur la vraie prod (93 assets, 128 plats × 6 langues, formulaire réel, redirections, Lighthouse) ; 4 correctifs déployés ; le dashboard connecté reste à tester à la main. Verdict : prêt pour la démo.
**Qui :** Youssef. **Preuve :** `f5d2318`, `docs/RAPPORT-RECETTE-2026-09-08.md`.

### D-026 — 2026-09-13 — Création de ce système d'exploitation ; états des clients arrêtés
**Décision :** l'équipe tient un journal des décisions, un tableau clients et une fiche équipe dans `ops/`. États arrêtés ce jour : **Cap Grill = LIVRÉ**, **Caprice = PRÊT À LIVRER**, **Bistrot+ et Art+ = À NÉGOCIER** (aucune négociation menée). Rôles : Bayram et Idriss prospectent et négocient ; Youssef et Haroun développent côte à côte ; sur Caprice, Haroun a fait le menu, Youssef le stock.
**Qui :** Youssef. **Preuve :** `ops/`.

### D-027 — 2026-09-13 — Compte gérant supplémentaire Cap Grill : gabrielle@capgrill.org
**Décision :** un accès **gérant complet** (5 onglets) pour Gabrielle. Email `gabrielle@capgrill.org` (le domaine `.tn` est refusé par Supabase à l'inscription), mot de passe convenu oralement (format « Prénom + année »). Le compte a été créé par l'API publique de sign-up, donc **non confirmé** : `sql/0008_admin_gabrielle.sql` le confirme et l'ajoute à `is_main_admin()` — **à lancer dans le SQL Editor**.
**Qui :** Youssef. **Preuve :** `sql/0008_admin_gabrielle.sql`.
> ⚠️ Découvert au passage : **l'inscription publique est ouverte** sur le projet Supabase capgrill (n'importe qui peut créer un compte ; sans danger grâce aux RLS par email, mais le README recommandait de la fermer). À faire : Authentication › Sign In / Providers › Email › désactiver « Allow new users to sign up ».

### D-028 — 2026-09-14 — Les négociateurs ont un nom : Bayram et Idriss
**Décision :** l'équipe compte quatre personnes. **Bayram** et **Idriss** portent la prospection et la négociation ; Youssef et Haroun le développement. Leur approche : aller voir le gérant, nommer la catégorie et la douleur, puis passer la main pour une démo sur le menu réel. Établissements approchés : Cap Grill, Caprice, Art+, Bistrot+ (+ Fares, Captain). Reste à préciser par eux qui a mené quel rendez-vous.
**Qui :** Youssef. **Preuve :** `ops/TEAM.md`.

### D-029 — 2026-09-14 — Deux secteurs, six personnes, rémunération par parts — PROPOSÉ, à valider
**Décision (proposée) :** Menu4All s'organise en deux secteurs vendant à la même clientèle : **Web** (Youssef, Bayram, Haroun — responsable Youssef) et **Marketing** (Haroun, Idriss, Aziz, Drago — responsable Haroun). Tout membre peut apporter et signer un client dans les deux secteurs. Chaque contrat encaissé se découpe en parts fixes : en une fois **Signature 15 % · Apport 5 % · Socle 10 % · Réalisation 50 % · Caisse 20 %** ; récurrent **Signature 10 % (12 mois) · Apport 5 % (12 mois) · Réalisation 60 % · Caisse 25 %**. Payé sur l'encaissé ; rôles et poids écrits ici avant de commencer. Offres marketing proposées : Présence 250 DT/mois, Croissance 450 DT/mois, Shooting 300 DT, Lancement 600 DT.
**Qui :** Youssef (proposition), à valider par les six en réunion la semaine du 15/09. **Pourquoi :** l'équipe grandit et personne ne savait comment répartir ; un modèle par parts paie le travail réellement fait, quel que soit le secteur.
**Preuve :** `ops/PLAN-2026-09-DEUX-SECTEURS.md`, `ops/REMUNERATION.md`.
> ❓ Reste à trancher en réunion : O-9 à O-13 ci-dessous. Tant que cette ligne dit « PROPOSÉ », rien n'est dû à personne sur cette base.

---

## Décisions encore ouvertes (à trancher)

| # | Question | Qui tranche | Depuis |
|---|---|---|---|
| O-1 | Grille tarifaire officielle : août (800/1 000/1 500/6 000) ou septembre (1 000/1 300/2 000/7 500) ? | Youssef | D-019, 02/09 |
| O-2 | Hébergement à la remise : Cloudflare Pages ou un Vercel Pro pour tout le portefeuille ? | Youssef + Haroun | D-015, 21/08 |
| O-3 | Architecture standard des prochains clients : modèle Cap Grill (RLS + auth Supabase) ou modèle Caprice (API serveur + JWT) ? | Youssef + Haroun | D-021, 03/09 |
| O-4 | Caprice : pack vendu, prix, échéancier, date de remise | Bayram + Idriss | — |
| O-5 | Remise 2 salles Art+ (Flashback+ / R+) | Youssef | D-006 |
| O-6 | Nostraliva et MANEKEN : prospects réels ou archives ? | Youssef | — |
| O-7 | Domaine capgrill.org sur le compte personnel : régulariser ou documenter l'exception ? | Youssef | D-010 |
| O-8 | Fermer l'inscription publique sur le projet Supabase capgrill (découvert le 13/09 : ouverte) | Youssef | D-027, 13/09 |
| O-9 | Rétroactivité de la grille de rémunération sur Cap Grill (1 500 DT) et Caprice | Youssef + Haroun + Bayram + Idriss | D-029, 14/09 |
| O-10 | Parts fondateurs sur le surplus de la caisse commune en fin d'année | Youssef + Haroun | D-029, 14/09 |
| O-11 | Remise « deux secteurs » (site + marketing) : 10 % sur la ligne la moins chère ? | Youssef + Haroun | D-029, 14/09 |
| O-12 | Budget publicitaire toujours payé par le client, jamais avancé par la caisse ? | Haroun | D-029, 14/09 |
| O-13 | Prénoms et rôles exacts des nouveaux (Aziz, Drago, Idriss) ; responsable Marketing confirmé ? | Youssef | D-029, 14/09 |
