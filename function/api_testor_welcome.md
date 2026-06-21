```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [function] api_testor_welcome
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_welcome():
  # return p_results


-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

results = pytestor.api_testor_welcome()
print( results )

    ----------------------------

+----------------------------------------+
| message                                |
+----------------------------------------+
| Welcome to myTestor 0.0.1!             |
| There are 37 published API procedures: |
| proc: api_testor_current_user          |
| proc: api_testor_login                 |
| proc: api_testor_logout                |
| proc: api_testor_user_rights           |
| proc: api_testor_create_user           |
| proc: api_testor_change_password       |
| proc: api_testor_suite                 |
| proc: api_testor_case                  |
| proc: api_testor_suite_case            |
| proc: api_testor_clean                 |
| proc: api_testor_test                  |
| proc: api_testor_finish                |
| proc: api_testor_result                |
| proc: api_testor_option                |
| proc: api_testor_e_functions           |
| proc: api_testor_e_procedures          |
| proc: api_testor_e_tables              |
| proc: api_testor_version               |
| proc: api_testor_source                |
| proc: api_testor_source_list           |
| proc: api_testor_true                  |
| proc: api_testor_not_true              |
| proc: api_testor_success               |
| proc: api_testor_failed                |
| proc: api_testor_error                 |
| proc: api_testor_equals                |
| proc: api_testor_not_equals            |
| proc: api_testor_greater_than          |
| proc: api_testor_not_greater_than      |
| proc: api_testor_less_than             |
| proc: api_testor_not_less_than         |
| proc: api_testor_same                  |
| proc: api_testor_not_same              |
| proc: api_testor_contains              |
| proc: api_testor_not_contains          |
| proc: api_testor_man                   |
| proc: api_testor_pattern               |
| There are 4 published API functions:   |
| func: api_testor_has_right             |
| func: api_testor_is_online             |
| func: api_testor_escape                |
| func: api_testor_unescape              |
+----------------------------------------+

    ----------------------------
```