# Publication GitHub Pages

1. Créer un dépôt GitHub public, branche `main`.
2. Décompresser le ZIP et transférer tout son contenu à la racine du dépôt, y compris `.github/workflows/pages.yml`.
3. Settings > Pages > Build and deployment > Source : GitHub Actions.
4. Actions > Deploy GitHub Pages > Run workflow (main). L'adresse est affichée dans le job deploy.

Les médias ne figuraient pas dans le ZIP original. Les liens pointent donc vers le site Manus public d'origine. Leur disponibilité et les téléchargements cross-origin ne sont pas garantis. Pour rendre le site indépendant, placer les fichiers originaux (noms exacts dans `scripts/media-list.json`) dans `client/public/manus-storage/`, puis relancer le déploiement. Les fichiers locaux seront utilisés automatiquement. Les médias dépassant 100 Mo doivent être compressés ou hébergés séparément.

Test local : Node.js 22, `corepack enable`, `pnpm install --frozen-lockfile`, `pnpm dev`. Pour la compilation Pages : `pnpm build:pages` puis `pnpm preview` (racine par défaut). Le workflow configure automatiquement le préfixe du dépôt. Les sauvegardes localStorage du domaine Manus ne sont pas transférées vers GitHub Pages.

Le code de l'énigme, les pages et les styles sont conservés. GitHub Pages est statique : les secrets de l'énigme restent visibles dans le JavaScript public.
