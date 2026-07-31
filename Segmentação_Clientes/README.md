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
|---|---|
| `Invoice` | Código de identificação da transação. Códigos iniciados por `C` representam cancelamentos. |
| `StockCode` | Código de identificação do produto. |
| `Description` | Descrição do produto. |
| `Quantity` | Quantidade de itens adquiridos na transação. |
| `InvoiceDate` | Data e horário da transação. |
| `Price` | Preço unitário do produto. |
| `Customer ID` | Código de identificação do cliente. |
| `Country` | País de residência do cliente. |

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
