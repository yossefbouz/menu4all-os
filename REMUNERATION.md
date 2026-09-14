# Menu4All — Modèle de rémunération par contrat

*Proposition du 14/09/2026 (Youssef), à valider en réunion d'équipe. Tant que ce n'est pas signé dans `DECISIONS.md`, ce sont des chiffres de travail, pas des engagements.*

## Le principe en une phrase

**Chaque dinar encaissé sur un contrat est découpé en cinq parts fixes, et chaque part va à la personne qui a fait le travail correspondant.** Pas de salaire, pas de part « parce qu'on est là » : on est payé pour signer, pour apporter, pour construire, et pour avoir bâti le socle.

## Les cinq parts d'un contrat en une fois (Bronze, Silver, Gold, Diamond, Design seul, Shooting, Lancement)

| Part | % | À qui | Pour quoi |
|---|---|---|---|
| **Signature** | **15 %** | La personne qui a mené la négociation et fait signer | Le rendez-vous, la démo, la négociation, la signature. Si deux personnes ont mené le rendez-vous ensemble : 7,5 % chacune. |
| **Apport** | **5 %** | La personne qui a trouvé le client | Le nom, le contact, la porte ouverte. Si c'est la même personne que la signature, elle cumule (20 %). |
| **Socle** | **10 %** | Youssef + Haroun (5 % chacun) | Le code de base réutilisé (Menu4All Base, espace gérant, backend, décks, outillage). Côté marketing : la part va à la **caisse** tant que le kit marketing (templates, calendrier, process) n'existe pas ; le jour où il existe, elle va à ceux qui l'ont construit. |
| **Réalisation** | **50 %** | Les personnes qui ont livré, selon les poids fixés au lancement | Le site, la carte, le module, les contenus, le shooting, la campagne. Les poids (ex. 70 / 30) sont écrits dans `DECISIONS.md` **avant** de commencer. |
| **Caisse commune** | **20 %** | Menu4All | Domaines, hébergement (Vercel Pro, Cloudflare), outils, impressions QR, déplacements, réserve. Le surplus de fin d'année est réparti selon les parts fondateurs (à définir — O-10). |

Total : 100 %.

## Les parts d'un contrat récurrent (mensuel 79/99/139/549 DT, maintenance, hébergement 50 DT/mois, packs marketing mensuels)

| Part | % | À qui | Note |
|---|---|---|---|
| **Signature** | **10 %** | Le signataire | Pendant **12 mois** seulement, puis cette part rejoint la caisse. |
| **Apport** | **5 %** | L'apporteur | Pendant 12 mois seulement, puis caisse. |
| **Réalisation** | **60 %** | Les personnes qui font le travail du mois (mises à jour de carte, contenus, suivi) | Poids fixés au lancement, révisables chaque trimestre. |
| **Caisse commune** | **25 %** | Menu4All | Idem ci-dessus. |

Pas de part « socle » sur le récurrent : le socle est payé sur la vente initiale.

## Les 7 règles

1. **Payé sur l'encaissé, jamais sur le signé.** Un contrat 1 500 DT en 40 / 30 / 30 verse 40 % des parts à la signature, 30 % après l'essai, 30 % à la fin. Si le client ne paie pas la dernière tranche, personne ne la touche.
2. **Tout est écrit avant de commencer.** À l'ouverture d'un contrat, une ligne dans `DECISIONS.md` fixe : qui a apporté, qui a signé, qui réalise et avec quels poids. Pas de ligne = pas de paiement.
3. **Un contrat, un responsable.** Le responsable du contrat est celui qui répond au client et qui déclenche les paiements. Par défaut : le responsable de secteur.
4. **Les casquettes se cumulent.** Bayram peut apporter, signer et réaliser le même contrat : il touche les trois parts.
5. **On peut vendre l'autre secteur.** Un membre marketing qui fait signer un site Gold touche la Signature (15 %) ; la Réalisation va au secteur Web. Et inversement.
6. **Le contrat mixte se découpe par ligne.** Site Gold 1 500 DT + pack marketing 450 DT/mois : la vente une fois suit la grille « une fois », le mensuel suit la grille « récurrent », chacune avec ses propres réalisateurs.
7. **Un litige se tranche à deux.** Youssef et Haroun tranchent ensemble ; la décision est écrite dans `DECISIONS.md`.

## Registre des paiements

Chaque encaissement client et chaque versement à un membre sont inscrits dans `ops/PAIEMENTS.md` (date, client, montant reçu, part, bénéficiaire, montant versé). Versement dans les **7 jours** suivant l'encaissement.

## Trois exemples chiffrés

### A — Site Gold 1 500 DT, en une fois
Bayram a trouvé le client et mené la négociation seul. Poids de réalisation fixés au lancement : Youssef 70 / Haroun 30.

| Part | Montant | Bénéficiaire |
|---|---|---|
| Signature 15 % | 225 DT | Bayram |
| Apport 5 % | 75 DT | Bayram |
| Socle 10 % | 150 DT | Youssef 75 · Haroun 75 |
| Réalisation 50 % | 750 DT | Youssef 525 · Haroun 225 |
| Caisse 20 % | 300 DT | Menu4All |

Résultat : **Bayram 300 · Youssef 600 · Haroun 300 · caisse 300.** Versé en trois fois (600 / 450 / 450 DT reçus), au prorata.

### B — Pack marketing « Croissance » 450 DT/mois
Idriss a apporté le contact, Aziz a fait signer. Réalisation du mois : Drago 60 / Aziz 40.

| Part | Montant / mois | Bénéficiaire |
|---|---|---|
| Signature 10 % | 45 DT | Aziz (12 mois) |
| Apport 5 % | 22,50 DT | Idriss (12 mois) |
| Réalisation 60 % | 270 DT | Drago 162 · Aziz 108 |
| Caisse 25 % | 112,50 DT | Menu4All |

Résultat : **Aziz 153 · Drago 162 · Idriss 22,50 · caisse 112,50**, chaque mois.

### C — Contrat mixte : Gold 1 500 DT + Croissance 450 DT/mois
Ligne 1 (site) suit l'exemple A. Ligne 2 (marketing) suit l'exemple B. Remise « deux secteurs » proposée : **10 % sur la ligne la moins chère** (à valider — O-11).

## Ce que ce modèle ne couvre pas (et qui reste à trancher)

- **Rétroactivité** : appliquer la grille à Cap Grill (1 500 DT, livré) et Caprice (montant à inscrire) ? Proposition : oui pour la part Signature/Apport de Bayram et Idriss (le terrain a été fait), les parts Réalisation et Socle restant entre Youssef et Haroun tels qu'ils l'ont déjà convenu. → O-9.
- **Parts fondateurs** sur le surplus de la caisse. → O-10.
- **Budget publicitaire** (Meta/Google Ads) : toujours payé par le client, jamais avancé par la caisse. Proposition, à confirmer. → O-12.
