# Detecção de Fraudes em Cartão de Crédito

Este projeto contém experimentos de detecção de fraude em transações de cartão de crédito usando três abordagens:

- Regressão Logística
- Autoencoder
- XGBoost

Os notebooks estão na pasta `notebooks/` e os resultados gerados estão na pasta `results/`.

## Fonte dos Dados

O dataset usado é o **Credit Card Fraud Detection Dataset 2023**, disponível no Kaggle:

```text
https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023
```

Arquivo esperado:

```text
creditcard_2023.csv
```

O arquivo CSV não está versionado no Git porque tem aproximadamente 325 MB.

## Configuração dos Dados

Após baixar o dataset no Kaggle, crie a pasta `data/` na raiz do projeto e coloque o CSV nela:

```powershell
mkdir data
```

O caminho final deve ser:

```text
data/creditcard_2023.csv
```

Os notebooks foram configurados para funcionar tanto quando executados pela raiz do projeto no VS Code quanto diretamente pela pasta `notebooks/`.

## Ambiente

Crie e ative um ambiente virtual Python:

```powershell
python -m venv .venv
.\.venv\Scripts\activate
```

Instale as dependências:

```powershell
pip install -r requirements.txt
```

## Execução

Execute os notebooks nesta ordem:

```text
notebooks/projeto_tcc_credit_card_fraud_1_supervised.ipynb
notebooks/projeto_tcc_credit_card_fraud_2_unsupervised.ipynb
notebooks/projeto_tcc_credit_card_fraud_3_xgboost.ipynb
```

Os resultados são salvos automaticamente em `results/`, incluindo métricas em CSV e gráficos em PNG.

## Resultados Gerados

Os principais arquivos de saída são:

```text
results/logistic_regression_metrics.csv
results/autoencoder_metrics.csv
results/xgboost_metrics.csv
results/model_comparison.csv
results/model_comparison_metrics.png
```

O arquivo `results/model_comparison.csv` consolida a comparação final entre os modelos.
