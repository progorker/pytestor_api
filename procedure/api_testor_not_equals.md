```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
 [procedure] api_testor_not_equals
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_not_equals( p_token, p_suite_id, p_case_id, p_code, p_operand, p_value ):
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

test_code = 'not_equals.1'
dbl_a = 2.5
dbl_b = 3.5
test_id = pytestor.api_testor_not_equals( token, suite_id, case_id, test_code, dbl_a, dbl_b )
print( "\nTest ID: " + str(test_id) + "\n" )

beauty = False
results = pytestor.api_testor_finish( token, suite_id, beauty )
print( "\n===== Results: Finished =====\n" + str(results) + "\n" )

page_no = 1
beauty = False
results = pytestor.api_testor_success( token, suite_id, page_no, beauty )
print( "\n===== Results: Success =====\n" + str(results) + "\n" )


    ----------------------------

Token: 52c4dc85324b8b75e6375055d5c836a4


Suite ID: 1


Case ID: 12


Test ID: 10


===== Results: Finished =====


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 9       | GREEN  | pyTestorTrial | 1  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 1); | $) call api_testor_source('_token_', 1, 'a'); |
+------------------------------------------+-----------------------------------------------+



===== Results: Success =====


+--------------+--------------+---------------------------------------------------------------------------+
| case         | test         | message                                                                   |
+--------------+--------------+---------------------------------------------------------------------------+
| test_numbers | not_equals.1 | [not_equals.1] test (not_equals) is success. \nOperand: 2.5\nValue: 3.5\n |
+--------------+--------------+---------------------------------------------------------------------------+

    ----------------------------

```