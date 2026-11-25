# Vérification intermédiaire — porte HORROR

Les fiches `/cauchemar/twilight` et `/cauchemar/pinkie` s’ouvrent correctement. Le sceau `Fragment / HORROR` affiche respectivement `H` et `O`, et les pages exposent bien leurs interactions existantes. Le parcours d’enregistrement local des fragments peut continuer avec les quatre autres fiches.

Rainbow Dash et Rarity s’ouvrent correctement et affichent chacune le fragment `R`. La progression attendue est maintenant H-O-R-R, avec Fluttershy et Applejack restant à visiter avant de tester la saisie du code.

Fluttershy et Applejack s’ouvrent correctement et affichent respectivement `O` et `R`. Les six visites du parcours H-O-R-R-O-R ont maintenant été effectuées dans la session de test ; l’étape suivante consiste à vérifier que `/horror` reconnaît les six fragments et accepte uniquement le code HORROR.

Après les six visites, `/horror` reconnaît bien `6 / 6 fragments retrouvés`, affiche les lettres H-O-R-R-O-R et active le champ de code. Le dossier reste scellé tant que le code correct n’est pas soumis ; le test du code incorrect a confirmé que l’accès n’est pas accordé.

Le code incorrect est refusé, puis le code `HORROR` est accepté après la collecte des six fragments. La page passe à `OPEN`, le bouton devient `DOSSIER OUVERT` et la section `La creepypasta originale` apparaît avec ses cinq chapitres narratifs. Le parcours de déverrouillage est validé.
