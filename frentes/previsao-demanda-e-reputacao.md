# Previsão de Demanda + Reputação Proativa

Liberado por Rodrigo em 17/09/2026. Conciliação financeira adiada.

## Forecast Demand Innova
- Lê ocupação/reservas do InAudit (Supabase).
- Previsão 7 e 14 dias por unidade.
- Cron 7h. Digest + áudio OGG ptt no Innova Ops.
- PDCA semanal: acurácia vs real.

## Reputação Proativa Innova
- Monitora reviews <4★ / reclamações graves.
- Gera rascunho de resposta (desculpa + ação + convite).
- Draft only — humano aprova antes de publicar.
- Cron a cada 4h 8–20h. Alerta imediato em texto puro.
- PDCA semanal: taxa de recuperação e tempo de resposta.

Handoffs: picos → Recepção/Inbox Ops; folgas → Tune; review aprovado → humano.
