# RustyGames
Projet de dévelopement d'un jeu vidéo en Rust avec le moteur de jeu Bevy et le moteur physique Heron. Nous avions 2 semaines intensives pour prendre en main le language et l'architecture ECS du moteur de jeu puis designer et implémenter le jeu choisi en équipe de 5. Le Level Design a été réaliser à l'aide de l'outil LDTK.

Le joueur incarne un slime qui possède le pouvoir de manipuler la gravité. A l'aide de R et T, le joueur peut provoquer une rotation du monde à 90° dans un sens, ou dans l'autre. Les flèches directionnelles sont utilisé pour le déplacement à droite et à gauche. Le but est alors de résoudre un ensemble de puzzle dans le but d'atteindre un drapeau pour avancer de salle en salle.

# Images
![01](https://github.com/MonsieurMajy/slime/assets/90928733/6fae2266-6ac3-44c7-9433-cef9360f3829)
![02](https://github.com/MonsieurMajy/slime/assets/90928733/c632b02d-3d85-48a5-af66-84f803c1a0ff)
![03](https://github.com/MonsieurMajy/slime/assets/90928733/5b269d04-e46d-4596-a09a-2921367f3308)
![04](https://github.com/MonsieurMajy/slime/assets/90928733/f04a256c-df9f-416d-9d18-ee02f7fad684)
![05](https://github.com/MonsieurMajy/slime/assets/90928733/3645d662-40d4-475e-ac9d-0747051f78f0)
![06](https://github.com/MonsieurMajy/slime/assets/90928733/4c5acf09-497f-439f-b7bf-1bd8f71c731f)


# Design Document
## Controle
R et T pour changer le sens de la gravité
Flèches droite et gauche pour se déplacer

## type de jeu
puzzle avec plateforme et gravité 


## Pitch 
Le joueur incarne un blob qui à la capacité de changer l’action de la gravité sur le monde, il devra ingénieusement utiliser ce pouvoir pour accéder à la sortie de cette cage infernale.


## Niveaux

Au début, les niveaux auront le moins d'éléments possibles et seront rapidement réalisables pour que le joueur prenne en main les différentes mécaniques principales à offrir. Puis au fur et à mesure, il y aura plus de nouveaux éléments, mécaniques, pièges et ennemis éventuellement, avec des niveaux plus gros.

(dernier niveau : l'extérieur, pas dans une cage? ) 
 
## Mouvement de base : 
	- en ligne droite sur une même paroi
	- changement de parois adjacentes : changement de gravité
	- saut ? 
	
## Eléments : 
	Sortie : porte, tube ou  drapeau ? 
	entrée : même que sortie mais fermé
	
### Eléments soumis à la gravitée :
		- boîtes -> Peut tomber sur une switch sous l’effet de la gravité et activer une porte

### Eléments fixe : 
		- spikes -> tue le joueur et le fait reset jusqu’au début du niveau
		- ventilateurs -> ventilateurs
		
### Autre éléments qui bougent : 
		- ennemi 1  -> slime avec un mouvement aléatoire 
		- ennemi 2  -> slime qui bouge en même temps que le joueur
		- plateformes -> certaines bougent et ont un mouvement qui reste le même,  certaines sont statiques, certaines se cassent après le passage	
	
### Pièges : 
		- Activation par bouton
		- De l’eau/du gaz qui envahit le niveau ? Et faut boucher les fuites avec les briques
		- Des truc qui explosent en repoussant le joueur et les briques proches
		- Enfermer le slime dans une boite (contrôle de la gravité depuis l'intérieur et devoir faire ‘tomber’ la boite dans la sortie ou sur quelque chose qui va casser la boite)

### Mécaniques : 
		- Le slime peut se diviser en 2 et on peut contrôler les 2 en même temps
		- Une salle avec un vortex au milieu qui aspire les objets ou unités vers son centre
	
### Consommable  :
On peut récupérer des objets activables qui donnent un gros bonus de vitesse pendant 1s.

#### Buffs et debuffs possibles:
 	- Sauts plus haut
 	- Perception du temps ralentie
	- Télékinésie
 	- Annihilation des ennemies sous un certain radius
 	- vitesse décrue
	- vision floue/restreinte
	- ennemis plus agressifs peu importe ce qui se passe


