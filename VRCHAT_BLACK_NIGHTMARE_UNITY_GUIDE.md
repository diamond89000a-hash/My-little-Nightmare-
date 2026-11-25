# Guide d’intégration Unity/VRChat — Nightmare Relics

## État du pack

Le fichier `black-nightmare-vrchat-asset-prototypes.zip` contient six prototypes OBJ low-poly et leurs fichiers MTL. Ils servent de base de blocage et de référence de silhouette. Ils ne sont pas encore skinnés au rig quadrupède de Black et ne doivent pas être téléversés tels quels comme avatar final.

## Import dans Blender ou Unity

Importez chaque paire `.obj` + `.mtl` dans Blender, appliquez une échelle cohérente, puis positionnez les pièces sur un harnais dorsal, les flancs ou la queue. Fusionnez ensuite les meshes avec le mesh principal de Black. Le résultat attendu pour Quest est un seul Skinned Mesh Renderer lorsque le modèle final le permet.

Les prototypes utilisent une géométrie volontairement simple. La phase de production devra remplacer les volumes de blocage par une retopologie propre, ajouter les biseaux indispensables à la lisibilité, puis projeter les détails dans un atlas partagé. Les six accessoires doivent conserver une silhouette claire de profil et de trois quarts.

## Variante Quest

La variante Quest doit utiliser un matériau mobile VRChat opaque ou cutout, une texture atlas maximale de 1024×1024 et des couleurs plates. Supprimez les lights, cameras, cloth, rigidbodies, colliders, particles lourdes, audio sources et shaders non compatibles Android. Les animations doivent être portées par des os déjà présents, des blend shapes simples ou une activation statique.

L’objectif de conception est de rester sous 10 000 triangles pour l’avatar complet et sous 10 MB après compression, avec un nombre minimal de meshes et de material slots. VRChat indique que les valeurs finales doivent être contrôlées dans le SDK et que les limites peuvent évoluer [1] [2].

## Variante PC

La variante PC peut recevoir une texture plus détaillée, des normales précalculées et une animation d’activation légère. Évitez néanmoins les systèmes qui augmentent fortement les draw calls ou la charge de simulation. L’avatar doit rester confortable en présence de plusieurs utilisateurs.

## Animations et menu d’avatar

Chaque relique peut correspondre à un booléen dans un menu radial : `Nightmare_Twilight`, `Nightmare_Pinkie`, `Nightmare_Rainbow`, `Nightmare_Rarity`, `Nightmare_Fluttershy` et `Nightmare_Applejack`. Sur Quest, l’animation peut être réduite à une visibilité on/off. Sur PC, l’activation peut ajouter une rotation lente au livre ou au miroir, mais sans particules ni lumière dynamique.

## Validation avant upload

Avant l’upload, contrôlez dans le SDK le nombre de triangles, de meshes, de materials, de bones, de PhysBones et la mémoire texture. Testez séparément la version PC et la version Android/Quest sur un appareil réel ou dans un profil de performance proche de la cible. La documentation VRChat recommande également d’utiliser le Unity Profiler et de viser une hiérarchie de mesh très compacte [2] [3].

## Références

[1]: https://creators.vrchat.com/avatars/avatar-performance-ranking-system "VRChat Creation — Performance Ranks"
[2]: https://creators.vrchat.com/platforms/android/quest-content-optimization/ "VRChat Creation — Android Content Optimization"
[3]: https://creators.vrchat.com/avatars/avatar-optimizing-tips/ "VRChat Creation — Avatar Optimization Tips"
