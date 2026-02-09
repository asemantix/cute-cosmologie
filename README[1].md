# L'Univers Énergeia — Guide de déploiement

## 🚀 Étape 1 : Créer le compte PayPal.me (5 minutes)

1. Allez sur **https://www.paypal.com/paypalme**
2. Connectez-vous à votre compte PayPal (ou créez-en un)
3. Choisissez votre lien, par exemple : `paypal.me/ThaOra` ou `paypal.me/Asemantix`
4. Une fois créé, votre lien de paiement sera : `https://paypal.me/VOTRE_NOM/14.99EUR`

**→ Ensuite, ouvrez `index.html` et remplacez :**
```
https://paypal.me/VOTRE_LIEN_PAYPAL/14.99EUR
```
par votre vrai lien, ex :
```
https://paypal.me/ThaOra/14.99EUR
```

## 🌐 Étape 2 : Acheter le nom de domaine (5 minutes)

Allez sur **un des registrars suivants** :
- **OVH** (français) : https://www.ovh.com/fr/domaines/
- **Namecheap** : https://www.namecheap.com
- **Gandi** (français) : https://www.gandi.net

Recherchez et achetez : **univers-energeia.app**
(Si .com n'est pas dispo, essayez .fr, .io, ou .tech)

Prix : environ 10-15 €/an.

## 📦 Étape 3 : Créer le dépôt GitHub (10 minutes)

1. Allez sur **https://github.com** (créez un compte si besoin, c'est gratuit)
2. Cliquez sur **"New repository"** (le bouton vert "+")
3. Nom du dépôt : `univers-energeia` (ou `univers-energeia.github.io`)
4. Visibilité : **Public**
5. Cliquez **"Create repository"**

### Uploader les fichiers :
1. Dans le dépôt créé, cliquez **"uploading an existing file"**
2. Glissez-déposez les 2 fichiers :
   - `index.html` (la page du site)
   - `CNAME` (le fichier de domaine)
3. Cliquez **"Commit changes"**

### Activer GitHub Pages :
1. Allez dans **Settings** → **Pages** (menu de gauche)
2. Source : sélectionnez **"Deploy from a branch"**
3. Branch : **main** / dossier **/ (root)**
4. Cliquez **Save**

Votre site sera en ligne sur `https://VOTRE_NOM.github.io/univers-energeia/` en quelques minutes.

## 🔗 Étape 4 : Relier le nom de domaine (15 minutes)

### Côté registrar (OVH, Namecheap, Gandi...) :

Allez dans la **gestion DNS** de votre domaine et ajoutez ces enregistrements :

**Enregistrements A (pour le domaine nu univers-energeia.app) :**
```
Type: A    Host: @    Value: 185.199.108.153
Type: A    Host: @    Value: 185.199.109.153
Type: A    Host: @    Value: 185.199.110.153
Type: A    Host: @    Value: 185.199.111.153
```

**Enregistrement CNAME (pour www) :**
```
Type: CNAME    Host: www    Value: VOTRE_NOM.github.io.
```

### Côté GitHub :
1. **Settings** → **Pages**
2. Dans **"Custom domain"**, entrez : `univers-energeia.app`
3. Cliquez **Save**
4. Cochez **"Enforce HTTPS"** (peut prendre quelques minutes à apparaître)

⏳ Propagation DNS : de 10 minutes à 24 heures (généralement 30 min).

## ✅ Étape 5 : Vérifier

Après propagation, votre site sera accessible sur :
- **https://univers-energeia.app** ✓
- **https://www.univers-energeia.app** ✓

## 💡 Rappels importants

### À remplacer dans index.html :
1. `https://paypal.me/VOTRE_LIEN_PAYPAL/14.99EUR` → votre vrai lien PayPal
2. `https://www.amazon.fr/dp/VOTRE_ASIN_KINDLE` → votre lien Amazon Kindle (quand publié)
3. Si vous changez le prix, modifiez aussi le texte "Acheter — 14,99 €"

### Pour recevoir le paiement PayPal et envoyer le livre :
- Le lecteur clique "Acheter" → PayPal s'ouvre → il paye 14,99 €
- Vous recevez une notification PayPal avec son email
- Vous lui envoyez le PDF par email (depuis asemantix@proton.me)

### Alternative automatisée (plus tard) :
- **Gumroad** (https://gumroad.com) : vente + livraison automatique du PDF
- **Ko-fi** (https://ko-fi.com) : similaire, très simple
- Ces plateformes prennent une petite commission mais envoient le fichier automatiquement

## 📁 Structure des fichiers

```
univers-energeia/
├── index.html    ← La page du site (tout-en-un)
├── CNAME         ← Fichier pour le domaine personnalisé
└── README.md     ← Ce fichier
```

---
© 2025 ThaÔra · AION ASEMANTIX™ · 39 brevets INPI
