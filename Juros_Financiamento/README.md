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
| :------: | :-------: |
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

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

| Variável | Significado | Tratamento sugerido |
|---|---|---|
| **`interest_rate`** | Taxa de juros anual | **Alvo**, em percentual |
| `loan_amount` | Valor do financiamento | Numérica, em USD |
| `income` | Renda bruta anual considerada na análise | Numérica, em **milhares de USD** |
| `property_value` | Valor do imóvel utilizado na decisão | Numérica, em USD |
| `loan_to_value_ratio` | Relação entre dívidas garantidas pelo imóvel e seu valor | Numérica, em percentual |
| `loan_term` | Prazo do financiamento | Numérica, em meses |
| `loan_type` | Tipo de financiamento/garantia governamental | Categórica |
| `loan_purpose` | Compra, reforma, refinanciamento etc. | Categórica |
| `lien_status` | Prioridade da garantia hipotecária | Categórica |
| `occupancy_type` | Residência principal, segunda residência ou investimento | Categórica |
| `construction_method` | Construção no local ou habitação manufaturada | Categórica |
| `total_units` | Número de unidades residenciais | Categórica, pois também contém faixas |
| `conforming_loan_limit` | Enquadramento no limite de valor aplicável às GSEs | Categórica |

| Campos ou grupos | Minha recomendação inicial |
|---|---|
| `county_code`, `lei` e variáveis econômicas da região | Testar posteriormente, verificando o ganho em validação |
| `activity_year` | Guardar para separar períodos e avaliar estabilidade temporal |
| `action_taken` | Usar para selecionar contratos concedidos; retirar de `X` após o filtro |
| `rate_spread`, `hoepa_status` | Excluir: podem revelar condições de preço ligadas ao alvo |
| `discount_points`, `lender_credits`, custos e encargos | Excluir da primeira versão: são negociados junto com as condições de preço |
| `purchaser_type`, `denial_reason-*` | Excluir: informações posteriores à etapa em que queremos prever |
| Raça, etnia, sexo e idade | Reservar para comparar cobertura e erros entre grupos |
| `derived_loan_product_type`, `derived_dwelling_category` | Evitar duplicação com os campos que originaram essas categorias |
