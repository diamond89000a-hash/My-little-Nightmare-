# My Little Nightmare

Site vitrine sombre et immersif consacré à l’univers fictif **My Little Nightmare** et à son personnage central, **Black**, le dieu des cauchemars.

Le projet présente une expérience narrative inspirée des archives interdites, des rêves perturbés et des six cauchemars des Mane Six. Il combine une direction artistique de cabinet de curiosités nocturne, des dossiers interactifs, des vidéos, des illustrations, des contenus audio et des éléments communautaires liés à l’univers de Black.

> Le contenu narratif, les personnages et les archives présentés sur ce site sont fictionnels.

## Fonctionnalités

- Page d’introduction immersive avant l’entrée dans le site.
- Présentation de l’univers, de Black et de ses archives.
- Pages de cauchemar dédiées à Twilight Sparkle, Pinkie Pie, Rainbow Dash, Rarity, Fluttershy et Applejack.
- Collection progressive des six lettres du mot secret `HORROR`.
- Page d’archive protégée par le code `HORROR`.
- Déblocage de la creepypasta originale après récupération des six fragments.
- Transmission vidéo accessible dans le dossier Horror déverrouillé.
- Rituel d’invocation fictif avec ambiance audio sombre et apparition de Black.
- Galerie et pages de preuves liées à l’univers.
- Page du panthéon et des autres dieux du Royaume des cauchemars.
- Page de téléchargement des skins Minecraft Bedrock de Black.
- Liens externes vers les vidéos et le groupe Discord de la communauté.
- Interface responsive adaptée aux écrans desktop et mobiles.
- Design sombre avec typographies éditoriales, accents cramoisis et effets d’archive.

## Stack technique

- **React 19**
- **TypeScript**
- **Vite**
- **Tailwind CSS 4**
- **Wouter** pour le routage côté client
- **Lucide React** pour les icônes
- **Framer Motion** pour les animations disponibles dans l’interface
- **Express** et **esbuild** pour le serveur de production fourni par le template
- **pnpm** pour la gestion des dépendances

## Prérequis

Avant de commencer, installer :

- Node.js 20 ou une version plus récente recommandée ;
- pnpm 10, ou une version compatible avec le champ `packageManager` du projet ;
- Git si le projet doit être cloné depuis GitHub.

Vérifier les versions installées :

```bash
node --version
pnpm --version
git --version
```

## Installation

Cloner le dépôt puis entrer dans le dossier du projet :

```bash
git clone https://github.com/diamond89000a-hash/my-little-nightmare.git
cd my-little-nightmare
```

Installer les dépendances :

```bash
pnpm install
```

## Développement local

Lancer le serveur Vite en mode développement :

```bash
pnpm dev
```

Le site sera généralement disponible à l’adresse suivante :

```text
http://localhost:3000
```

Le serveur de développement utilise le mode `--host`, ce qui permet également de tester le site depuis un autre appareil connecté au même réseau lorsque la configuration réseau l’autorise.

## Commandes disponibles

| Commande | Description |
| --- | --- |
| `pnpm install` | Installe les dépendances du projet. |
| `pnpm dev` | Lance Vite en mode développement avec rechargement automatique. |
| `pnpm check` | Vérifie le typage TypeScript sans générer de fichiers. |
| `pnpm build` | Génère le build de production Vite et bundle le serveur avec esbuild. |
| `pnpm start` | Lance le serveur compilé en mode production. |
| `pnpm preview` | Prévisualise le build Vite généré. |
| `pnpm format` | Formate les fichiers avec Prettier. |

Avant de publier une modification, il est recommandé d’exécuter :

```bash
pnpm check
pnpm build
```

## Tester le build de production

Générer les fichiers de production :

```bash
pnpm build
```

Puis lancer le serveur compilé :

```bash
pnpm start
```

Le build produit les fichiers statiques dans `dist/public` ainsi qu’un bundle serveur dans `dist/index.js`.

## Routes principales

| Route | Contenu |
| --- | --- |
| `/` | Page d’introduction et seuil d’entrée dans l’univers. |
| `/site` | Accueil principal de My Little Nightmare. |
| `/cauchemar/:slug` | Page d’un cauchemar individuel. |
| `/journal` | Journal audio et éléments narratifs associés. |
| `/preuves` | Page des preuves et transmissions récupérées. |
| `/dossier-interdit` | Dossier consacré au panthéon et aux dieux. |
| `/horror` | Archive Horror, fragments, code secret et creepypasta déverrouillable. |
| `/rituel` | Rituel d’invocation fictif de Black. |
| `/minecraft` | Téléchargement des skins Minecraft Bedrock. |

