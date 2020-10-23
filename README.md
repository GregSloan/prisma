# prisma

To use this repo:

1. edit the IP address in docker-compose.yml to be public IP of the target VM
2. edit line 2 of content_web/Dockerfile: `COPY . /usr/share/nginx/html/{super_secret_key_string}/ (default is 'a')`
3. edit line 3 of line 13 of node-proxy/default.conf: `location ~* /{super_secret_key_string} {`
4. docker build content_web -t content_web
5. docker build node-proxy -t node-proxy
6. docker-compose up -d
7. add `content.pirsmags.com {ip-of-target-VM}` to /etc/hosts of system you're browsing from
8. browse to https://content.prismags.com/{super_secret_key_string}/
9. login with credentials `customer1:mypassword`
10. Browse to any other location at https://content.prismags.com - receive 500 error
