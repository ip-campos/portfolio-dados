# Predição de Churn com Machine Learning
## Sobre o projeto

Este projeto apresenta uma comparação entre modelos de Machine Learning para predição de churn de clientes de um banco. Os modelos escolhidos foram:
- **Random Forest**;
- **Regressão Logística**;
- **XGBoost**.

Os modelos foram comparados entre si em métricas como acurácia, recall e precisão. Além disso, é proposto um modelo simplificado de perda de receita para comparar a economia de receita da implementação do modelo no cenário simulado.

## Conjunto de dados

Foi utilizado o conjunto de dados Churn Modelling, disponibilizado gratuitamente na plataforma Kaggle.

- **Fonte:** [Churn Modelling](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling/data)
- **Contexto:** Informações dos clientes de um banco e uma variável binária que indica se o cliente fechou sua conta com o banco ou não.

**Descrição dos dados:**

| Variável | Descrição |
| :------: | :------- |
| CustomerId | Número de identificação único do cliente |
| Surname | Sobrenome do cliente |
| CreditScore | Pontuação de crédito do cliente |
| Geography | País de origem do cliente |
| Gender | Gênero do cliente |
| Age | Idade do cliente |
| Tenure | Número de anos que o cliente utiliza os serviços do banco |
| Balance | Saldo total da conta do cliente |
| NumOfProducts | Número de produtos do banco que o cliente utiliza |
| HasCrCard | Indicador binário se o cliente tem cartão de crédito no banco ou não |
| IsActiveMember | Indicador binário se o cliente é um membro ativo do banco ou não |
| EstimatedSalary | Salário estimado do cliente |
| Exited | Indicador binário se o cliente encerrou sua conta ou não |

## Resultados

Os modelos foram avaliados em um conjunto de teste com 2.000 clientes, considerando o desempenho preditivo e uma simulação de economia com ações de retenção.

| Métrica | Random Forest | Regressão logística | XGBoost |
| :-----: | :-----------: | :-----------------: | :-----: |
| Acurácia | 80,4% | 71,5% | 78,8% |
| Recall da classe churn | 74,4% | 70,5% | 77,9% |
| AUC | 0,86 | 0,78 | 0,86 |
| Economia simulada por cliente | R$ 9,24 | R$ 6,98 | R$ 9,34 |

O XGBoost apresentou o maior recall e a maior economia simulada, com resultados próximos aos do Random Forest, que obteve maior acurácia.

A simulação considera perda mensal de R$ 100 por cliente que sai, desconto de 20% para os clientes sinalizados e retenção de todos os que receberem a oferta. Os valores representam um cenário hipotético, sem validação do impacto em uma campanha real.

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
