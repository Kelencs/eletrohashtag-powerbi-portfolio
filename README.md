# EletroHashtag — Análise de Vendas e Devoluções com Power BI

## Visão geral
Projeto de Business Intelligence desenvolvido no Power BI para explorar o desempenho comercial e as devoluções da EletroHashtag. O relatório disponibiliza três páginas analíticas principais — **Geral**, **Análises** e **Devoluções** — além de uma página de capa e duas páginas de tooltip utilizadas como recursos complementares de contexto.

Este repositório documenta o produto sob as perspectivas de negócio, requisitos, indicadores, modelo, qualidade, testes e evolução. A documentação descreve o que é identificável no arquivo `Hashtag Eletro.pbix` e separa funcionalidades existentes de propostas de melhoria.

## Estrutura do relatório
| Página | Finalidade |
|---|---|
| Capa | Entrada/navegação do relatório |
| Geral | Indicadores executivos, comparação temporal e distribuição das vendas |
| Análises | Exploração do desempenho por dimensões e árvore de decomposição |
| Devoluções | Acompanhamento de devoluções, faturamento perdido e distribuição geográfica |
| Tooltip Devoluções | Detalhamento contextual associado à análise de devoluções |
| Tooltip Vendas | Detalhamento contextual associado à análise de vendas |

> **Escopo correto:** Top 5 Vendas e Top 5 Devoluções não são páginas independentes neste arquivo. As páginas de tooltip também não devem ser contabilizadas como dashboards analíticos.

## Principais recursos identificados
- Cartões de Faturamento Total, Lucro Total, Total Vendas e Margem na página Geral.
- Comparação de faturamento atual versus ano anterior por mês.
- Distribuição de vendas por tipo de loja.
- Análises por tipo de produto, continente e país.
- Árvore de decomposição na página Análises, com dimensões Marca, Tipo do Produto e Nome Produto.
- Parâmetro de análise e segmentações por País, Continente e Datas.
- Indicadores de Faturamento Perdido, Devoluções, % Devoluções e % Faturamento Perdido.
- Evolução mensal e mapa de % Devoluções por Continente.
- Páginas de tooltip para contexto adicional de vendas e devoluções.

## Documentação
- [Visão do produto](docs/01-visao-do-produto.md)
- [Requisitos e histórias de usuário](docs/03-requisitos-e-historias.md)
- [Catálogo de indicadores](docs/04-catalogo-de-indicadores.md)
- [Modelo de dados e arquitetura — pontos a confirmar](docs/06-modelo-de-dados-e-arquitetura.md)
- [Qualidade de dados e testes](docs/07-qualidade-de-dados-e-testes.md)
- [Riscos e decisões](docs/10-riscos-e-decisoes.md)
- [Roadmap](docs/11-roadmap.md)
- [Plano de testes](docs/12-plano-de-testes.md)
- [Storytelling dos dashboards](docs/13-storytelling-dos-dashboards.md)

## Tecnologias e recursos
- Microsoft Power BI
- Power Query e DAX (a confirmar por inspeção do arquivo/modelo)
- Visuais nativos e visuais personalizados presentes no PBIX

## Como visualizar
Abra `Hashtag Eletro.pbix` no Power BI Desktop. Para publicar o arquivo, confirme antes se os dados incorporados podem ser compartilhados e se não há informações confidenciais.

## Limites desta documentação
A inspeção da estrutura do PBIX permite identificar páginas, tipos de visuais, títulos e campos vinculados aos visuais. Ela não comprova, por si só, a correção matemática das medidas DAX, a qualidade da fonte, os relacionamentos completos ou a execução de processos de governança. Esses pontos estão descritos como validações pendentes, não como capacidades já homologadas.

## Próximas validações recomendadas
1. Conferir as fórmulas DAX e suas definições oficiais.
2. Reconciliar os cartões com a fonte de dados.
3. Validar relacionamentos, cardinalidade e direção de filtro.
4. Executar os cenários do plano de testes e registrar evidências.
5. Confirmar o comportamento de tooltips, parâmetros, segmentações e interações.
