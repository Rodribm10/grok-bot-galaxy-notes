# Meeting Orchestrator — bot despachante de reuniões

> Criado em 22/09/2026. Status: em construção (pedido ao CoS via Firstmate).

## Ideia
Um bot que **escuta a reunião em tempo real** (não só no fim) e faz o que for preciso — não fica preso a um exemplo fixo.

## Fontes
- **Vexa** (app de ouvir/transcrever reunião) já roda no servidor house e já transcreve pro Rodrigo.
- O bot novo **consome** a transcrição do Vexa; não substitui.

## Três funções
1. **Despachar** — o que foi deliberado e já tem bot pra resolver (InAudit, bot de sistema, etc.) → lança pro bot certo executar.
2. **Detectar recorrência** — coisas que voltam toda reunião → sugere criar fluxo novo (bot existente ou bot/MCP novo) pra automatizar de vez.
3. **Propor fluxo** — se a demanda recorrente não tem bot, propõe criar um (ex.: um bot por aplicativo que o Rodrigo tem, pra ajuste).

## Exemplo (só exemplo, não é o escopo)
Reunião delibera: "corrigir bug X no InAudit" → bot manda pro agente InAudit.
"Ajustar permissão Y no sistema" → bot manda pro bot de engenharia.
Se "pedir relatório Z" se repete 3 reuniões → propõe MCP/bot novo.

## Multi-usuário Vexa (gerentes)
Hoje só o Rodrigo usa. Pra liberar pras gerentes:
- Vexa self-hosted é multi-usuário: `POST /admin/users` (email, nome, limite de bots) gera token próprio, escopado (`bot` / `bot+tx`).
- Caminho simples: Vexa Dashboard (painel web open-source) num container apontando pro gateway; cada gerente entra com o próprio token.
- Google Meet: bot cai na sala de espera → a gerente host precisa admitir.
- Primeiro passo: provisionar 1 gerente de teste, validar, depois rolar pro time.

## Status
- [ ] Provisionar gerentes no Vexa (1 teste primeiro)
- [ ] Criar o bot Meeting Orchestrator (despachar + detectar recorrência + propor fluxo)
- [ ] Um bot por aplicativo do Rodrigo (ajuste), conforme demanda recorrente aparecer
