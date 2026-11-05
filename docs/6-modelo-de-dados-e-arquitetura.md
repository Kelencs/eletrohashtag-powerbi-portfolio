# 6. Modelo de Dados e Arquitetura

## Modelo identificado no material do projeto
- Tabelas fato: `fVendas`, `fDevoluções`
- Dimensões: `dProdutos`, `dLojas`, `dCalendario`
- Tabela dedicada às medidas DAX

O PDF não permite confirmar chaves, cardinalidades, direção dos relacionamentos ou linhagem dos sistemas de origem.

## Princípios recomendados de modelagem
- Utilizar esquema estrela: dimensões filtram fatos.
- Preferir relacionamentos 1:N e filtro unidirecional, salvo necessidade documentada.
- Definir e documentar a granularidade de cada tabela fato.
- Validar chaves substitutas/de negócio e integridade referencial.
- Utilizar dimensão calendário contínua, com datas únicas e atributos de ano/mês/trimestre; marcá-la como tabela de datas.
- Evitar muitos-para-muitos e filtros bidirecionais ambíguos sem justificativa.
- Centralizar medidas e organizá-las em pastas de exibição.
- Preferir medidas explícitas e convenções consistentes de nomes e formatos.

## Questões a resolver
1. Qual é a granularidade das fatos de vendas e devoluções?
2. As devoluções estão vinculadas às transações de venda originais?
3. Preço e custo são snapshots históricos ou atributos atuais do produto?
4. Quais são os sistemas de origem oficiais e as etapas de ingestão?
5. O calendário é fiscal ou gregoriano?
6. Existem múltiplas moedas ou questões de fuso horário?
7. As dimensões mudam lentamente e como o histórico é preservado?
