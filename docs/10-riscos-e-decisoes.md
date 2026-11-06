## 10 — Riscos e Decisões

## 1. Objetivo
Registrar riscos de interpretação, qualidade e evolução do relatório, diferenciando fatos observados de hipóteses que precisam ser verificadas.

## 2. Riscos identificados

| ID | Risco | Impacto potencial | Mitigação |
|---|---|---|---|
| R-01 | Fórmulas dos KPIs não documentadas | Interpretação divergente de faturamento, lucro e margem | Catalogar e aprovar medidas DAX |
| R-02 | Denominador de % Devoluções não definido | Taxa pode ser interpretada incorretamente | Formalizar numerador e denominador |
| R-03 | Base de Faturamento Perdido não definida | Perda financeira pode ser calculada de forma inconsistente | Validar regra com negócio |
| R-04 | Períodos YoY/MoM incompletos | Comparações temporais enviesadas | Definir tratamento de períodos parciais |
| R-05 | Filtros cruzados inesperados | Usuário pode interpretar valores fora do contexto | Testar interações e estados de filtro |
| R-06 | Localização geográfica incorreta | Mapa pode atribuir dados à região errada | Validar país/continente e geocodificação |
| R-07 | Campos ou relacionamentos sem documentação | Dificuldade de manutenção | Documentar modelo semântico |
| R-08 | Tooltip apresenta contexto incorreto | Detalhamento pode induzir a erro | Testar contexto herdado do visual de origem |

## 3. Decisões e premissas
- O escopo analítico confirmado é composto pelas páginas Geral, Análises e Devoluções.
- Capa e tooltips são recursos de navegação/contexto, não dashboards analíticos independentes.
- Top 5 Vendas e Top 5 Devoluções não devem ser descritos como páginas independentes nesta versão do PBIX.
- Fórmulas e regras de negócio serão consideradas pendentes até serem verificadas nas medidas DAX e aprovadas.
- Governança, testes, operação e critérios de aceite descritos no portfólio são práticas propostas, salvo evidência de implementação.

## 4. Registro de decisão
| Decisão | Estado | Justificativa |
|---|---|---|
| Documentar três dashboards analíticos | Confirmada pela estrutura do relatório | Reflete as páginas existentes |
| Documentar tooltips separadamente | Confirmada | Há duas páginas de tooltip |
| Publicar fórmulas dos KPIs | Pendente | Requer inspeção e validação das medidas |
| Declarar arquitetura estrela | Pendente | Requer confirmação do modelo |
| Declarar atualização agendada/RLS | Não confirmado | Requer evidência de configuração |

## 5. Tratamento
Riscos devem ser priorizados por probabilidade e impacto após avaliação com os responsáveis pelo produto e pelos dados. Não classificar uma hipótese como defeito sem reproduzir e validar o comportamento.
