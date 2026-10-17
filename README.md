# Site HACK'MAZONE — tout est prêt, voici comment le mettre en ligne

Ce dossier contient **l'intégralité de ton site**, prêt à publier sur GitHub Pages avec ton domaine **hackmazone.fr**. Les images et ton logo sont déjà inclus.

## Contenu du dossier
```
index.html                      → page principale (Cyber / IA / IE)
publications.html               → ton blog (ajoute un article quand tu veux)
style.css                       → design du site
legal.css                       → design des pages légales
mentions-legales.html
politique-confidentialite.html
politique-cookies.html
cgv-cgu.html
mediation-consommation.html
CNAME                           → contient "hackmazone.fr" (ne pas renommer)
assets/
  ├── logo-mark.png             → ton logo (fond transparent)
  ├── logo-full.png             → logo + texte
  ├── hero.jpg                  → image d'accueil (filigrane retiré)
  ├── vision.jpg                → image section spatiale
  ├── ia.jpg                    → image section IA
  └── badges/                   → déposer ici tes badges certifs officiels (optionnel)
```

---

## ÉTAPE 1 — Mettre les fichiers sur GitHub

### Méthode simple (sans ligne de commande)
1. Va sur **github.com** → connecte-toi → bouton **New** (nouveau dépôt).
2. Nom du dépôt : **hackmazone** · coche **Public** · clique **Create repository**.
3. Sur la page du dépôt vide : clique **uploading an existing file**.
4. **Glisse-dépose TOUT le contenu de ce dossier** (y compris le sous-dossier `assets/`) → **Commit changes**.

### Méthode git (si tu préfères le terminal)
```bash
cd hackmazone
git init
git add .
git commit -m "Site HACK'MAZONE"
git branch -M main
git remote add origin https://github.com/TON-COMPTE/hackmazone.git
git push -u origin main
```

## ÉTAPE 2 — Activer GitHub Pages
1. Dans le dépôt → **Settings** → **Pages**.
2. **Source** : *Deploy from a branch* → branche **main** → dossier **/ (root)** → **Save**.
3. Attends 1–2 min : une URL `https://TON-COMPTE.github.io/hackmazone` apparaît. Le site est déjà en ligne.

## ÉTAPE 3 — Brancher ton domaine hackmazone.fr
1. Toujours dans **Settings → Pages → Custom domain** : écris **hackmazone.fr** → **Save**.
   (Le fichier `CNAME` fait déjà ce travail, mais confirme-le ici.)
2. Chez **Infomaniak** (Manager → Domaines → hackmazone.fr → **Modifier la zone DNS**), ajoute :
```
A      @   185.199.108.153
A      @   185.199.109.153
A      @   185.199.110.153
A      @   185.199.111.153
AAAA   @   2606:50c0:8000::153
AAAA   @   2606:50c0:8001::153
AAAA   @   2606:50c0:8002::153
AAAA   @   2606:50c0:8003::153
CNAME  www TON-COMPTE.github.io.
```
   ⚠️ Avant ça, assure-toi d'avoir bien remis **« Serveurs DNS Infomaniak »** (pas Wix).
3. Reviens dans **Settings → Pages** et coche **Enforce HTTPS** (une fois le DNS propagé, quelques heures max).

➡️ Ton site est en ligne sur **https://hackmazone.fr** ✅

---

## À PERSONNALISER (3 petites choses)

1. **Tes liens** : remplace `VOTRE-PROFIL` par ton URL LinkedIn dans `index.html` et `publications.html` (recherche « VOTRE-PROFIL »). WhatsApp est déjà réglé sur ton numéro.
2. **Le formulaire de contact** : crée un compte gratuit sur **formspree.io**, récupère ton identifiant, et remplace `VOTRE_ID` dans `index.html` (`action="https://formspree.io/f/VOTRE_ID"`). Tel + email + WhatsApp fonctionnent déjà sans rien faire.
3. **Un champ légal** : dans `mentions-legales.html`, complète (ou supprime) la ligne TVA surlignée.

## Publier un article
Ouvre `publications.html`, copie un bloc `<article class="pub-card">…</article>`, change la date, le titre et le texte. Place le plus récent en premier. Pousse le fichier sur GitHub → c'est en ligne.

## Changer une image plus tard
Remplace simplement le fichier dans `assets/` en gardant le même nom (`hero.jpg`, `vision.jpg`, `ia.jpg`).
