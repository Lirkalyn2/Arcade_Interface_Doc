##############
Game Interface
##############

.. contents:: Table of Contents


*****************
1. Initialization
*****************

virtual void launch_game()
==========================

This function allows the core to initiate the game by defining the essential values of the game like the starting position of Pac-Man, the Ghost or more simply, to initialize the map.

virtual void create_map(std::string map)
========================================

This function permits to the lib game to read the .txt, who contains the map. The argument of this function is the .txt of the map.

void fill_the_map()
===================

This function permits to add all the little food to the map.

void empty_square()
===================

This function permits to create the blank square at the middle of the map of Pacman and create the “house” of the Ghosts.

virtual void set_map(std::vector<std::string)
=============================================

This function is a setter for the map of the game wich is stocked in a std::vector<std::string>.

virtual std::vector<std::string set_map()
=========================================

This function allows the core and the different parts of the games to access to the final map of the game. With that, the core can know every displacement made by the player or the ghost and can send it to the graphical libs.

virtual std::vector<Sprite_Info_G_t> get_sprite()
=================================================

virtual Player \*get_hero()
===========================

Permit to the launcher to access and modify basic elements of Pacman.

virtual Enemy \*get_enemy(int)
==============================

This function grants a direct access to the Ghost to the launcher. With this function, the launcher can now initialize the different starting values of each ghost. In Pac-Man, there are 4 Ghosts. The int in parameter is to permit the Game Core to know wich Ghost has to be get.

virtual void on_map()
=====================

Allows the Game Core to “set” the different animate elements in the map.


*************
2. Game Logic
*************

virtual bool is_Win()
=====================

This function return true if the functions get_left_pacgommes() returns 0. It allows to the core to know if the Player has won the game or not.

int get_left_pacgommes()
========================

This function counts the number of little food or “Pac-Gommes” left on the map. It returns the counted number.

virtual void change_enemy()
===========================

These functions change the form of the Ghosts when Pac-Man eat a Super Pac-Gommes.

virtual void enemy_displacements()
==================================

This function is the inialization of the AI for Ghosts’ movements.

virtual void on_move()
======================

This function is the function who grants the continuous movement of the player.