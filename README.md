nginx-geoip2 Role
=========

Role to create nginx snippet to configure geoip2

Role Variables
--------------

```
nginx_geoip2_country: false
nginx_geoip2_city: false

# see https://github.com/leev/ngx_http_geoip2_module#example-usage for more details
# suggested use
nginx_geoip2_country:
  settings:
    - "auto_reload 5m"
    ...
  fastcgi_params:
    COUNTRY_CODE: $geoip2_data_country_code
    ...
```

----------------

```
#   requirements.yml
#
#   Example
# - src: https://github.com/ergontech-ansible-roles/nginx-geoip2
#   version: master
#   name: nginx-geoip2
```

License
-------

[MIT](LICENSE)