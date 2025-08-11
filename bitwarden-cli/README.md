# Bitwarden CLI

## Installation

- https://bitwarden.com/help/cli/

### Ubuntu

```bash
curl -LO https://github.com/bitwarden/cli/releases/download/v1.22.1/bw-linux-1.22.1.zip && \
  unzip bw-linux-1.22.1.zip && rm bw-linux-1.22.1.zip && \
  chmod +x ./bw && sudo mv ./bw /usr/local/bin/
```

### Docker

```bash
docker run --rm -it hoanghaix86/bitwarden-cli bash
```

## Command

```bash
# ex: https://vaultwarden.xxxx.ts.net
export BW_SERVER=
# ex: K5zwQPwm2AkukkMy5Jti6LLIVWfJnC
export BW_CLIENTSECRET=
# ex: user.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
export BW_CLIENTID=
# ex: VaultwardenPassword
export BW_PASSWORD=
```

```bash
bw config server $BW_SERVER

bw login --apikey

export BW_SESSION=$(bw unlock --passwordenv BW_PASSWORD --raw)

bw list items --search mega | jq '.[] | {id: .id, username: .login.username}'

bw get totp xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

```bash
bw lock

bw logout
```