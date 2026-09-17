# Engineering — Lingxi (Day 1)

## Maturity ladder
Autocomplete → Ask & Edit → Agentic Coding → Automations (Cloud Agent) → Autonomous Coding (Grok Code).

## Grok Bot for eng
- Execução de tarefa 24/7, MCP tools, gerencia Cursor Cloud Agents, memória & rotinas.
- Casos ao vivo: Nightly Code Cleanup, TestFlight Seat Management, Auto-fix Everything.
- Fleet board (FlyLo Engineering Fleet): Task, Owner, Stage, PRs, Cloud agent, Last commit.

## Workflow rules (stealable)
- Todo código via cloud agents; prove tip/mergeability/CI/product proof.
- Humanos possuem todo merge.
- Um cloud agent por stream de PR.
- Board-first (Stage=Working row antes de lançar).
- Não re-board PR de outro owner.
- Padrão P0: board → cloud agent → interrupt watch de 5 min (stall/sleep 300/drift) → playbook fan-out.

## What we learned (Eng)
- Trate bots como interns.
- Se você desbloqueia a mesma coisa repetidamente, automatize um nível a mais.
- Comece com um feedback loop.