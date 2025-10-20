# Pipeline de Classificação - Análise de Crédito Alemão

Este projeto demonstra a implementação de diferentes tipos de pipelines de machine learning usando o scikit-learn para análise de dados de crédito alemão.

## Descrição do Projeto

O projeto utiliza o conjunto de dados German Credit Data para demonstrar diferentes abordagens de criação de pipelines de machine learning, incluindo:

1. Pipeline Básico
2. Make Pipeline
3. Column Transformer
4. Pipeline com Múltiplos Classificadores

## Estrutura do Projeto

- `pipeline_tutorial.ipynb`: Notebook Jupyter principal com todo o código e explicações
- `german_credit_data.csv`: Dataset de crédito alemão
- `.gitignore`: Configurações de arquivos ignorados pelo Git

## Funcionalidades Implementadas

- Pré-processamento de dados com StandardScaler e SimpleImputer
- Transformação de variáveis categóricas com OneHotEncoder
- Implementação de diferentes tipos de pipelines
- Avaliação de múltiplos classificadores, incluindo:
  - KNeighbors
  - SVM
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - AdaBoost
  - Gradient Boosting
  - XGBoost

## Requisitos

- Python 3.x
- pandas
- scikit-learn
- numpy
- xgboost

## Como Usar

1. Clone o repositório
2. Instale as dependências necessárias
3. Execute o notebook `pipeline_tutorial.ipynb`

## Estrutura dos Pipelines

O projeto demonstra diferentes abordagens de pipeline:

```python
# Pipeline Básico
pipe = Pipeline([
    ('scaler', StandardScaler()),
    ('imputer', SimpleImputer()),
    ('clf', DecisionTreeClassifier())
])

# Make Pipeline
make_pipe = make_pipeline(
    MinMaxScaler(),
    SimpleImputer(),
    LogisticRegression()
)

# Column Transformer
preprocessor = ColumnTransformer(transformers=[
    ('num_continuas', StandardScaler(), numericas_continuas),
    ('str_categoricas', OneHotEncoder(), string_categoricas)
])
```