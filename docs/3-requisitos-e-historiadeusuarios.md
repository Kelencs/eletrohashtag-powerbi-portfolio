# 3. Requisitos e Histórias de Usuário

Prioridade: **P0** = essencial para MVP/validação; **P1** = importante; **P2** = evolução posterior. Prioridades propostas.

## US-01 — Visão executiva (P0)
**Como** gerente comercial, **quero** visualizar os indicadores de faturamento, lucro, quantidade vendida e margem, **para** acompanhar rapidamente o desempenho do negócio.

Critérios de aceite:
- Dado que existam dados válidos para o período selecionado, quando eu abrir a Visão Geral, então os quatro indicadores devem aparecer com rótulos, unidades e período aplicável.
- Os valores devem respeitar os filtros ativos e as definições aprovadas.
- Se não houver dados, o relatório deve apresentar um estado vazio claro, sem exibir zero de forma enganosa.

## US-02 — Comparação ano contra ano (P0)
**Como** gerente comercial, **quero** comparar o desempenho atual com o período equivalente do ano anterior, **para** identificar crescimento ou retração.

Critérios de aceite:
- Os valores atual e comparativo e a variação percentual devem usar períodos comparáveis.
- Se não houver dados do período anterior ou o denominador for zero, exibir N/A ou mensagem acordada.
- A comparação deve utilizar o calendário aprovado e a lógica temporal documentada.

## US-03 — Análise por região e canal (P1)
**Como** gerente comercial, **quero** segmentar faturamento e vendas por continente e tipo de loja, **para** identificar concentração e oportunidades.

Critérios de aceite:
- Os visuais devem responder aos filtros compatíveis.
- Os totais dos segmentos devem reconciliar com o total geral, considerando exclusões documentadas.
- Moeda, percentuais e rótulos devem ter formatação consistente.

## US-04 — Investigação de produto e marca (P0)
**Como** analista de vendas, **quero** filtrar por marca, tipo de produto e produto, **para** investigar o desempenho dos produtos.

Critérios de aceite:
- Os filtros devem permitir o comportamento de seleção aprovado.
- Indicadores e visuais devem atualizar preservando o contexto dos filtros.
- “Produto mais vendido” deve usar métrica aprovada e critério de desempate determinístico.

## US-05 — Loja com maior volume (P1)
**Como** gerente comercial, **quero** identificar a loja com maior quantidade vendida, **para** direcionar ações comerciais.

Critérios de aceite:
- A loja destacada deve ser a maior pela medida aprovada de quantidade vendida no contexto atual dos filtros.
- Empates devem seguir regra documentada.
- Nome e quantidade devem corresponder à mesma loja e ao mesmo contexto.

## US-06 — Monitoramento de devoluções (P0)
**Como** gestor de devoluções, **quero** acompanhar quantidade, taxa e faturamento perdido, **para** detectar aumentos e impacto financeiro.

Critérios de aceite:
- Quantidade, taxa e faturamento perdido devem seguir definições aprovadas e denominadores claramente identificados.
- A análise mensal deve responder aos filtros de período, marca e produto.
- Registros duplicados de devolução não devem inflar as medidas.

## US-07 — Produtos mais devolvidos (P1)
**Como** gestor de devoluções, **quero** visualizar os cinco produtos com maior quantidade devolvida, **para** priorizar investigações.

Critérios de aceite:
- O ranking deve apresentar até cinco produtos no contexto atual dos filtros.
- A métrica do ranking (quantidade ou valor) deve estar explícita.
- Empates devem seguir regra determinística.

## US-08 — Exploração por mês/categoria (P1)
**Como** analista de negócio, **quero** selecionar mês ou categoria e visualizar indicadores e rankings relacionados, **para** responder perguntas específicas.

Critérios de aceite:
- A seleção deve atualizar todos os visuais dependentes.
- Ausência de seleção deve apresentar orientação clara ou padrão aprovado.
- Interações entre filtros devem ser testadas e documentadas.

## US-09 — Transparência da atualização (P1)
**Como** Data Steward, **quero** consultar o horário da última atualização bem-sucedida, **para** avaliar a atualidade dos dados.

Critérios de aceite:
- A data/hora da última atualização bem-sucedida e o fuso horário devem estar disponíveis.
- Falhas de atualização devem alertar o responsável definido.
- Dados fora do SLA de atualidade acordado devem ser sinalizados.

## US-10 — Controle de acesso (P0)
**Como** Data Owner, **quero** limitar o acesso ao relatório e ao conjunto semântico a grupos autorizados, **para** proteger os dados de negócio.

Critérios de aceite:
- Somente grupos aprovados podem acessar workspace, modelo semântico e relatório.
- Se houver restrições por linha, RLS deve ter casos de teste positivos e negativos.
- Exportação e compartilhamento devem seguir a política organizacional.

## US-11 — Validação da qualidade de dados (P0)
**Como** Data Steward, **quero** acompanhar regras de qualidade e reconciliação, **para** garantir confiabilidade dos indicadores publicados.

Critérios de aceite:
- Verificações de completude, validade, unicidade e integridade referencial devem rodar em frequência acordada.
- Falhas críticas devem bloquear publicação ou gerar incidente conforme severidade definida.
- Resultados e evidências devem ser armazenados.

## US-12 — Definições dos indicadores (P1)
**Como** usuário de negócio, **quero** consultar definição, fórmula, unidade e responsável de cada indicador, **para** interpretar os números corretamente.

Critérios de aceite:
- Cada indicador publicado deve ter definição, fórmula, granularidade, filtros e responsável documentados.
- Definições aprovadas devem estar acessíveis no relatório ou catálogo vinculado.
- Alterações devem ser versionadas.

## Requisitos não funcionais (propostos)
- Desempenho: acordar tempo de resposta alvo e testar com volume representativo.
- Acessibilidade: contraste legível, rótulos claros, navegação por teclado e títulos significativos.
- Confiabilidade: SLA de atualização e escalonamento de incidentes definidos antes da produção.
- Segurança: privilégio mínimo; RLS somente quando necessária e devidamente testada.
- Manutenibilidade: medidas organizadas, convenções de nomes e modelo/documentação versionados.
