```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_create_user
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_create_user( p_token, p_username, p_password, p_api_call, p_user_make, p_user_demo, p_quota ):
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

new_username = 'demo'
new_password = 'homosapien'
api_call = True
user_make = False
user_demo = False
quota = 1024 * 1024 * 768
pytestor.api_testor_create_user( token, new_username, new_password, api_call, user_make, user_demo, quota )


    ----------------------------

Token: 0cd3481c38e5692aa3b2a7df7a554b20

    ----------------------------

```