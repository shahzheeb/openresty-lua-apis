1. brew install openresty/brew/openresty



Create a project directory anywhere as per your convienence.
Create two directories - conf and logs
create nginx.conf file inside conf.
Start the openresty/nginx -> openresty -p `pwd`/ -c conf/nginx.conf
To stop: openresty -s stop
To reload:  openresty -s reload
To get a list of CLI options: openresty -h




http://localhost:8080/sayhello



Good References:
https://openresty.org/en/getting-started.html
http://www.staticshin.com/programming/definitely-an-open-resty-guide/
