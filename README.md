# 🏓 Ping Paris — Guide de déploiement

## Ton projet contient 3 fichiers principaux

| Fichier | Rôle |
|---|---|
| `index.html` | Le site public avec la carte |
| `app.html` | L'appli de collecte sur téléphone |
| `tables.json` | Les données des tables |

---

## Étape 1 — Créer un compte GitHub

1. Va sur [github.com](https://github.com)
2. Clique sur **Sign up**
3. Saisis ton email, un mot de passe, un nom d'utilisateur
4. Valide ton compte par email

---

## Étape 2 — Créer un dépôt (repository)

1. Clique sur le **+** en haut à droite → **New repository**
2. Nom du dépôt : `ping-pong-paris` (tout en minuscules)
3. Coche **"Add a README file"**
4. Coche **Public**
5. Clique sur **Create repository**

---

## Étape 3 — Uploader les fichiers

1. Dans ton dépôt, clique sur **Add file → Upload files**
2. Glisse-dépose les 3 fichiers : `index.html`, `app.html`, `tables.json`
3. En bas, clique sur **Commit changes**

---

## Étape 4 — Activer GitHub Pages

1. Dans ton dépôt, clique sur **Settings** (onglet tout à droite)
2. Dans le menu gauche, clique sur **Pages**
3. Sous "Source", sélectionne **main** et dossier **/ (root)**
4. Clique **Save**
5. Attends 2 minutes, ton site sera disponible à :
   **`https://TON_NOM.github.io/ping-pong-paris/`**

---

## Étape 5 — Ajouter l'appli sur ton téléphone

1. Sur ton téléphone, ouvre **Safari** (iPhone) ou **Chrome** (Android)
2. Va sur : `https://TON_NOM.github.io/ping-pong-paris/app.html`
3. **iPhone** : tape le bouton partager → "Sur l'écran d'accueil"
4. **Android** : tape les 3 points → "Ajouter à l'écran d'accueil"
5. L'icône apparaît comme une vraie appli !

---

## Workflow terrain → site

### Sur le terrain (avec l'appli)
1. Ouvre PingCollect sur ton téléphone
2. Remplis le formulaire : nom, arrondissement
3. Appuie sur 📡 pour la position GPS automatique
4. Prends une photo
5. Ajoute les horaires si c'est un jardin public
6. Enregistre

### Le soir (sur ordinateur)
1. Dans l'appli, onglet **Exporter**
2. Copie le JSON
3. Va sur GitHub → fichier `tables.json`
4. Clique sur ✏️ (crayon) pour modifier
5. Ajoute les nouvelles entrées dans le tableau existant
6. Clique **Commit changes**
7. Site mis à jour en 1 minute !

### Pour les photos
Les photos sont stockées en base64 dans l'appli. Pour les mettre sur le site :
1. Sur GitHub, crée un dossier `images`
2. Upload tes photos dedans (ex: `table_square_batignolles.jpg`)
3. Dans `tables.json`, le champ `photo` doit pointer vers : `images/nom_photo.jpg`

---

## Modifier les données directement

Le fichier `tables.json` suit ce format :

```json
{
  "id": 6,
  "nom": "Nom du lieu",
  "arrondissement": "18e",
  "lat": 48.8900,
  "lng": 2.3450,
  "photo": "images/ma_photo.jpg",
  "horaires": "Lun–Dim 8h–21h",
  "notes": "Tables près de l'entrée nord",
  "acces_libre": true
}
```

---

## Donner un vrai nom de domaine (optionnel, payant)

Tu peux acheter un domaine (ex: `pingparis.fr`) sur OVH (~7€/an) et le relier à GitHub Pages en suivant la doc GitHub.

---

*Projet créé avec ❤️ pour les amateurs de ping-pong parisiens*
