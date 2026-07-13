# KCP — Kaizen Corporation

Site vitrine de l'agence de marketing digital **KCP** (Kaizen Corporation).
Un seul fichier autonome : `index.html` (HTML + CSS + JS + logo intégré). Aucune dépendance à installer.

---

## Mettre le site en ligne avec GitHub Pages

### Option A — sans terminal (recommandé la première fois)

1. Sur github.com, clique sur **New** (ou le **+** en haut à droite → *New repository*).
2. Donne un nom au dépôt, par ex. `kcp-site`. Laisse-le en **Public** (obligatoire pour Pages gratuit). Ne coche rien d'autre. → **Create repository**.
3. Sur la page du dépôt vide, clique **uploading an existing file** (ou *Add file → Upload files*).
4. Glisse-dépose le fichier **`index.html`** (et `README.md` si tu veux). → **Commit changes**.
5. Onglet **Settings** → menu de gauche **Pages**.
6. Sous *Build and deployment* → *Source* : choisis **Deploy from a branch**.
7. Branche : **main**, dossier : **/ (root)**. → **Save**.
8. Attends 1 à 3 minutes, recharge la page Pages : l'URL publique s'affiche en haut.

➡️ Ton site sera à : `https://<ton-pseudo>.github.io/kcp-site/`

> Astuce : si tu nommes le dépôt exactement `<ton-pseudo>.github.io`, le site sort直接 sur `https://<ton-pseudo>.github.io/` (racine, sans sous-dossier).

### Option B — avec Git (pour les mises à jour ensuite)

Le dossier est déjà un dépôt Git avec un premier commit. Il te reste à le relier à GitHub :

```bash
# dans le dossier kcp-site/
git remote add origin https://github.com/<ton-pseudo>/kcp-site.git
git branch -M main
git push -u origin main
```

Puis active Pages comme aux étapes 5-8 ci-dessus.
Pour publier une modification plus tard :

```bash
git add .
git commit -m "mise à jour du site"
git push
```

---

## Vérifier que ça marche

- La page Pages (Settings → Pages) affiche « Your site is live at … ».
- L'URL s'ouvre et montre l'animation d'ouverture puis le site.
- Si tu vois une page **404** : vérifie que le fichier s'appelle bien `index.html`, qu'il est à la **racine** du dépôt, que le dépôt est **Public**, et regarde l'onglet **Actions** pour d'éventuelles erreurs de build.

## Modifier le site

Tout est dans `index.html`. Points utiles à personnaliser :
- l'email `bonjour@kcp.agency` (dans le pied de page) → ton vrai email ;
- le formulaire de contact est en démo (il affiche une confirmation sans envoyer) — à brancher sur un service type Formspree, ou en `mailto:`.

## Domaine personnalisé (plus tard)

Si tu achètes un domaine (ex. `kcp.fr`), ajoute un fichier nommé `CNAME` (sans extension) à la racine contenant `kcp.fr`, puis configure les DNS chez ton registrar. GitHub fournit le HTTPS automatiquement.
