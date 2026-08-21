# Veículo

### Veículo for Claude, ChatGPT and AI agents

Look up a vehicle by license plate against official sources (make/model, year, status, restrictions). Platform-hosted, no credentials, pay per query with prepaid credit.

- 📊 **1 tool**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Veículo`, URL `https://api.mcp.ai/p_veiculo`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=veiculo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF92ZWljdWxvIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=veiculo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_veiculo%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_veiculo
```

---

## 1 tool

| Tool | Description |
|---|---|
| `veiculo_dados` | Consulta os dados de um veículo pela placa + RENAVAM (marca/modelo, ano, combustível, situação, restrições). |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_veiculo` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
