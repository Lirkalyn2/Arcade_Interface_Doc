################
Window_Interface
################

.. contents:: Table of Contents

******************************************************************
(G) Means that the function is different for each graphic library.
******************************************************************


*******************************************************
1. Actions on window (Actions linked to graphical libs)
*******************************************************

bool Initialize_Window(int opt = 0) (G)
=======================================

Initialize the window according to the choosen option (opt), if opt is not given it's value is 0 and the window is created with the default values.

Returns true on success, false on failure.

option
------

    -1: is only for the launcher, you can go up to 160 characters per lines and 40 lines. the window is 1920x1080. one character will have the following dimensions, lenght = 12 Px and height = 27 Px.
    0: is for the games, you can go up to 64 characters per lines and 36 lines. the window is 1920x1080. one character will have the following dimensions, lenght = 30 Px and height = 30 Px.
    1: is for the games, you can go up to 42 characters per lines and 24 lines. the window is 1280x720. one character will have the following dimensions, lenght = 30 Px and height = 30 Px.
    2: is for the games, you can go up to 24 characters per lines and 16 lines. the window is 720x480. one character will have the following dimensions, lenght = 30 Px and height = 30 Px.

void Display_Window() (G)
=========================

Display the window on screen.

int Get_Input_Window() const (G)
================================

Return the input gottent by the graphical library in the form of a number, accordingly to the map below.

input map
---------

    a = 0
    b = 1
    c = 2
    d = 3
    e = 4
    f = 5
    g = 6
    h = 7
    i = 8
    j = 9
    k = 10
    l = 11
    m = 12
    n = 13
    o = 14
    p = 15
    q = 16
    r = 17
    s = 18
    t = 19
    u = 20
    v = 21
    w = 22
    x = 23
    y = 24
    z = 25
    Spacebar = 26
    0 = 27
    1 = 28
    2 = 29
    3 = 30
    4 = 31
    5 = 32
    6 = 33
    7 = 34
    8 = 35
    9 = 36
    Up Arrow = 37;
    Down Arrow = 38;
    Left Arrow = 39;
    Right Arrox = 40;
    Backspace = 41;
    F1 = 42;
    F2 = 43;
    F3 = 44;
    F4 = 45;
    F5 = 46;
    F6 = 47;
    F7 = 48;
    F8 = 49;
    Enter = 50;

void Stop_Window() (G)
======================

Stop and close the Window.

bool Sprite_Info_Get_n_Set(std::vector<Sprite_Info_t> sprite) (G)
=================================================================

Get the information about the sprite and put them in the class variable Sprite_Inf.


*****************
2. Actions on map
*****************

bool Initialize_Map(FILE \*fd, size_t lenght = 0, size_t height = 0)
====================================================================

Initialize the map with an alreday open file descirptor, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Initialize_Map(char \**map, size_t lenght = 0, size_t height = 0)
======================================================================

Initialize the map with bi-dimensional array of char, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Initialize_Map(std::vector<std::string> map, size_t lenght = 0, size_t height = 0)
=======================================================================================

Initialize the map with vector of string, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Initialize_Map(std::ifstream fd, size_t lenght = 0, size_t height = 0)
===========================================================================

Initialize the map with an alreday open ifstream, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Update_Map(char \**map, size_t lenght = 0, size_t height = 0)
==================================================================

Update the map with bi-dimensional array of char so we can display a new map on screen, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Update_Map(std::vector<std::string> map, size_t lenght = 0, size_t height = 0)
===================================================================================

Update the map with vector of string so we can display a new map on screen, the limit in lenght (x), and the limit in height (y).
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.


Called Window but act on map
----------------------------

bool Add_Elem_Window(char sprite, size_t pos_x = 0, size_t pos_y = 0)
=====================================================================

Add the given sprite to the given location in the map, which result in it's addition on the screen when displaying if the position is between the limit of the window.
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Add_Elem_Window(char \*sprite, size_t pos_x = 0, size_t pos_y = 0)
=======================================================================

Add the given sprite to the given location in the map, which result in it's addition on the screen when displaying if the position is between the limit of the window.
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Add_Elem_Window(std::string sprite, size_t pos_x = 0, size_t pos_y = 0)
============================================================================

