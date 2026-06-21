```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
[procedure] api_testor_e_procedures
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_e_procedures( p_mysql_database, p_find ):
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
names = pytestor.api_testor_e_procedures( mysql_db, mysql_find )
print( "\nProcedures: " + str(names) + "\n" )


    ----------------------------

Procedures: api_testor_case , api_testor_change_password , api_testor_clean , api_testor_contains , api_testor_create_user , api_testor_current_user , api_testor_equals , api_testor_error , api_testor_e_functions , api_testor_e_procedures , api_testor_e_tables , api_testor_failed , api_testor_finish , api_testor_greater_than , api_testor_less_than , api_testor_login , api_testor_logout , api_testor_man , api_testor_not_contains , api_testor_not_equals , api_testor_not_greater_than , api_testor_not_less_than , api_testor_not_same , api_testor_not_true , api_testor_option , api_testor_pattern , api_testor_result , api_testor_same , api_testor_source , api_testor_source_list , api_testor_success , api_testor_suite , api_testor_suite_case , api_testor_test , api_testor_true , api_testor_user_rights , api_testor_version

    ----------------------------

```