# ÉcoWeb - Application Web Éco-conçue

> **Challenge Green IT** — NoctEvent × O2Switch

Application web démontrant les meilleures pratiques d'éco-conception numérique, conçue pour minimiser l'empreinte environnementale tout en offrant une expérience utilisateur moderne et professionnelle.

---

## 📊 Métriques de Performance Environnementale

| Métrique | ÉcoWeb | Moyenne Web | Amélioration |
|----------|--------|-------------|--------------|
| **Éléments DOM** | ~180 | ~1500 | **8× moins** |
| **Poids total** | ~30 Ko | ~2400 Ko | **80× plus léger** |
| **Requêtes HTTP** | 1 | ~80 | **80× moins** |
| **CO₂ par visite** | ~0.006g | ~0.5g | **83× moins polluant** |

---

## ✨ Fonctionnalités

### 1. Éco-Score en Temps Réel
- Calcul automatique du score environnemental de la page (0-100)
- Affichage visuel avec jauge SVG animée
- Grade de performance (A+ à E)
- Métriques détaillées : CO₂/visite, arbres équivalents, énergie consommée

### 2. Analyseur de Site Web
- Simulation d'analyse environnementale pour n'importe quelle URL
- Évaluation des éléments DOM, taille et requêtes HTTP
- Indicateurs visuels colorés (vert/jaune/rouge)
- Recommandations personnalisées d'optimisation

### 3. Calculateur d'Impact Carbone
- Estimation de l'empreinte carbone annuelle d'un site
- Paramètres personnalisables : visites, pages/visite, poids moyen
- Équivalences concrètes : km en voiture, arbres nécessaires, énergie kWh

### 4. Section Pédagogique
- Explication des 8 principes d'éco-conception appliqués
- Comparaison chiffrée avec un site web moyen
- FAQ interactive sur le Green IT

---

## 🌱 Principes d'Éco-conception Appliqués

### Architecture
| Principe | Implémentation |
|----------|----------------|
| **Fichier unique** | HTML, CSS et JS regroupés → 1 seule requête HTTP |
| **Zéro dépendances** | Aucune librairie externe (pas de React, jQuery, etc.) |
| **Pas d'images** | Design 100% CSS, icônes en emoji Unicode |

### Performance
| Principe | Implémentation |
|----------|----------------|
| **Polices système** | `system-ui` → 0 Ko de fonts téléchargées |
| **CSS optimisé** | Variables CSS, minification, pas de framework |
| **JavaScript minimal** | Vanilla JS pur, ~2 Ko de code fonctionnel |

### Expérience Utilisateur
| Principe | Implémentation |
|----------|----------------|
| **Thème sombre** | Économie d'énergie sur écrans OLED/AMOLED |
| **Responsive léger** | Media queries minimales avec CSS Grid |
| **Accessibilité** | HTML sémantique, ARIA, navigation clavier |

---

## 🛠️ Stack Technique

```
HTML5      → Structure sémantique
CSS3       → Variables, Grid, Flexbox, animations
JavaScript → Vanilla ES5 (compatibilité maximale)
SVG        → Jauge de score animée
```

**Aucune dépendance externe** — Le projet n'utilise :
- ❌ Aucun framework JS (React, Vue, Angular)
- ❌ Aucun framework CSS (Tailwind, Bootstrap)
- ❌ Aucune police web (Google Fonts)
- ❌ Aucun CDN externe
- ❌ Aucune image/média

---

## 📁 Structure du Projet

```
green-it/
├── index.html    # Application complète (HTML + CSS + JS)
└── README.md     # Documentation
```

**1 seul fichier** = 1 seule requête HTTP = impact minimal

---

## 🚀 Déploiement

### Développement local
```bash
# Serveur Python
python3 -m http.server 8080

# Ou avec Node.js
npx serve .
```

### Production
Le fichier `index.html` peut être déployé sur n'importe quel hébergeur statique :
- **O2Switch** (partenaire du challenge)
- Netlify, Vercel, GitHub Pages
- Tout serveur Apache/Nginx

**Recommandations serveur :**
- Activer la compression Gzip/Brotli
- Configurer le cache HTTP (max-age: 1 an pour fichier unique)
- Utiliser HTTP/2

---

## 📈 Calculs Environnementaux

### Formules utilisées

**CO₂ par visite :**
```
CO₂ (g) = Poids page (Ko) × 0.0002
```
*Facteur incluant : datacenter, réseau, terminal utilisateur*

**Équivalent arbres :**
```
Arbres = (CO₂ annuel en g) / 21000
```
*Un arbre absorbe ~21 kg de CO₂/an*

**Équivalent voiture :**
```
km = (CO₂ en kg) / 0.12
```
*Émission moyenne : 120g CO₂/km*

---

## ♿ Accessibilité

- ✅ HTML sémantique (`<main>`, `<nav>`, `<section>`, `<header>`)
- ✅ Lien "Skip to content" pour lecteurs d'écran
- ✅ Attributs ARIA (`aria-label`, `aria-expanded`, `role`)
- ✅ Navigation clavier complète (Tab, Enter, Space)
- ✅ Contraste suffisant (WCAG AA)
- ✅ Focus visible sur éléments interactifs

---

## 🎨 Design System

### Palette de couleurs
| Variable | Valeur | Usage |
|----------|--------|-------|
| `--bg` | `#0a0f14` | Arrière-plan principal |
| `--surface` | `#12181f` | Cartes et sections |
| `--accent` | `#22c55e` | Éléments interactifs, succès |
| `--warning` | `#eab308` | Alertes modérées |
| `--danger` | `#ef4444` | Alertes critiques |

### Typographie
```css
font: 16px/1.65 system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
```
*Polices natives du système → 0 requête, rendu instantané*

---

## 📋 Critères du Challenge

Le projet répond aux 3 critères d'évaluation :

| Critère | Objectif | Résultat |
|---------|----------|----------|
| **Éléments DOM** | Minimiser | ~180 éléments |
| **Poids des données** | Minimiser | ~30 Ko |
| **Requêtes HTTP** | Minimiser | 1 requête |

---

## 🔮 Évolutions Possibles

- [ ] Mode hors-ligne avec Service Worker
- [ ] Export PDF du rapport d'analyse
- [ ] API réelle pour analyser des URLs externes
- [ ] Internationalisation (EN, ES, DE)
- [ ] Mode clair optionnel avec `prefers-color-scheme`

---

## 📄 Licence

Projet open-source créé pour le **Challenge Green IT** organisé par **NoctEvent** en partenariat avec **O2Switch**.

---

<p align="center">
  <strong>🌱 Conçu avec sobriété numérique</strong><br>
  <em>Chaque octet compte.</em>
</p>
