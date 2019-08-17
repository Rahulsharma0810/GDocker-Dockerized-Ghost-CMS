**GDocker**

GDocker is the easiest way to run Ghost in Docker from trusted sources and strong steering control on  setup.

Features**
---

1. Ghost 2.X.
2. Offiical Nginx Image Support.
3. Let's Encrypt SSL Support.
4. AWS S3 Images Support.
5. Mariadb/Mysql instead of sqlite.
6. Mounted Ghost theme folder.


**Configuration**
---

1. Just Copy your ssl files in `Nginx/nginx/certs/`

    ```bash
├── README
    ├── cert.pem
    ├── chain.pem
    ├── fullchain.pem
    └── privkey.pem
    ```
    in `ghost.tld.conf.sample` change
    
    `ssl_certificate    /etc/nginx/certs/tld.com/fullchain.pem;`
`ssl_certificate_key    /etc/nginx/certs/tld.com/privkey.pem`

2. Run **Mysql** Container with `.env` 

   `docker-compose up -d --force-recreate`

3. Build Ghost image with

   `docker build -t ghost:0.1 .`

   and run Ghost with `docker-compose up -d --force-recreate`

4. At Last, Run Nginx Container with

   `docker-compose up -d --force-recreate`

Donations**
---

This is free, open-source software. If you'd like to support the development of future projects, or say thanks for this one, Give this Repo ★★★ & ♥♥♥.
