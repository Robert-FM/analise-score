# ANALISE-SCORE

Sistema de **Credit Scoring** desenvolvido em Python para previsão de risco de inadimplência utilizando técnicas de Machine Learning. O projeto realiza treinamento de modelos, avaliação de métricas e disponibiliza uma interface web interativa com Streamlit para simulação de risco de crédito.

---

## 📌 Objetivo

O objetivo deste projeto é prever a probabilidade de inadimplência de clientes com base em características financeiras e cadastrais, auxiliando processos de análise de crédito.

---

## 🚀 Tecnologias Utilizadas

- Python 3.14
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Joblib
- UV (gerenciador de ambientes e dependências)

---

## 📂 Estrutura do Projeto

```bash
ANALISE-SCORE/
│
├── app/
│   └── app.py
│
├── data/
│   └── credit_risk_dataset.csv
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

## 📊 Funcionalidades

- Treinamento automático de múltiplos modelos:
  - Logistic Regression
  - Random Forest
  - Gradient Boosting
- Seleção automática do melhor modelo via ROC-AUC
- Geração de relatórios de métricas
- Salvamento do modelo treinado
- Interface web interativa para simulação de risco
- Pipeline completo de pré-processamento

---

## ⚙️ Pré-processamento

O pipeline inclui:

- Tratamento de valores ausentes
- Normalização de variáveis numéricas
- Codificação One-Hot para variáveis categóricas
- Separação treino/teste estratificada

---

## 📈 Métricas Avaliadas

O projeto calcula automaticamente:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de confusão
- Classification Report

---

## 🧠 Modelos Utilizados

### Logistic Regression

Modelo linear simples e interpretável.

### Random Forest

Modelo baseado em árvores de decisão com ensemble.

### Gradient Boosting

Modelo de boosting para melhoria incremental do desempenho.

---

## 🔧 Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/Robert-FM/analise-score.git
cd analise-score
```

---

## 📦 Ambiente com UV

### Instalar o UV

#### Linux/Mac

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Windows (PowerShell)

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

---

### Criar ambiente virtual

```bash
uv venv
```

---

### Ativar ambiente

#### Linux/Mac

```bash
source .venv/bin/activate
```

#### Windows

```powershell
.venv\Scripts\activate
```

---

### Instalar dependências

```bash
uv sync
```

ou

```bash
uv pip install -r requirements.txt
```

---

## ▶️ Treinar os Modelos

```bash
python src/train_model.py
```

O treinamento irá:

- Comparar os modelos
- Selecionar o melhor
- Salvar o modelo em:

```bash
models/credit_scoring_model.joblib
```

Também serão gerados relatórios em:

```bash
reports/
```

---

## 🌐 Executar a Interface Web

```bash
streamlit run app/app.py
```

A aplicação abrirá automaticamente no navegador.

---

## 🖥️ Interface da Aplicação

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
  - Risco moderado
  - Alto risco

---

## 📌 Dataset

O projeto utiliza um dataset de risco de crédito contendo informações financeiras e comportamentais dos clientes.

### Variável alvo

```python
loan_status
```

---

## 📄 Arquivos Importantes

### `app/app.py`

Arquivo responsável pela interface web utilizando Streamlit.

### `src/train_model.py`

Pipeline completo de treinamento, avaliação e persistência do modelo.

---

## 📚 Melhorias Futuras

- Deploy em nuvem (Render, Railway ou AWS)
- Explicabilidade com SHAP/LIME
- API REST com FastAPI
- Dashboard analítico
- Monitoramento de drift
- Balanceamento de classes avançado

---

## 👨‍💻 Autor

**Robert Fernandes de Melo**

- Física | Machine Learning | Data Science
- Python • IA • Visão Computacional • Django

---

## 📜 Licença

Este projeto é destinado para fins educacionais e de portfólio.