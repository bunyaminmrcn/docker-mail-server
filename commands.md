

```sh
cp -R .secrets ~

chmod 600 ~/.secrets/certbot/cloudflare.ini

apt install python3-pip python3-certbot-dns-cloudflare

pip install --upgrade cloudflare==2.3.1

certbot certonly   --dns-cloudflare   --dns-cloudflare-credentials ~/.secrets/certbot/cloudflare.ini  -d mail.domain.com
```