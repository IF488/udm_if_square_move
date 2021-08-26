# udm_if_square_move
Ce package contient le package de la partie 3 du TP4
Il permet de décrire un carré avec le Turtlebot3 en faisant appel au service move_base/goal


## Installation
Pour installer ce noeud il faut le cloner dans le dossier src de votre catkin workspace (catkin_ws).

```
cd catkin_ws/src
git clone https://github.com/IF488/udm_if_square_move.git
catkin build
cd ..
source devel/setup.bash
```

## Execution
Dans un premier terminal, lancer Gazebo:

```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

Dans un deuxième terminal, lancer le noeud de navigation présent dans le package:

```
roslaunch udm_if_square_move turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

Dans un troisième terminal, lancer le noeud movebase_square.py

```
rosrun udm_if_square_move movebase_square.py
```

PS: La map utilisé est fourni dans le fichier. Placer map.yaml et map.pgm dans le fichier HOME de votre PC. Vous pouvez aussi placer la map dans un autre fichier à condition de changer l'argument dans la command ci-dessous.
