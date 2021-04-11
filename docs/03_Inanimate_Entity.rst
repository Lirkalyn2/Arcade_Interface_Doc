################
Inanimate_Entity
################

Inherit Entity

.. contents:: Table of Contents

*****************************************************************************************
Only use by the Launcher. Same code for all graphic library. Same explications as Entity.
*****************************************************************************************


*********************
1. Actions on Sprites
*********************

bool Sprite_Setter()
====================

Set the sprite to the default value P.

Returns true on success, false on failure.

bool Sprite_Setter(char \*sprite)
=================================

Set the sprite to the given value (here a char \*).

Returns true on success, false on failure.

bool Sprite_Setter(std::string sprite)
======================================

Set the sprite to the given value (here a std::string).

Returns true on success, false on failure.

std::string Sprite_Getter_Whole() const
=======================================

Get the variable Sprite who contains the whole sprite.


**********************
2. Actions on Position
**********************

bool Pos_Setter(size_t x = 0, size_t y = 0)
===========================================

Set the position to the given values (0 by default).

Returns true on success, false on failure.

size_t Pos_X_Getter() const
===========================

Get the value of the x component of the position.

size_t Pos_Y_Getter() const
===========================

Get the value of the y component of the position.


******************
3. Actions on Size
******************

bool Length_Height_Setter(size_t Length = 0, size_t Height = 0)
===============================================================

Set the Length and Height of the entity's sprite(s) to the given values (0 for both if not given).

Returns true on success, false on failure.

bool Length_Setter(size_t Length = 0)
=====================================

Set the Length of the entity's sprite(s) to the given value (0 if not given).

Returns true on success, false on failure.

bool Height_Setter(size_t Height = 0)
=====================================

Set the Height of the entity's sprite(s) to the given value (0 if not given).

Returns true on success, false on failure.

size_t Length_Getter() const
============================

Get the Length of the entity's sprite(s).

size_t Height_Getter() const
============================

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
