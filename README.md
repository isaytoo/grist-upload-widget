# 📤 Grist Upload Widget

> **FR** | [EN](#-grist-upload-widget-1)

---

## 🇫🇷 Grist Upload Widget

Un widget Grist simple et élégant pour uploader des fichiers (images, vidéos, PDF, audio…) vers le service de stockage de votre choix et enregistrer automatiquement l'URL dans votre document Grist.

### ✨ Fonctionnalités

- **📁 Upload universel** — Images, vidéos, PDF, audio et tout autre type de fichier
- **☁️ Multi-provider** — Cloudinary, Supabase Storage, AWS S3 / compatible (R2, B2, MinIO), ou URL personnalisée
- **💾 Sauvegarde automatique** — L'URL du fichier est enregistrée directement dans la colonne Grist mappée
- **📊 Barre de progression** — Suivi en temps réel de l'upload
- **🎨 Thème clair/sombre** — S'adapte automatiquement au thème de l'OS ou de Grist
- **⚡ Léger** — Fichier unique, aucune dépendance externe

### � URLs du widget

| Hébergeur | URL |
|-----------|-----|
| Vercel | `https://grist-upload-widget.vercel.app` |
| GitHub Pages | `https://isaytoo.github.io/grist-upload-widget` |

### � Installation

1. Dans votre document Grist, ajoutez une vue **Widget personnalisé**
2. Entrez l'une des URLs ci-dessus
3. Définissez le **Niveau d'accès** sur **Accès complet au document**
4. Dans le **Panneau Créateur**, mappez la colonne :
   - **Colonne de destination** *(obligatoire)* — colonne Text qui recevra l'URL du fichier uploadé
5. Sélectionnez un fichier → cliquez **Enregistrer dans Grist**

### ⚙️ Configuration du provider

Au premier chargement, le widget affiche automatiquement l'écran de configuration. Vous pouvez aussi y accéder via le bouton **⚙ Configurer**.

| Provider | Paramètres requis |
|----------|------------------|
| **Cloudinary** | Cloud Name + Upload Preset (Unsigned) |
| **Supabase Storage** | URL projet + Bucket + Clé API (anon key) |
| **AWS S3 / compatible** | Endpoint + Bucket + Access Key + Secret Key |
| **URL personnalisée** | Endpoint POST + Authorization (optionnel) + champ JSON de retour |

La configuration est sauvegardée dans les options du widget Grist — elle persiste entre les sessions.

### ⚠️ Note CORS

Si vous hébergez Grist en self-hosted, l'extension Chrome **[Grist Widget Bridge](https://github.com/isaytoo/grist-widget-bridge)** est nécessaire pour débloquer les appels CORS vers `api.cloudinary.com`.

Dans le popup de l'extension, ajoutez `https://api.cloudinary.com/*` dans la section **"API externe (CORS)"**.

### 🛠️ Développement local

```bash
git clone https://github.com/isaytoo/grist-upload-widget.git
cd grist-upload-widget
npx serve .
```

### 📄 Licence

Apache License 2.0 — © 2026 Said Hamadou (isaytoo)

---

## 🇬🇧 Grist Upload Widget

A simple and elegant Grist widget to upload files (images, videos, PDFs, audio…) to the storage provider of your choice and automatically save the URL in your Grist document.

### ✨ Features

- **📁 Universal upload** — Images, videos, PDFs, audio and any other file type
- **☁️ Multi-provider** — Cloudinary, Supabase Storage, AWS S3 / compatible (R2, B2, MinIO), or custom URL
- **💾 Auto-save** — The file URL is saved directly into the mapped Grist column
- **📊 Progress bar** — Real-time upload progress tracking
- **🎨 Light/dark theme** — Automatically adapts to the OS or Grist theme
- **⚡ Lightweight** — Single file, no external dependencies

### 🔗 Widget URLs

| Host | URL |
|------|-----|
| Vercel | `https://grist-upload-widget.vercel.app` |
| GitHub Pages | `https://isaytoo.github.io/grist-upload-widget` |

### 🚀 Installation

1. In your Grist document, add a **Custom Widget** view
2. Enter one of the URLs above
3. Set the **Access level** to **Full document access**
4. In the **Creator Panel**, map the column:
   - **Destination column** *(required)* — Text column that will receive the uploaded file URL
5. Select a file → click **Save to Grist**

### ⚙️ Provider Configuration

On first load, the widget automatically opens the configuration screen. You can also access it via the **⚙ Configure** button.

| Provider | Required parameters |
|----------|--------------------|
| **Cloudinary** | Cloud Name + Upload Preset (Unsigned) |
| **Supabase Storage** | Project URL + Bucket + API Key (anon key) |
| **AWS S3 / compatible** | Endpoint + Bucket + Access Key + Secret Key |
| **Custom URL** | POST endpoint + Authorization (optional) + JSON response field |

The configuration is saved in the Grist widget options — it persists between sessions.

### ⚠️ CORS Note

If you host Grist self-hosted, the Chrome extension **[Grist Widget Bridge](https://github.com/isaytoo/grist-widget-bridge)** is required to unblock CORS calls to `api.cloudinary.com`.

In the extension popup, add `https://api.cloudinary.com/*` in the **"External API (CORS)"** section.

### 🛠️ Local Development

```bash
git clone https://github.com/isaytoo/grist-upload-widget.git
cd grist-upload-widget
npx serve .
```

### 📄 License

Apache License 2.0 — © 2026 Said Hamadou (isaytoo)
