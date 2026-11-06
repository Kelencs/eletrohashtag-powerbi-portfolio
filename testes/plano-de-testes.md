# Plano de Testes — Projeto EletroHashtag Power BI

**Projeto:** EletroHashtag — Análise de Vendas e Devoluções  
**Categoria:** Business Intelligence | Power BI | Qualidade de Dados  
**Responsável pelo planejamento:** Product Owner de Dados  
**Status:** Proposta de validação

---

## 1. Objetivo

Estabelecer os cenários e critérios de validação necessários para garantir que os dashboards do projeto EletroHashtag apresentem informações consistentes, cálculos corretos e comportamento adequado diante de filtros e interações.

O plano contempla testes funcionais, validação de indicadores, qualidade dos dados, modelagem e experiência de utilização.

## 2. Escopo dos testes

Serão validadas as cinco páginas do projeto:

| Dashboard | Objetivo da validação |
|---|---|
| Geral | Validar indicadores executivos e evolução das vendas |
| Análises | Validar segmentações por produto, marca e loja |
| Devoluções | Validar indicadores de devolução e perdas financeiras |
| Top 5 Devoluções | Validar ranking de produtos devolvidos |
| Top 5 Vendas | Validar ranking de produtos por faturamento |

Também serão avaliados os relacionamentos do modelo de dados, medidas DAX, filtros, segmentações e consistência entre os indicadores.

## 3. Estratégia de testes

A estratégia será dividida em seis frentes:

1. **Testes funcionais:** verificar se os elementos dos dashboards funcionam conforme esperado.
2. **Testes de indicadores:** validar fórmulas e resultados das medidas DAX.
3. **Testes de qualidade de dados:** verificar integridade, consistência e completude.
4. **Testes de filtros e interações:** verificar se os filtros afetam corretamente os visuais.
5. **Testes de modelo de dados:** validar relacionamentos e propagação dos filtros.
6. **Testes de usabilidade:** avaliar clareza, legibilidade e facilidade de interpretação.

## 4. Cenários de testes funcionais

### 4.1 Dashboard Geral

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT-001 | Validar apresentação do faturamento total | O cartão deve apresentar o valor correspondente à base e aos filtros aplicados |
| CT-002 | Validar cálculo do lucro total | O resultado deve corresponder à regra de negócio definida |
| CT-003 | Validar quantidade de vendas | O indicador deve respeitar o critério de contagem definido |
| CT-004 | Validar margem apresentada | O percentual deve corresponder à fórmula de margem aprovada |
| CT-005 | Validar comparação mensal | Os valores devem corresponder aos períodos selecionados |
| CT-006 | Validar distribuição por canal | Os valores devem respeitar a classificação de loja física e online |
| CT-007 | Validar filtros de período | Os indicadores e gráficos devem responder ao período selecionado |

### 4.2 Dashboard Análises

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT-008 | Filtrar por marca | Os gráficos devem apresentar somente os dados da marca selecionada |
| CT-009 | Filtrar por produto | Os indicadores devem refletir o produto selecionado |
| CT-010 | Filtrar por loja | Os resultados devem corresponder à loja selecionada |
| CT-011 | Alternar entre faturamento e vendas | Os gráficos devem atualizar conforme a métrica selecionada |
| CT-012 | Validar produto com maior volume | O produto destacado deve corresponder ao maior valor no contexto filtrado |

### 4.3 Dashboard Devoluções

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT-013 | Validar total de devoluções | A quantidade deve corresponder à base de devoluções |
| CT-014 | Validar faturamento perdido | O valor deve seguir a regra de cálculo aprovada |
| CT-015 | Validar percentual de devoluções | O percentual deve respeitar o denominador definido |
| CT-016 | Validar percentual de faturamento perdido | O cálculo deve utilizar a base financeira correta |
| CT-017 | Validar evolução mensal | Os valores devem respeitar o calendário e o período selecionado |
| CT-018 | Validar análise por marca | Os resultados devem refletir corretamente a marca selecionada |

