
# Women's Clothing E-Commerce: Analyse de la satisfaction client

Analyse de bout en bout de 23 486 avis clients d'un site de prêt-à-porter féminin.
L'objectif : comprendre ce qui rend les clientes satisfaites, et surtout ce qui les
déçoit — pour en tirer des actions concrètes.

## Contexte

Ce jeu de données ne contient ni prix ni ventes. On n'analyse donc pas le chiffre
d'affaires, mais la **satisfaction** : notes, recommandations et commentaires écrits.

## La base de données (disponible sur Kaggle)

23 486 avis, 11 colonnes : âge de la cliente, note (/5), recommandation (oui/non),
commentaire écrit, catégorie du vêtement (division / département / classe) et utilité
de l'avis.

## Démarche

L'analyse est structurée autour de 8 questions, chacune reliée à une décision :

| # | Question | Objectif |
|---|----------|----------|
| Q0 | Les données sont-elles fiables ? | Traiter les valeurs manquantes |
| Q1 | Les clientes sont-elles satisfaites ? | Note moyenne + recommandation |
| Q2 | Quelles catégories déçoivent ? | Satisfaction par type de vêtement |
| Q3 | L'âge influence-t-il la note ? | Comparaison par tranches d'âge |
| Q4 | Positif vs négatif : qu'est-ce qui change ? | Croisement note / reco / commentaire |
| Q5 | Peut-on prédire la recommandation ? | Modèle testé avec et sans la note |
| Q6 | Que disent les mots des avis ? | Analyse de texte positif vs négatif |
| Q7 | Où sont précisément les problèmes ? | Matière & taille croisées par rayon |

## Résultats clés

- **La clientèle est globalement satisfaite** : note moyenne 4,2/5, 82 % de recommandation.
- **L'âge n'explique pas la satisfaction** : c'est l'expérience produit qui compte, pas
  le profil de la cliente (confirmé par un modèle prédictif sans la note, AUC 0,56).
- **Deux causes de déception dominent** : la matière et la taille.
- **Chaque problème a une adresse** : les robes concentrent les critiques sur la matière
  (66 % des avis négatifs), les bas sur la taille (56 %).

## Recommandations

1. Enrichir l'information sur la matière (composition, photos de texture), en priorité
   sur les robes.
2. Fiabiliser le guide des tailles, en priorité sur les bas.
3. Mettre en avant les qualités reconnues (confort, tombé) sur les produits bien notés.

## Limites

- Ce sont des avis, pas des ventes : on mesure la satisfaction, pas le chiffre d'affaires
  ni les retours réels.
- Les commentaires proviennent d'une clientèle légèrement plus critique que la moyenne
  (les clientes satisfaites écrivent moins). Les proportions sont des signaux de priorité,
  pas le ressenti de toutes les clientes.

## Outils

Python · pandas · matplotlib · scikit-learn

## Contenu du dépôt

- `analyse_women_clothing.ipynb` : le notebook complet (code, visualisations, conclusions)
- `dashboard_vetements.png` : tableau de bord de synthèse
- `data/` : le jeu de données

---

*Projet personnel réalisé dans le cadre de ma préparation à une alternance de Data Analyst,
avec l'accompagnement d'outils d'IA pour progresser plus efficacement.*
