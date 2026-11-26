<p align="center">
  <a href="https://ag.tavardt.com/fr/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Auditeur d'Optimisation pour Moteurs Génératifs (GEO)

[![Auditeur GEO](https://img.shields.io/badge/TAVARDT-Recherche%20IA%20GEO-5b3cf5.svg)](https://tools.tavardt.com/fr/audit-visibilite-moteurs-ia/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Moteur d'évaluation automatisé pour Generative Engine Optimization (GEO) et Answer Engine Optimization (AEO), analysant l'accès des robots d'IA, les entités Schema.org et les signaux de citation sémantique.

L'outil évalue la visibilité des environnements web au sein des architectures de génération augmentée par récupération (RAG) utilisées par SearchGPT, Perplexity AI, Claude, Gemini et Apple Intelligence. Conçu sans aucune dépendance logicielle externe, il fonctionne nativement dans la console Python et au sein des chaînes de déploiement continu.

***

## Capacités d'Évaluation GEO et Périmètre Algorithmique

Le référencement classique se concentrait sur la répétition de mots-clés et l'autorité des liens. Les moteurs génératifs actuels rédigent des réponses contextuelles en interrogeant des graphes de connaissances structurés et des sources d'information fiables.

* **Contrôle des Directives pour Robots d'IA**: Vérification rigoureuse des autorisations dans le fichier `robots.txt` pour les agents majeurs: GPTBot, OAI-SearchBot, PerplexityBot, ClaudeBot, Google-Extended et Applebot-Extended.
* **Extraction d'Entités Sémantiques**: Validation de la présence de métadonnées Schema.org au format JSON-LD (`application/ld+json`), permettant aux modèles d'IA de contextualiser marques et produits.
* **Hiérarchie Sémantique et Balises Clés**: Contrôle des titres H1 et des balises méta description afin d'assurer un découpage textuel optimal lors de l'indexation.
* **Notation Algorithmique de Préparation GEO**: Score quantitatif de 0 à 100 points segmentant le domaine en Haute Visibilité, Visibilité Modérée ou Accès Restreint.
* **Performance et Zéro Dépendance**: Code exécutable via la bibliothèque standard de Python, garantissant des vérifications quasi instantanées sur toute machine.

***

## Matrice de Vérification et de Notation GEO

<table>
  <thead>
    <tr>
      <th align="left">Dimension Évaluée</th>
      <th align="left">Pondération</th>
      <th align="left">Règle de Validation Technique</th>
      <th align="left">Impact sur la Synthèse et les Citations par l'IA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Présence du robots.txt</strong></td>
      <td>20 Points</td>
      <td>Code HTTP 200 valide sur l'adresse /robots.txt.</td>
      <td>Assure aux robots d'exploration une lecture directe des règles de crawl.</td>
    </tr>
    <tr>
      <td><strong>Autorisation des Robots d'IA</strong></td>
      <td>30 Points</td>
      <td>Absence d'instruction Disallow: / bloquant les robots cibles.</td>
      <td>Évite l'exclusion du domaine des sources citées dans les moteurs conversationnels.</td>
    </tr>
    <tr>
      <td><strong>Schema.org JSON-LD</strong></td>
      <td>30 Points</td>
      <td>Présence de balises application/ld+json valides dans le code.</td>
      <td>Apporte un ancrage explicite des entités dans les graphes de connaissances globaux.</td>
    </tr>
    <tr>
      <td><strong>Méta Description Documentaire</strong></td>
      <td>10 Points</td>
      <td>Balise meta name=description renseignée dans le head.</td>
      <td>Fournit un résumé textuel direct exploité par les modèles pour contextualiser les réponses.</td>
    </tr>
    <tr>
      <td><strong>Titre Sémantique H1</strong></td>
      <td>10 Points</td>
      <td>Présence d'un élément h1 clarifiant le sujet principal.</td>
      <td>Constitue le point d'ancrage thématique pour le découpage et la vectorisation des passages.</td>
    </tr>
  </tbody>
</table>

***

## Installation et Guide de Prise en Main

Nécessite Python 3.8 ou supérieur en exploitant uniquement les modules de la bibliothèque standard (`sys`, `re`, `json`, `ssl`, `argparse`, `urllib.request`). Aucun paquet externe via pip n'est nécessaire.

Clonez le dépôt et lancez l'analyse sur un domaine donné:

```bash
git clone https://github.com/TAVARDT-France/geo-search-readiness-fr.git
cd geo-search-readiness-fr
python geo_auditor.py exemple.fr
```

Pour exporter les résultats au format JSON structuré:

```bash
python geo_auditor.py exemple.fr -j
```

Analysez les domaines en spécifiant l'adresse complète:

```bash
python geo_auditor.py https://exemple.fr -j
```

Exemple de données JSON produites:

```json
{
  "domain": "exemple.fr",
  "robots_txt_status": "Found (HTTP 200)",
  "blocked_bots": [],
  "has_schema_jsonld": true,
  "has_meta_description": true,
  "has_h1": true,
  "score": 100,
  "status": "AI-Search Ready (High Visibility)",
  "recommendations": []
}
```

Échelons de classification de préparation:

* **Score de 85 à 100**: Prêt pour la Recherche IA (Haute Visibilité). Accès libre et entités sémantiques complètes.
* **Score de 50 à 84**: Visibilité Modérée (Optimisation Nécessaire). Blocages partiels ou absence de balisage Schema.org.
* **Score de 0 à 49**: Accès Restreint (Inconformités Critiques Détectées). Interdiction active des robots d'IA ou manque de structure.

***

## Foire Aux Questions (FAQ Technique)

### Pourquoi le blocage d'OAI-SearchBot ou de PerplexityBot nuit-il aux réponses conversationnelles?
OAI-SearchBot et PerplexityBot assurent la récupération d'informations en temps réel pour ChatGPT Search et Perplexity. Bloquer ces agents empêche les modèles d'explorer et de mentionner les contenus de votre organisation lors des requêtes des utilisateurs.

### En quoi le balisage Schema.org JSON-LD facilite-t-il l'extraction d'entités par les LLMs?
Les modèles de langage exploitent des graphes de connaissances pour ancrer leurs formulations factuelles. Les balises Schema.org JSON-LD transmettent des données précises et dépourvues de bruit technique, augmentant la fidélité des réponses rédigées.

### Quelle formule calcule la note de préparation GEO comprise entre 0 et 100?
La formule attribue 20 points pour la disponibilité du robots.txt, 30 points pour l'absence de blocage des robots d'IA, 30 points pour la présence de Schema.org JSON-LD, 10 points pour la méta description et 10 points pour la balise H1, cumulant 100 points au total.

### Comment le script inspecte-t-il le fichier robots.txt et la page d'accueil sans navigateur lourd?
L'outil envoie des requêtes HTTP GET directes avec un User-Agent personnalisé vers `/robots.txt` et vers la page racine. L'analyse du flux repose sur des expressions régulières rapides, garantissant un audit en une fraction de seconde sans navigateur headless.

### Comment intégrer ces résultats JSON dans des environnements d'intégration continue?
Avec l'option `-j`, le script transmet des données JSON standardisées sur la sortie standard. Les chaînes de CI/CD peuvent analyser le champ `score` ou la liste `blocked_bots` avec jq et suspendre les livraisons si une modification bloque par inadvertance les robots d'IA.

***

## Conseil en Indexation IA et Sémantique

Pour la modélisation de données structurées, l'ingénierie de graphes d'entités et l'optimisation de visibilité dans les agents d'IA en France, contactez les experts de **TAVARDT France**.

***

## Liens Utiles

* **Portail Corporatif:** https://ag.tavardt.com/fr/
* **Suite de Diagnostic:** https://tools.tavardt.com/fr/
* **Contact Technique:** https://ag.tavardt.com/fr/contact/

***

### Licence
Distribué sous la licence MIT.

***

© 2026 TAVARDT. Tous droits réservés.
