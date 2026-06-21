```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_e_functions
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_e_functions( p_mysql_database, p_find ):
  # return p_names


-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

mysql_db = 'mytestor'
mysql_find = ''
names = pytestor.api_testor_e_functions( mysql_db, mysql_find )
print( "\nFunctions: " + str(names) + "\n" )


    ----------------------------

Functions: api_testor_escape , api_testor_has_right , api_testor_is_online , api_testor_unescape

    ----------------------------

```