# My Little Nightmare — Concept de map VRChat

## Vision générale

La map sera un monde hybride mêlant exploration libre, escape game horrifique non graphique et espace de rencontre. Le joueur pénétrera dans une archive abandonnée située entre Equestria, le monde réel et le royaume des rêves. Black agit comme guide invisible : il observe les visiteurs, modifie certains éléments du décor et ouvre progressivement les passages vers les cauchemars des Mane Six.

L’expérience doit rester inquiétante sans dépendre du gore. La tension viendra des sons lointains, des changements subtils de décor, des livres vierges, des portes impossibles et des messages qui semblent répondre aux joueurs présents.

## Parcours principal

| Zone | Fonction | Atmosphère | Interaction principale |
|---|---|---|---|
| Vestibule de l’archive | Arrivée et rencontre | Hall sombre, sceau de Black, écrans dormants | Choisir « Explorer » ou « Se réunir » |
| Salle du dossier Black | Présentation de l’univers | Vitrines, portraits, fragments audio | Activer des fiches et écouter des extraits |
| Bibliothèque de Twilight | Escape game 1 | Livres vierges, encre froide, horloge bloquée | Retrouver des mots cachés et ouvrir la sortie |
| Cuisine de Pinkie Pie | Escape game 2 | Couleurs fanées, four allumé, fête silencieuse | Recomposer une recette et éviter les fausses pistes |
| Couloir des six cauchemars | Exploration narrative | Six portes, une lumière différente par porte | Choisir une porte et découvrir une scène |
| Galerie du panthéon secret | Lore et collection | Planche-contact, portraits contaminés | Examiner les six dieux et leurs symboles |
| Place de la Faille | Rencontre sociale | Cour centrale sous un ciel fissuré | Discuter, poser des photos et écouter l’ambiance |
| Chambre de Black | Final secret | Espace noir, lune rouge, miroir sans reflet | Résoudre l’énigme finale et débloquer une sortie |

## Boucle de jeu

Un visiteur commence dans le vestibule, découvre les règles de l’archive, puis choisit une première zone. Les énigmes peuvent être réalisées seul ou à plusieurs. Chaque résolution active un fragment de sceau et modifie légèrement la place centrale. Après trois fragments, la Chambre de Black devient accessible. Les visiteurs qui préfèrent discuter peuvent rester dans la Place de la Faille sans être forcés à participer à l’escape game.

Le monde doit proposer deux chemins complémentaires. Le chemin « archive » privilégie les textes, les portraits et les enregistrements. Le chemin « cauchemar » privilégie les portes, les énigmes, les changements de lumière et les apparitions discrètes. Les deux chemins se rejoignent dans la Chambre de Black.

## Interactions proposées

Les objets interactifs seront peu nombreux mais significatifs : livres à feuilleter, boutons de transmission, portes à symbole, miroirs, lanternes, cartes à assembler et sceaux à activer. Chaque interaction aura une version simple compatible Quest : pointer, toucher, saisir un objet léger ou utiliser un bouton proche.

Black pourra apparaître sous forme de silhouette, de reflet ou de voix, sans jumpscare obligatoire. Les événements seront déclenchés par la progression collective plutôt que par des effets agressifs. Un panneau permettra de réduire les flashs, les sons soudains et les effets de distorsion pour préserver le confort des visiteurs.

## Direction artistique

La map reprend le **cabinet de curiosités nocturne** du site : charbon bleuté, ivoire ancien et cramoisi de la Faille. Les surfaces doivent évoquer du bois sombre, du papier vieilli, du métal peint et du verre poussiéreux. Le cramoisi est réservé aux yeux de Black, aux sceaux, aux alertes et aux fractures dimensionnelles.

Les constructions doivent privilégier des formes simples, des silhouettes fortes et des éclairages localisés. Les détails coûteux seront concentrés dans les zones importantes ; les espaces de circulation resteront plus sobres pour préserver les performances Quest.

## Compatibilité PC + Quest

La version Quest devra utiliser des matériaux simples, des textures compressées, peu de lumières temps réel et des effets de brume limités. Les éléments décoratifs complexes seront remplacés par des textures, des cartes d’émission ou des variantes simplifiées. Les systèmes interactifs devront rester fonctionnels sans dépendre d’effets exclusifs au PC.

La version PC pourra recevoir des ombres plus riches, des particules supplémentaires et une ambiance sonore plus détaillée. L’architecture du monde restera identique afin que les visiteurs PC et Quest puissent parcourir les mêmes zones ensemble.

## Préparation Unity à prévoir

Le projet nécessitera Unity avec le support VRChat Worlds, le SDK officiel VRChat et un projet configuré pour produire une version PC puis une version Android/Quest. La structure recommandée sera organisée ainsi : `Scenes`, `World`, `Materials`, `Textures`, `Audio`, `Prefabs`, `Interactables`, `Lighting`, `Quest_Optimized` et `Documentation`.

Aucun projet Unity ne peut encore être construit directement, car Unity et le SDK VRChat ne sont pas installés et aucun dossier de travail n’est lié dans Manus Desktop. La prochaine étape pratique sera de lier un dossier, installer l’environnement Unity compatible avec le SDK VRChat, puis créer une scène prototype contenant uniquement le vestibule et la Place de la Faille.

## Prototype recommandé

Le premier prototype doit rester petit : un hall d’arrivée, une porte vers la bibliothèque de Twilight, une zone sociale et un premier bouton de transmission. Ce prototype permettra de tester l’échelle, les déplacements, l’éclairage, les interactions et les performances PC/Quest avant de construire les six cauchemars et le panthéon complet.

> Objectif de production : créer d’abord une expérience courte, stable et explorable, puis étendre progressivement l’univers sans sacrifier la lisibilité ni le confort VR.
