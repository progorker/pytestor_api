```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_pattern
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_pattern( p_module, p_kind, p_code, p_variant ):
  # return p_pattern


    ----------------------------
             p_module
    ----------------------------

+ 'mytestor'
+ 'mytestorproxy'
+ 'phptestor'
+ 'pytestor'


    ----------------------------
              p_kind
    ----------------------------

+ 'table'
+ 'function'
+ 'procedure'


    ----------------------------
             p_variant
    ----------------------------

+ 'scrp'
+ 'proc'
+ '_'



-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

module = 'mytestor'
kind = 'procedure'
code = 'api_testor_login'
variant = 'scrp'
pattern = pytestor.api_testor_pattern( module, kind, code, variant )
print( "\nPattern: \n" + str(pattern) + "\n" )


    ----------------------------

Pattern: 
set @v_token = '_';
set @v_username = 'mytestor';
set @v_password = 'rzutomqahegpnyx';
call api_testor_login( @v_token, @v_username, @v_password ); select @v_token as `Token`;
call api_testor_logout( @v_token );

    ----------------------------

```