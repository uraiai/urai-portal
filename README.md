# Urai Portal

**Share your local LLMs securely with your team — no port forwarding, no cloud hosting, no data leaving your network.**

Urai Portal connects your local AI infrastructure to [Urai Chat](https://chat.app.urai.dev), giving your organization hybrid inference: use cloud models when convenient, switch to your own hardware when you need privacy, cost control, or specialized models.

## How it works

1. **Install Urai Portal** on any machine running an LLM (Ollama, llama.cpp, vLLM, or any OpenAI-compatible server)
2. **Create a portal on urai chat** - copy the node id and create a portal on urai chat
3. **Use Urai Chat** as usual — requests route seamlessly to your local models through an encrypted tunnel

No firewall changes. No VPN. No exposed ports. Your models stay on your hardware, and all traffic is end-to-end encrypted.

## Features

- **Auto-discovery** — automatically detects Ollama and llama.cpp instances running on your machine
- **End-to-end encryption** — all inference traffic is encrypted between Urai Chat and your local server
- **Zero configuration networking** — works behind NATs, firewalls, and corporate networks without any port forwarding
- **System tray app** — runs quietly in your menu bar on macOS, out of the way until you need it
- **Hybrid inference** — seamlessly mix cloud and local models in Urai Chat based on your needs
- **Auto-updates** — the macOS app keeps itself up to date automatically

## Install

### macOS (Apple Silicon)

Download the latest `.dmg` from [Releases](https://github.com/uraiai/urai-portal/releases), open it, and drag Urai Portal to Applications.

The app runs as a system tray icon. Click it to see your Node ID, discovered backends, and copy your Node ID to share with your team.

### Linux (headless server)

```bash
curl -L https://github.com/uraiai/urai-portal/releases/latest/download/urai-portal-server-linux-x86_64 -o urai-portal-server
chmod +x urai-portal-server
./urai-portal-server --upstream-url http://localhost:11434
```

The server prints your Node ID on startup. Share it with your team to connect via Urai Chat.

## Why local inference?

- **Cost control** — use your own GPUs instead of paying per token
- **Specialized models** — run fine-tuned or domain-specific models not available in the cloud
- **Compliance** — meet data residency and regulatory requirements
- **Low latency** — skip the round trip to the cloud for local users

