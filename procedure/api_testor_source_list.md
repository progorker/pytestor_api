```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_source_list
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_source_list( p_token, p_suite_id, p_page_no, p_beauty = False ):
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

page_no = 1
beauty = False
results = pytestor.api_testor_source_list( token, suite_id, page_no, beauty )
print( "\n=====] Result: Source List [=====\n" + str(results) + "\n" )


    ----------------------------

Token: bcfc50e3328830855f9f85567fce0fde


Suite ID: 1


Option (src_dir): /bioogr/works/pyTestorTrial


Option (src:test_numbers): /test_numbers.py


=====] Result: Source List [=====


+--------------+------------------+------------------+---------------------------------------------+
| rel_key      | abs_key          | rel_value        | abs_value                                   |
+--------------+------------------+------------------+---------------------------------------------+
| test_numbers | src:test_numbers | /test_numbers.py | /bioogr/works/pyTestorTrial/test_numbers.py |
+--------------+------------------+------------------+---------------------------------------------+

    ----------------------------

```