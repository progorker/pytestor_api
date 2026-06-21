```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [function] api_testor_escape
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_escape( p_input ):
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

input = '{"n": 2}'
results = pytestor.api_testor_escape( input )
print( results )

    ----------------------------

{__dq__n__dq__: 2}

    ----------------------------

```