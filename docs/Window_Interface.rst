****************
Window_Interface
****************

.. contents:: Table of Contents

Actions on window (Actions linked to graphical libs)
====================================================

Initialize_Window()
-------------------

Initialize the window with default values.

Initialize_Window(int opt)
--------------------------

Initialize the window according to the choosen option.

option
^^^^^^

W.I.P

Display_Window()
----------------

Display the window on screen.

Get_Input_Window()
------------------

Return the input gottent by the graphical library in the form of number, accordingly to the map below.

input map
^^^^^^^^^

W.I.P


Actions on map
==============

Initialize_Map(char \*fd, size_t limit_x, size_t limit_y)
---------------------------------------------------------

Initialize the map with an alreday open file descirptor, the limit in lenght (x), and the limit in height (y).

Initialize_Map(char \**map, size_t limit_x, size_t limit_y)
-----------------------------------------------------------

Initialize the map with bi-dimensional array of chat, the limit in lenght (x), and the limit in height (y).

Called Window but act on map
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Add_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
--------------------------------------------------------

Add the given sprite to the given location in the map, which result in it's addition on the screen when displaying.

Add_Elem_Window(Inanimate_Entity &Inanimate_Entity)
---------------------------------------------------

Add the given Inanimate_Entity to the location it include in the map, which result in it's addition on the screen when displaying.

Add_Elem_Window(Animate_Entity &Animate_Entity)
-----------------------------------------------

Add the given Animate_Entity to the location it include in the map, which result in it's addition on the screen when displaying.

Remove_Elem_Window(size_t pos_x, size_t pos_y)
----------------------------------------------

Remove the element at the given location in the map if it's not a Forbidden_Chars, which result in it's disappearance on the screen when displaying.

Remove_Elem_Window(Inanimate_Entity &Inanimate_Entity)
------------------------------------------------------

Remove the given Inanimate_Entity at the location it include in the map, which result in it's disappearance on the screen when displaying.

Remove_Elem_Window(Animate_Entity &Animate_Entity)
--------------------------------------------------

Remove the given Animate_Entity at the location it include in the map, which result in it's disappearance on the screen when displaying.

Move_Elem_Window(size_t old_x, size_t old_y, size_t new_x, size_t new_y)
------------------------------------------------------------------------

Move the element from the old location given, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Move_Elem_Window(Inanimate_Entity &Inanimate_Entity, size_t new_x, size_t new_y)
--------------------------------------------------------------------------------

Move the given Inanimate_Entity from the old location it include, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Move_Elem_Window(Animate_Entity &Animate_Entity, size_t new_x, size_t new_y)
----------------------------------------------------------------------------

Move the given Animate_Entity from the old location it include, to the new location given (in the map) if it's not a Forbidden_Chars, which result in it's movement on the screen when displaying.

Is_Elem_Window(char sprite)
---------------------------

Return true if the given sprite is in the map, otherwise return false.

Is_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
-------------------------------------------------------

Return true if the given sprite is in the given position in the map, otherwise return false.

Actions on forbidden_chars
==========================

Add_Forbidden_Chars(char forbidden_char)
----------------------------------------

Add the given element to the list of forbidden_char (given in the form of a single char) to the list.

Add_Forbidden_Chars(char \*forbidden_char)
------------------------------------------

Add the given element to the list of forbidden_char (given in the form of a char \*) to the list.

Add_Forbidden_Chars(std::string forbidden_char)
-----------------------------------------------

Add the given element to the list of forbidden_char (given in the form of a string) to the list.

Remove_Forbidden_Chars(char forbidden_char)
-------------------------------------------

Remove the given element (given in the form of a single char) from the list of forbidden_char.

Remove_Forbidden_Chars(char \*forbidden_char)
---------------------------------------------

Remove the given element (given in the form of a char \*) from the list of forbidden_char.

Remove_Forbidden_Chars(std::string forbidden_char)
--------------------------------------------------

Remove the given element (given in the form of a string) from the list of forbidden_char.

Free
====

Free_All()
----------

Free all memory used (if any) by this class