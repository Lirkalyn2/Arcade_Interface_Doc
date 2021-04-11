###############
Ghost Interface
###############

.. contents:: Table of Contents


**********************
1. Getters and setters
**********************

virtual int get_x_pos()
=======================

Return the position x of Ghost.

virtual int get_y_pos()
=======================

Return the position y of Ghost.

virtual void set_y_pos(int)
===========================

Set the y position of the Ghost. It takes the new y position as parameter.

virtual void set_x_pos(int)
===========================

Set the x position of the Ghost. It takes the new x position as parameter.


void dead_setter(char c)
========================

Allow to modify the ascii_character of the ghost when is dead. It takes the ascii character as parameter.

void eatable_setter(char c)
===========================

Allow to modify the ascii_character of the ghost when is eatable. It takes the ascii character as parameter.

void get_setter(char c)
=======================

Allow to modify the ascii_character of the ghost when is eatable.


**********************
2. Movements Functions
**********************

void displacement (std::vector<std::string>, Pacman \*, int)
============================================================

This function is the main core for tha AI of the Ghost. It takes a std::vector<std::sting> which is the map of the Game, a Pacman * which is the player allows the Ghost Class to get the player positions, and an int which is the score and allows to differentiate the two phase of the ghost displacements : the exit of their “house” and the chase of Pac-Man.