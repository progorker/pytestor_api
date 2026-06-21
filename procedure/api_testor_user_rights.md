```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_user_rights
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_user_rights( p_token ):
  # return p_api_call, p_user_make, p_user_demo, p_storage_full


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

api_call, user_make, user_demo, storage_full = pytestor.api_testor_user_rights( token )
print( "\nApi Call: " + ('yes' if api_call else 'no') + "\nUser Make: " + ('yes' if user_make else 'no') + "\nUser Demo: " + ('yes' if user_demo else 'no') + "\nStorage Full: " + ('yes' if storage_full else 'no') + "\n" )


    ----------------------------

Token: 6c116c8e7f503326af8738174dd20bfc


Api Call: yes
User Make: no
User Demo: yes
Storage Full: no

    ----------------------------

```