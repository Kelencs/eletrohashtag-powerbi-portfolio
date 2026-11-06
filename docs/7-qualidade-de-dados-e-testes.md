# 07 — Qualidade de Dados e Testes

## 1. Objetivo
Definir controles para avaliar a confiabilidade dos dados que alimentam os indicadores de vendas e devoluções.

## 2. Dimensões de qualidade
| Dimensão | Pergunta de controle | Exemplo de validação |
|---|---|---|
| Completude | Campos críticos estão preenchidos? | Datas, identificadores, valores e categorias não nulos |
| Unicidade | Há duplicidade indevida? | Identificadores únicos na granularidade esperada |
| Validade | Os valores respeitam formatos e domínios? | Datas válidas, valores monetários numéricos |
| Consistência | Os dados concordam entre tabelas e páginas? | País associado ao continente correto |
| Integridade | As referências encontram correspondência? | Chaves relacionadas existentes |
| Atualidade | Os dados estão atualizados? | Data de carga dentro da frequência acordada |
| Acurácia | Os valores refletem a fonte? | Reconciliação de totais e amostras |

## 3. Controles específicos do projeto
- Conferir se o total de vendas segue a granularidade definida.
- Validar o tratamento de cancelamentos e devoluções no faturamento.
- Verificar se o faturamento perdido utiliza a regra financeira aprovada.
- Confirmar que os percentuais utilizam denominadores consistentes.
- Conferir a classificação de tipo de loja, tipo de produto, marca, país e continente.
- Validar datas e períodos usados nas comparações YoY e MoM.
- Avaliar registros sem país/continente ou sem categoria.
- Verificar se filtros não produzem totais inesperados.

## 4. Reconciliação
Para cada KPI:
1. Selecionar um período e contexto de filtro conhecidos.
2. Obter o resultado no Power BI.
3. Calcular o mesmo indicador diretamente na fonte ou em consulta independente.
4. Comparar os resultados.
5. Investigar diferenças de granularidade, filtros, nulos, duplicidades e regras de negócio.
6. Registrar evidência e conclusão.

## 5. Evidências
Manter, por cenário:
- identificador do teste;
- contexto de filtros;
- valor esperado;
- valor obtido;
- resultado;
- captura de tela ou consulta de apoio;
- data e responsável pela execução.

## 6. Situação
Este documento estabelece controles propostos. Não há afirmação de que as verificações foram executadas ou aprovadas. O status deve ser preenchido somente após a execução.
