# django-ninja

https://django-ninja.rest-framework.com/


* form-data 数据格式

```
----------------------------072668657324383867386750
Content-Disposition: form-data; name="username"

admin
----------------------------072668657324383867386750
Content-Disposition: form-data; name="password"

abc111
----------------------------072668657324383867386750--

```

* x-wwww-from-urlencode

```
username=tom&password=tom111
```


什么情况是必须用form-data ?

* 文件上传



