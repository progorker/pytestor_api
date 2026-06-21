```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
  [function] api_testor_is_online
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_is_online( p_token ):
  # return p_online


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

online = pytestor.api_testor_is_online( token )
print( "\nOnline: " + ('yes' if online else 'no') + "\n" )

    ----------------------------

Token: ff560357549770cddf124af34a023901


Online: yes

    ----------------------------
```