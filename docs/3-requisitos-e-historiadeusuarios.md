# 03 — Requisitos e Histórias de Usuário

## 1. Objetivo
Registrar necessidades funcionais coerentes com as páginas e recursos identificados no arquivo `Hashtag Eletro.pbix`. As histórias abaixo descrevem comportamentos a validar; não significam que todos os critérios já foram homologados.

## 2. Épico A — Visão executiva (Geral)

### US-01 — Consultar indicadores comerciais
**Como** gestor comercial, **quero** visualizar faturamento, lucro, total de vendas e margem, **para** acompanhar o desempenho geral.

**Critérios de aceite**
- Os quatro indicadores devem ser exibidos na página Geral.
- Os valores devem respeitar os filtros aplicáveis.
- Cada indicador deve possuir definição e regra de cálculo documentadas.
- Os valores devem ser reconciliados com a fonte antes da homologação.

### US-02 — Comparar faturamento entre anos
**Como** gestor, **quero** comparar o faturamento atual com o ano anterior por mês, **para** identificar variações temporais.

**Critérios de aceite**
- O visual deve apresentar a comparação mensal prevista.
- O período atual e o período de comparação devem estar alinhados.
- Meses sem dados devem seguir regra definida (zero, vazio ou não exibir).
- A regra de comparação anual deve ser validada para períodos incompletos.

### US-03 — Analisar distribuição comercial
**Como** gestor, **quero** visualizar vendas por tipo de loja e faturamento por tipo de produto, **para** entender a composição do resultado.

**Critérios de aceite**
- As categorias exibidas devem corresponder aos valores da fonte.
- Totais e percentuais devem ser coerentes com o contexto filtrado.
- Rótulos, unidades e títulos devem ser compreensíveis.

### US-04 — Explorar resultado geográfico
**Como** analista, **quero** consultar os resultados por continente e país, **para** identificar diferenças regionais.

**Critérios de aceite**
- A hierarquia ou estrutura geográfica deve permitir interpretação correta.
- Países devem estar associados ao continente correto.
- Filtros de ano devem afetar o visual conforme esperado.

## 3. Épico B — Exploração analítica (Análises)

### US-05 — Decompor o resultado por dimensões
**Como** analista, **quero** decompor os resultados por marca, tipo de produto e nome do produto, **para** investigar os fatores associados ao desempenho.

**Critérios de aceite**
- A árvore de decomposição deve disponibilizar as dimensões identificadas.
- A expansão de cada dimensão deve atualizar a análise corretamente.
- O resultado deve respeitar filtros de contexto.

### US-06 — Alternar a métrica analisada
**Como** usuário, **quero** utilizar o parâmetro de análise, **para** alternar a perspectiva exibida.

**Critérios de aceite**
- O parâmetro deve apresentar as opções configuradas no relatório.
- A seleção deve atualizar os visuais dependentes.
- O nome da métrica e sua unidade devem permanecer claros.
- As opções e medidas associadas devem ser documentadas após inspeção do modelo.

### US-07 — Filtrar por geografia e período
**Como** usuário, **quero** filtrar por país, continente e datas, **para** restringir a análise ao contexto desejado.

**Critérios de aceite**
- Cada segmentação deve aceitar as seleções previstas.
- Os visuais afetados devem refletir a seleção.
- A opção de limpar filtros deve restaurar o contexto padrão, se disponível.
- Não devem ocorrer filtros cruzados inesperados.

## 4. Épico C — Monitoramento de devoluções (Devoluções)

### US-08 — Monitorar indicadores de devolução
**Como** gestor, **quero** visualizar faturamento perdido, devoluções e percentuais relacionados, **para** acompanhar o impacto das devoluções.

**Critérios de aceite**
- Os quatro indicadores identificados devem estar disponíveis.
- Numeradores, denominadores e regras de cálculo devem ser documentados.
- Valores devem ser reconciliados com a fonte.
- Divisão por zero e ausência de dados devem ser tratadas.

### US-09 — Acompanhar evolução mensal
**Como** analista, **quero** visualizar o percentual mensal de devoluções, **para** identificar variações ao longo do tempo.

**Critérios de aceite**
- O eixo temporal deve seguir a dimensão de calendário definida.
- A métrica deve ser calculada com denominador consistente.
- Períodos sem registros devem seguir regra documentada.

### US-10 — Investigar distribuição geográfica
**Como** gestor, **quero** visualizar o percentual de devoluções por continente, **para** identificar regiões que merecem investigação.

**Critérios de aceite**
- A localização deve ser reconhecida corretamente pelo visual.
- A métrica apresentada deve corresponder ao continente selecionado.
- A ausência de localização deve ser tratada de forma explícita.

### US-11 — Investigar devoluções por produto
**Como** analista, **quero** explorar devoluções por marca, tipo de produto e nome do produto, **para** priorizar análises de causa.

**Critérios de aceite**
- As dimensões devem estar disponíveis no visual.
- A ordenação e a agregação devem corresponder à métrica selecionada.
- A análise deve respeitar filtros de ano e tipo de produto.

## 5. Épico D — Contexto adicional (Tooltips)

### US-12 — Consultar detalhes contextuais de vendas e devoluções
**Como** usuário, **quero** visualizar informações complementares ao interagir com os visuais, **para** obter contexto sem sair da página principal.

**Critérios de aceite**
- Tooltip Vendas deve apresentar detalhes coerentes com o ponto selecionado.
- Tooltip Devoluções deve apresentar detalhes coerentes com o ponto selecionado.
- Os valores devem respeitar o contexto do visual de origem.
- O tooltip não deve ser tratado como página independente de dashboard.

## 6. Priorização sugerida
| Prioridade | Histórias | Justificativa |
|---|---|---|
| Alta | US-01, US-02, US-08, US-09 | Indicadores centrais e confiabilidade da leitura |
| Alta | US-05, US-06, US-07 | Capacidade de exploração e análise |
| Média | US-03, US-04, US-10, US-11 | Aprofundamento por dimensões |
| Média | US-12 | Contexto complementar |

A priorização é uma proposta de produto e deve ser validada com stakeholders.
