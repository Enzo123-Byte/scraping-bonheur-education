# Scraping — Bonheur & Éducation par pays

Constitution d'un jeu de données pays par pays croisant **scores de bonheur** et **indices d'éducation**, à partir de sources publiques.

## Objectif

Produire un CSV exploitable reliant, pour chaque pays :

- les scores du **World Happiness Report** ;
- les **indices d'éducation** : Education Index, taux d'alphabétisation, taux de scolarisation.

## Pipeline

1. **Récupération** — requêtes HTTP sur les sources publiques, avec en-têtes navigateur pour éviter les blocages.
2. **Extraction** — parsing HTML (BeautifulSoup, lxml, html5lib) et lecture des tableaux.
3. **Normalisation** — harmonisation des noms de pays entre sources, qui est la principale difficulté de l'exercice.
4. **Consolidation** — jointure des sources et export.

## Contenu

| Fichier | Description |
|---|---|
| `Projet/scraping_bonheur_education.ipynb` | Le notebook complet, du fetching à l'export |
| `Projet/happiness_education_dataset.csv` | Le jeu de données produit |

## Stack

Python · requests · BeautifulSoup · pandas · NumPy

## Licence

MIT — voir [LICENSE](LICENSE).
