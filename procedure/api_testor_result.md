```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_result
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_result( p_token, p_suite_id, p_beauty = False ):
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

case_code = 'test_numbers'
case_id = pytestor.api_testor_case( token, suite_id, case_code )
print( "\nCase ID: " + str(case_id) + "\n" )

test_code = 'contains.1'
str_a = 'Hello world!'
str_b = 'world'
test_id = pytestor.api_testor_contains( token, suite_id, case_id, test_code, str_a, str_b )
print( "\nTest ID: " + str(test_id) + "\n" )

beauty = False
results = pytestor.api_testor_finish( token, suite_id, beauty )
print( "\n===== Results: Finished =====\n" + str(results) + "\n" )

page_no = 1
beauty = False
results = pytestor.api_testor_success( token, suite_id, page_no, beauty )
print( "\n===== Results: Success =====\n" + str(results) + "\n" )

beauty = False
results = pytestor.api_testor_result( token, suite_id, beauty )
print( "\n===== Results: Result =====\n" + str(results) + "\n" )


    ----------------------------

Token: 5546609046480ae3e9846dd4c2a52cd2


Suite ID: 1


Case ID: 18


Test ID: 16


===== Results: Finished =====


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 15      | GREEN  | pyTestorTrial | 1  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 1); | $) call api_testor_source('_token_', 1, 'a'); |
+------------------------------------------+-----------------------------------------------+



===== Results: Success =====


+--------------+------------+----------------------------------------------------------------------------------+
| case         | test       | message                                                                          |
+--------------+------------+----------------------------------------------------------------------------------+
| test_numbers | contains.1 | [contains.1] test (contains) is success. \nOperand: Hello world!\nValue: world\n |
+--------------+------------+----------------------------------------------------------------------------------+



===== Results: Result =====


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 15      | GREEN  | pyTestorTrial | 1  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 1); | $) call api_testor_source('_token_', 1, 'a'); |
+------------------------------------------+-----------------------------------------------+

    ----------------------------

```