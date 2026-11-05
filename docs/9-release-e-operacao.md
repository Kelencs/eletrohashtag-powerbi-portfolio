# 9. Release e Operação

## Decisões operacionais a acordar
| Tema | Controle proposto |
|---|---|
| Atualização | Definir frequência, janela, SLA e responsável |
| Monitoramento | Alertar falha ou dados desatualizados; manter histórico |
| Ambientes | Separar desenvolvimento, teste/homologação e produção |
| Versionamento | Versionar PBIX/PBIP, DAX, documentação e notas de versão |
| Suporte | Definir canal, severidade, prazo de resposta e escalonamento |
| Release | Checklist de regressão, aprovação de negócio, rollback e comunicação |

## Checklist de release
- [ ] Definições dos indicadores e stakeholders impactados revisados
- [ ] Testes de qualidade e reconciliação aprovados
- [ ] Medidas críticas e filtros testados em regressão
- [ ] Permissões / RLS revisadas
- [ ] Atualização concluída no ambiente de destino
- [ ] Versões do relatório e modelo semântico registradas
- [ ] Notas de versão e limitações conhecidas publicadas
- [ ] Plano de rollback disponível
- [ ] Aceite de negócio registrado

## Modelo de registro de incidente
- ID / data do incidente
- Severidade e impacto no negócio
- Relatório, conjunto de dados e período afetado
- Sintomas e detecção
- Causa-raiz
- Resolução e evidências de validação
- Responsável e comunicação
- Ação preventiva / história de acompanhamento
