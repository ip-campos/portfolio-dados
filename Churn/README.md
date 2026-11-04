# Predição de Churn com Machine Learning
## Sobre o projeto

Este projeto apresenta uma comparação entre modelos de Machine Learning para predição de churn de clientes de um banco. Os modelos escolhidos foram:
- **Random Forest**;
- **Regressão Logística**;
- **XGBoost**.

Eles serão comparados entre si em métricas como acurácia, recall e precisão. Além disso, é proposto um modelo simplificado de perda de receita para comparar a eficiência financeira da implementação do modelo.

## Conjunto de dados

Foi utilizado o conjunto de dados Churn Modelling, disponibilizado gratuitamente na plataforma Kaggle.

- **Fonte:** [Churn Modelling](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling/data)
- **Contexto:** Detalhes do clientes de um banco e uma variável binária que indica se o cliente fechou sua conta com o banco ou não.

**Descrição dos dados:**

| Variável | Descrição |
| :------: | :-------: |
| Customer ID | Número de identificação único do cliente |
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
| Exited | Indicador binário se o cliente terminou sua conta ou não |

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
