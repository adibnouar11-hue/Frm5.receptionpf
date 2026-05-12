# 📦 Réception PF — Checklist FRM5

**Application mobile (PWA) de checklist de réception des produits finis au magasin PF**

> Référence : GS-SOP-009-05/FRM5 · Version 04

---

## 📱 Aperçu

Application Progressive Web App (PWA) permettant aux opérateurs warehouse de remplir la checklist de réception des produits finis directement depuis leur smartphone Android, en remplacement du formulaire papier.

### Fonctionnalités

- **4 étapes guidées** : Identification → Transport → Réception physique → Formulaire final
- **Validation par étape** avec confirmation obligatoire et alerte sur les champs manquants
- **Sauvegarde automatique** du brouillon en cours (reprise après fermeture)
- **Historique local** des formulaires complétés
- **Reproduction fidèle** du formulaire officiel FRM5 pour impression
- **Mode hors-ligne** (fonctionne sans connexion après premier chargement)
- **Installable** sur Android comme une application native

### Points de contrôle couverts

| Étape | Contenu |
|-------|---------|
| ① Identification | Date/heure, quai, type produit, thermosensible, vide de ligne, fournisseur agréé, quantité |
| ② Transport | État véhicule, température, palettes (HT, propreté, filmage), contenants |
| ③ Réception | Conditions stockage, aspect contenants, data loggers, étiquetage, corrélation lots/quantités, logbook |
| ④ Formulaire | Reproduction complète FRM5 avec bloc signatures — prêt à imprimer |

---

## 🚀 Installation

### Pour les opérateurs (Android)

1. Ouvrir le lien de l'application dans **Google Chrome**
2. Appuyer sur **⋮** (menu) → **« Ajouter à l'écran d'accueil »**
3. L'icône **PF** apparaît — l'app s'ouvre en plein écran

### Pour le déploiement (GitHub Pages)

1. Cloner ce repository
2. Le fichier `index.html` est l'application complète (zéro dépendance)
3. GitHub Pages sert automatiquement l'app à l'URL :
   ```
   https://<votre-pseudo>.github.io/<nom-du-repo>/
   ```

---

## 🔒 Données & Confidentialité

- **Aucune donnée ne transite par internet** — tout est stocké localement sur l'appareil (localStorage)
- **Aucun serveur backend** — l'app est 100% côté client
- **Aucun tracking, aucun cookie tiers**
- Le repository public ne contient que le code source (le formulaire vide)

---

## 🏗️ Architecture

```
FRM5_Reception_PF/
└── index.html      ← Application complète (HTML + CSS + JS)
                       • PWA manifest (inline)
                       • Service Worker (inline)
                       • Stockage localStorage
                       • Impression CSS @media print
```

**Stack** : Vanilla HTML/CSS/JS — zéro framework, zéro dépendance, zéro build.

---

## 📋 Référence documentaire

| Champ | Valeur |
|-------|--------|
| Référence SOP | GS-SOP-009-05 |
| Formulaire | FRM5 |
| Version | 04 |
| Date d'application | 20/11/2025 |
| Périmètre | Magasin Produits Finis |

---

## 📄 Licence

Usage interne — LDM Groupe.
