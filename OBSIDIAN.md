# Grok Bot Galaxy — Documentação Completa (Obsidian)

> Espelho do vault Obsidian. Atualizado em 17/09/2026.

## 1. Fontes do evento
- Day 1 (15/09): https://x.com/i/broadcasts/1AxRnZbVpjaxl
- Day 2 (16/09): https://x.com/i/broadcasts/1PKqrNyvmYwGb
- Day 3 (17/09): pendente — captura agendada 21h30 BRT
- Repo oficial de notas: https://github.com/Roenel/Grok-Bot-Galaxy-Notes
- Repo local (Rodrigo): https://github.com/Rodribm10/grok-bot-galaxy-notes
- Página do evento: https://x.ai/galaxy

## 2. Estrutura do repo local
- `day1/` — KEY_TAKEAWAYS, MINDSET_AND_STACK, ENGINEERING, PM, FOUNDERS
- `day2/` — KEY_TAKEAWAYS, SALES_ENGINEERING, SDR_AND_SUPPORT
- `bot-base/` — SYSTEM_PROMPT (Mentor), QUICKSTART
- `OBSIDIAN.md` — este arquivo

## 3. Modelo Galaxy (o que a gente implantou)
- Maturidade: Ask → Do → Delegate → Staff
- Um bot = um job; handoff com outcome + contexto mínimo
- Humano aprova ações externas (enviar, publicar, pagar)
- Templates/skills compartilhados; rotinas; exception-only pings
- Staff = função com time de bots, não blank box

## 4. Mapeamento Day → bots atuais
### Day 1 — Founders / 101 / Eng / PM
- Founders → Estrategista, Angelina, Close Prep Dono, Proto Feedback
- 101/Eng → bot-base do Mentor, Supervisor, Chief of Staff
- PM → Inbox Ops (triagem), Research ICP

### Day 2 — Sales Engineering / Sales / SDR / Support
- Sales Engineering → Stalk Concorrência, Battle Card Blair IA, Research ICP
- Sales → Echo Comercial Dono, Close Prep Dono
- SDR → Echo Comercial, Attention List CEO
- Support → Tune Atendimento, Alert Innova, Relatórios

### Day 3 — Marketing Ops / Post-Sales / Marketing (a capturar)
- Proposta de implantação pendente após 21h30 BRT

## 5. Bots ativos (21)
**Dono com IA:** Estrategista, Angelina, Close Prep Dono, Research ICP, Echo Comercial Dono, Cecilia, Shoop, Chief of Staff, Supervisor
**Hotel Innova:** Inbox Ops, Alert, Recepção, Relatórios, Stalk, Battle Card, Tune, Proto Feedback, Attention List, Marketing Prime, Avaliador
**Orquestração:** Grok Bot Galaxy Mentor, Firstmate

## 6. Canais WhatsApp (GOWA)
- *Innova Ops* `120363429131390808@g.us` — Ops, Recepção, Alert, Inbox, Tune, Proto, Stalk, Attention
- *Innova Comercial* `120363411960769415@g.us` — Angelina, Echo, Close Prep, Research, Battle Card
- Fallback DM: `556182098580` (chip Rodrigo-leo-auditoria)
- Device header: `X-Device-Id: Rodrigo-leo-auditoria`

## 7. Schema de áudio (vencedor)
- Endpoint: POST /send/audio no container gowa-app_api (via Portainer)
- Formato: OGG Opus, <5 min, `ptt: true`
- Voz: edge-tts pt-BR-FranciscaNeural → ffmpeg → /app/statics/media
- Caption: 1 linha `*negrito*` + data/unidade
- Depois: /send/message com texto formatado

## 8. Formatação WhatsApp (obrigatória em todos)
- Negrito: `*texto*` (nunca `**`)
- Itálico: `_texto_`
- Bullets: `•` ou `─`; emojis no título; quebras de linha
- Máx 8–12 linhas no digest; skill `whatsapp-gowa-formatting`

## 9. Regras de ouro
1. Dia anterior completo (00:00–23:59), nunca o dia corrente
2. Só fatos concretos — sem score/nota vaga
3. Dois negócios separados: Dono ≠ Hotel
4. Draft-only até liberação explícita
5. Quiet se vazio (exception-only)

## 10. Próximos passos
- [ ] Capturar Day 3 às 21h30 e propor implantações
- [ ] Conectar Chatwoot (token 401 desde ago/2026)
- [ ] Mapear unidade Baia/Padova
- [ ] Validar QNN01 offline
- [ ] Criar grupos GOWA se ainda não existirem
