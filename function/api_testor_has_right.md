```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
  [function] api_testor_has_right
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_has_right( p_token, p_right_code ):
  # return p_right


    ----------------------------
           p_right_code
    ----------------------------

+ 'api_call'
+ 'user_make'
+ 'user_demo'
+ 'storage_full'


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

right_code = 'api_call'
right = pytestor.api_testor_has_right( token, right_code )
print( f"\nRight ({right_code}): " + ('yes' if right else 'no') + "\n" )

    ----------------------------

Token: b2a2dc882202d4f6b36149a656f5a040


Right (api_call): yes

    ----------------------------
```