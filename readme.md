# Goal
1. 80 port proxy to 8080 port. If work, will show 'proxy'
2. `http://localhost:8080` can't access, must return 404.

# steps
1. `apt-get update`
2. `apt-get install -y libapache2-mod-proxy-html libxml2-dev apache2 build-essential`
3. Proxy Modules
    - `a2enmod proxy proxy_http proxy_ajp rewrite proxy_balancer proxy_connect proxy_html xml2enc`
4. 設定 `site-enabled/default.conf` & `ports.conf`
5. `apache2ctl restart`

# reference
- https://httpd.apache.org/docs/current/expr.html