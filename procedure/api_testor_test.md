```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_test
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_test( p_token, p_suite_id, p_case_id, p_test_code, p_condition, p_message ):
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

test_code = 'greater.1'
condition = 2 > 1
message = '[greater.1] test is success!'
test_id = pytestor.api_testor_test( token, suite_id, case_id, test_code, condition, message )
print( "\nTest ID: " + str(test_id) + "\n" )

beauty = False
results = pytestor.api_testor_finish( token, suite_id, beauty )
print( "\n===== Results: Finished =====\n" + str(results) + "\n" )

page_no = 1
beauty = False
results = pytestor.api_testor_success( token, suite_id, page_no, beauty )
print( "\n===== Results: Success =====\n" + str(results) + "\n" )


    ----------------------------

Token: 344796a0afddd34746114e168f2d0532


Suite ID: 1


Case ID: 23


Test ID: 21


===== Results: Finished =====


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 18      | GREEN  | pyTestorTrial | 1  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 1); | $) call api_testor_source('_token_', 1, 'a'); |
+------------------------------------------+-----------------------------------------------+



===== Results: Success =====


+--------------+-----------+------------------------------+
| case         | test      | message                      |
+--------------+-----------+------------------------------+
| test_numbers | greater.1 | [greater.1] test is success! |
+--------------+-----------+------------------------------+

    ----------------------------

```