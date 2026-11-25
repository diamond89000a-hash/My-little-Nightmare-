# Pack 3D — Les cauchemars des Mane Six pour Black

## Intention

Le pack est conçu pour un avatar quadrupède de Black dans VRChat. Chaque élément doit évoquer un cauchemar précis sans reproduire de scène graphique : silhouettes, objets-symboles et effets sobres sont privilégiés afin de conserver l’identité psychologique de *My Little Nightmare* tout en restant lisible en réalité virtuelle.

## Structure du pack

| Cauchemar | Élément 3D proposé | Emplacement recommandé | Fonction visuelle |
|---|---|---|---|
| Twilight Sparkle | Livre flottant aux pages vierges, avec sceau violet très discret | Harnais dorsal ou orbite lente autour des épaules | Représenter la connaissance effacée |
| Pinkie Pie | Cupcake fissuré avec cœur rouge opaque, sans détail graphique | Petit accessoire latéral ou médaillon dorsal | Évoquer le sucre devenu inquiétant |
| Rainbow Dash | Aile brisée stylisée transformée en insigne, sans modifier le rig principal | Plaque d’épaule ou élément dorsal | Représenter l’impossibilité de voler |
| Rarity | Éclat de miroir et ruban de couture désassemblé | Collier, crinière ou harnais | Évoquer la création ignorée et l’identité fragmentée |
| Fluttershy | Porte miniature de cabane avec ombre intérieure abstraite | Élément dorsal ou pendentif | Évoquer la cabane et le reflet inquiétant |
| Applejack | Grappe de pommes noires et petite silhouette de chauve-souris pleine | Flanc, selle ou queue | Faire référence à « Bats! » et à la perte de contrôle |

## Contraintes de production PC + Quest

La cible de conception est un avatar Quest raisonnable, même si une variante PC peut recevoir davantage de détails. Le budget de référence du pack complet est de **moins de 10 000 triangles pour l’avatar final**, avec une préférence pour un seul Skinned Mesh Renderer, un seul atlas de texture et un ou deux matériaux maximum. Les éléments sont donc pensés comme une pièce fusionnable dans le mesh principal plutôt que comme six objets skinnés indépendants.

Chaque accessoire doit fonctionner avec des matériaux compatibles mobile VRChat. Les détails complexes seront simulés par des silhouettes, des couleurs plates et quelques normales précalculées pour la version PC. La version Quest doit utiliser un matériau mobile opaque ou cutout avec une texture maximale de 1024 px, sans lumière, caméra, cloth, rigidbody, particules lourdes ni shader propriétaire non compatible.

| Cible | Budget de conception |
|---|---:|
| Triangles ajoutés par élément | 150 à 500 |
| Triangles ajoutés pour les six éléments | 1 800 à 2 400 |
| Textures | Un atlas 1024×1024 partagé |
| Matériaux | 1 mobile, 1 PC optionnel |
| Meshes | Fusion dans le mesh principal à l’export |
| PhysBones | Aucun par défaut ; animation via blend shapes ou os existants |
| Transparence | Évitée ; cutout seulement si nécessaire |

## Règles pour l’avatar quadrupède

Les pièces doivent respecter une silhouette lisible de trois quarts et de profil. Elles seront placées sur des points stables du corps — selle, flancs, collier, queue ou harnais — afin de ne pas gêner les pattes ni le contact au sol. Les six éléments doivent pouvoir être activés séparément dans Unity, mais la version Quest finale devra être fusionnée et limitée à un seul rendu skinné autant que possible.

Les animations prévues sont volontairement simples : apparition progressive du sceau, rotation lente du livre ou du miroir sur PC, et version statique sur Quest. Aucun élément ne doit dépendre d’un système de particules, d’un collider ou d’une simulation physique pour rester fiable et performant.

## Livrables visuels prévus

Le pack commencera par six concepts visuels cohérents, un par cauchemar, destinés à guider la modélisation low-poly. Chaque concept devra montrer une pièce 3D isolée sur fond sombre neutre, en vue trois quarts, avec une silhouette claire et sans texte intégré. La modélisation et l’export Unity pourront ensuite être réalisés à partir de ces références lorsque le dossier Unity de l’avatar sera lié.

> Les seuils de performance sont des objectifs de conception, pas une garantie automatique de classement VRChat. Le SDK et Unity doivent confirmer les statistiques de l’avatar final avant l’upload.

## Sources techniques

Les recommandations s’appuient sur la documentation officielle VRChat relative aux classements de performance, à l’optimisation Android/Quest et aux conseils d’optimisation des avatars [1] [2] [3].

## Références

[1]: https://creators.vrchat.com/avatars/avatar-performance-ranking-system "VRChat Creation — Performance Ranks"
[2]: https://creators.vrchat.com/platforms/android/quest-content-optimization/ "VRChat Creation — Android Content Optimization"
[3]: https://creators.vrchat.com/avatars/avatar-optimizing-tips/ "VRChat Creation — Avatar Optimization Tips"
