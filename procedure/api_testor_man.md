```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_man
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_man( p_module, p_kind, p_code ):
  # return p_man


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
man = pytestor.api_testor_man( module, kind, code )
print( "\nManual: \n" + str(man) + "\n" )


    ----------------------------

Manual: 
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
     API References of myTestor
           ----- oOo -----
    [procedure] api_testor_login
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

procedure api_testor_login ( 
  out p_token varchar(36),
  in p_username varchar(1024),
  in p_password varchar(4096)
)


-------|__/-------------------------
               USAGE
------------------------------------

$) set @v_token = '_'; call api_testor_login( @v_token, 'mytestor', 'rzutomqahegpnyx' ); select @v_token;

    ----------------------------

+----------------------------------+
| @v_token                         |
+----------------------------------+
| 52a49370db50e54c02ec8956b981fab4 |
+----------------------------------+

    ----------------------------


    ----------------------------

```