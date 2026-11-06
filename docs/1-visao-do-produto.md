# 01 — Visão do Produto

## 1. Contexto
A EletroHashtag possui dados relacionados a vendas e devoluções. O relatório Power BI organiza essas informações em três páginas analíticas para apoiar a leitura do desempenho comercial e a investigação de perdas associadas às devoluções.

## 2. Problema de negócio
Sem uma visão consolidada e navegável, gestores e áreas comerciais podem ter dificuldade para acompanhar indicadores, comparar períodos e identificar dimensões que merecem investigação. O relatório procura reduzir essa fragmentação por meio de indicadores e análises interativas.

## 3. Objetivo do produto
Disponibilizar uma visão analítica que permita:
- acompanhar faturamento, lucro, volume de vendas e margem;
- comparar o faturamento entre períodos, incluindo referência ao ano anterior;
- explorar resultados por tipo de loja, produto, país e continente;
- analisar devoluções, faturamento perdido e sua evolução;
- aprofundar a investigação por marca, tipo de produto e produto.

## 4. Usuários e necessidades
| Perfil potencial | Necessidade |
|---|---|
| Gestão comercial | Acompanhar desempenho e tendências |
| Gestão financeira | Monitorar faturamento, lucro, margem e perdas |
| Operação/estoque | Investigar produtos e categorias com desempenho relevante |
| Análise de dados | Explorar dimensões, filtros e variações temporais |

Os perfis são personas de referência para documentação; não representam confirmação de usuários reais ou entrevistas realizadas.

## 5. Escopo funcional identificado no PBIX
### Página Geral
Cartões de Faturamento Total, Lucro Total, Total Vendas e Margem; comparação mensal de faturamento atual versus ano anterior; vendas por tipo de loja; faturamento por tipo de produto; visão por continente e país; segmentação por ano.

### Página Análises
Árvore de decomposição com Marca, Tipo do Produto e Nome Produto; parâmetro de análise; segmentações por País, Continente e Datas; visuais complementares de análise de produto e tipo de produto.

### Página Devoluções
Cartões de Faturamento Perdido, Devoluções, % Devoluções e % Faturamento Perdido; evolução mensal de % Devoluções; mapa de % Devoluções por Continente; análise por Marca, Tipo do Produto e Nome Produto; segmentação por ano e tipo de produto.

### Recursos complementares
Capa e páginas Tooltip Devoluções e Tooltip Vendas. Os tooltips oferecem contexto adicional, não constituindo páginas analíticas independentes.

## 6. Fora do escopo confirmado
Não foram identificadas páginas independentes chamadas “Top 5 Vendas” ou “Top 5 Devoluções”. Rankings desse tipo não devem ser descritos como dashboards próprios sem evidência de que existam em outra versão do relatório.

Também não se deve afirmar que o relatório contém alertas automáticos, previsão, metas, RLS, atualização agendada ou monitoramento operacional sem validação específica.

## 7. Indicadores de sucesso propostos
- Indicadores reconciliados com a fonte de dados.
- Filtros e interações funcionando conforme regras definidas.
- Usuários conseguindo responder às perguntas de negócio previstas.
- Redução de divergências de interpretação por meio de definições padronizadas.

Esses são critérios propostos para avaliar o produto, não resultados medidos.
