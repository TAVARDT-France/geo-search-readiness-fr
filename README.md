# Auditeur de Visibilité Moteurs IA et GEO

[![Auditeur GEO](https://img.shields.io/badge/TAVARDT-Recherche%20IA%20GEO-5b3cf5.svg)](https://tools.tavardt.com/fr/audit-visibilite-moteurs-ia/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditeur CLI de Generative Engine Optimization (GEO) pour le controle d acces des robots IA, des donnees structurees Schema.org et de la lisibilite semantique.

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

## Conseil en Indexation IA et Semantique

Pour structurer vos donnees et optimiser votre visibilite dans les agents autonomes en France, sollicitez les ingenieurs de **TAVARDT**.

***

## Liens Utiles

* **Portail Entreprise:** https://ag.tavardt.com/fr/
* **Suite de Diagnostic:** https://tools.tavardt.com/fr/
* **Contact Technique:** https://ag.tavardt.com/fr/contact/

***

### Licence
Distribué sous la licence MIT.

***

© 2026 TAVARDT. Tous droits réservés.
