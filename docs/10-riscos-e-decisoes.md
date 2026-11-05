# 10. Riscos e Decisões em Aberto

## Riscos
| Risco | Impacto | Mitigação |
|---|---|---|
| Definições de indicadores não aprovadas | Interpretações divergentes | Aprovação do Data Owner e catálogo |
| Preço/custo não históricos | Faturamento/lucro histórico incorreto | Confirmar origem e estratégia de snapshot histórico |
| Denominador da taxa de devolução desalinhado | Taxa enganosa | Aprovar população, período e unidade |
| Linhagem desconhecida | Baixa confiança e dificuldade de investigar incidentes | Documentar linhagem origem-relatório |
| SLA de atualização indefinido | Usuários podem agir com dados antigos | Definir SLA e expor atualidade |
| Modelo de acesso não especificado | Acesso indevido ou restrição excessiva | Classificar dados e validar grupos/RLS |
| Empates de ranking sem regra | Resultados inconsistentes | Definir desempate determinístico |

## Decisões em aberto
| ID | Decisão | Responsável sugerido |
|---|---|---|
| D-01 | Confirmar sistemas de origem, responsáveis e ingestão | Data Owner / Engenharia |
| D-02 | Aprovar definições de faturamento, lucro, custo, preço e devoluções | Negócio / Financeiro |
| D-03 | Confirmar granularidade e chaves das fatos | Engenharia de BI |
| D-04 | Confirmar calendário fiscal/civil e períodos parciais | PO / Data Owner |
| D-05 | Definir grupos de acesso, RLS e política de exportação | Data Owner / Segurança |
| D-06 | Definir SLAs de atualização e qualidade | PO / Engenharia |
| D-07 | Reconciliar números do dashboard com fonte oficial | Steward / Negócio |
| D-08 | Aprovar métrica de ranking e critérios de desempate | PO / Negócio |
| D-09 | Revisar DAX quanto a contexto, denominadores e uso de preço/custo relacionado | Engenharia de BI / PO |
