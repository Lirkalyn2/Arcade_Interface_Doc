################
Pacman Interface
################

.. contents:: Table of Contents


**********************
1. Getters and setters
**********************

virtual int get_x_pos()
=======================

Return the position x of Pac-Man.

virtual int get_y_pos()
=======================

Return the position y of Pac-Man.

virtual void set_y_pos(int)
===========================

Set the y position of the player. It takes the new y position as parameter.

virtual void set_x_pos(int)
===========================

Set the x position of the player. It takes the new x position as parameter.

void set_killer_time(int time = 50)
===================================

Define for how long Pac-Man can kill a Ghost before the Ghost can eat him again. It takes the defined time as parameter. The default value ‘50’ is approximately 10 seconds when we play the game.

void set_can_kill(bool)
=======================

Permit to trigger a Boolean of verification if pacman can kill or not. It takes as parameter the new Boolean of verification.

int get_killer_time()
=====================

Returns how last the effect which allows Pac-Man to kill a Ghost.


**********************
2. Movements Functions
**********************

Virtual Void Move_Player(Game \*, int)
======================================

Takes as parameter a Game * wich allows the class to access the different movements keys and an int which is the value of the key pressed by the player.
If the pressed key is a movement key, then the functions go in a movement function who is direction wished by the player. Otherwise, it call the function on_move();

Void go_right() / void go_left() / void go_up() / void go_down()
================================================================

Permit to move the player either to the right, to the left, to the up or to the bottom of the map.