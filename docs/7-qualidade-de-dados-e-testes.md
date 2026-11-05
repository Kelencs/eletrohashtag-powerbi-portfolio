# 7. Qualidade de Dados e Testes

## Regras de qualidade
| Regra | Teste / evidência | Severidade sugerida |
|---|---|---|
| Chaves de dimensão | Sem chaves duplicadas ou nulas | Bloqueante |
| Integridade referencial | Fatos encontram produto, loja e data válidos; exceções quantificadas | Alta |
| Quantidade | Vendas/devoluções não negativas, salvo ajuste documentado | Alta |
| Preço e custo | Valores válidos; tratamento de nulos/negativos documentado | Alta |
| Reconciliação | Totais do Power BI reconciliam com amostra da fonte aprovada | Bloqueante |
| Cobertura do calendário | Datas cobrem fatos e períodos comparativos | Alta |
| Inteligência temporal DAX | Testar ano, mês, múltipla seleção, ausência de histórico e ano parcial | Alta |
| Filtros cruzados | Produto, marca, loja, continente, canal e data | Média |
| Ranking | Top 5, empates e contexto de filtros | Média |
| Atualização | Sucesso, falha, atraso e timestamp | Alta |
| Acessibilidade | Contraste, títulos, unidades, teclado e texto alternativo | Média |

## Níveis de teste
- **Testes de dados:** esquema, chaves, nulos, domínios, integridade referencial e duplicidades.
- **Testes de medidas:** cálculo independente de valores esperados para recortes representativos.
- **Testes visuais:** comportamento dos filtros, rótulos, formatação, estados vazios e rankings.
- **UAT / homologação:** usuários de negócio executam cenários acordados e aprovam resultados.
- **Regressão:** repetir cenários críticos de indicadores e filtros após alterações.

## Cenários de homologação (UAT)
1. Selecionar um ano e reconciliar faturamento e quantidade com a fonte.
2. Selecionar uma marca e verificar atualização consistente dos visuais.
3. Comparar período com ano anterior quando houver histórico.
4. Selecionar período sem dados do ano anterior e verificar tratamento adequado.
5. Confirmar com o Data Owner o denominador e a unidade da taxa de devolução.
6. Validar ranking dos cinco produtos mais devolvidos e regra de empate.
7. Testar acesso autorizado e não autorizado, incluindo RLS se aplicável.
8. Confirmar horário da última atualização e comportamento de dados desatualizados.

## Evidências
Guardar caso de teste, filtros de entrada, resultado esperado, resultado obtido, aprovado/reprovado, testador, data e link do defeito.
