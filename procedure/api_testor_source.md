```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_source
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_source( p_token, p_suite_id, p_case_code, p_beauty = False ):
  # return p_results


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

suite_code = 'pyTestorTrial' 
suite_id = pytestor.api_testor_suite( token, suite_code )
print( "\nSuite ID: " + str(suite_id) + "\n" )

pytestor.api_testor_clean( token, suite_id )

data = '/bioogr/works/pyTestorTrial'
option_code = 'src_dir'
option_remove = False
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
data = None
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
print( f"\nOption ({option_code}): " + str(data) + "\n" ) 

data = '/test_numbers.py'
option_code = 'src:test_numbers'
option_remove = False
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
data = None
data = pytestor.api_testor_option( token, suite_id, data, option_code, option_remove )
print( f"\nOption ({option_code}): " + str(data) + "\n" ) 

case_code = 'test_numbers'
beauty = False
results = pytestor.api_testor_source( token, suite_id, case_code, beauty )
print( "\n=====] Result: Source [=====\n" + str(results) + "\n" )


    ----------------------------

Token: ad6b95c21333a1f0ba41052494d08e22


Suite ID: 1


Option (src_dir): /bioogr/works/pyTestorTrial


Option (src:test_numbers): /test_numbers.py


=====] Result: Source [=====


+----------+---------------------------------------------+
| Key      | Value                                       |
+----------+---------------------------------------------+
| Case     | test_numbers                                |
| Relative | /test_numbers.py                            |
| Absolute | /bioogr/works/pyTestorTrial/test_numbers.py |
| Root     | /bioogr/works/pyTestorTrial                 |
+----------+---------------------------------------------+

    ----------------------------

```