# 5. Governança de Dados

## Objetivos de governança
- Estabelecer responsáveis pelos dados e indicadores.
- Padronizar o vocabulário de negócio.
- Proteger os dados com controles de acesso apropriados.
- Monitorar qualidade e atualidade.
- Manter rastreabilidade de mudanças e incidentes.

## Matriz RACI (proposta)
| Atividade | Product Owner | Data Owner | Data Steward | Engenharia de BI |
|---|---|---|---|---|
| Priorizar backlog | A/R | C | C | C |
| Aprovar definições de indicadores | R | A | C | C |
| Aprovar exceções de qualidade | C | A | R | C |
| Modelo e pipeline de dados | C | C | C | A/R |
| Acesso e classificação | C | A | R | R |
| Release e operação | A | C | C | R |
| Aceite de negócio | R | A | C | C |

A = accountable (responsável final); R = responsável pela execução; C = consultado.

## Controles mínimos de governança
1. **Ownership:** nomear Data Owner de negócio e responsável técnico para cada conjunto de dados e indicador.
2. **Catálogo:** documentar nome, descrição, domínio, origem, granularidade, frequência de atualização, classificação, responsável e linhagem.
3. **Glossário:** padronizar faturamento, lucro, venda, devolução, loja online, marca e região.
4. **Qualidade:** monitorar completude, validade, unicidade, consistência, integridade referencial e atualidade.
5. **Segurança:** classificar dados, aplicar privilégio mínimo, revisar acessos e avaliar LGPD se houver dados pessoais.
6. **Gestão de mudanças:** versionar medidas, modelo, definições e relatório; comunicar alterações que afetem indicadores.
7. **Incidentes:** registrar impacto, período afetado, causa-raiz, correção, responsável e prevenção.

## Ciclo de vida de um problema de dados
Registro → triagem/severidade → atribuição de responsável → análise de causa-raiz → correção → regressão/reconciliação → comunicação aos stakeholders → encerramento e prevenção.

## Severidade sugerida
- **Crítica:** indicador materialmente incorreto ou exposição de dados restritos; considerar suspender publicação.
- **Alta:** conjunto importante desatualizado ou indicador-chave incorreto.
- **Média:** defeito localizado com alternativa de contorno.
- **Baixa:** questão visual ou de usabilidade menor.
