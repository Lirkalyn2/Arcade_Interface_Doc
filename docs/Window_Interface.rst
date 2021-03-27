################
Window_Interface
################

.. contents:: Table of Contents


*******************************************************
1. Actions on window (Actions linked to graphical libs)
*******************************************************

Initialize_Window(int opt = 0, size_t limit_x = 0, size_t limit_y = 0)
======================================================================

Initialize the window according to the choosen option (opt), if opt is not given it's value is 0 and the window is created with the default apparence and given lenght (x) and height (y) if themselves are not 0.

option
------

    W.I.P

Display_Window()
================

Display the window on screen.

Get_Input_Window() const
========================

Return the input gottent by the graphical library in the form of a number, accordingly to the map below.

input map
---------

W.I.P


*****************
#. Actions on map
*****************

Initialize_Map(char \*fd, size_t limit_x = 0, size_t limit_y = 0)
=================================================================

Initialize the map with an alreday open file descirptor, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Initialize_Map(char \**map, size_t limit_x = 0, size_t limit_y = 0)
===================================================================

Initialize the map with bi-dimensional array of char, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Called Window but act on map
----------------------------

Add_Elem_Window(char sprite, size_t pos_x = 0, size_t pos_y = 0)
================================================================

Add the given sprite to the given location in the map, which result in it's addition on the screen when displaying if the position is between the limit of the window.
The default value for x and y if they a not given is 0.

Add_Elem_Window(Inanimate_Entity &Inanimate_Entity)
===================================================

Add the given Inanimate_Entity to the location it include in the map, which result in it's addition on the screen when displaying.

Add_Elem_Window(Animate_Entity &Animate_Entity)
===============================================

Add the given Animate_Entity to the location it include in the map, which result in it's addition on the screen when displaying.

Remove_Elem_Window(size_t pos_x, size_t pos_y)
==============================================

Remove the element at the given location in the map if it's not a Forbidden_Chars, which result in it's disappearance on the screen when displaying.

Remove_Elem_Window(Inanimate_Entity &Inanimate_Entity)
======================================================

Remove the given Inanimate_Entity at the location it include in the map, which result in it's disappearance on the screen when displaying.

Remove_Elem_Window(Animate_Entity &Animate_Entity)
==================================================

Remove the given Animate_Entity at the location it include in the map, which result in it's disappearance on the screen when displaying.

Move_Elem_Window(size_t old_x, size_t old_y, size_t new_x, size_t new_y)
========================================================================

Move the element from the old location given, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Move_Elem_Window(Inanimate_Entity &Inanimate_Entity, size_t new_x, size_t new_y)
================================================================================

Move the given Inanimate_Entity from the old location it include, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Move_Elem_Window(Animate_Entity &Animate_Entity, size_t new_x, size_t new_y)
============================================================================

Move the given Animate_Entity from the old location it include, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Is_Elem_Window(char sprite)
===========================

Return true if the given sprite is in the map, otherwise return false.

Is_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
=======================================================

Return true if the given sprite is in the given position in the map, otherwise return false.


*****************************
#. Actions on forbidden_chars
*****************************

Add_Forbidden_Chars(char forbidden_char)
========================================

Add the given element to the list of forbidden_char (given in the form of a single char) to the list.

Add_Forbidden_Chars(char \*forbidden_char)
==========================================

Add the given element to the list of forbidden_char (given in the form of a char \*) to the list.

Add_Forbidden_Chars(std::string forbidden_char)
===============================================

Add the given element to the list of forbidden_char (given in the form of a string) to the list.

Remove_Forbidden_Chars(char forbidden_char)
===========================================

Remove the given element (given in the form of a single char) from the list of forbidden_char.

Remove_Forbidden_Chars(char \*forbidden_char)
=============================================

Remove the given element (given in the form of a char \*) from the list of forbidden_char.

Remove_Forbidden_Chars(std::string forbidden_char)
==================================================

Remove the given element (given in the form of a string) from the list of forbidden_char.

std::string Get_Forbidden_Chars() const
=======================================

Return the Forbidden Chars in the form of a string;


*******
#. Free
*******

Free_All()
==========

Free all memory used (if any) by this class.


************
#. Variables
************

char \*\*Map
============

Char \*\* containing the map of the game.

size_t Limit_X
==============

Limit in lenght (x) of the map.

size_t Limit_Y
==============

Limit in heigœ (y) of the map.

int Window_Opt
==============

Option use for creating the window

std::string Forbidden_Chars
===========================

The string who contain the forbidden chars.