Les six pages de cauchemar utilisent les identifiants suivants :

```text
twilight
pinkie
rainbow
rarity
fluttershy
applejack
```

## Déverrouillage de l’archive Horror

La page `/horror` conserve la progression dans le `localStorage` du navigateur. Pour débloquer l’archive :

1. Ouvrir les six pages de cauchemar.
2. Récupérer chaque lettre du mot secret.
3. Revenir sur la page Horror.
4. Saisir le code :

```text
HORROR
```

Une fois l’archive ouverte, la creepypasta originale, la transmission vidéo et le lien vers le groupe Discord deviennent visibles.

Pour réinitialiser la progression dans un navigateur de développement, supprimer les clés `mln-nightmare-found-*` et `mln-horror-unlocked` dans le stockage local du site.

## Structure du projet

```text
.
├── client/
│   ├── public/              # Petits fichiers publics de configuration
│   └── src/
│       ├── components/      # Composants réutilisables et composants UI
│       ├── contexts/        # Contextes React, notamment le thème
│       ├── hooks/           # Hooks réutilisables
│       ├── lib/             # Fonctions utilitaires
│       ├── pages/           # Pages et routes de l’expérience
│       ├── App.tsx          # Routage principal
│       ├── const.ts         # Constantes côté client
│       └── index.css        # Design tokens et styles globaux
├── server/
│   └── index.ts             # Point d’entrée du serveur de production
├── shared/
│   └── const.ts             # Constantes partagées
├── patches/                 # Correctifs de dépendances
├── package.json             # Scripts et dépendances
├── pnpm-lock.yaml           # Verrouillage des versions pnpm
├── tsconfig.json            # Configuration TypeScript
├── vite.config.ts           # Configuration Vite
└── README.md                # Documentation du projet
```

## Médias et stockage

Les images, vidéos et fichiers audio volumineux ne doivent pas être ajoutés directement dans `client/public` ou `client/src`. Dans l’environnement WebDev, les médias sont hébergés dans le stockage persistant puis référencés par leur chemin de stockage.

Pour un nouveau média destiné au site, conserver l’original en dehors du dossier du projet et utiliser le workflow d’upload prévu par l’environnement :

```bash
manus-upload-file --webdev chemin/vers/le-fichier.png
```

Le chemin retourné peut ensuite être utilisé dans le code React, par exemple :

```tsx
<img src="/manus-storage/mon-image.png" alt="Description de l’image" />
```

Éviter de committer des fichiers binaires lourds dans GitHub afin de conserver un dépôt rapide à cloner et à déployer.

## Ajouter une nouvelle page

1. Créer un composant dans `client/src/pages/`.
2. Ajouter la route correspondante dans `client/src/App.tsx`.
3. Réutiliser les composants et les tokens déjà présents dans `client/src/index.css`.
4. Vérifier l’affichage desktop et mobile.
5. Exécuter `pnpm check` puis `pnpm build`.
6. Tester la navigation et les liens externes avant de pousser la modification.

## Déploiement

Le projet peut être déployé sur une plateforme compatible avec une application Vite/Node.js. Le processus général est :

```bash
pnpm install
pnpm build
pnpm start
```

Le serveur doit utiliser la commande `pnpm start` après la génération du build. Pour un hébergement statique uniquement, les fichiers Vite générés dans `dist/public` peuvent être servis par un serveur web statique, à condition que le routage SPA soit configuré pour rediriger les routes inconnues vers `index.html`.

## Contribution

Pour proposer une modification :

1. Créer une branche dédiée :

   ```bash
   git checkout -b feature/ma-modification
   ```

2. Modifier le projet et vérifier le résultat.
3. Lancer les contrôles :

   ```bash
   pnpm check
   pnpm build
   ```

4. Créer un commit descriptif.
5. Pousser la branche et ouvrir une Pull Request.

Les nouvelles contributions doivent respecter la direction artistique sombre, maintenir une bonne lisibilité et rester compatibles avec les écrans mobiles.

## Communauté

Le groupe Discord associé à l’univers de Black est accessible depuis l’archive Horror après son déverrouillage :

[Rejoindre le groupe Discord](https://discord.gg/VeRpMD6Szg)

## Licence

Le projet est déclaré sous licence **MIT** dans `package.json`. Vérifier les droits d’utilisation des ressources externes, des vidéos, des musiques, des images et des liens intégrés avant toute redistribution publique.
