Exploitation des images prises par des caméras de surveillance
=============================================================

La conjointe de la victime a révélé que la veille du meurtre, la victime avait passé une partie de sa soirée à décoder un message secret. La victime aurait affirmé avoir ramassé ce message secret, scotché à un caillou, lorsqu'elle récupérait sa bicyclette au parking à vélos du lycée, avant d'aller à son entraînement de basket, le même jour.

Le visionnage des caméras de surveillance du parking à vélos, atteste cette version puisque aux alentours des 16h35, on peut observer la scène suivante:

Caméra 1:

- 16:36:18 La victime entre dans le champ de vision de la caméra, s'approche de son vélo et semble oeuvrer pour détacher un antivol.

- 16:36:23 En arrière plan, on peut distinguer à travers le grillage de l'enceinte du lycée, le bas de pantalon et les chaussures d'une personne s'approchant depuis l'extérieur du parking à vélo. La victime occupée sur son vélo ne voit pas cette personne.

- 16:32:25 La personne extérieure sort du champ de vision de la caméra rapidement. C'est à ce moment là que la victime se tourne vers la façade du batiment d'enseignement technologique comme attirée par un bruit, elle fait quelques pas et ramasse un objet sur le sol.

- 16:37:05 La victime inspecte un moment l'objet ramassé, semble détacher quelquechose qui se révèle être un bout de papier qu'elle observe un moment et glisse dans son sac à dos.

- 16:37:51 Elle retourne ensuite à son vélo puis quitte les lieux.

Caméra 2:

- 16:36:24.16 Un tâche floue apparait sur la vidéo. Le visionnage image par image révèle le déplacement dans les airs d'un objet de petite taille en direction du batiment des enseignements technologiques par dessus l'abri du parking à vélo.

La personne observée incomplètement à partir de 16:36:23 n'est visible sur aucune autre caméra. Nous avons la conviction que cette personne jette effectivement une pierre sur laquelle serait attaché le message codé depuis ce lieu vers le batiment
d'enseignement technologique. Nous appelerons dorénavant cette personne le lanceur.

Une visite du parking à vélo a permis à la police scientifique d'effectuer les relevés suivants:

- On a retrouvé une pierre à l'endroit où la victime avait laissé un objet sur la vidéo. On a pu relever des traces de colle sur cette pierre. On a pu aussi relever des traces d'un choc entre la pierre et la facade du bâtiment. Un point d'impact a été identifié sur le mur.

On a pu effectuer dans le plan de la trajectoire du caillou, un ensemble de mesures.

Partie 1: Schéma des lieux.
========

