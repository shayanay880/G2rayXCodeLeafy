<div align="center">

# G2Leafy

> Web dashboard for deploying and managing Xray VLESS xHTTP servers on GitHub Codespaces.

[![License](https://img.shields.io/github/license/Code-Leafy/G2Leafy?style=flat-square&color=2DC94E)](LICENSE)
[![Stars](https://img.shields.io/github/stars/Code-Leafy/G2Leafy?style=flat-square&color=2DC94E)](https://github.com/Code-Leafy/G2Leafy/stargazers)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)

</div>

## Overview

G2Leafy runs a browser dashboard backed by a Python server inside a GitHub Codespace to manage an Xray VLESS xHTTP gateway. It automates port forwarding, client creation, subscriptions, traffic monitoring, and core controls.

> The optional keep-alive feature can keep the Codespace active while the proxy is in use; use it in line with GitHub's usage policies.

## Preview

<div align="center">
<img src="assets/preview.png" alt="G2Leafy dashboard" width="720">
</div>

## Features

- Browser dashboard for clients, QR codes, and subscription links.
- VLESS xHTTP config generation for `*.app.github.dev` forwarding domains.
- Live RX/TX, uptime, CPU/RAM/disk, and Codespace quota estimates.
- Subscription Lab with custom per-client layouts.
- Community config network via `configs.txt`.

## Quick start

1. Fork the repository.
2. Open your fork and click **Code → Codespaces → Create codespace on main**.
3. Wait 1–2 minutes for the container to build and launch `g2leafy.py`.
4. Open the forwarded port printed in the terminal, e.g. `https://<name>-8080.app.github.dev/`.

If the backend doesn't start automatically:

```bash
python3 g2leafy.py
```

> Port `443` is the Xray gateway, so browsing it returns `400`. Use the generated VLESS or subscription link in a client instead.

## Community subscription

```text
https://raw.githubusercontent.com/Code-Leafy/G2Leafy/main/configs.txt
```

## Project structure

```text
G2Leafy/
├── g2leafy.py        # Python backend, dashboard server, Xray manager
├── index.html        # Web dashboard
├── configs.txt       # Community-donated subscriptions
├── assets/           # Preview media
├── .devcontainer/    # Codespaces setup
└── LICENSE
```

## License

[MIT](LICENSE)

> Educational use. You are responsible for complying with local laws and GitHub's policies.
