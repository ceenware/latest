# ceenware public release assets

This repository publishes public installer and updater scripts for ceenware private projects. Each project uses its own GitHub Release tag.

## Install

MoChat:

```bash
curl -fsSL https://github.com/ceenware/latest/releases/download/product-scrm-wework-mochat/install.sh | bash
```

YuanQue:

```bash
curl -fsSL https://github.com/ceenware/latest/releases/download/product-scrm-wework-yuanque/install.sh | bash
```

The installer creates a systemd timer that refreshes `update.sh` and updates the GHCR image every six hours. The application environment is stored under `/opt/ceenware/<repository>/.env`.

The container images are published at:

- `ghcr.io/ceenware/product-scrm-wework-mochat:latest`
- `ghcr.io/ceenware/product-scrm-wework-yuanque:latest`

If a package is private, log in to GHCR once before installation or provide `GHCR_USERNAME` and `GHCR_TOKEN` in the installer environment. The token only needs read access to the package.
