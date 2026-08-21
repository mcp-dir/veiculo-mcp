---
name: veiculo-mcp
description: Skill da REST API do Veículo na MCP.AI: 1 endpoint em /api/veiculo. Consulta dados de um veículo pela placa em fontes oficiais (marca/modelo, ano, situação, restrições). Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Veículo — REST API skill

Você tem acesso à **Veículo** REST API na MCP.AI.

> Consulta dados de um veículo pela placa em fontes oficiais (marca/modelo, ano, situação, restrições). Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/veiculo
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/veiculo/dados \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"placa":"...","renavam":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/veiculo/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `veiculo_dados`

Consulta os dados de um veículo pela placa + RENAVAM (marca/modelo, ano, combustível, situação, restrições). _(POST /api/veiculo/dados)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `placa` | string | Sim | Placa do veículo (Mercosul ou antiga). |
| `renavam` | string | Sim | RENAVAM do veículo. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_veiculo` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
