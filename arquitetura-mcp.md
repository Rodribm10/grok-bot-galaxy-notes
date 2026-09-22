# Arquitetura MCP — Grok orquestra o Grok Bot

> Documentado em 22/09/2026. NÃO esquecer.

## O que é
O Grok (este chat) não tem acesso nativo aos agentes do Grok Bot.
A ponte é um servidor MCP que o Mentor sobe na box e expõe via tunnel.

## Como ligar (passo a passo)
1. No app Grok Bot (celular), abre o **Grok Bot Galaxy Mentor** e manda:
   > Instala o Grok Bot MCP do repositório github.com/quabug/grok-bot-mcp e me devolve o endpoint MCP público com OAuth. Se o repo não existir ou falhar, sobe um servidor MCP próprio expondo a API dos agentes — listar, ler transcript e mandar mensagem — e me devolve o endpoint com OAuth. Quando estiver no ar, testa listando os agentes e me diz se funcionou.
2. O Mentor devolve um endpoint tipo `https://….trycloudflare.com/mcp`.
3. No Grok (web): grok.com/connectors → New Connector → Custom → cola o endpoint → autoriza OAuth.
4. No card de autorização, pede a **owner password** (consent). Ela fica em `/workspace/grok-bot-mcp/secrets/OWNER_PASSWORD.txt` na box. Pede pro Mentor: `cat /workspace/grok-bot-mcp/secrets/OWNER_PASSWORD.txt`.
5. Volta neste chat e manda: "conectou, testa listar os agentes".

## Ferramentas que a ponte libera
- `list_agents` — lista os agentes (resolve por nome)
- `message_agent` — manda prompt pra um agente pelo nome
- `check_replies` — puxa a resposta de um agente

## ⚠️ Armadilha de roteamento por nome (CRÍTICO)
O MCP resolve agente **pelo nome**, não pelo ID.
- Se existir um agente lixo chamado "New Agent" (cadastro duplicado/teste), `message_agent("Chief of Staff", …)` pode cair no lixo em vez do CoS de verdade.
- Sempre que uma mensagem "some" (inbox vazia, sem resposta), suspeitar disso primeiro.
- Correção: pedir pro Firstmate/Mentor apagar os "New Agent" sem função e devolver a lista limpa com nomes únicos.
- Regra: **nunca mandar pro Estrategista** coisa de orquestração/sistema — ele é de aquisição (Dono com IA). Orquestração = CoS, Pastor da Frota, Firstmate ou Mentor.

## Tunnel instável
O hostname `*.trycloudflare.com` é quick tunnel: se cair, a URL muda.
Solução: pedir token de tunnel nomeado pro Mentor fixar URL estável.

## Estado atual (22/09)
- Endpoint: `https://yes-functions-pathology-radar.trycloudflare.com/mcp`
- 35 agentes listados com sucesso
- Inbox limpa no momento da conexão