### 4.4 Dashboard Top 5 Devoluções

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT-019 | Validar ranking dos cinco produtos | Devem aparecer os cinco produtos com maior valor conforme a métrica utilizada |
| CT-020 | Alterar mês selecionado | O ranking deve ser atualizado para o período escolhido |
| CT-021 | Validar percentual de devoluções | O percentual deve corresponder à regra de negócio definida |
| CT-022 | Validar ordenação do ranking | Os produtos devem ser apresentados em ordem decrescente |

### 4.5 Dashboard Top 5 Vendas

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT-023 | Validar ranking de faturamento | Os cinco produtos devem corresponder aos maiores valores |
| CT-024 | Alterar categoria | O ranking deve considerar somente a categoria selecionada |
| CT-025 | Validar faturamento total | O valor deve corresponder à soma dos registros considerados |
| CT-026 | Validar ordenação | Os produtos devem ser apresentados em ordem decrescente de faturamento |

## 5. Testes de qualidade de dados

| ID | Regra de validação | Resultado esperado |
|---|---|---|
| QD-001 | Verificar campos obrigatórios | Não devem existir valores ausentes em campos críticos |
| QD-002 | Verificar duplicidade de identificadores | Não devem existir duplicidades indevidas nas chaves |
| QD-003 | Verificar integridade referencial | As chaves estrangeiras devem encontrar correspondência nas dimensões |
| QD-004 | Verificar valores financeiros | Não devem existir valores inválidos ou inconsistentes |
| QD-005 | Verificar datas | As datas devem estar em formato válido e dentro do período esperado |
| QD-006 | Verificar registros de devolução | Os registros devem seguir as regras de relacionamento com as vendas |
| QD-007 | Verificar atualização dos dados | A atualização deve refletir a fonte de dados conforme a frequência definida |

## 6. Testes de medidas DAX

As medidas DAX devem ser comparadas com cálculos independentes realizados diretamente sobre a fonte de dados ou por meio de consultas SQL, quando disponíveis.

| ID | Medida ou funcionalidade | Validação |
|---|---|---|
| DAX-001 | Faturamento total | Comparar a medida com a soma dos valores de venda |
| DAX-002 | Lucro total | Comparar com a regra de cálculo de lucro aprovada |
| DAX-003 | Margem | Validar a relação entre lucro e faturamento |
| DAX-004 | Total de vendas | Conferir o critério de contagem utilizado |
| DAX-005 | Total de devoluções | Comparar com os registros válidos de devolução |
| DAX-006 | Variação mensal | Validar comparação entre períodos equivalentes |
| DAX-007 | Acumulados temporais | Validar MTD, QTD e YTD, quando aplicáveis |
| DAX-008 | Comparação anual | Validar os resultados de ano atual versus ano anterior |

**Atenção:** antes da aprovação, devem ser documentadas as fórmulas oficiais e os critérios de negócio de cada indicador. Por exemplo, é necessário definir se o faturamento considera descontos, cancelamentos e devoluções.

## 7. Testes do modelo de dados

| ID | Cenário | Resultado esperado |
|---|---|---|
| MD-001 | Validar relacionamento entre fatos e dimensões | Os relacionamentos devem respeitar as chaves definidas |
| MD-002 | Validar tabela calendário | Deve existir correspondência entre as datas e a dimensão calendário |
| MD-003 | Validar direção de filtragem | Os filtros devem se propagar conforme o desenho do modelo |
| MD-004 | Verificar cardinalidade | Os relacionamentos devem apresentar cardinalidade adequada |
| MD-005 | Validar ausência de ambiguidade | Não devem existir caminhos de filtragem conflitantes |
| MD-006 | Validar interação entre tabelas de vendas e devoluções | Os indicadores devem respeitar a lógica de negócio estabelecida |

## 8. Testes de usabilidade

