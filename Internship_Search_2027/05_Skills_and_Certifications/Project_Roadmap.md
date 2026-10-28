# Feuille de route des projets portfolio

Point de départ : tes deux projets sont **terminés mais privés**. Un recruteur ne peut donc rien vérifier avant l'entretien. Statut de toutes les lignes ci-dessous : **non commencé**. Rien n'entre au CV avant d'être terminé et confirmé par toi.

## Option 0 (la plus rentable) — rendre vérifiable ce qui existe déjà
- **Pricing, couverture et risques d'options** : si le code t'appartient (projet personnel, ou projet académique dont le règlement autorise la publication), nettoie-le et publie-le avec un README (méthodes, résultats, tests). Charge : 6 à 10 h. **Question à trancher** : cadre du projet et droit de publier.
- **Market making RL (équipe de 6)** : ne publie qu'avec l'accord de l'équipe ; sinon, un résumé technique de **ta** partie (sans code) peut figurer sur ton profil.

## P1 — Bibliothèque de pricing C++20 + Python (familles : Quant Analyst / Quant Dev / Pricing / Structuring)
- **Périmètre** : Payoff, Model, Engine ; Black–Scholes analytique ; Monte Carlo (antithétique, variable de contrôle) ; Crank–Nicolson ; Greeks (bump-and-reprice avec nombres aléatoires communs) ; pybind11 ; comparaison avec QuantLib.
- **Livrables** : dépôt public, README avec courbes de convergence, tests unitaires, CI.
- **Validation** : écart avec la formule fermée < 1e-3 ; parité call-put ; Greeks Monte Carlo et EDP cohérents.
- **Charge** : 40 à 60 h · **Stack** : C++20, CMake, GoogleTest ou Catch2, Python, pybind11.
- **Démontrer** : lien GitHub sur le CV + 2 graphiques dans le README.

## P2 — Moteur de risque de marché « façon FRTB » (familles : Market Risk / Model Validation / Asset Management)
- **Périmètre** : portefeuille multi-actifs sur données publiques ; VaR historique et filtrée (FHS) ; ES à 97,5 % ; horizons de liquidité ; stress tests historiques ; backtesting (Kupiec, Christoffersen, feux tricolores de Bâle) ; rapport rédigé comme une note de validation de modèle.
- **Référence** : Basel Framework MAR — https://www.bis.org/basel_framework/standard/MAR.htm
- **Charge** : 30 à 45 h · **Stack** : Python, pandas, NumPy, SciPy, pytest.
- **Recouvrement** : ce projet ressemble à ton projet privé. Choisis entre l'Option 0 et P2, ne fais pas les deux.

## P3 — Scoring crédit et ECL IFRS 9 (famille : Credit Risk)
- **Périmètre** : modèle de PD (régression logistique, WoE/IV, Gini/AUC, calibration) sur le jeu Kaggle « Give Me Some Credit » ; staging et ECL simplifiés ; documentation de validation.
- **Données** : https://www.kaggle.com/c/GiveMeSomeCredit (conditions d'usage Kaggle à respecter).
- **Charge** : 25 à 35 h.

## P4 — Provisionnement IARD (famille : Actuariat)
- **Périmètre** : Chain Ladder, Mack (erreur de prévision), Bornhuetter–Ferguson sur des triangles publics ; analyse de sensibilité.
- **Outil** : chainladder (CAS) — https://github.com/casact/chainladder-python
- **Charge** : 15 à 25 h.

## Arbitrage conseillé
Au plus deux projets avant janvier 2027, pour ne pas freiner les candidatures : **P1** (si tu vises d'abord quant / pricing), puis **Option 0 ou P2** (risque de marché). P3 et P4 seulement si une offre de crédit ou d'actuariat devient prioritaire.

---

## Mise à jour du 2026-10-14 — projets par famille (cibles : marchés et investissement)

Statut de toutes les lignes : **non commencé**. Détails et ordre conseillé dans le plan « Plan de candidature – marchés et investissement » (Claude Docs).

| Famille | Projet | Charge | Livrable | Ligne CV après achèvement |
|---|---|---|---|---|
| Quant (Natixis Algo Trading, QRT) | Exécution optimale (Almgren–Chriss) et probabilité de fill sur le carnet d'ordres C++ simulé | 25–35 h | Dépôt public, tests, README avec coûts d'exécution vs benchmark TWAP | « Exécution optimale sur carnet d'ordres – Python, C++ » + lien |
| Trading, structuration | Pricer d'autocall : Monte Carlo, Greeks par bump (nombres aléatoires communs), sensibilité vol/corrélation, interface Excel/VBA | 30–40 h | Dépôt + classeur Excel/VBA | « Pricer d'autocall – Monte Carlo, Greeks – Python, Excel/VBA » |
| Sales, product specialist | Note de marché hebdomadaire d'une page (taux, actions, volatilité) | 2 h/semaine pendant 6–8 semaines | Notes publiées (LinkedIn ou PDF) | « Note de marché hebdomadaire, N numéros » |
| Gestion d'actifs, sélection de fonds | Comparateur d'allocations (60/40, minimum variance, risk parity, Black–Litterman) avec coûts, factsheet mensuelle ; variante due diligence de fonds (Fama–French, analyse de style) | 30–40 h (variante 15–20 h) | Dépôt + factsheet PDF ; données Kenneth French Data Library | « Allocation d'actifs et factsheet – Python » |
| Recherche quant en gestion d'actifs | Bibliothèque de stress tests multi-actifs (scénarios historiques et hypothétiques) — sujet d'un ancien IREF chez Amundi en 2025 | 25–35 h | Dépôt avec tests et documentation | « Bibliothèque de stress tests – Python » |
| Private equity, dette privée | Modèle LBO Excel d'une ETI française cotée + mémo d'investissement d'une page en anglais | 20–30 h | Classeur + mémo PDF | « Modèle LBO et mémo d'investissement – Excel » |
| Risque de marché | Option 0 : publier le projet options/VaR avec backtesting documenté (Kupiec, feux tricolores) | 6–10 h | Dépôt public | Lien GitHub sur le projet existant |

Règle inchangée : au plus 5 à 6 h par semaine tant que des candidatures prioritaires sont ouvertes ; au plus deux projets avant janvier 2027.
