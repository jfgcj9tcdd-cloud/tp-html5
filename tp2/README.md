# TPs HTML5 — Guide de soumission GitHub

## Structure du dépôt

```
/
├── tp1/
│   └── index.html          # TP1 : CV/Portfolio personnel
├── tp2/
│   └── index.html          # TP2 : Formulaire d'inscription
└── tp3/
    ├── style.css            # CSS partagé
    ├── index.html           # Accueil
    ├── about.html           # Équipe
    ├── services.html        # Services
    ├── gallery.html         # Galerie
    └── contact.html         # Contact
```

---

## Comment mettre en ligne sur GitHub

### 1. Créer le dépôt GitHub
1. Aller sur [github.com](https://github.com) → **New repository**
2. Nom : `tp-html5` (ou celui demandé par votre prof)
3. Visibilité : **Public**
4. Cliquer **Create repository**

### 2. Initialiser et pousser depuis votre dossier

```bash
# Dans le dossier contenant tp1/, tp2/, tp3/
git init
git add .
git commit -m "Initial commit — TP1, TP2, TP3"
git branch -M main
git remote add origin https://github.com/VOTRE_USERNAME/tp-html5.git
git push -u origin main
```

### 3. Activer GitHub Pages (facultatif mais recommandé)
1. Dans le dépôt → **Settings** → **Pages**
2. Source : `Deploy from a branch`
3. Branch : `main` / `/ (root)`
4. Sauvegarder → votre site est accessible en ligne !

### 4. Soumettre sur Classroom
Coller l'URL de votre dépôt (ex: `https://github.com/VOTRE_USERNAME/tp-html5`) dans la case GitHub Classroom.

---

## Contenu par TP

### TP1 — Page CV/Portfolio (Débutant)
- Structure sémantique : `<header>`, `<main>`, `<footer>`, `<section>`, `<nav>`
- Navigation avec ancres internes (`#accueil`, `#apropos`, `#competences`, `#formations`, `#contact`)
- Section "À propos" avec photo (`<img alt="...">`) et description
- Liste compétences (`<ul>`) et en cours d'apprentissage (`<ol>`)
- Tableau formations/expériences (`<table>`, `<thead>`, `<tbody>`, `<th>`, `<td>`)
- Liens réseaux sociaux avec `target="_blank"` et `rel="noopener noreferrer"`
- Hiérarchie des titres correcte (h1 → h6)

### TP2 — Formulaire d'inscription (Intermédiaire)
- Champs : nom, prénom, email, téléphone, date de naissance, mot de passe + confirmation, pays (datalist), genre (radio), intérêts (checkboxes), biographie (textarea + maxlength), photo (file), CGU (checkbox required)
- Validations HTML5 : `type="email"`, pattern téléphone français, pattern mot de passe (min 8 car., 1 maj., 1 chiffre), âge minimum 18 ans
- Tous les champs obligatoires avec `required`
- Messages d'erreur personnalisés via `setCustomValidity()`
- Bonus : `<fieldset>` + `<legend>`, attribut `autocomplete`

### TP3 — Site vitrine multi-pages (Avancé)
- 5 pages HTML avec navigation cohérente
- Images responsives avec `srcset`, `sizes` et `<picture>`
- Vidéo avec `autoplay`, `muted`, `loop`, `playsinline`
- Tableau de tarifs avec `colspan` et `rowspan`
- Formulaire de contact avec tous types d'inputs (text, email, tel, url, range, select, textarea, checkbox)
- Services avec `<details>` / `<summary>` (accordéon natif HTML5)
- Footer avec plan du site et mentions légales
- Métadonnées SEO complètes (Open Graph, Twitter Card, meta description)
- Carte via `<iframe>` OpenStreetMap
