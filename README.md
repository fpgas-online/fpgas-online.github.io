# website

The https://fpgas.online landing page -- a static site published with
GitHub Pages.

## Layout

| Path | Purpose |
|------|---------|
| `site/` | The published content. `site/index.html` is the whole landing page (self-contained HTML + inline CSS, no build step). |
| `.github/workflows/pages.yml` | Deploys `site/` to GitHub Pages on every push to `main` (and via manual dispatch). |

## Deployment

Pushing to `main` runs the `Deploy GitHub Pages` workflow, which uploads
`site/` as a Pages artifact and deploys it. The Pages source for this repo
is set to "GitHub Actions" (not "deploy from branch").

The site is currently served at https://fpgas-online.github.io/website/ ;
pointing https://fpgas.online at it (custom domain + DNS) is the next step.

To preview locally:

```bash
uv run --no-project python -m http.server 8000 --directory site
```

## Repositories

| Repository | Description |
|------------|-------------|
| [fpgas.online-test-designs](https://github.com/fpgas-online/fpgas.online-test-designs) | LiteX-based test designs that verify FPGA boards are working |
| [fpgas.online-infra](https://github.com/fpgas-online/fpgas.online-infra) | Ansible infrastructure for fpgas.online |
| [fpgas.online-site](https://github.com/fpgas-online/fpgas.online-site) | Django web application for fpgas.online |
| [fpgas.online-poe](https://github.com/fpgas-online/fpgas.online-poe) | SNMP PoE switch management |
| [fpgas.online-cam](https://github.com/fpgas-online/fpgas.online-cam) | Camera capture and streaming for Raspberry Pi boards |
| [fpgas.online-setup-pi](https://github.com/fpgas-online/fpgas.online-setup-pi) | Raspberry Pi environment setup for fpgas.online nodes |
| [fpgas.online-netboot-pi](https://github.com/fpgas-online/fpgas.online-netboot-pi) | Netboot filesystem preparation tools |
| [fpgas.online-tools](https://github.com/fpgas-online/fpgas.online-tools) | Utility scripts and tools |
| [website](https://github.com/fpgas-online/website) | The fpgas.online website |
| [apt](https://github.com/fpgas-online/apt) | APT package repository (GitHub Pages) |
| [todo](https://github.com/fpgas-online/todo) | TODO items tracking |
