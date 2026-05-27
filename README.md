# ANALISE-SCORE

Sistema de **Credit Scoring com Machine Learning** para previsão de risco de inadimplência, desenvolvido em Python.

O projeto realiza:

- Pré-processamento de dados
- Análise estatística exploratória
- Treinamento e comparação de modelos
- Avaliação automática de métricas
- Persistência do melhor modelo
- Simulação interativa via Streamlit

---

# 🚀 Objetivo

O objetivo deste projeto é prever a probabilidade de inadimplência de clientes com base em características financeiras e cadastrais.

O sistema utiliza técnicas de Machine Learning para auxiliar processos de análise de crédito e tomada de decisão.

---

# 🛠️ Tecnologias Utilizadas

## Linguagem

- Python

## Bibliotecas

- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Joblib

## Ambiente e Dependências

- UV
- Virtual Environment (venv)

---

# 📂 Estrutura do Projeto

```bash
ANALISE-SCORE/
│
├── .venv/
│
├── analise-estatistica/
│   └── analise-dados.ipynb      # Análise exploratória e estatística
│
├── app/
│   └── app.py                   # Interface Streamlit
│
├── data/
│   ├── 01-raw/
│   │   └── credit_risk_dataset.csv
│   │
│   └── 02-processed/
│       └── credit_risk_processed.csv
│
├── models/
│   └── credit_scoring_model.joblib
│
├── reports/
│   ├── metrics_full.json
│   └── metrics_summary.csv
│
├── src/
│   └── train_model.py
│
├── .gitignore
├── .python-version
├── main.py
├── pyproject.toml
├── README.md
└── uv.lock
```

---

# 📊 Funcionalidades

✅ Treinamento automático de múltiplos modelos  
✅ Comparação automática de desempenho  
✅ Pipeline completo de pré-processamento  
✅ Geração automática de métricas  
✅ Persistência do melhor modelo  
✅ Interface web interativa com Streamlit  
✅ Análise estatística exploratória  

---

# ⚙️ Pipeline de Machine Learning

O pipeline inclui:

- Tratamento de valores ausentes
- Normalização de variáveis numéricas
- One-Hot Encoding para variáveis categóricas
- Separação treino/teste estratificada
- Comparação automática entre modelos
- Seleção do melhor modelo via ROC-AUC
- Exportação do modelo treinado

---

# 🤖 Modelos Avaliados

| Modelo | Descrição |
|---|---|
| Logistic Regression | Modelo linear interpretável |
| Random Forest | Ensemble baseado em árvores |
| Gradient Boosting | Boosting incremental para melhor performance |

---

# 📈 Métricas Avaliadas

O projeto calcula automaticamente:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de confusão
- Classification Report

---

# 📦 Instalação

## 1. Clonar o repositório

```bash
git clone https://github.com/Robert-FM/analise-score.git
cd analise-score
```

---

# 🔧 Configuração do Ambiente

## Instalar o UV

### Linux/Mac

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Windows (PowerShell)

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

---

## Criar ambiente virtual

```bash
uv venv
```

---

## Ativar ambiente virtual

### Linux/Mac

```bash
source .venv/bin/activate
```

### Windows

```powershell
.venv\Scripts\activate
```

---

## Instalar dependências

```bash
uv sync
```

---

# ▶️ Treinando os Modelos

```bash
python src/train_model.py
```

O treinamento irá:

- Comparar os modelos
- Selecionar automaticamente o melhor
- Salvar o modelo treinado
- Gerar relatórios de desempenho

---

# 🌐 Executando a Aplicação Web

```bash
streamlit run app/app.py
```

A aplicação abrirá automaticamente no navegador.

---

# 🖥️ Interface da Aplicação

A aplicação permite inserir informações como:

- Idade
- Renda anual
- Tipo de moradia
- Tempo de emprego
- Finalidade do empréstimo
- Taxa de juros
- Histórico de crédito

E retorna:

- Probabilidade estimada de inadimplência
- Classificação do risco:
  - Baixo risco
  - Médio risco
  - Alto risco

---

# 📌 Dataset

O projeto utiliza um dataset de risco de crédito contendo informações financeiras e comportamentais dos clientes.

## Variável alvo

```python
loan_status
```

---

# 📊 Análise Exploratória

A pasta `analise-estatistica/` contém notebooks utilizados para:

- Exploração dos dados
- Análise estatística
- Identificação de padrões
- Distribuição das variáveis
- Correlação entre atributos
- Avaliação inicial da inadimplência

---

# 📈 Melhorias Futuras

- Deploy em nuvem (AWS, Render ou Railway)
- API REST com FastAPI
- Explicabilidade com SHAP/LIME
- Monitoramento de drift
- Balanceamento de classes avançado
- MLflow para rastreamento de experimentos
- Dockerização da aplicação

---

# 👨‍💻 Autor

## Robert Fernandes de Melo

- Física
- Machine Learning
- Data Science
- Visão Computacional
- Desenvolvimento Python

---

# 📜 Licença

Este projeto foi desenvolvido para fins educacionais, estudos em Machine Learning e composição de portfólio profissional.