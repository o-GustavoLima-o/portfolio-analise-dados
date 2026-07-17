# Portfólio — Análise de Dados | Grupo Culinê

Projetos que desenvolvi como **Analista de Dados no Grupo Culinê** (grupo de restaurantes), construindo do zero a camada de dados e indicadores do negócio: integração com APIs, pipelines de tratamento em JavaScript (Google Apps Script), planilhas estruturadas como camada de dados e dashboards em Looker Studio para as áreas de operação, atendimento, qualidade e gestão de pessoas.

> 🔒 **Nota de privacidade:** todos os prints deste repositório tiveram valores, metas e nomes internos **desfocados na captura**, e os números citados nos textos são **fictícios/ilustrativos**, para preservar dados internos da empresa.

## Stack e competências

- **Visualização:** Google Looker Studio (dashboards multi-página, filtros dinâmicos, scorecards comparativos, árvore de KPIs)
- **Engenharia de dados leve:** Google Apps Script (JavaScript) — consumo de API REST do ERP (Saipos), tratamento de dados com deduplicação, retry para falhas intermitentes e regras de virada de turno
- **Camada de dados:** Google Sheets estruturado como fonte para os dashboards
- **IA aplicada:** análise automatizada de perfil comportamental (DISC) integrada à planilha de respostas
- **Negócio:** KPIs de food service — faturamento por canal, ticket médio, CMV, tempo de produção, metas escalonadas, NPS/avaliações multicanal

## Projetos

| # | Projeto | Descrição |
|---|---------|-----------|
| 01 | [Dashboard de Desempenho Operacional](01-dashboard-faturamento/) | Faturamento por canal, tempo de produção e análise de cardápio, alimentado por integração via API com o ERP |
| 02 | [Dashboard de Metas](02-dashboard-metas/) | Acompanhamento diário e semanal de metas escalonadas (Bronze / Prata / Ouro) vs. realizado, com projeção |
| 03 | [Dashboard de Atendimento WhatsApp](03-dashboard-atendimento/) | Tempo de resposta, volume de conversas e classificação de reclamações por categoria |
| 04 | [Dashboard de Avaliações Multicanal](04-dashboard-avaliacoes/) | Consolidação das avaliações de clientes — Google, iFood e sistema interno — em um só painel |
| 05 | [Dashboard de Metas dos Gerentes](05-dashboard-metas-gerentes/) | Ranking de gerentes por pilares de resultado, execução e liderança |
| 06 | [Sistema de Teste DISC com análise por IA](06-sistema-teste-disc/) | Web app próprio para aplicação de teste DISC em entrevistas, com respostas em planilha e painel de análise via IA |

## Arquitetura geral

```
ERP Saipos ──► API REST ──► Coletor em Apps Script (JavaScript) ──► Google Sheets ──► Looker Studio
                              • deduplicação por chave única        (camada de dados)   (dashboards)
                              • retry em falhas intermitentes
                              • regras de virada de turno
Outras fontes (WhatsApp, Google, iFood, avaliações internas, formulários) ──► Google Sheets ──► Looker Studio
```

---

*Repositório de portfólio — os painéis originais estão em produção no ambiente interno da empresa e não são acessíveis publicamente.*
