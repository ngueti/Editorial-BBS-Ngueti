# Comment mettre le site en ligne sur Vercel

Ce dossier `site/` contient l'intégralité du site bilingue, prêt à déployer.

## Structure
```
site/
├── index.html          → Page d'accueil (choix FR / EN)
├── lire/index.html     → Éditorial en français
├── en/index.html       → Éditorial en anglais
├── assets/             → Les 9 images (format WebP, optimisées)
└── vercel.json         → Configuration (URLs propres)
```

Une fois en ligne, les adresses seront :
- `votre-site.vercel.app/`        → accueil
- `votre-site.vercel.app/lire`    → article français
- `votre-site.vercel.app/en`      → article anglais

Le sélecteur de langue (FR / EN) en haut à droite de chaque article relie les deux versions ; le losange ◆ ramène à l'accueil.

---

## Méthode 1 — Glisser-déposer (la plus simple, sans logiciel)

1. Rendez-vous sur **https://vercel.com/new**
2. Cherchez l'option **« Deploy a folder »** (déployer un dossier) ou faites glisser
   directement le dossier `site/` dans la zone d'import.
3. Donnez un nom au projet (ex. `editorial-ngueti-bbs`).
4. Cliquez sur **Deploy**. En moins d'une minute, le site est en ligne.

> Astuce : si vous voulez remplacer le projet existant `editorial-ngueti-bbs`
> (dont seule la page d'accueil est actuellement déployée), donnez le même nom,
> ou déployez sous un nouveau nom puis supprimez l'ancien.

---

## Méthode 2 — Avec Vercel CLI (pour les habitués du terminal)

1. Installez l'outil une seule fois :
   ```
   npm i -g vercel
   ```
2. Dans un terminal, placez-vous dans ce dossier :
   ```
   cd chemin/vers/site
   ```
3. Déployez en production :
   ```
   vercel --prod
   ```
   Suivez les invites (connexion à votre compte, nom du projet). Terminé.

---

## Vérifier que tout fonctionne

Après déploiement, ouvrez :
- l'accueil → les deux cartes FR / EN et le portrait doivent s'afficher ;
- `/lire` → l'éditorial français complet, avec la galerie BBS et les images ;
- `/en` → la version anglaise ;
- le bouton **FR / EN** en haut à droite → bascule correcte entre les deux langues.

## Rendre le site public (si besoin)

Vous avez déjà désactivé la protection. Si un nouveau projet la réactive par défaut :
**Settings → Deployment Protection → Disabled**, puis **Save**.

## Domaine personnalisé (optionnel)

Pour une adresse à votre nom (ex. `editorial.mondomaine.com`) :
**Settings → Domains → Add**, puis suivez les instructions DNS de Vercel.

---

*Tous les fichiers sont autonomes et optimisés (site complet ≈ 190 Ko).
Aucune dépendance externe hormis les polices Google (Cormorant Garamond + Montserrat),
chargées automatiquement.*
