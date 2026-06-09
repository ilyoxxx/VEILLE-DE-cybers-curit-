![Logo](/logo.svg)

# 🛡️ CyberSec Watch v2

**Plateforme de veille mondiale en cybersécurité** — Dashboard temps réel sans authentification, connecté aux vraies APIs publiques mondiales.

---

## 🚀 Lancement en 30 secondes

```bash
npm install
npm start
# → http://localhost:3000
```

C'est tout. Aucune clé API requise.

---

## 🌍 Sources de données réelles

| Source | Endpoint | Données |
|--------|----------|---------|
| **NVD/NIST** | `services.nvd.nist.gov` | CVEs temps réel, scores CVSS |
| **CISA KEV** | `cisa.gov` | Vulnérabilités activement exploitées |
| **RansomWatch** | GitHub `joshhighet/ransomwatch` | Groupes ransomware & victimes |
| **Shodan/Censys** | Simulé honeypot-style | Ports exposés, stats exposition |
| **Live Threat Feed** | `/api/stream` SSE | Attaques mondiales en direct |

---

## 📡 API REST — tous les endpoints

```
GET  /api/cve/recent?days=7&severity=CRITICAL&limit=40   CVEs récents NVD
GET  /api/cve/:id                                         Détail CVE
GET  /api/kev                                             CISA KEV catalogue
GET  /api/ransomware                                      Groupes & victimes
GET  /api/threats/live?limit=80                           Attaques simulées
GET  /api/threats/stats                                   Statistiques globales
GET  /api/internet/health                                 Santé internet, BGP
GET  /api/stream                                          SSE flux temps réel
```

---

## 🖥️ Vues du dashboard

| Onglet | Contenu |
|--------|---------|
| **Dashboard** | Carte mondiale live, flux d'attaques, KPIs, graphiques |
| **CVE Database** | Bibliothèque NVD avec recherche, filtres, scores CVSS |
| **CISA KEV** | Catalogue officiel US des vulnérabilités exploitées |
| **Ransomware** | Top groupes actifs, victimes récentes indexées |
| **Internet** | Santé réseau mondial, BGP, DDoS, ports exposés |

---

## 🏗️ Architecture

```
cybersec-watch/
├── server.js          Express + toutes les routes API
├── public/
│   ├── index.html     SPA single-page
│   ├── css/style.css  Design system (Syne + JetBrains Mono)
│   └── js/app.js      Canvas map, SSE, fetch APIs, vues
└── package.json
```

---

## 🎨 Stack technique

- **Backend** : Node.js + Express, node-cache, axios, SSE
- **Frontend** : Vanilla JS ES6+, Canvas API (world map), CSS Grid
- **Typo** : Syne (display) · JetBrains Mono (données) · Outfit (corps)
- **Design** : Blanc/Bleu électrique, war room aesthetic

---
> **Avertissement légal et éthique**
>
> Ce projet a été réalisé exclusivement dans un cadre éducatif, pédagogique, de recherche, d'analyse et de démonstration technique. Son objectif est de permettre la compréhension des mécanismes étudiés, l'apprentissage des technologies utilisées ainsi que l'amélioration des compétences en informatique, réseaux et cybersécurité.
>
> Toute utilisation de ce projet à des fins malveillantes, frauduleuses, illégales, d'intrusion non autorisée, de perturbation de services, de cyberattaque ou de toute autre activité portant atteinte à des personnes, des systèmes informatiques ou des organisations est strictement interdite.
>
> L'auteur décline toute responsabilité concernant l'usage qui pourrait être fait de ce projet après sa diffusion. Chaque utilisateur demeure seul responsable de ses actions et s'engage à respecter les lois, règlements et normes en vigueur dans son pays.
>
> Conformément aux dispositions du Code pénal français relatives aux atteintes aux systèmes de traitement automatisé de données (STAD), notamment les articles 323-1 à 323-7, toute tentative d'accès frauduleux, de maintien non autorisé, d'altération, de suppression ou de modification de données peut faire l'objet de sanctions pénales.

> En utilisant ce projet, vous reconnaissez avoir pris connaissance de cet avertissement et acceptez d'en faire un usage strictement légal, éthique et conforme aux bonnes pratiques de la cybersécurité.
>
> L'auteur ne pourra être tenu responsable des dommages directs ou indirects, matériels ou immatériels, résultant d'une mauvaise utilisation, d'une modification ou d'un détournement des fonctionnalités présentées dans ce projet.

---

# ⚖️ Mentions légales, responsabilité et conditions d'utilisation

## 1. Présentation

**CyberSec Watch v2** est une plateforme de veille et de visualisation des menaces cyber développée à des fins exclusivement éducatives, pédagogiques, informatives et de recherche. L'objectif du projet est de centraliser et d'afficher des informations publiques relatives à la cybersécurité afin de faciliter la compréhension des vulnérabilités, des menaces émergentes, des campagnes ransomware et de l'état général de la sécurité numérique mondiale.

Le projet a été conçu comme un outil de consultation et d'analyse de données ouvertes. Il ne constitue pas un outil offensif, un framework d'exploitation, un scanner de vulnérabilités ou un logiciel destiné à compromettre des systèmes informatiques.

