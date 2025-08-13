# MEGA CMD

## Installation

- https://mega.io/cmd

### Ubuntu

```bash
curl -LO https://mega.nz/linux/repo/xUbuntu_24.04/amd64/megacmd-xUbuntu_24.04_amd64.deb && \
    apt-get install "${PWD}/megacmd-xUbuntu_24.04_amd64.deb" && \
    rm "${PWD}/megacmd-xUbuntu_24.04_amd64.deb"
```

### Docker

```bash
docker run --rm -it hoanghaix86/mega-cmd bash
```

## Command

```bash
# ex: email@gmail.com
export MEGA_EMAIL=
# ex: MegaPassword
export MEGA_PASSWORD=
# ex: cli-backup/0.0.0
export MEGA_USER_AGENT=
```

```bash

mega-login --auth-code=<2fa_code> <email> <password>

mega-ls

mega-lpwd

mega-put <local> <remote>

mega-logout
```
