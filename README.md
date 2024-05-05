


```
[root@log web]# cat nginx_error.log 
May  5 16:04:48 web nginx_error: 2024/05/05 16:04:48 [error] 4380#4380: *2 open() "/usr/share/nginx/html/favicon.ico" failed (2: No such file or directory), client: 192.168.56.1, server: _, request: "GET /favicon.ico HTTP/1.1", host: "192.168.56.110", referrer: "http://192.168.56.110/"
```
```
[root@log web]# cat nginx_access.log 
May  5 16:01:52 web nginx_access: 127.0.0.1 - - [05/May/2024:16:01:52 +0300] "GET / HTTP/1.1" 200 4833 "-" "curl/7.29.0"
May  5 16:04:48 web nginx_access: 192.168.56.1 - - [05/May/2024:16:04:48 +0300] "GET / HTTP/1.1" 200 4833 "-" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:124.0) Gecko/20100101 Firefox/124.0"
May  5 16:04:48 web nginx_access: 192.168.56.1 - - [05/May/2024:16:04:48 +0300] "GET /img/centos-logo.png HTTP/1.1" 200 3030 "http://192.168.56.110/" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:124.0) Gecko/20100101 Firefox/124.0"
May  5 16:04:48 web nginx_access: 192.168.56.1 - - [05/May/2024:16:04:48 +0300] "GET /img/html-background.png HTTP/1.1" 200 1801 "http://192.168.56.110/" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:124.0) Gecko/20100101 Firefox/124.0"
May  5 16:04:48 web nginx_access: 192.168.56.1 - - [05/May/2024:16:04:48 +0300] "GET /img/header-background.png HTTP/1.1" 200 82896 "http://192.168.56.110/" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:124.0) Gecko/20100101 Firefox/124.0"
```
