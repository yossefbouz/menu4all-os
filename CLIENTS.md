# Menu4All — Tableau de bord clients

*État au 13/09/2026. Légende des états dans [README.md](README.md).*

## Le tableau

| Client | État | Pack / montant | Contact | Négocié par | Construit par | Prochaine action (qui) |
|---|---|---|---|---|---|---|
| **Cap Grill** — Marina Cap Monastir | 🟢 **LIVRÉ** | Gold — 1 500 DT (40/30/30) | Si Slim | Bayram + Idriss | Youssef + Haroun | Lancer le bloc de suppression `sql/GO-LIVE-2026-09-07.sql` puis envoyer le message de livraison (Youssef) |
| **Caprice** | 🔵 **PRÊT À LIVRER** | *(pack et prix à inscrire)* | *(à compléter)* | Bayram + Idriss | Haroun (menu) + Youssef (stock) | Vérifier que la connexion admin marche en prod (variables Vercel), fixer la date de remise (Haroun) |
| **Art+** — Flashback+ et R+ (2 salles) | 🟡 **À NÉGOCIER** | Gold ×2 + module tableau des tables — ≈ 3 000 DT visés | Amine Dababi | Bayram + Idriss | — | Mener le rendez-vous avec la proposition `clients/art/` (Bayram / Idriss) |
| **Bistrot+** | 🟡 **À NÉGOCIER** | Gold — 1 500 DT ou 139 DT/mois | *(à compléter)* | Bayram + Idriss | — | Obtenir ~15 photos du menu + nom du gérant pour préparer la démo (Bayram / Idriss) |
| **Fares** | 🟡 À NÉGOCIER | Design seul — 300 DT | Fares | Bayram + Idriss | — | Récupérer le menu + logo (Bayram / Idriss) |
| **Captain** | 🟡 À NÉGOCIER | QR hors-ligne — 300 à 800 DT selon option | Fraj Chrif | Bayram + Idriss | — | Tenir le RDV prévu début août, choisir l'option O1/O2/O3 |
| **Kavos Café** | ⚪ À QUALIFIER | — | *(à compléter)* | Bayram + Idriss | — | Identifier la catégorie et le contact |
| **Nostraliva** — Monastir | ⚫ SANS SUITE | Standard 1 190 DT/an (grille de juillet) | — | — | Youssef (paquet de pitch, 17/07) | Décider : relancer ou archiver |
| **MANEKEN** (glacier) | ⚪ PROTOTYPE | — | *(à compléter)* | — | Youssef (démo cliquable, 07/09) | Dire si c'est un prospect réel ou une démo générique |

**Pipeline signé ou livré :** Cap Grill 1 500 DT + Caprice *(montant à inscrire)*.
**Pipeline à négocier (grille d'août) :** ≈ 3 000 + 1 500 + 300 + 300–800 ≈ **5 100 à 5 600 DT**.

---

## Fiches

### Cap Grill — 🟢 LIVRÉ
- **En ligne :** https://capgrill.org · carte https://capgrill.org/menu.html · espace gérant https://capgrill.org/admin.html
- **Ce qui est livré :** vitrine, carte 128 plats en 6 langues, QR de table (menu consultatif — les serveurs saisissent les commandes), espace gérant complet (commandes temps réel, plan de salle 60 tables, réservations, journal + graphiques, carte du jour prix/ruptures), compte service, guide serveurs, décks de formation FR/EN.
- **Comptes :** `admin@capgrill.tn` (gérant), `service@capgrill.tn` (salle), `youssefbouzgarrouyb1@gmail.com` (fondateurs), `gabrielle@capgrill.org` (gérant supplémentaire, créé le 13/09 — **activer avec `sql/0008`**).
- **Reste à faire (hors code) :** bloc de suppression GO-LIVE (Youssef, à la main), message de livraison au patron (rédigé, non envoyé), validation des prix `(?)` par Si Slim, mot de passe du compte service choisi par le patron, impression des QR 31–60 vers capgrill.org, facture 1 500 DT.
- **Docs :** `clients/resto-cap-grill/docs/HANDOFF.md` (Loops 1–10), `RAPPORT-RECETTE-2026-09-08.md`, `MESSAGE-CLIENT-MISE-EN-PRODUCTION.md`.

### Caprice — 🔵 PRÊT À LIVRER
- **Dépôt :** `new client/caprice/` → GitHub `youssefbouzgarrouyb1-droid/caprice`, projet Vercel `caprice`.
- **Menu (Haroun, 03/09) :** site public FR/EN/AR, 16 catégories avec photos (cafés, thés, jus, mojitos, crêpes, paninis, tacos, plats, chicha…), QR, admin avec éditeur de prix (login par mot de passe haché + JWT, Supabase via clé service côté serveur).
- **Stock (Youssef, 05/09) :** registre d'inventaire, mouvements en journal jamais effacé, position de stock, point de commande, dates de danger/rupture, suggestions de commande par fournisseur, tableau de bord avec projection 14 jours ; présentation client 16 slides (`site/presentation.html`).
- **Point ouvert (06/09) :** le login admin en prod exige 5 variables d'environnement sur Vercel (`ADMIN_PASSWORD_HASH` notamment) — le doc est corrigé, **vérifier qu'elles sont posées**.
- **À inscrire :** pack vendu, prix, contact du gérant, date de remise.

### Art+ (Flashback+ et R+) — 🟡 À NÉGOCIER
- **Le besoin :** cafés d'études, règle « une consommation toutes les 2 h » ; tableau des tables en direct (vert libre / rouge consommation / orange dépassé / gris occupé sans commande).
- **Préparé :** proposition `clients/art/ART-Menu4All-Presentation-FR.html` (+ EN), 10 slides, septembre 2026, **avec une grille tarifaire différente de celle d'août** (voir D-018).
- **Manque :** les deux menus, le nombre de tables par salle, confirmation de la règle des 2 h.

### Bistrot+ — 🟡 À NÉGOCIER
- **Le besoin :** petite surface très fréquentée, prix qui bougent (pénuries), ruptures quotidiennes → édition de prix instantanée + bascule « épuisé ».
- **Stratégie décidée (05/08) :** gérant méfiant (a déjà essayé le numérique) → on arrive avec **son** menu déjà en ligne, on lui fait changer un prix devant lui. Le mensuel (139 DT) est l'angle le plus facile.
- **Manque :** photos du menu (~15 articles), nom/logo, nom et téléphone du gérant.

### Fares / Captain / Kavos / Nostraliva / MANEKEN
Voir le tableau ; détails dans `MASTER-PLAN-2026-08.md` (Fares, Captain, Kavos), `clients/nostraliva/docs/` et `new client/maneken/README.md`.
