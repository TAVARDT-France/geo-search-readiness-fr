# Auditeur de Visibilité Moteurs IA et GEO

[![Auditeur GEO](https://img.shields.io/badge/TAVARDT-Recherche%20IA%20GEO-5b3cf5.svg)](https://tools.tavardt.com/fr/audit-visibilite-moteurs-ia/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Auditeur CLI de Generative Engine Optimization (GEO) pour le controle d acces des robots IA, des donnees structurees Schema.org et de la lisibilite semantique.

Developpe et maintenu par la division d ingenierie semantique et d indexation IA de **TAVARDT**.

***

## Fonctionnalites d Audit GEO

* **Acces des Robots d Indexation IA**: Analyse des directives dans `robots.txt` pour les agents tels que GPTBot, OAI-SearchBot, PerplexityBot, ClaudeBot et Google-Extended.
* **Extraction d Entites Semantiques**: Verification du balisage structure Schema.org en JSON-LD.
* **Signaux Semantiques Fondamentaux**: Controle des balises H1 et des meta descriptions pour l extraction par les modeles d IA.
* **Score d Eligibilite**: Evaluation algorithmique sur 100 points accompagnee d axes prioritaires de correction.

***

## Installation et Utilisation

Fonctionne avec Python 3.8 ou superieur sans bibliotheque externe.

```bash
git clone https://github.com/TAVARDT-France/geo-search-readiness-fr.git
cd geo-search-readiness-fr
python geo_auditor.py entreprise.fr
```

Pour exporter les donnees en JSON:

```bash
python geo_auditor.py entreprise.fr -json
```

***

## Diagnostic Web en Ligne

Pour des analyses poussees et un suivi continu de votre presence dans les moteurs IA, consultez l outil officiel:

* **Auditeur de Recherche IA et GEO**
* **[Portail Entreprise TAVARDT](https://ag.tavardt.com/fr/)**

***

## Conseil en Indexation IA et Semantique

Pour structurer vos donnees et optimiser votre visibilite dans les agents autonomes en France, sollicitez les ingenieurs de **TAVARDT**.

***

© 2026 TAVARDT. Tous droits réservés.
