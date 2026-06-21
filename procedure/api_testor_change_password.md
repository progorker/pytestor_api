```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
     API References of pyTestor
           ----- oOo -----
[procedure] api_testor_change_password
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_change_password( p_token, p_password ):
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

new_password = 'homosapien'
pytestor.api_testor_change_password( token, new_password )


    ----------------------------

Token: 2048853d1bd2b62354e314d51564da72

    ----------------------------

```