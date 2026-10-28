# Elias Ouafi

**Data Engineer — Azure & Databricks.** Île-de-France.

Je construis des pipelines de données de bout en bout : ingestion, modélisation,
orchestration, qualité et mise en production. 5 ans en data, dont 2 ans en
ingénierie de données, en France et au Canada.

## Ce que je fais

- **Pipelines & ETL** — Databricks, PySpark, Azure Synapse, SQL
- **Modélisation** — dimensionnelle (étoile, flocon), OLTP / OLAP
- **Industrialisation** — CI/CD Azure DevOps, infrastructure as code (Bicep), Git, tests
- **Qualité de données** — contrôles automatisés, couverture, fiabilisation des flux
- **Restitution** — Power BI

Aujourd'hui chez **AXA** (assurance, Nanterre) sur les pipelines et les contrôles
qualité de la souscription. Auparavant **Distech Controls** et **Matrox Video** au
Canada.

## Projets principaux

### [ou-brancher-mon-entreprise](https://github.com/Elias-Ouafi/ou-brancher-mon-entreprise) — où implanter un projet électrique de 1 à 50 MW

Une adresse française en entrée ; en sortie, la réponse à « puis-je brancher mon
projet ici ? » pour un data center, un hub de bornes de recharge, un site industriel
ou logistique : qui raccorde et à quelle échéance, la facture (prix Eurostat, part
acheminement TURPE 7), le carbone du réseau, les risques du site et le foncier.
Données publiques uniquement (RTE, Enedis, Eurostat, ADEME, Géorisques, DVF…),
chaque chiffre avec sa source et sa limite.

- **Architecture médaillon** : ingestion PySpark vers un bronze Parquet immuable,
  `MERGE` idempotent dans DuckDB, silver et gold en dbt-duckdb
- **Une vingtaine de sources ouvertes** : API paginées, quotas, nouvelles
  tentatives, repli local quand une API tombe
- **Qualité** : 473 tests sans réseau, dont un `dbt build` complet sur une base
  synthétique qui reproduit les pièges des sources ; CI GitHub Actions sur chaque PR
- **Restitution** : ligne de commande, rapports PDF et carte 3D hors ligne en three.js

![Carte 3D générée pour une adresse à Lyon](https://raw.githubusercontent.com/Elias-Ouafi/ou-brancher-mon-entreprise/main/docs/exemples/carte_lyon_decision.png)

### [breastcancer](https://github.com/Elias-Ouafi/breastcancer) — détection du cancer du sein, de la donnée brute à l'application

Le projet où je pousse le plus loin le côté ingénierie : pipeline PySpark sur le
dataset Breast Cancer Wisconsin, pipeline imagerie sur des séries DICOM (TCIA
Breast-Cancer-Screening-DBT, BreakHis), modèle de segmentation, application
d'inférence, le tout conteneurisé avec Docker et couvert par une CI GitHub Actions
et des tests.

Démo exécutable depuis un clone, sans téléchargement de dataset :

```bash
pip install -r requirements.txt
python run_demo.py
```

Les résultats et leurs limites sont documentés honnêtement dans `Final_Report.md`
et `DEMO.md`. *Research use only — ce n'est pas un dispositif médical.*

## Autres dépôts

Travaux d'analyse réalisés pendant mon MSc en Intelligence d'affaires à HEC
Montréal — NLP, statistiques, analyses multidimensionnelles sous Python et SAS.

| Dépôt | Sujet |
|---|---|
| [JournalAnalysis](https://github.com/Elias-Ouafi/JournalAnalysis) | NLP sur un corpus de presse : fusion de sources, lisibilité, performance des articles |
| [MbamAnalysis](https://github.com/Elias-Ouafi/MbamAnalysis) | Funnel marketing et arbre de décision pour le Musée des beaux-arts de Montréal |
| [Analyses_Multi](https://github.com/Elias-Ouafi/Analyses_Multi) | ACP, classification, régression logistique sous SAS |
| [InferenceAnalysis](https://github.com/Elias-Ouafi/InferenceAnalysis) | Inférence statistique sur l'espérance de vie par pays, sous SAS |

## Stack

`Python` `SQL` `PySpark` `Databricks` `Azure Synapse` `Azure Data Lake` `Bicep`
`Azure DevOps` `Git` `Docker` `Power BI`

## Me contacter

[LinkedIn](https://linkedin.com/in/ouafielias)
