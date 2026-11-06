# 04 — Catálogo de Indicadores

## 1. Objetivo
Padronizar o significado dos indicadores apresentados no relatório. Os nomes abaixo foram identificados nos visuais do PBIX. As fórmulas oficiais precisam ser confirmadas nas medidas DAX e nas regras da fonte antes de homologação.

## 2. Indicadores da página Geral

| Indicador | Descrição de negócio | Regra a confirmar |
|---|---|---|
| Faturamento Total | Valor financeiro associado às vendas | Confirmar se considera descontos, cancelamentos, impostos e devoluções |
| Lucro Total | Resultado financeiro atribuído às vendas | Confirmar componentes de custo e despesas incluídos |
| Total Vendas | Volume de vendas | Confirmar se é contagem de linhas, transações, pedidos ou unidades |
| Margem | Relação percentual entre lucro e faturamento | Confirmar fórmula; hipótese comum: lucro / faturamento |
| Faturamento Atual vs Ano Anterior | Comparação mensal entre períodos | Confirmar alinhamento de datas e tratamento de período parcial |
| Crescimento YoY | Variação em relação ao período equivalente do ano anterior | Confirmar se exibido como valor ou percentual e fórmula exata |
| Distribuição por Tipo de Loja | Composição de vendas por tipo de loja | Confirmar métrica usada no visual |
| Faturamento por Tipo do Produto | Faturamento segmentado por tipo de produto | Confirmar agregação e filtros |

## 3. Indicadores da página Análises

| Recurso | Descrição | Regra a confirmar |
|---|---|---|
| Árvore de decomposição | Exploração por Marca, Tipo do Produto e Nome Produto | Identificar a medida analisada e a ordem de expansão padrão |
| Parâmetro | Alternância de perspectiva analítica | Registrar opções e medidas vinculadas |
| Crescimento MoM | Comparação mensal, identificada nos recursos visuais | Confirmar fórmula, mês de referência e tratamento de mês sem dados |
| Análise por produto/loja | Destaques exibidos nos visuais complementares | Confirmar métrica, universo e contexto de filtros |

## 4. Indicadores da página Devoluções

| Indicador | Descrição de negócio | Regra a confirmar |
|---|---|---|
| Faturamento Perdido | Valor financeiro atribuído às devoluções | Confirmar se usa preço de venda, valor líquido ou outra base |
| Devoluções | Quantidade de devoluções | Confirmar se conta registros, pedidos, itens ou unidades |
| % Devoluções | Proporção de devoluções | Definir numerador e denominador |
| % Faturamento Perdido | Proporção do faturamento perdido sobre uma base financeira | Definir denominador e período |
| % Devoluções Mensal | Evolução temporal do percentual | Confirmar se a taxa é recalculada por mês ou média de taxas |
| % Devoluções por Continente | Distribuição geográfica da taxa | Confirmar associação geográfica e denominador |

## 5. Definições obrigatórias antes da homologação
Para cada indicador, registrar:
- Nome de negócio e nome técnico da medida.
- Descrição e finalidade.
- Fórmula DAX completa.
- Numerador e denominador, quando aplicável.
- Unidade (R$, %, quantidade).
- Granularidade.
- Tabelas e colunas de origem.
- Regras para nulos, cancelamentos e duplicidades.
- Comportamento esperado sob filtros.
- Responsável pela aprovação da regra.

## 6. Validações prioritárias
1. Confirmar se “Total Vendas” representa pedidos, transações, linhas ou unidades.
2. Confirmar fórmula de margem e componentes do lucro.
3. Confirmar denominador de % Devoluções.
4. Confirmar base financeira de Faturamento Perdido.
5. Validar se as comparações YoY e MoM comparam períodos equivalentes.
6. Verificar consistência dos totais entre páginas quando o contexto de filtro for equivalente.

**Nota:** não assumir fórmulas apenas pelo nome do cartão. O catálogo deve ser atualizado com as expressões DAX reais e aprovadas.
