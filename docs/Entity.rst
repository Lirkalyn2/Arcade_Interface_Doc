######
Entity
######

.. contents:: Table of Contents


*********************
1. Actions on Sprites
*********************

Sprite_Setter()
===============

Set the sprite to the default value (depending on the graphical library).

Sprite_Setter(char \*sprite)
============================

Set the sprite to the given value (here a char \*).

Sprite_Setter(std::string sprite)
=================================

Set the sprite to the given value (here a std::string).


**********************
2. Actions on Position
**********************

Pos_Setter(size_t x = 0, size_t y = 0)
======================================

Set the position to the given values (0 by default).

Pos_X_Getter() const
====================

Get the value of the x component of the position.

Pos_Y_Getter() const
====================

Get the value of the y component of the position.


******************
3. Actions on Size
******************

Length_Height_Setter(size_t Length = 0, size_t Height = 0)
==========================================================

Set the Length and Height of the entity's sprite(s) to the given values (0 for both if not given).

Length_Setter(size_t Length = 0)
================================

Set the Length of the entity's sprite(s) to the given value (0 if not given).

Height_Setter(size_t Height = 0)
================================

Set the Height of the entity's sprite(s) to the given value (0 if not given).

Length_Getter() const
=====================

Get the Length of the entity's sprite(s).

Height_Getter() const
=====================

Get the Height of the entity's sprite(s).


*******
4. Free
*******

Free_All()
==========

Free all memory used (if any) by this class


************
5. Variables
************

size_t Pos_X
============

Position x of the Entity.

size_t Pos_Y
============

Position y of the Entity.

size_t Length
=============

Length of the entity's sprite(s)

size_t Height
=============

Height of the entity's sprite(s)