- Verificar se os títulos dos gráficos são claros.
- Avaliar se os indicadores possuem nomes e unidades compreensíveis.
- Verificar se os filtros são intuitivos.
- Validar se os gráficos facilitam a identificação de tendências.
- Avaliar a consistência visual entre as páginas.
- Verificar se os percentuais e valores monetários possuem formatação adequada.
- Garantir que os dashboards não apresentem informações cortadas ou sobrepostas.

## 9. Critérios de entrada e saída

### Critérios de entrada

- Base de dados disponível.
- Modelo de dados estruturado.
- Medidas DAX implementadas.
- Regras de negócio documentadas.
- Dashboards disponíveis para validação.

### Critérios de saída

- Todos os cenários críticos executados.
- Indicadores financeiros reconciliados com a fonte.
- Filtros e interações validados.
- Inconsistências críticas corrigidas.
- Evidências dos testes registradas.
- Aprovação funcional dos resultados.

## 10. Registro de execução dos testes

Cada cenário deve possuir um registro de execução:

| ID | Status | Evidência | Observação |
|---|---|---|---|
| CT-001 | Não executado | Pendente | Aguardando validação |
| CT-002 | Não executado | Pendente | Aguardando validação |
| CT-003 | Não executado | Pendente | Aguardando validação |

**Status possíveis:**
- Não executado
- Aprovado
- Reprovado
- Bloqueado
- Em correção

Os resultados devem ser atualizados durante a execução efetiva dos testes. Não considerar um cenário aprovado sem evidência.

## 11. Gestão de defeitos

Quando uma inconsistência for identificada, registrar:

- Identificador do defeito.
- Dashboard afetado.
- Indicador ou funcionalidade envolvida.
- Descrição do problema.
- Resultado esperado.
- Resultado encontrado.
- Evidência visual.
- Severidade.
- Responsável pela correção.
- Status da correção.
- Resultado do reteste.

### Classificação de severidade

| Severidade | Definição |
|---|---|
| Crítica | Indicador financeiro incorreto ou falha que compromete decisões importantes |
| Alta | Filtro, cálculo ou visualização com impacto relevante |
| Média | Problema funcional com impacto limitado |
| Baixa | Ajuste visual ou melhoria de apresentação |

## 12. Riscos identificados

| Risco | Impacto | Ação preventiva |
|---|---|---|
| Divergência entre indicadores | Decisões incorretas | Reconciliação com a fonte |
| Fórmulas DAX incorretas | Resultados inconsistentes | Testes independentes das medidas |
| Filtros com comportamento inesperado | Interpretação equivocada | Testes de interação |
| Dados duplicados | Superestimação de indicadores | Regras de unicidade |
| Relacionamentos incorretos | Totais divergentes | Validação do modelo |
| Ausência de documentação das métricas | Falta de padronização | Catálogo de indicadores |

## 13. Critérios de aprovação do projeto

O projeto poderá ser considerado validado quando:

1. Os indicadores principais apresentarem resultados reconciliados.
2. As regras de negócio estiverem documentadas.
3. Os filtros e segmentações funcionarem corretamente.
4. O ranking dos produtos apresentar os resultados esperados.
5. Os relacionamentos do modelo estiverem validados.
6. As inconsistências identificadas estiverem corrigidas ou formalmente registradas.
7. As evidências de execução estiverem disponíveis.

## 14. Resultado esperado

A aplicação deste plano de testes busca assegurar que o EletroHashtag Power BI seja uma solução confiável de análise comercial, permitindo que usuários e gestores interpretem corretamente os indicadores de vendas, faturamento, lucro e devoluções.

O objetivo é garantir que as informações apresentadas sejam consistentes, rastreáveis e adequadas para apoiar decisões de negócio.

---

**Responsabilidade do Product Owner de Dados:** garantir que os critérios de negócio estejam claros, que os indicadores atendam às necessidades dos usuários e que os resultados sejam validados antes de serem considerados prontos para utilização.
