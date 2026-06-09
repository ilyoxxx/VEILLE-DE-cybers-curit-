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
>
> En utilisant ce projet, vous reconnaissez avoir pris connaissance de cet avertissement et acceptez d'en faire un usage strictement légal, éthique et conforme aux bonnes pratiques de la cybersécurité.
>
> L'auteur ne pourra être tenu responsable des dommages directs ou indirects, matériels ou immatériels, résultant d'une mauvaise utilisation, d'une modification ou d'un détournement des fonctionnalités présentées dans ce projet.

