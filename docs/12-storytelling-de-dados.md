# 12 — Storytelling dos Dashboards

## 1. Narrativa geral do produto
O relatório conta uma história em três etapas: primeiro, apresenta a saúde comercial; depois, permite explorar os fatores associados ao desempenho; por fim, direciona a atenção para as devoluções e seu impacto.

A narrativa deve ser usada como roteiro de leitura. As hipóteses e oportunidades indicadas precisam ser confirmadas com análises adicionais antes de serem tratadas como causas ou recomendações definitivas.

## 2. Dashboard Geral — Qual é a saúde do negócio?
**Pergunta de negócio:** como estão faturamento, lucro, volume de vendas e margem?

A página Geral reúne Faturamento Total, Lucro Total, Total Vendas e Margem. A comparação mensal de faturamento atual versus ano anterior permite observar a evolução temporal. Os visuais por tipo de loja, tipo de produto, continente e país ajudam a decompor a composição do resultado.

**Roteiro de apresentação:**
“Começamos pela visão executiva para entender a dimensão do desempenho comercial. Os indicadores resumem faturamento, lucro, volume e margem. Em seguida, a comparação com o ano anterior ajuda a contextualizar a evolução ao longo dos meses. Por fim, as quebras por canal, produto e geografia apontam onde aprofundar a investigação.”

**Decisões que pode apoiar:** aprofundar análise de canais, produtos e regiões; investigar variações relevantes; direcionar perguntas para áreas comerciais e financeiras.

**Cuidados:** validar fórmula da margem, conceito de vendas e comparabilidade dos períodos.

## 3. Dashboard Análises — O que está associado ao desempenho?
**Pergunta de negócio:** quais marcas, tipos de produto e produtos contribuem para o resultado analisado?

A página Análises oferece árvore de decomposição por Marca, Tipo do Produto e Nome Produto, parâmetro de análise e filtros por País, Continente e Datas. Os visuais complementares permitem observar destaques e variações, incluindo crescimento mensal conforme configuração do relatório.

**Roteiro de apresentação:**
“Depois de observar o resultado geral, precisamos entender como ele se distribui. A árvore de decomposição permite explorar o indicador por marca, tipo de produto e produto. O parâmetro de análise amplia a exploração, enquanto os filtros geográficos e temporais ajudam a delimitar o contexto. Assim, saímos de uma visão agregada para perguntas mais específicas.”

**Decisões que pode apoiar:** priorização de análises por marca ou produto; investigação de variações; planejamento comercial e de estoque, desde que combinado com dados operacionais.

**Cuidados:** documentar as opções do parâmetro, a métrica selecionada e o significado dos visuais complementares.

## 4. Dashboard Devoluções — Onde investigar perdas?
**Pergunta de negócio:** qual é a dimensão das devoluções e como elas variam no tempo e por região/produto?

A página apresenta Faturamento Perdido, Devoluções, % Devoluções e % Faturamento Perdido. A evolução mensal permite acompanhar variações; o mapa mostra % Devoluções por Continente; o gráfico por Marca, Tipo do Produto e Nome Produto permite aprofundar a investigação. Há segmentação por Ano e Tipo do Produto.

**Roteiro de apresentação:**
“Vendas e faturamento não contam toda a história da operação. Também precisamos acompanhar devoluções e seu impacto financeiro. Os indicadores mostram a dimensão do tema; a evolução mensal ajuda a identificar períodos que merecem atenção; e as visões geográfica e por produto ajudam a localizar onde investigar. O próximo passo é cruzar essas ocorrências com motivos de devolução, qualidade, logística e atendimento, se esses dados estiverem disponíveis.”

**Decisões que pode apoiar:** priorizar investigação de regiões, marcas e produtos; solicitar análise de causa; avaliar ações corretivas.

**Cuidados:** definir o denominador da taxa, a regra de faturamento perdido e a granularidade da contagem.

## 5. Tooltips — Como aprofundar sem interromper a leitura?
O relatório contém Tooltip Vendas e Tooltip Devoluções. Eles são recursos contextuais para oferecer detalhes adicionais quando o usuário interage com visuais.

**Roteiro de apresentação:**
“Além das páginas principais, os tooltips ajudam a consultar informações complementares sem navegar para outra página. O valor desse recurso depende de o contexto do ponto selecionado ser preservado corretamente.”

**Validação necessária:** confirmar que cada tooltip recebe os filtros do visual de origem e apresenta informações coerentes com o item selecionado.

## 6. Fechamento executivo
“A solução organiza a análise em uma sequência: compreender o desempenho, explorar seus componentes e investigar as devoluções. O objetivo é transformar indicadores em perguntas melhores e apoiar decisões mais fundamentadas. A confiabilidade dessas decisões depende da validação das regras de negócio, das medidas e da qualidade dos dados.”

## 7. Limites da narrativa
Não afirmar que um produto, marca ou região causa aumento de vendas ou devoluções apenas pela correlação visual. Não apresentar rankings Top 5 como páginas independentes nesta versão do PBIX. Não declarar resultados financeiros como validados sem reconciliação com a fonte.
