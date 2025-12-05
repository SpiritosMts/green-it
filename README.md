# ÉcoWeb - Application Web Éco-conçue

> **Challenge Green IT** — NoctEvent × O2Switch

---

## Présentation

ÉcoWeb est une application web éco-conçue qui permet d'analyser et de réduire l'empreinte carbone des sites web. Elle a été développée dans le cadre du Challenge Green IT organisé par NoctEvent en partenariat avec O2Switch.

L'application met en pratique les principes du numérique responsable tout en offrant des outils concrets pour sensibiliser et calculer l'impact environnemental du web.

---

## Métriques de performance

| Métrique | ÉcoWeb | Site moyen | Gain |
|----------|--------|------------|------|
| Éléments DOM | ~160 | ~1500 | 10× moins |
| Poids total | ~22 Ko | ~2400 Ko | 100× plus léger |
| Requêtes HTTP | 1 | ~80 | 80× moins |
| CO₂ par visite | ~0.004g | ~0.5g | 125× moins |

---

## Fonctionnalités

### Éco-Score en temps réel
L'application calcule automatiquement un score environnemental (0-100) basé sur :
- Le nombre d'éléments DOM
- Le poids de la page en Ko
- Le nombre de requêtes HTTP

Une jauge SVG animée affiche le résultat avec un grade (A+ à D).

### Calculateur d'impact carbone
Permet d'estimer l'empreinte carbone annuelle d'un site selon :
- Le nombre de visites mensuelles
- Le nombre de pages par visite
- Le poids moyen par page

Résultats exprimés en kg CO₂, km en voiture, arbres nécessaires et kWh.

### Internationalisation
L'application est disponible en français (par défaut) et en anglais. Le choix de langue est conservé dans le navigateur.

### Section pédagogique
- 6 principes d'éco-conception expliqués
- Comparaison avec un site web moyen
- FAQ sur le Green IT

---

## Principes d'éco-conception appliqués

### Architecture minimale
- **Fichier unique** : HTML, CSS et JavaScript regroupés dans un seul fichier
- **Zéro dépendances** : aucune librairie externe (React, jQuery, etc.)
- **Pas d'images** : design 100% CSS avec icônes emoji

### Performance optimisée
- **Polices système** : utilisation de `system-ui` sans téléchargement
- **CSS natif** : variables CSS, Grid et Flexbox sans framework
- **JavaScript vanilla** : code léger compatible tous navigateurs

### Expérience utilisateur
- **Thème sombre** : économie d'énergie sur écrans OLED
- **Design responsive** : adaptation mobile avec media queries minimales
- **Accessibilité** : HTML sémantique et navigation clavier

---

## Technologies utilisées

```
HTML5        Structure sémantique
CSS3         Variables, Grid, Flexbox, animations
JavaScript   Vanilla ES5 (compatibilité maximale)
SVG          Jauge de score animée
```

Le projet n'utilise aucun framework, aucune police externe, aucun CDN et aucune image.

---

## Structure du projet

```
green-it/
├── index.html    Application complète
└── README.md     Documentation
```

Un seul fichier = une seule requête HTTP = impact minimal.

---

## Installation et déploiement

### Développement local

```bash
# Avec Python
python3 -m http.server 8080

# Avec Node.js
npx serve .

# Avec PHP
php -S localhost:8080
```

Ouvrir ensuite http://localhost:8080 dans le navigateur.

### Production

Le fichier `index.html` peut être déployé sur n'importe quel hébergeur :
- O2Switch (partenaire du challenge)
- Netlify, Vercel, GitHub Pages
- Serveur Apache, Nginx

**Optimisations serveur recommandées :**
- Compression Gzip ou Brotli
- Cache HTTP avec max-age long
- HTTP/2 activé

---

## Formules de calcul

### CO₂ par visite
```
CO₂ (g) = Poids (Ko) × 0.0002
```
Facteur incluant datacenter, réseau et terminal.

### Équivalent arbres
```
Arbres = CO₂ annuel (kg) / 21
```
Un arbre absorbe environ 21 kg de CO₂ par an.

### Équivalent voiture
```
km = CO₂ (kg) / 0.12
```
Émission moyenne d'une voiture : 120g CO₂/km.

---

## Accessibilité

- HTML sémantique (`main`, `nav`, `section`, `header`)
- Navigation clavier fonctionnelle
- Contrastes conformes WCAG AA
- Labels explicites sur les formulaires

---

## Critères du challenge

| Critère | Objectif | Résultat |
|---------|----------|----------|
| Éléments DOM | Minimiser | ~160 |
| Poids des données | Minimiser | ~22 Ko |
| Requêtes HTTP | Minimiser | 1 |

---

## Licence

Projet créé pour le Challenge Green IT organisé par NoctEvent en partenariat avec O2Switch.

---

*Conçu avec sobriété numérique — Chaque octet compte.*
