# workflowchatbot

Este repositório contém os arquivos JSON dos workflows n8n utilizados na automação de consultas processuais para o time jurídico da Midea Carrier.

## Workflows Principais
- **Workflow_Principal.json** – Chatbot com ferramentas de consulta de processos.
- **SUB_WORKFLOW_1___Autentica__o_PDPJ.json** – Autenticação no PDPJ com armazenamento de tokens.
- **SUB_WORKFLOW___Login_Apoia_SSO.json** – Gerencia sessão no Apoia utilizando token PDPJ.
- **Workflow_MCP_Server.json** – Exemplo opcional de endpoint MCP para expor ferramentas.

## Requisitos
- n8n v1.95.3
- Tabela Postgres `pdpj_tokens` para tokens do PDPJ.
- Tabela Postgres `apoia_sessions` para sessões Apoia.

Os dados de CPF e senha do PDPJ são definidos diretamente nos nós de login.

## Uso
Importe os arquivos `.json` no n8n e configure as credenciais do Postgres e OpenAI. O workflow principal utiliza sub-workflows como ferramentas da "AI Agent". O arquivo `Workflow_MCP_Server.json` demonstra como expor o workflow via Model Context Protocol.