Utiliser le logiciel [geogebra](https://www.geogebra.org/) pour réaliser une modélisation de la situation.

L'origine du repère est choisi au bas du grillage délimitant l'enceinte du lycée.

1. Régler les arrondis à 15 décimales (option /Arrondi).

1. Construire le segment pour le toit du parking à vélo A(0,3) et B(4.6,3).

1. Placer le point C(7.75,4.22) pour la caméra 1.

1. Tracer la droite (CB) qui constitue la limite du champ de vision de la caméra produite par le toit du parking à vélo empèchant de voir davantage le lanceur.

1. L'angle formé par la partie la plus haute observable du lanceur et ses chaussures (où il se tient donc sur le sol) est de 1.46°. Construire cet angle et en déduire la position du personnage extérieur.

1. On suppose que le point d'impact sur le mur correspond au point D(7.75,1.956) où l'on a retrouvé une marque. Placer ce point.

Partie 2: Exploitation de la trajectoire.
========

La caméra 2 révèle les données suivantes:

|t(s)|24.16|24.2|24.24|24.28|24.32|24.36|24.4|24.44|24.48|
|---|---|---|---|---|---|---|---|---|---|
|x(m)|0.3|1.1|1.9|2.7|3.5|4.3|5.1|5.9|6.7|
|h(m)|3.856|4.184|4.384|4.456|4.4|4.216|3.904|3.464|2.896|

1. Rentrer les couples (x,h) dans le tableur de geogebra. Sélectionner la plage de valeurs et demander à géogebra de produire la liste de points correspondante.

1. Combien la caméra prend-t-elle d'images par seconde ?

1. La trajectoire réalisée par le caillou est une parabole, c'est à dire le graphe d'une fonction de la forme ax^2+bx+c. Réaliser un tel graphe sur géogebra. Valider la proposition de créer trois curseurs pour les trois paramètres a,b,c.

1. Ajuster les trois paramètres pour faire passer la courbe le plus près possible des points placés précédemment.

1. Dans la champ de saisie utiliser la fonction polynôme avec trois points de la trajectoire.

1. La trajectoire obtenue est elle compatible avec le point d'impact retrouvé sur le mur ?

1. Des études ont montré que les projectiles lancés à la main sont lachés 10 centimètres au dessus de la tête, quelle est la taille du lanceur ?

<!-- -0.1x2+0.55x+3.7 (-2.3872,1.81715) -->

Partie 3: Chute de corps dotés d'une vitesse initiale.
=========

Tout objet est attiré par tout autre objet de masse non nulle. Cependant, l'attraction qu'exerce un objet sur un autre, à la surface de la terre est négligeable davant l'attraction exercée par la terre sur ces objets. On appelle pesanteur cette dernière attraction.

On suppose que la taille des objets que nous allons considérer est suffisament petite pour que l'on puisse considérer la terre comme un demi-espace de masse homogène dont la surface est donc un plan qualifié d'horizontal.

Chute verticale d'un corps:
--------------

Un corps laché (sans vitesse initiale) au voisinage de la surface de la terre se met en mouvement depuis sa position initiales en accélérant dans la direction verticale et vers le bas jusqu'à heurter la surface de la terre. Sa trajectoire est verticale. Nous allons voir que son mouvement est uniformément accélré.

1. La force F verticale vers le bas qui s'exerce sur ce corps vaut mg où m est la masse de ce corps et g la constante de pesanteur qui est une accélération. En appliquant le principe fondamental de la dynamique, montrer que le mouvement du corps est uniformément accéléré.

2. En prenant pour origine du temps, le moment où le corps commence sa chute, quelle est sa vitesse au bout d'une seconde ? 2 secondes  ? t secondes ?

3. On admet alors que la position du corps à l'instant t vaut h(t)=h(0)-0.5gt^2. On appelle équation horaire du mouvement l'équation y=h(t). En utilisant un curseur pour le paramètre t et en construisant le point (0,h(t)) réaliser sous géogebra une animation de la chute d'un corps.

4. Si maintenant le corps est lancée verticalement avec la vitesse v, on admet que la nouvelle équation horaire du mouvement obtenu est h(t)=h(0)+vt-0.5gt^2.
Réaliser une simulation d'un tel mouvement avec géogebra.

Chute parabolique d'un corps:
-----------------------------

Si maintenant le corps est lancé dans un direction non verticale. On considère le plan engendré par la verticale et la direction du vecteur vitesse. On choisit un repère orthonormé d'axes horizontal et vertical et d'origine un point sur le sol. On note (u,v) les composantes du vecteur vitesse au commencement du mouvement qu'on choisit comme origine du temps. L'équation horaire pour la coordonnée verticale est la même que précédemment. Horizontalement, l'objet réalise un mouvement uniforme de vitesse constante u. Ainsi, l'équatio horaire du mouvement est:

x(t)=x(0)+ut et y(t)=y(0)+vt-0.5gt^2.

1. Réaliser une simulation d'un tel mouvement sur géogébra.

1. On se place maintenant dans le cas où (x(0),y(0))=(0,0) est l'origine du repère. Dans ce cas, t=x(t)/u. En remplaçant t par cette valeur dans l'équation horaire y(t), donner une équation y=g(x) pour la trajectoire du corps.

1.  On appelle portée de la trajectoire la distance à laquelle le corps se trouve sur le sol de sa position initiale.
Si on double la vitesse initiale du corps, réaliser à l'aide de géogebra une conjecture reliant la portée de la trajectoire initiale et celle de la trajectoire obtenue.

1. Résoudre l'équation y(x)=0. En déduire une formule pour la portée de la trajectoire.

1. Démontrer alors la conjecture précédente.
