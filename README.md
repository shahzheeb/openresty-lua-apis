1. brew install openresty/brew/openresty
2. Create a project directory anywhere as per your convienence.
3. Create two directories - conf and logs
4. Create nginx.conf file inside conf.
```$xslt
worker_processes  1;
error_log logs/error.log;
events {
    worker_connections 1024;
}
http {
    server {
        listen 8080;
        location /sayhello {
            default_type text/html;
            content_by_lua '
                ngx.say("<p>hello, world !!!</p>")
            ';
        }
    }
}
```
                                      
5. Start the ```openresty/nginx -> openresty -p `pwd`/ -c conf/nginx.conf```

Other useful commands:
```
openresty -s stop
openresty -s reload
openresty -h
```

6. http://localhost:8080/sayhello

Good References:
https://openresty.org/en/getting-started.html
http://www.staticshin.com/programming/definitely-an-open-resty-guide/