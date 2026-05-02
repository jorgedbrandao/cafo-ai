# Cafo Commercial Memory

This file acts as the contextual memory for playbook generation and usage. Every time a new playbook is created or significantly updated, log the context here.

## Logging Format
When adding an entry, use the following format:

```markdown
### Log Date: YYYY-MM-DD
* **Playbook Generated:** [Filename]
* **Target Audience:** [Persona]
* **Business Context:** [Trigger event or scenario]
* **Key Objections Covered:** [List 2-3 main objections addressed]
* **Next Action/Trigger:** [When should a human or agent consult this playbook again?]
```

## Logs

### Log Date: 2026-05-02 (novo)
* **Playbook Generated:** 2026-05-02_site_para_cafeterias_outbound.md
* **Target Audience:** Persona Lucas — cafeteria independente, 1 unidade, Instagram ativo, ainda não nos conhece (cold).
* **Business Context:** Playbook de prospecção fria — DM no Instagram com elogio específico + gap digital, migração pro WhatsApp, oferta de protótipo em 48h sem compromisso. Funil: Cold → DM → WhatsApp → cardápio + fotos → protótipo → handoff pro pitch playbook.
* **Key Objections Covered:** "Não conheço vocês" (desconfiança inicial), "Manda o orçamento aí" (commodity trap), "Tenho amigo que faz site", "Tô na correria", visualizou e não respondeu.
* **Next Action/Trigger:** Usar como ponto de partida em qualquer cafeteria nova (cold). Ao receber cardápio + fotos no WhatsApp, transicionar para `2026-05-02_site_para_cafeterias_pitch.md`.

### Log Date: 2026-05-02 (atualizado)
* **Playbook Generated:** 2026-05-02_site_para_cafeterias_pitch.md
* **Target Audience:** Persona Lucas — Dono(a) de Cafeteria Independente, 1 unidade, caixa apertado, ICP atual do produto low-cost.
* **Business Context:** Pitch de baixo custo (R$ 497 pagamento único, parcelável em 10x, entrega em 7 dias, sem mensalidade) para cafeterias que já consideraram site mas travaram no orçamento de agência (R$ 3k–8k) ou tentaram Wix/Linktree e ficou amador. Renovação opcional R$ 297/ano após 12 meses.
* **Key Objections Covered:** "Posso fazer no Wix de graça", "Agência cobrou R$ 5 mil", "Meu Instagram basta", "E se eu não gostar?", "R$ 497 ainda tá apertado", "Vai ter pegadinha de mensalidade?".
* **Next Action/Trigger:** Usar em todo outbound/inbound de cafeteria independente com Instagram ativo. Este é o playbook principal do GTM atual.

### Log Date: 2026-05-02 (arquivado)
* **Playbook:** 2026-05-02_site_para_franquias_pitch.md → movido para `playbooks/_roadmap_fase_2/`
* **Motivo do arquivamento:** Franquias e redes (3+ unidades) não são ICP do produto low-cost. Compram plataforma com SLA, integração ERP e governança — escopo enterprise. Reativar quando o tier superior do Cafo Frame estiver pronto.

### Log Date: 2026-05-02 (removido)
* **Playbook:** 2026-05-02_landing_page_pitch.md → deletado.
* **Motivo da remoção:** O produto Cafo Frame agora é "site profissional pra cafeteria" (escopo único), não landing pages standalone para subscription/B2B/torrefação. Esses casos exigem e-commerce/funil de venda — explicitamente fora de escopo conforme nova estratégia (seção 8 do Business Strategy).
