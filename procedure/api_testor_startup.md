```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '  \ || || |/ -_|_-<  _/ _ \ '_|
 |_|_|_\_, ||_|\___/__/\__\___/_|  
=======|__/=========================
    API References of pyTestor
           ----- oOo -----
   [procedure] api_testor_startup
====================================


-------|__/-------------------------
               SYNTAX
------------------------------------

def pytestor.api_testor_startup():
  # no return
  global g_testor_dir, g_suite_code, g_testor_username, g_testor_password, g_token, g_src_dir, g_suite_id, g_last_version, g_clear_version


-------|__/-------------------------
               USAGE
------------------------------------

$)

import sys
import os

t_testor_dir = '../pyTestor'

sys.path.append( os.path.abspath( t_testor_dir ) )

import pytestor

pytestor.g_testor_dir = '/bioogr/psk-19/pyTestor'
pytestor.g_suite_code = 'pyTestorCheck'
pytestor.g_testor_username = 'mytestor'
pytestor.g_testor_password = 'rzutomqahegpnyx'
pytestor.g_last_version = 0
pytestor.g_src_dir = '/bioogr/psk-19/pyTestorCheck'
pytestor.g_clear_version = False
pytestor.g_token = '_'
pytestor.g_suite_id = -1

pytestor.api_testor_startup()

g_token = pytestor.g_token
g_suite_id = pytestor.g_suite_id

v_case_code = 'test_numbers';
v_case_id = pytestor.api_testor_case( g_token, g_suite_id, v_case_code )
print( "\nCase ID: " + str(v_case_id) + "\n" )

v_test_code = 'equals.1'
v_num_a = 30.3
v_num_b = 30.3
v_test_id = pytestor.api_testor_equals( g_token, g_suite_id, v_case_id, v_test_code, v_num_a, v_num_b )

pytestor.api_testor_shutdown()


    ----------------------------

Case ID: 21


========== Results: Finished ==========


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 2       | GREEN  | pyTestorCheck | 2  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 2); | $) call api_testor_source('_token_', 2, 'a'); |
+------------------------------------------+-----------------------------------------------+



========== Results: Source List ==========



========== Results: Success ==========


+--------------+----------+---------------------------------------------------------------------+
| case         | test     | message                                                             |
+--------------+----------+---------------------------------------------------------------------+
| test_numbers | equals.1 | [equals.1] test (equals) is success. \nOperand: 30.3\nValue: 30.3\n |
+--------------+----------+---------------------------------------------------------------------+



========== Results: Failed ==========



========== Results: Result ==========


+---------+--------+---------------+----+---------------+--------------+------------+------------+
| version | status | code          | id | success_count | failed_count | test_count | case_count |
+---------+--------+---------------+----+---------------+--------------+------------+------------+
| 2       | GREEN  | pyTestorCheck | 2  | 1             | 0            | 1          | 1          |
+---------+--------+---------------+----+---------------+--------------+------------+------------+


+------------------------------------------+-----------------------------------------------+
| To re-print:                             | To get source file of [a] test case:          |
+------------------------------------------+-----------------------------------------------+
| $) call api_testor_result('_token_', 2); | $) call api_testor_source('_token_', 2, 'a'); |
+------------------------------------------+-----------------------------------------------+

    ----------------------------

```