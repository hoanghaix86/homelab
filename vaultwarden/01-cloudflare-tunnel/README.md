# Vaultwarden

```bash
echo -n "********" | argon2 "$(openssl rand -base64 32)" -e -id -k 65540 -t 3 -p 4
```

<!--
Install `cloudflared`

```bash
mkdir -p --mode=0755 /usr/share/keyrings
curl -fsSL https://pkg.cloudflare.com/cloudflare-main.gpg | tee /usr/share/keyrings/cloudflare-main.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/cloudflare-main.gpg] https://pkg.cloudflare.com/cloudflared any main" | tee /etc/apt/sources.list.d/cloudflared.list
apt-get update && apt-get install cloudflared -y
```

Create Tunnel

```bash
cloudflared tunnel create vps
```

```yml
tunnel: de8dae75-b873-4d4c-a417-5d4853859182
credentials-file: /home/x86/.cloudflared/de8dae75-b873-4d4c-a417-5d4853859182.json

ingress:
  - hostname: vaultwarden.envs.io.vn
    service: http://127.0.0.1:20080

  - service: http_status:404
```
-->