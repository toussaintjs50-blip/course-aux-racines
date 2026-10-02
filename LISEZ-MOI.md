# La Course aux Racines

## Jouer
Décompressez l'archive dans un dossier puis ouvrez index.html avec Google Chrome. Conservez style.css et game.js à côté. Aucun serveur, téléchargement supplémentaire ou connexion Internet n'est nécessaire.

Choisissez un mode, une difficulté, une durée et un décor. Pilotez avec ↑ et ↓ ou les boutons tactiles. Espace met en pause. Le changement d'onglet suspend automatiquement le jeu. Le bouton Son coupe tous les effets.

## Fichiers
- index.html : accueil, réglages, interface de partie et résultats.
- style.css : présentation, couleurs, adaptation aux petits écrans.
- game.js : questions, formations, défilement, collisions, sons et statistiques.

## Modifier les paramètres
CONFIG, au début de game.js, regroupe points, racines, limite des encadrements, vitesse du personnage, hauteurs des voies, vitesses par difficulté, accélération, grades et environnements/personnages. Les options de durée sont dans le sélecteur duration d'index.html ; mettez aussi à jour CONFIG.durations pour conserver la documentation cohérente. Les nouveaux modes ou durées doivent être ajoutés au formulaire si vous élargissez les choix.

Les formations sont dans nextQuestion(). Le terrain utilise des coordonnées de 1100 × 560 et s'adapte à la largeur de l'écran. Après un changement de vitesses, gardez un délai suffisant pour rejoindre la bonne réponse et éviter les distracteurs. En expert, la séparation de 500 pixels d'un objet précédant la bonne réponse est dimensionnée pour les vitesses actuelles.

## Règles et pédagogie
Chaque bonne réponse rapporte 100 points, sans multiplicateur ni retrait en cas d'erreur. Une collision termine la question. Toutes les réponses de la question disparaissent avant la suivante. Les erreurs et passages affichent la correction, reprise aussi dans le bilan. Les racines sont proposées par sacs mélangés complets dans tous les niveaux. Le mode encadrement parcourt les intervalles de 1–2 à 14–15, avec un entier strictement entre les carrés voisins.

Le pourcentage inclut les questions laissées passer. Une question inachevée à la fin du temps est exclue du bilan. Le record est conservé uniquement pendant l'ouverture de la page, sans stockage ni collecte de données. Le bouton Terminer permet d'obtenir le bilan avant la fin du temps.

## Vérifications
La syntaxe JavaScript et des tests automatisés sur 9000 questions ont été vérifiés : cycles complets, unicité des choix, exactitude des encadrements, score, collisions, erreurs, passages et fin du chronomètre. Ces tests utilisent une interface simulée ; une validation visuelle et un essai en classe sur les ordinateurs cibles restent utiles pour ajuster les vitesses.
