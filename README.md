# HOMELAB

## Repo

1. Install `git`

```bash
apt-get install -y git
```

2. Install `gh`

```bash
curl -LO https://github.com/cli/cli/releases/download/v2.79.0/gh_2.79.0_linux_amd64.tar.gz
tar -xzvf gh_2.79.0_linux_amd64.tar.gz
mv gh_2.79.0_linux_amd64/bin/gh /usr/local/bin/gh
chmod 0700 /usr/local/bin/gh
rm -r gh_2.79.0_linux_amd64*
```

3. Init Repo on Local

```bash
git init . --initial-branch=main

git add .
git commit -m 'chore: init repo'
```

4. Create Repo on GitHub

```bash
gh repo create --public --source=. --push
```