---

## 2. Nature des données utilisées

Les informations affichées par CyberSec Watch v2 proviennent exclusivement de sources publiques, ouvertes ou librement accessibles sur Internet.

Ces sources peuvent notamment inclure :

- National Vulnerability Database (NVD)
- National Institute of Standards and Technology (NIST)
- Cybersecurity and Infrastructure Security Agency (CISA)
- Bases de données publiques de vulnérabilités
- Dépôts Open Source
- Flux publics de renseignement sur les menaces (Threat Intelligence)
- Sources communautaires librement accessibles
- Référentiels publics de cybersécurité

L'application ne réalise aucune collecte de données personnelles privées, aucun contournement de mesures de sécurité et aucune extraction illégale d'informations.

---

## 3. Utilisations autorisées

CyberSec Watch v2 peut être utilisé dans les contextes suivants :

- Formation et apprentissage de la cybersécurité
- Enseignement académique
- Veille technologique
- Recherche scientifique
- Sensibilisation à la sécurité informatique
- Analyse de données publiques
- Démonstrations pédagogiques
- Études de tendances de menaces
- Travaux universitaires
- Laboratoires de test isolés
- Environnements de recherche contrôlés

L'utilisateur s'engage à utiliser le projet uniquement dans un cadre légal et conforme aux réglementations applicables.

---

## 4. Utilisations strictement interdites

Il est strictement interdit d'utiliser tout ou partie du projet pour :

- Réaliser des cyberattaques
- Faciliter des intrusions informatiques
- Mener des campagnes malveillantes
- Déployer des logiciels malveillants
- Contourner des dispositifs de sécurité
- Collecter illégalement des informations
- Effectuer des actions de reconnaissance non autorisées
- Exploiter des vulnérabilités sur des systèmes tiers
- Réaliser des attaques par déni de service (DoS/DDoS)
- Diffuser des contenus illicites
- Participer à des activités criminelles ou frauduleuses
- Porter atteinte à la confidentialité, l'intégrité ou la disponibilité de systèmes d'information

Toute utilisation contraire à ces règles engage exclusivement la responsabilité de l'utilisateur.

---

## 5. Absence de garantie

Le projet est fourni **« en l'état »**, sans aucune garantie expresse ou implicite.

L'auteur ne garantit notamment pas :

- L'exactitude absolue des données affichées
- La disponibilité permanente des sources externes
- L'absence d'erreurs techniques
- L'exhaustivité des informations présentées
- La compatibilité avec tous les environnements
- La disponibilité continue des API tierces utilisées

Les données affichées dépendent de services externes pouvant être modifiés, limités, suspendus ou supprimés sans préavis.

---

## 6. Limitation de responsabilité

L'auteur, les contributeurs et toute personne ayant participé au développement de CyberSec Watch v2 ne pourront être tenus responsables :

- D'une mauvaise utilisation du projet
- D'une utilisation illégale du logiciel
- D'une mauvaise interprétation des données affichées
- D'une interruption de service
- D'une perte de données
- D'un dommage matériel ou logiciel
- D'un préjudice financier
- D'un préjudice commercial
- D'un incident de sécurité résultant de l'utilisation du projet

L'utilisateur reconnaît utiliser le logiciel sous sa seule et entière responsabilité.

---

## 7. Conformité légale

L'utilisateur est seul responsable du respect des lois, réglementations et obligations applicables dans son pays ou sa juridiction.

En particulier, l'utilisateur s'engage à respecter :

- Les réglementations relatives à la cybersécurité
- Les réglementations relatives à la protection des données
- Les lois relatives à la fraude informatique
- Les règles de propriété intellectuelle
- Les conditions d'utilisation des API et services tiers

Pour les utilisateurs situés en France, les atteintes aux systèmes de traitement automatisé de données (STAD) sont notamment réprimées par les articles **323-1 à 323-7 du Code pénal**.

---

## 8. Propriété intellectuelle

Le code source, l'architecture, l'interface graphique, la documentation et les éléments créés spécifiquement pour CyberSec Watch v2 demeurent protégés par les lois relatives à la propriété intellectuelle.

Les marques, logos, noms d'organisations, bases de données et services tiers mentionnés dans le projet restent la propriété exclusive de leurs détenteurs respectifs.

---

## 9. Acceptation des conditions

En utilisant, installant, modifiant, compilant, exécutant ou redistribuant CyberSec Watch v2, l'utilisateur reconnaît avoir lu, compris et accepté l'intégralité des présentes conditions.

L'utilisateur accepte également que toute action réalisée à l'aide du projet relève exclusivement de sa responsabilité personnelle.

---

## 10. Clause finale

CyberSec Watch v2 est un projet de veille et d'analyse destiné à promouvoir la connaissance, la sensibilisation et la compréhension des enjeux de cybersécurité.

Le projet n'a pas été conçu, développé ou distribué dans le but de faciliter des activités malveillantes. Toute utilisation contraire à cet objectif est expressément désapprouvée par l'auteur et relève exclusivement de la responsabilité de l'utilisateur concerné.
