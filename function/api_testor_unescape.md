```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [function] api_testor_unescape
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_unescape( p_input ):
  # return p_output


-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

input = '{__dq__n__dq__: 2}'
results = pytestor.api_testor_unescape( input )
print( results )

    ----------------------------

{"n": 2}

    ----------------------------

```