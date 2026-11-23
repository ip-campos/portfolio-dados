# Predição de Churn com Machine Learning
## Sobre o projeto

Este projeto desenvolve e compara modelos de XGBoost e regressão linear para estimar taxas de juros a partir das características de financiamentos imobiliários.

O trabalho inclui limpeza dos dados, análise exploratória, pré-processamento em pipelines, otimização de hiperparâmetros e avaliação por validação cruzada e conjunto de teste.

O projeto também servirá como base para o desenvolvimento de uma aplicação end-to-end.

## Conjunto de dados

Foi analisado um conjunto de dados de solicitações e operações de financiamento imobiliário referentes a imóveis localizados na Carolina do Norte, Estados Unidos, em 2025. O conjunto foi coletado a partir da Home Mortgage Disclosure Act (HMDA) e disponibilizados publicamente na plataforma HMDA do FFIEC.

- **Fonte:** [HMDA](https://ffiec.cfpb.gov/)
- **Contexto:** Informações de solicitações e operações de financiamento imobiliário referentes a imóveis localizados na Carolina do Norte, Estados Unidos, em 2025 e a respectiva taxa de juros associada a essa operação.

**Descrição dos dados:** O conjunto de dados completo, os códigos das categorias e os valores especiais podem ser consultados no [dicionário oficial de dados da HMDA](https://ffiec.cfpb.gov/documentation/publications/loan-level-datasets/lar-data-fields).
| Variável | Descrição | Tipo / Unidade |
| :---: | :--- | :--- |
| `interest_rate` | Taxa de juros anual do financiamento. **Variável alvo do modelo.** | Numérica — % |
| `loan_amount` | Valor do financiamento. | Numérica — US$ |
| `income` | Renda bruta anual considerada na decisão de crédito. | Numérica — milhares de US$ |
| `property_value` | Valor do imóvel considerado na decisão de crédito. | Numérica — US$ |
| `loan_to_value_ratio` | Relação entre o total das dívidas garantidas pelo imóvel e seu valor (CLTV). | Numérica — % |
| `loan_term` | Prazo contratual do financiamento. | Numérica — meses |
| `loan_type` | Modalidade do financiamento: convencional ou com seguro/garantia governamental. | Categórica |
| `loan_purpose` | Finalidade do financiamento, como compra, reforma ou refinanciamento. | Categórica |
| `lien_status` | Prioridade da garantia hipotecária: primeiro grau ou subordinada. | Categórica |
| `occupancy_type` | Uso do imóvel: residência principal, segunda residência ou investimento. | Categórica |
| `construction_method` | Método de construção: no local ou habitação manufaturada. | Categórica |
| `total_units` | Quantidade de unidades residenciais, apresentada em valores individuais ou faixas. | Categórica ordinal |
| `conforming_loan_limit` | Enquadramento do valor financiado no limite para financiamentos conformes. | Categórica |
| `business_or_commercial_purpose` | Indica se a operação tem finalidade predominantemente empresarial ou comercial. | Categórica |
| `intro_rate_period` | Prazo até a primeira possibilidade de alteração da taxa de juros. | Numérica — meses |
| `balloon_payment` | Indica pagamento balão: parcela substancialmente maior que as demais. | Categórica |
| `interest_only_payment` | Indica a previsão contratual de pagamentos apenas de juros. | Categórica |
| `negative_amortization` | Indica possibilidade de aumento do saldo devedor pela incorporação de juros não pagos. | Categórica |
| `other_nonamortizing_features` | Indica outras condições contratuais que permitem pagamentos sem amortização integral. | Categórica |
| `prepayment_penalty_term` | Período de vigência da penalidade por pagamento antecipado. | Numérica — meses |
| `open-end_line_of_credit` | Indica se a operação é uma linha de crédito aberta (rotativa). | Categórica |
| `reverse_mortgage` | Indica se a operação é uma hipoteca reversa. | Categórica |
| `county_code` | Código FIPS de estado e condado do imóvel. | Categórica |
| `lei` | Identificador da instituição financeira (Legal Entity Identifier). | Categórica |

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost