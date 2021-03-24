****************
Window_Interface
****************

.. contents:: Table of Contents

Actions on window (Actions linked to graphical libs)
====================================================

Initialize_Window()
-------------------

Initialize_Window(int opt)
--------------------------

Display_Window()
----------------

Get_Input_Window()
------------------

Actions on map
==============

Initialize_Map(char \*fd, size_t limit_x, size_t limit_y)
---------------------------------------------------------

Initialize_Map(char \**map, size_t limit_x, size_t limit_y)
-----------------------------------------------------------

Add_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
--------------------------------------------------------

Add_Elem_Window(Inanimate_Entity &Inanimate_Entity)
---------------------------------------------------

Add_Elem_Window(Animate_Entity &Animate_Entity)
-----------------------------------------------

Remove_Elem_Window(size_t pos_x, size_t pos_y)
----------------------------------------------

Remove_Elem_Window(Inanimate_Entity &Inanimate_Entity)
------------------------------------------------------

Remove_Elem_Window(Animate_Entity &Animate_Entity)
--------------------------------------------------

Move_Elem_Window(size_t old_x, size_t old_y, size_t new_x, size_t new_y)
------------------------------------------------------------------------

Move_Elem_Window(Inanimate_Entity &Inanimate_Entity, size_t new_x, size_t new_y)
--------------------------------------------------------------------------------

Move_Elem_Window(Animate_Entity &Animate_Entity, size_t new_x, size_t new_y)
----------------------------------------------------------------------------

Is_Elem_Window(char sprite)
---------------------------

Is_Elem_Window(size_t pos_x, size_t pos_y, char sprite)
-------------------------------------------------------

Actions on forbidden_chars
==========================

Add_Forbidden_Chars(char forbidden_char)
----------------------------------------

Add_Forbidden_Chars(char \*forbidden_char)
------------------------------------------

Add_Forbidden_Chars(std::string forbidden_char)
-----------------------------------------------

Remove_Forbidden_Chars(char forbidden_char)
-------------------------------------------

Remove_Forbidden_Chars(char \*forbidden_char)
---------------------------------------------

Remove_Forbidden_Chars(std::string forbidden_char)
--------------------------------------------------

Free
====

Free_All()
----------