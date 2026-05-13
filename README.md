# 📤 Grist Upload Widget

> **FR** | [EN](#-grist-upload-widget-1)

---

## 🇫🇷 Grist Upload Widget

Un widget Grist simple et élégant pour uploader des fichiers (images, vidéos, PDF, audio…) vers **Cloudinary** et enregistrer automatiquement l'URL dans votre document Grist.

### ✨ Fonctionnalités

- **📁 Upload universel** — Images, vidéos, PDF, audio et tout autre type de fichier
- **☁️ Stockage Cloudinary** — Upload sécurisé via un preset Cloudinary configurable
- **💾 Sauvegarde automatique** — L'URL du fichier est enregistrée directement dans la colonne Grist mappée
- **📊 Barre de progression** — Suivi en temps réel de l'upload
- **🎨 Thème clair/sombre** — S'adapte automatiquement au thème de l'OS ou de Grist
- **⚡ Léger** — Fichier unique, aucune dépendance externe

### 🚀 Installation

1. Dans votre document Grist, ajoutez une vue **Widget personnalisé**
2. Entrez l'URL du widget : `https://grist-upload-widget.vercel.app`
3. Définissez le **Niveau d'accès** sur **Accès complet au document**
4. Dans le **Panneau Créateur**, mappez la colonne :
   - **Colonne de destination** *(obligatoire)* — colonne Text qui recevra l'URL du fichier uploadé
5. Sélectionnez un fichier → cliquez **Enregistrer dans Grist**

### ⚙️ Configuration Cloudinary

Le widget utilise un compte Cloudinary avec les paramètres suivants (à modifier directement dans `index.html`) :

```js
const CLOUD_NAME   = "votre-cloud-name";
const UPLOAD_PRESET = "votre-upload-preset";
```

**Créer un Upload Preset Cloudinary :**
1. Connectez-vous sur [cloudinary.com](https://cloudinary.com)
2. Allez dans **Settings → Upload → Upload presets**
3. Créez un preset en mode **Unsigned**
4. Copiez le nom du preset dans `UPLOAD_PRESET`

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

A simple and elegant Grist widget to upload files (images, videos, PDFs, audio…) to **Cloudinary** and automatically save the URL in your Grist document.

### ✨ Features

- **📁 Universal upload** — Images, videos, PDFs, audio and any other file type
- **☁️ Cloudinary storage** — Secure upload via a configurable Cloudinary preset
- **💾 Auto-save** — The file URL is saved directly into the mapped Grist column
- **📊 Progress bar** — Real-time upload progress tracking
- **🎨 Light/dark theme** — Automatically adapts to the OS or Grist theme
- **⚡ Lightweight** — Single file, no external dependencies

### 🚀 Installation

1. In your Grist document, add a **Custom Widget** view
2. Enter the widget URL: `https://grist-upload-widget.vercel.app`
3. Set the **Access level** to **Full document access**
4. In the **Creator Panel**, map the column:
   - **Destination column** *(required)* — Text column that will receive the uploaded file URL
5. Select a file → click **Save to Grist**

### ⚙️ Cloudinary Configuration

The widget uses a Cloudinary account with the following parameters (edit directly in `index.html`):

```js
const CLOUD_NAME    = "your-cloud-name";
const UPLOAD_PRESET = "your-upload-preset";
```

**Create a Cloudinary Upload Preset:**
1. Log in at [cloudinary.com](https://cloudinary.com)
2. Go to **Settings → Upload → Upload presets**
3. Create a preset in **Unsigned** mode
4. Copy the preset name into `UPLOAD_PRESET`

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
