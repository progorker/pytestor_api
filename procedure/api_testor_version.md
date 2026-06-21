```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_version
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_version( p_token, p_suite_id, p_cur_ver ):
  # no return


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
suite_id = pytestor.api_testor_suite( token, suite_code )
print( "\nSuite ID: " + str(suite_id) + "\n" )

option_code = 'ver:cur'
option_remove = True
data = None
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
version = 15
pytestor.api_testor_version( token, suite_id, version )
option_remove = False
data = None
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
print( f"\nOption ({option_code}): " + str(data) + "\n" )


    ----------------------------

Token: 5d10859780cbdeb729855660cf552975


Suite ID: 1


Option (ver:cur): 15

    ----------------------------

```