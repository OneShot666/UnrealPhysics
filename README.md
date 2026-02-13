# \# UnrealPhysics

# 

# Use the power of physic to finish these challenges !

# 

# ---

# 

# \## 🌀 Description du gameplay

# 

# Ce projet est une exploration technique des systèmes de physique, d'interaction et de possession sous Unreal Engine. 

# Il se compose de trois mécaniques distinctes, présentes dans un des trois niveaux du jeu.

# 

# 

# \### 🕹️ Mécaniques utilisées

# 

# 1\. Manipulation d'objets

# 

# Ce niveau introduit un système d'interaction basé sur la détection d'objets et l'attachement dynamique.

# Le joueur peut attraper des cubes et autres objets movibles en utilisant un système de grab déjà présent dans Unreal Engine.

# 

# Comportements Chromatiques : La physique des cubes après les avoir lâcher dépend de leur couleur :

# \- Rouge : Continue de suivre le joueur

# \- Orange : Tombe et cesse de suivre lel joueur

# \- Rose : Devient complètement statique tant qu'il n'est pas attrapé de nouveau

# 

# 2\. Système de Propulsion

# 

# Focus sur le changement de point de vue et la gestion des trajectoires.

# Possession de Canon : À l'approche d'un canon, le joueur quitte son personnage pour le posséder.

# Il peut alors s'orienter pour viser, tirer ou sortir du canon.

# Power Charge : Un système de jauge de puissance affiche la force de propulsion lors du tir.

# 

# 3\. Physique avancée \& Pouvoirs

# 

# Surfaces Glissantes : Quand le joueur arrive sur de la glace, cette dernière a une friction proche de zéro, ce qui a pour effet de faire glisser le joueur et rendre ses mouvements plus compliqués.

# Balles Rebondissantes : Le joueur peut attraper des balles et lancer lâcher avec un certain élan afin de les faire rebondir. 

# Ces balles ont été configurées avec une restitution élevée pour conserver leur énergie cinétique.

# Le "Push" : Une onde de choc qui repousse les objets proches avec une puissante force.

# 

# 

# \### 🛠️ Choix techniques

# 

# Fonctionnalités adéquates : Utilisations de noeuds tels que "Add Impulse" ou "GrabComponent" pour gérer les forces appliquées aux objets.

# Attributs intrinsèques : Modifications et créations de matériaux physiques pour ajouter des propriétés intéressantes aux objets et décors (balles, glace...)

# Communication par référence : Mise en place de variables "Expose on Spawn" afin de lier des widgets aux acteurs (ex: canons) de manière robuste.

# Organisation des blueprints : Utilisation des dossiers, ajouts de noeuds, couleurs et commentaires pour garder une architecture propre et lisible.

# Interface utilisateur : Création d'interfaces dynamiques (ex: barre de progression, inputs) afin d'indiquer au joueur les actions disponibles.

# Gestion des inputs : Utilisation d'IMC et IA pour gérer la transition fluide entre le déplacement du personnage et le contrôle des canons.

# 

# 

# \### ⚠️ Problèmes rencontrés

# 

# 1\. Chômage cubique

# 

# Problème : Difficulté à "redonner vie" aux cubes une fois lachés.

# Solution : Désactiver la physique à l'impact du sol et configuré leur character movement.

# 

# 2\. Mains glissantes

# 

# Problème : Au lancement, les cubes n'accepter d'être attrapés qu'au 2e essai après divers changements de mécaniques.

# Solution : Leur faire croire à leur création qu'ils sont lâchés pour que le grab du joueur marche dès le premier essai.

# 

# 3\. Des canons muets

# 

# Problème : Difficulté à modifier les textes de l'écran des canons dynamiquement. Aussi, difficulté à trouver le bon bouton "Set Text" parmi tous ceux existants.

# Solution : Activation de l'option "Is Variable" sur les composants Text Block et récupération de la référence du canon par le widget au lancement.

# 

# 4\. Affichage de la Souris dans les Menus

# 

# Problème : Curseur invisible lors du retour au menu principal.

# Solution : Utilisation des nœuds Set Input Mode UI Only et Set Show Mouse Cursor pour gérer son apparition ou non sur les menus.

# 

# 5\. Erreurs de Packaging

# 

# Problème : Échec de la compilation car le dossier de build était verrouillé par un processus tiers.

# Solution : Nettoyage manuel des dossiers Binaries et Intermediate, et vérification des processus fantômes dans le gestionnaire des tâches.

# 

# 

# \## Merci d'avoir joué !

# 

# @ Ouroboros Games - Tous droits réservés - 12 026



