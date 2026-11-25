# Manifeste visuel — Nightmare Relics pour Black

Les fichiers ci-dessous sont les **références visuelles 3D** du pack. Ils décrivent la forme, les matériaux et la silhouette des accessoires à modéliser ou à intégrer dans Unity. Ils ne remplacent pas encore des fichiers `.fbx`, `.glb` ou `.blend` : la modélisation finale nécessite le dossier Unity ou le modèle quadrupède de Black.

| Asset | Concept | Référence |
|---|---|---|
| Twilight — Blank Book Relic | Livre flottant aux pages vierges, couverture sombre et sceau violet | `/manus-storage/black-nightmare-asset-style-reference_e4efbfc3.png` |
| Pinkie — Fractured Cupcake | Cupcake sombre, cœur cramoisi opaque et bougie irrégulière | `/manus-storage/black-nightmare-asset-pinkie-cupcake_a562024f.png` |
| Rainbow — Frozen Wing | Insigne d’aile brisée avec fracture froide et détail bleu glacé | `/manus-storage/black-nightmare-asset-rainbow-wing_fcb2e52a.png` |
| Rarity — Ignored Mirror | Éclat de miroir, ruban de couture et pierre sourde | `/manus-storage/black-nightmare-asset-rarity-mirror_c3011814.png` |
| Fluttershy — Shed Door | Petite porte de cabane entrouverte avec ombre abstraite | `/manus-storage/black-nightmare-asset-fluttershy-door_e261ab4a.png` |
| Applejack — Bat Orchard | Pommes noires et silhouette pleine de chauve-souris | `/manus-storage/black-nightmare-asset-applejack-bat_60ad5a92.png` |

## Recommandation d’intégration

Pour la version **Quest**, fusionner les six pièces dans le mesh principal du quadrupède et conserver un atlas de texture partagé. Les accessoires doivent rester décoratifs et ne pas dépendre de colliders, rigidbodies, cloth, lights, particles ou audio sources. Pour la version **PC**, une variante peut ajouter des normales précalculées, une légère animation d’activation et des détails de surface, sans modifier la silhouette principale.

Le meilleur emplacement est un harnais dorsal léger, complété par deux points latéraux sur les flancs. Le livre, la porte et le miroir peuvent occuper le harnais ; le cupcake, l’aile et les pommes peuvent être répartis sur les flancs ou la queue. Chaque pièce doit pouvoir être activée séparément dans un menu d’avatar, puis fusionnée ou masquée dans la variante Quest.

## Étape nécessaire pour obtenir des meshes exportables

Un modèle 3D quadrupède de Black ou un dossier Unity lié doit être fourni avant la production de fichiers exportables. À ce moment-là, le pack pourra être retopologisé, skinné sur le rig existant, fusionné dans le mesh principal, atlacé, puis testé dans le SDK VRChat sur PC et Android/Quest.
