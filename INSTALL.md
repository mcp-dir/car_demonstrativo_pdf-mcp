# Instalação rápida

Cadastro Ambiental Rural: Demonstrativo (PDF) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_car_demonstrativo_pdf`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Cadastro Ambiental Rural: Demonstrativo (PDF)` / `https://api.mcp.ai/p_car_demonstrativo_pdf`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "car_demonstrativo_pdf": { "type": "http", "url": "https://api.mcp.ai/p_car_demonstrativo_pdf" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=car_demonstrativo_pdf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYXJfZGVtb25zdHJhdGl2b19wZGYifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "car_demonstrativo_pdf": { "url": "https://api.mcp.ai/p_car_demonstrativo_pdf" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=car_demonstrativo_pdf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_car_demonstrativo_pdf%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "car_demonstrativo_pdf": { "type": "http", "url": "https://api.mcp.ai/p_car_demonstrativo_pdf" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_car_demonstrativo_pdf
```

Dúvidas? [car_demonstrativo_pdf@mcp.ai](mailto:car_demonstrativo_pdf@mcp.ai)
