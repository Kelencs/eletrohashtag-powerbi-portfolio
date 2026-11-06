# 12 — Plano de Testes

## 1. Objetivo
Definir cenários para verificar se o relatório apresenta dados, indicadores, filtros e interações corretos. O plano cobre as páginas Geral, Análises e Devoluções, além dos tooltips.

## 2. Escopo
- Página Geral.
- Página Análises.
- Página Devoluções.
- Tooltip Devoluções.
- Tooltip Vendas.
- Medidas DAX, segmentações, parâmetro, interações e modelo semântico.

A Capa será verificada apenas quanto à navegação. Não há páginas independentes Top 5 Vendas ou Top 5 Devoluções nesta versão do arquivo.

## 3. Tipos de teste
- Funcional: comportamento de cartões, gráficos e navegação.
- Indicadores: cálculo e reconciliação de medidas.
- Filtros/interações: propagação de seleções.
- Temporal: comparação YoY/MoM e calendário.
- Geográfico: mapa por continente.
- Tooltip: contexto herdado do visual de origem.
- Qualidade: completude, validade, unicidade e integridade.
- Usabilidade: legibilidade, títulos, unidades e consistência visual.

## 4. Cenários de teste

### 4.1 Capa e navegação
| ID | Cenário | Resultado esperado |
|---|---|---|
| NAV-01 | Acionar botão de entrada | Navegar para a página pretendida |
| NAV-02 | Usar botões de navegação nas páginas | Destino correto e sem erro |
| NAV-03 | Retornar à página inicial, se houver ação disponível | Retorno à Capa |

### 4.2 Geral
| ID | Cenário | Resultado esperado |
|---|---|---|
| GER-01 | Conferir Faturamento Total | Reconciliado com a fonte e filtros aplicados |
| GER-02 | Conferir Lucro Total | Reconciliado com regra de lucro aprovada |
| GER-03 | Conferir Total Vendas | Contagem conforme granularidade documentada |
| GER-04 | Conferir Margem | Fórmula e denominador aprovados |
| GER-05 | Alterar Ano | Cartões e visuais reagem corretamente |
| GER-06 | Conferir Faturamento Atual vs Ano Anterior | Períodos comparáveis e valores corretos |
| GER-07 | Conferir vendas por Tipo de Loja | Categorias e agregações corretas |
| GER-08 | Conferir faturamento por Tipo do Produto | Valores corretos no contexto |
| GER-09 | Conferir Continente/País | Hierarquia geográfica consistente |

### 4.3 Análises
| ID | Cenário | Resultado esperado |
|---|---|---|
| ANA-01 | Expandir árvore por Marca | Decomposição correta |
| ANA-02 | Expandir por Tipo do Produto | Categorias e valores corretos |
| ANA-03 | Expandir por Nome Produto | Produtos correspondem ao contexto |
| ANA-04 | Alterar Parâmetro | Métrica/visual dependente é atualizado |
| ANA-05 | Filtrar País | Visuais afetados respeitam seleção |
| ANA-06 | Filtrar Continente | Visuais afetados respeitam seleção |
| ANA-07 | Filtrar Datas | Período aplicado corretamente |
| ANA-08 | Conferir visual complementar de produto/tipo | Informação e métrica coerentes |

### 4.4 Devoluções
| ID | Cenário | Resultado esperado |
|---|---|---|
| DEV-01 | Conferir Faturamento Perdido | Reconciliado com regra financeira aprovada |
| DEV-02 | Conferir Devoluções | Contagem conforme granularidade definida |
| DEV-03 | Conferir % Devoluções | Numerador e denominador aprovados |
| DEV-04 | Conferir % Faturamento Perdido | Base financeira e fórmula aprovadas |
| DEV-05 | Conferir evolução mensal | Datas e cálculo mensal corretos |
| DEV-06 | Filtrar Ano | Indicadores e visuais respeitam o filtro |
| DEV-07 | Filtrar Tipo do Produto | Indicadores e visuais respeitam o filtro |
| DEV-08 | Conferir mapa por Continente | Localização e taxa coerentes |
| DEV-09 | Conferir análise por Marca/Tipo/Nome Produto | Categorias e valores coerentes |

### 4.5 Tooltips
| ID | Cenário | Resultado esperado |
|---|---|---|
| TIP-01 | Acionar Tooltip Vendas em um ponto do visual | Detalhes correspondem ao ponto selecionado |
| TIP-02 | Acionar Tooltip Devoluções | Detalhes correspondem ao ponto selecionado |
| TIP-03 | Alterar filtros e repetir | Tooltip respeita o novo contexto |
| TIP-04 | Verificar conteúdo e legibilidade | Valores, rótulos e imagens são legíveis |

## 5. Testes de qualidade e modelo
| ID | Controle | Resultado esperado |
|---|---|---|
| QD-01 | Campos críticos nulos | Ausências identificadas e tratadas |
| QD-02 | Duplicidade | Duplicidades avaliadas na granularidade correta |
| QD-03 | Integridade referencial | Chaves relacionadas válidas |
| QD-04 | Datas | Datas válidas e períodos consistentes |
| QD-05 | Valores financeiros | Tipos e sinais coerentes com a regra |
| MD-01 | Relacionamentos | Cardinalidade e direção de filtro documentadas |
| MD-02 | Calendário | Relação e marcação de tabela de datas verificadas |
| MD-03 | Filtros cruzados | Sem propagação inesperada |
| DAX-01 | Medidas principais | Comparadas com cálculo independente |
| DAX-02 | YoY/MoM | Comparação temporal equivalente |

## 6. Critérios de entrada
- PBIX e fonte de dados disponíveis.
- Regras de negócio e fórmulas acessíveis.
- Contexto de filtros de teste definido.
- Ambiente de validação preparado.

## 7. Critérios de saída
- Cenários críticos executados.
- Divergências registradas e tratadas.
- KPIs reconciliados ou pendências formalizadas.
- Evidências anexadas.
- Aprovação funcional registrada pelo responsável.

## 8. Registro de execução
| ID | Status | Evidência | Observação |
|---|---|---|---|
| GER-01 | Não executado | Pendente | Aguardando reconciliação |
| GER-02 | Não executado | Pendente | Aguardando reconciliação |
| DEV-03 | Não executado | Pendente | Confirmar denominador |
| TIP-01 | Não executado | Pendente | Validar contexto |

Status possíveis: Não executado, Aprovado, Reprovado, Bloqueado ou Em correção. Não marcar como aprovado sem evidência.

## 9. Gestão de defeitos
Registrar ID, página, visual/indicador, filtros ativos, passos para reproduzir, resultado esperado, resultado obtido, evidência, severidade, responsável, correção e reteste.

## 10. Severidade
- Crítica: indicador financeiro incorreto ou erro que comprometa decisões relevantes.
- Alta: filtro ou cálculo com impacto significativo.
- Média: comportamento incorreto com impacto limitado.
- Baixa: ajuste visual ou de apresentação.

## 11. Pontos de atenção
Priorizar a definição de Total Vendas, Margem, Faturamento Perdido, % Devoluções e % Faturamento Perdido. Conferir também períodos incompletos em YoY/MoM e o contexto herdado pelos tooltips.

Este plano descreve testes planejados; não comprova que foram executados.
