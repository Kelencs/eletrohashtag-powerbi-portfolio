# 06 — Modelo de Dados e Arquitetura

## 1. Objetivo
Documentar a estrutura necessária para interpretar o relatório e estabelecer os pontos que precisam ser confirmados no modelo semântico do Power BI.

## 2. Arquitetura funcional observável
O arquivo PBIX contém:
- relatório Power BI com páginas Capa, Geral, Análises e Devoluções;
- páginas Tooltip Devoluções e Tooltip Vendas;
- visuais nativos e visuais personalizados;
- medidas e campos utilizados pelos visuais;
- recursos de segmentação, parâmetro e interação.

A estrutura interna do arquivo permite identificar campos associados aos visuais, mas não substitui a inspeção completa das consultas Power Query, tabelas, relacionamentos e expressões DAX.

## 3. Dimensões e campos observados
Os campos identificados em visuais incluem:
- Marca;
- Tipo do Produto;
- Nome Produto;
- Tipo;
- Mês;
- Ano;
- País;
- Continente;
- Datas;
- Inicio do Mês;
- Parâmetro.

Esses nomes representam campos utilizados no relatório. Não devem ser tratados automaticamente como nomes de tabelas ou como prova de uma modelagem estrela.

## 4. Elementos analíticos
| Página | Campos/dimensões identificados |
|---|---|
| Geral | Ano, Mês, Tipo, Tipo do Produto, Continente, País |
| Análises | Marca, Tipo do Produto, Nome Produto, Parâmetro, País, Continente, Datas |
| Devoluções | Inicio do Mês, Continente, Marca, Tipo do Produto, Nome Produto, Ano |

## 5. Pontos a confirmar no Power BI Desktop
- Nome e finalidade de todas as tabelas.
- Identificação das tabelas fato e dimensão.
- Chaves primárias e estrangeiras.
- Cardinalidade e direção de filtro dos relacionamentos.
- Existência e configuração da tabela calendário.
- Marcação da tabela calendário como tabela de datas.
- Medidas DAX e colunas calculadas.
- Parâmetros de campo ou parâmetros What-if, conforme aplicável.
- Consultas, etapas de transformação e origem dos dados.
- Configuração de atualização e credenciais, quando aplicável.

## 6. Validação do modelo
Recomenda-se documentar um diagrama do modelo com:
- nome da tabela;
- granularidade;
- chave;
- relacionamentos;
- descrição das colunas relevantes;
- origem e transformação;
- regras de qualidade.

## 7. Limitação e transparência
Não declarar que o projeto utiliza arquitetura estrela, determinada tabela fato ou dimensão, nem nomes de tabelas como `fVendas`, `dProdutos` ou `dCalendario`, sem confirmação no Model view ou no modelo semântico. Essas estruturas podem ser boas práticas recomendadas, mas não devem ser apresentadas como fatos sem evidência.

