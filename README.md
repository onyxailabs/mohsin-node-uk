# mohsin-node-uk — Dockerized VMess Proxy Node

A Dockerized VMess proxy node configuration (Xray-based) for personal VPN infrastructure. This repo holds the container build file and the proxy node's `config.json`.

## Files

- `Dockerfile` — builds the container image for the proxy node.
- `config.json` — Xray/VMess node configuration (inbound on port 8080, WebSocket path `/default/mohsin-vpn-service/v1.0/mohsin-node`).

## Run it

```bash
docker build -t mohsin-node-uk .
docker run -p 8080:8080 mohsin-node-uk
```

> **Security note:** `config.json` contains a client UUID that acts as a credential. Rotate it if it was ever shared or used outside your own infrastructure, and keep secrets out of public repos.

---

**Built by Muhammad Mohsin — Onyx AI** · [YouTube](https://www.youtube.com/@onyxaipk) · [All products](https://mohsina91.gumroad.com) · [Catalog](https://mohsinakramchandia91-bit.github.io/Catalog/)
