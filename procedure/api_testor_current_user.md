```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
[procedure] api_testor_current_user
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_current_user( p_token ):
  # return p_user_id, p_username


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

user_id, username = pytestor.api_testor_current_user( token )
print( "\nUser ID: " + str(user_id) + "\nUsername: " + str(username) + "\n" )


    ----------------------------

Token: 636fa50b708520bbdf69a5a348a4bbb5


User ID: 2
Username: mytestor

    ----------------------------

```