```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_suite_case
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_suite_case( p_token, p_suite_code, p_case_code ):
  # return p_suite_id, p_case_id


-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

username = 'mytestor'
password = 'rzutomqahegpnyx'
token = pytestor.api_testor_login( username, password )
print( "\nToken: " + token + "\n" )


suite_code = 'pyTestorTrial'
case_code = 'test_numbers'
suite_id, case_id = pytestor.api_testor_suite_case( token, suite_code, case_code )
print( "\nSuite ID: " + str(suite_id) + "\nCase ID: " + str(case_id) + "\n" )


    ----------------------------

Token: b3e7d04fcc3e937131b141e464e36f36


Suite ID: 1
Case ID: 22

    ----------------------------

```