Add the given sprite to the given location in the map, which result in it's addition on the screen when displaying if the position is between the limit of the window.
The default value for x and y if they a not given is 0.

Returns true on success, false on failure.

bool Add_Elem_Window(Inanimate_Entity \*inanimate_Entity)
=========================================================

Add the given Inanimate_Entity to the location it include in the map, which result in it's addition on the screen when displaying.

Returns true on success, false on failure.

bool Add_Whole_Elem_Window(Inanimate_Entity \*inanimate_Entity)
===============================================================

Add the whole Inanimate_Entity to the location it include in the map, which result in it's addition on the screen when displaying. (use for text)

Returns true on success, false on failure.

bool Remove_Elem_Window(size_t pos_x, size_t pos_y)
===================================================

Remove the element at the given location in the map if it's not a Forbidden_Chars, which result in it's disappearance on the screen when displaying.

Returns true on success, false on failure.

bool Remove_Elem_Window(Inanimate_Entity \*inanimate_Entity)
============================================================

Remove the given Inanimate_Entity at the location it include in the map, which result in it's disappearance on the screen when displaying.

Returns true on success, false on failure.

bool Move_Elem_Window(size_t old_x, size_t old_y, size_t new_x, size_t new_y)
=============================================================================

Move the element from the old location given, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Returns true on success, false on failure.

bool Move_Elem_Window(Inanimate_Entity \*inanimate_Entity, size_t new_x, size_t new_y)
======================================================================================

Move the given Inanimate_Entity from the old location it include, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Returns true on success, false on failure.

bool Is_Elem_Window(char sprite)
================================

Return true if the given sprite is in the map, otherwise return false.

bool Is_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
============================================================

Return true if the given sprite is in the given position in the map, otherwise return false.


*****************************
3. Actions on forbidden_chars
*****************************

bool Add_Forbidden_Chars(char forbidden_char)
=============================================

Add the given element to the list of forbidden_char (given in the form of a single char) to the list.

Returns true on success, false on failure.

bool Add_Forbidden_Chars(char \*forbidden_char)
===============================================

Add the given element to the list of forbidden_char (given in the form of a char \*) to the list.

Returns true on success, false on failure.

bool Add_Forbidden_Chars(std::string forbidden_char)
====================================================

Add the given element to the list of forbidden_char (given in the form of a string) to the list.

Returns true on success, false on failure.

bool Remove_Forbidden_Chars(char forbidden_char)
================================================

Remove the given element (given in the form of a single char) from the list of forbidden_char.

Returns true on success, false on failure.

bool Remove_Forbidden_Chars(char \*forbidden_char)
==================================================

Remove the given element (given in the form of a char \*) from the list of forbidden_char.

Returns true on success, false on failure.

bool Remove_Forbidden_Chars(std::string forbidden_char)
=======================================================

Remove the given element (given in the form of a string) from the list of forbidden_char.

Returns true on success, false on failure.

std::string Get_Forbidden_Chars() const
=======================================

Return the Forbidden Chars in the form of a string;


*******
4. Free
*******

Free_All() (G)
==============

Free all memory used (if any) by this class.


************
5. Variables
************

char \**Map
===========

Char \** containing the map of the game.

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

size_t Px_Case_X
================

Number of pixel a character takes on the x axis.

size_t Px_Case_Y
================

Number of pixel a character takes on the y axis.

std::vector<Sprite_Info_t> Sprite_Inf
=====================================

Vector of a structure who contains all the informations needed to draw a sprite on screen.

Sprite_Info_t (G)
=================

char c
------

The identification char to find the sprite on the map.

int stage
---------

the stage to know when to draw a sprite and in which category it is.

    -1: Only one, and only for a font file to display text.
    0: Sprite who never moves, optimisation possible on them.
    1: Sprite who aren't animated and can't move.
    2: Sprite who moves and are animated.

std::string img
---------------

Path toward the image for the sprite.

int lenght
----------

Lenght of the sprite (should be 30 Px but can be more).

int height
----------

Height of the sprite (should be 30 Px but can be more).