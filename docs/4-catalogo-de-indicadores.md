# 4. Catálogo de Indicadores

> As definições abaixo são interpretações iniciais das medidas visíveis no material do projeto. Devem ser validadas pelos responsáveis de negócio antes do uso em produção.

| Indicador / medida | Interpretação técnica inicial | Validação de negócio necessária |
|---|---|---|
| Faturamento Total | Soma de quantidade vendida × preço unitário relacionado | Preço histórico/atual, descontos, impostos, moeda e cancelamentos |
| Lucro Total | Faturamento menos quantidade × custo unitário relacionado | Custo histórico, despesas incluídas e margem negativa |
| Total de Vendas | Soma da quantidade vendida | Confirmar unidades vs pedidos vs linhas de transação |
| Margem de Lucro | Lucro total / faturamento total | Comportamento quando faturamento é zero; formato percentual |
| Faturamento Ano Anterior | Faturamento deslocado para o ano anterior | Calendário e comparabilidade |
| Crescimento YoY | (atual − ano anterior) / ano anterior | Histórico ausente e denominador zero |
| Crescimento MoM | (atual − mês anterior) / mês anterior | Primeiro mês e períodos incompletos |
| MTD / QTD / YTD | Acumulados do mês / trimestre / ano | Calendário civil ou fiscal e data de corte |
| Total de Devoluções | Soma da quantidade devolvida | Unidades, devoluções parciais e duplicidades |
| Faturamento Perdido | Quantidade devolvida × preço unitário relacionado | Valor bruto/líquido e tratamento de reembolso |
| Taxa de Devolução | Total devolvido / total vendido | Alinhamento de período, população e unidade |
| % Faturamento Perdido | Faturamento perdido / faturamento total | Denominador e população elegível |
| Vendas Online | Quantidade vendida filtrada para tipo de loja Online | Padronização dos valores de canal |
| Produto / Loja Top 1 | TOPN(1) por quantidade vendida | Desempate e contexto de filtros |

## Modelo de documentação de indicador
Para cada indicador em produção, registrar:
- Nome de negócio e definição
- Fórmula / medida do modelo semântico
- Unidade e moeda
- Granularidade e população elegível
- Dimensões e filtros
- Lógica temporal e fuso horário
- Tabelas de origem e linhagem
- Data Owner e responsável técnico
- Verificações de qualidade e limitações conhecidas
- Versão e data de aprovação
