```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
  [procedure] api_testor_e_tables
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_e_tables( p_mysql_database, p_find ):
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
names = pytestor.api_testor_e_tables( mysql_db, mysql_find )
print( "\nTables: " + str(names) + "\n" )


    ----------------------------

Tables: temp_names_table , testor_welcome

    ----------------------------

```