# Segmentação de Clientes com K-Means

## Sobre o projeto

Este projeto apresenta uma análise de segmentação de clientes de uma empresa de varejo online utilizando o algoritmo K-Means.

A análise foi desenvolvida a partir do modelo RFM, considerando três características do comportamento de compra:

- **Recência:** tempo desde a última compra do cliente;
- **Frequência:** número de compras realizadas;
- **Valor monetário:** valor total gasto pelo cliente.

## Conjunto de dados

Foi utilizado o conjunto de dados Online Retail II, disponibilizado pela UCI Machine Learning Repository.

- **Fonte:** [Online Retail II](https://doi.org/10.24432/C5CG6D)
- **Período dos dados:** dezembro de 2009 a dezembro de 2011
- **Contexto:** transações de uma empresa de varejo online sediada no Reino Unido, especializada na venda de artigos para presentes. Parte dos clientes também atua como revendedora.

## Descrição dos dados

| Variável | Descrição |
| :---: | :--- |
| `Invoice` | Código de identificação da transação. Códigos iniciados por `C` representam cancelamentos. |
| `StockCode` | Código de identificação do produto. |
| `Description` | Descrição do produto. |
| `Quantity` | Quantidade de itens adquiridos na transação. |
| `InvoiceDate` | Data e horário da transação. |
| `Price` | Preço unitário do produto. |
| `Customer ID` | Código de identificação do cliente. |
| `Country` | País de residência do cliente. |

## Resultados

A análise utilizou indicadores RFM — recência, frequência e valor monetário — de 5.868 clientes. O K-Means agrupou 5.178 clientes em quatro clusters. Outros 690 clientes, com valores extremos de gasto ou frequência, foram organizados em três grupos adicionais por regras.

| Segmento | Número de clientes |
| :------: | :----------------: |
| Baixo engajamento | 1.888 |
| Leais | 534 |
| Alto potencial |1.071 |
| Inativos | 1.685 |
| Grandes compradores | 265 |
| Superfrequentes | 64 |
| Campeões | 361 |

Os perfis identificados permitiram propor ações específicas de retenção, reativação, incentivo à recompra e atendimento personalizado. A separação dos clientes com valores extremos preservou sua análise sem influenciar diretamente a formação dos quatro clusters.

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
