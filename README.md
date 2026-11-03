
# Projet 13 — Amélioration du contrôle qualité des stocks

## Présentation du projet

Ce projet s'inscrit dans mon parcours de formation Data Analyst chez OpenClassrooms.

Il consiste à améliorer les contrôles de qualité des données de stock de Bottleneck, en utilisant Python et l'intelligence artificielle comme outil d'assistance technique.

L'objectif est de détecter les anomalies dans les données ERP, de comparer plusieurs approches et de proposer une méthode de contrôle plus robuste, sans modifier les données d'origine.

## Objectifs

- Vérifier la cohérence entre les quantités de stock et les statuts enregistrés.
- Détecter les quantités négatives et les valeurs manquantes.
- Identifier les statuts de stock manquants ou inconnus.
- Comparer plusieurs méthodes de contrôle.
- Documenter les expérimentations et les décisions techniques.
- Préserver les données ERP d'origine.

## Technologies utilisées

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Microsoft Excel
- ChatGPT (assistance à l'analyse et à la documentation)

## Méthodologie

Le projet repose sur quatre expérimentations successives :

1. Détection initiale des incohérences avec Pandas.
2. Calcul automatique du statut attendu avec NumPy.
3. Analyse des limites et des cas particuliers.
4. Mise en place de contrôles renforcés avec Pandas et NumPy.

Les règles métier utilisées sont les suivantes :

- Quantité supérieure à 0 : statut attendu `instock`.
- Quantité égale à 0 : statut attendu `outofstock`.
- Quantité négative : anomalie.
- Quantité manquante : anomalie.
- Statut manquant ou différent des valeurs autorisées : anomalie.
- Incohérence quantité/statut : anomalie.

## Résultats obtenus

| Indicateur | Résultat |
|---|---:|
| Produits analysés | 825 |
| Incohérences détectées initialement | 2 |
| Produits présentant une anomalie après amélioration | 4 |
| Taux final d'anomalies | 0,48 % |
| Produits supplémentaires identifiés | 2 |

### Répartition des anomalies

| Type d'anomalie | Nombre |
|---|---:|
| Quantités négatives | 2 |
| Incohérences quantité/statut | 2 |
| Quantités manquantes | 0 |
| Statuts manquants | 0 |
| Statuts inconnus | 0 |

La méthode renforcée a permis d'identifier deux produits supplémentaires présentant des quantités négatives.

## Utilisation critique de l'intelligence artificielle

ChatGPT a été utilisé pour proposer et comparer des approches de contrôle, identifier les limites des premières méthodes et structurer les expérimentations.

Les propositions ont été examinées et testées dans Jupyter Notebook. Les résultats ont été vérifiés à partir des règles métier et des données ERP.

Les prompts documentés sont des reconstitutions et non des transcriptions exactes des échanges originaux. Les versions précises des modèles utilisés restent à confirmer.

L'intelligence artificielle a joué un rôle d'assistance. La validation des résultats et les décisions techniques sont restées sous la responsabilité du Data Analyst.

## Tests et validation

Onze tests fonctionnels ont été réalisés, couvrant notamment :

- Le chargement et la structure des données.
- La détection des anomalies de quantité et de statut.
- Le calcul du bilan consolidé.
- L'identification des produits concernés.
- La préservation des données d'origine.

Des tests complémentaires sur des données synthétiques restent nécessaires pour les situations absentes du fichier ERP réel.

## Limites et perspectives

- Les données sources ne sont pas publiées afin de respecter leur confidentialité.
- Aucune correction automatique n'est appliquée aux données ERP.
- Les contrôles pourront être complétés par des tests synthétiques.
- La documentation et les résultats pourront être enrichis pour faciliter la réutilisation de la méthode.

## Auteur

**Roger AGNEROH**  
Data Analyst Junior — OpenClassrooms

Compétences : Python, SQL, Power BI, Excel, analyse de données et tableaux de bord.
