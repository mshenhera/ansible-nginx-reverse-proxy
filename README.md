Example:

```
tasks:
  - name: Setup Nginx
    import_role:
      name: nginx-reverse-proxy
    vars:
      nginx_reverse_proxy_proxies:
        - config_name: my-app
          backend_name: my-backend
          backends:
            - localhost:11111
          auth_basic_file: /etc/nginx/my-app.htpasswd
          auth_basic_user: secure-user
          auth_basic_password: "secure-password"
```
