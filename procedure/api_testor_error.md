```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_error
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_error( p_token, p_suite_id, p_case_id, p_test_code, p_message ):
  # return p_test_id


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

case_code = 'test_numbers'
case_id = pytestor.api_testor_case( token, suite_id, case_code )
print( "\nCase ID: " + str(case_id) + "\n" )

test_code = 'exception.1'
message = '[exception.1] Field is missing!'
test_id = pytestor.api_testor_error( token, suite_id, case_id, test_code, message )
print( "\nTest ID: " + str(test_id) + "\n" )

beauty = False
results = pytestor.api_testor_finish( token, suite_id, beauty )
print( "\n===== Results: Finished =====\n" + str(results) + "\n" )

page_no = 1
beauty = False
results = pytestor.api_testor_failed( token, suite_id, page_no, beauty )
print( "\n===== Results: Failed =====\n" + str(results) + "\n" )


    ----------------------------

Token: 0d4e5544962f89f9a7f266d0178deffd


Suite ID: 1


Case ID: 5


Test ID: 4


===== Results: Finished =====


+--------------+-------------+------------------------------------------------------------------------------------+
| case         | test        | message                                                                            |
+--------------+-------------+------------------------------------------------------------------------------------+
| test_numbers | exception.1 | [exception.1] test (error) is failed. \nMessage: [exception.1] Field is missing!\n |
+--------------+-------------+------------------------------------------------------------------------------------+


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 3       | RED    | pyTestorTrial | 1  | 0             | 1            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 1); | $) call api_testor_source('_token_', 1, 'a'); |
+------------------------------------------+-----------------------------------------------+



===== Results: Failed =====


+--------------+-------------+------------------------------------------------------------------------------------+
| case         | test        | message                                                                            |
+--------------+-------------+------------------------------------------------------------------------------------+
| test_numbers | exception.1 | [exception.1] test (error) is failed. \nMessage: [exception.1] Field is missing!\n |
+--------------+-------------+------------------------------------------------------------------------------------+

    ----------------------------

```