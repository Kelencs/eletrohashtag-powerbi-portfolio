# 11 — Roadmap de Evolução

## 1. Objetivo
Organizar oportunidades de evolução a partir das capacidades observadas no relatório. Este roadmap é uma proposta; não representa funcionalidades já implementadas ou compromissos de entrega.

## 2. Agora — Confiabilidade e clareza
- Confirmar fórmulas DAX e regras de negócio dos KPIs.
- Reconciliar faturamento, lucro, vendas e devoluções com a fonte.
- Documentar o parâmetro utilizado na página Análises.
- Validar interações, filtros e tooltips.
- Documentar modelo semântico e origem dos dados.
- Revisar títulos, unidades e descrições dos indicadores.

## 3. Próximo — Aprofundamento analítico
- Investigar motivos de devolução, caso a fonte contenha essa informação.
- Permitir análise por período, produto, marca e região com métricas padronizadas.
- Avaliar ranking de produtos como visual ou página adicional, se houver necessidade de negócio.
- Incluir metas e comparação com orçamento, caso existam metas aprovadas.
- Avaliar segmentação por canal e rentabilidade, conforme disponibilidade dos dados.

## 4. Futuro — Monitoramento e ação
- Avaliar alertas para variações relevantes de vendas ou devoluções.
- Criar acompanhamento de metas e indicadores críticos.
- Avaliar previsão de demanda somente após validação de histórico, granularidade e qualidade.
- Avaliar segurança por perfil (RLS) se houver requisito de acesso segmentado.
- Definir processo de atualização, monitoramento e suporte.

## 5. Priorização sugerida
| Iniciativa | Valor de negócio | Dependência | Prioridade sugerida |
|---|---|---|---|
| Validar KPIs e DAX | Muito alto | Acesso ao modelo e fonte | Alta |
| Validar filtros e tooltips | Alto | Cenários de teste | Alta |
| Documentar modelo semântico | Alto | Model view/Power Query | Alta |
| Análise de motivos de devolução | Alto | Campo de motivo disponível | Média |
| Ranking dedicado de produtos | Médio | Requisito validado | Média |
| Alertas e previsão | Potencialmente alto | Dados confiáveis e regra de negócio | Baixa/futura |

## 6. Critérios para entrada no roadmap
Uma iniciativa deve ter problema de negócio definido, usuário beneficiado, valor esperado, dados disponíveis, critérios de aceite e dependências conhecidas.

