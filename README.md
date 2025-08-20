# 📊 TelecomX 

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-orange?logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-green?logo=scikit-learn)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Plots-purple?logo=plotly)
![Colab](https://img.shields.io/badge/Google%20Colab-Notebooks-red?logo=googlecolab)

---

## 🎯 Objetivo

O projeto tem como objetivo **analisar e prever o churn de clientes** da TelecomX, aplicando um pipeline de **ETL, EDA e Modelagem Preditiva**.  
A empresa enfrenta alto índice de cancelamentos e busca entender os fatores que influenciam a evasão, antecipar clientes em risco e criar estratégias de retenção.

---

## 📘 Introdução

O **churn** é um dos maiores problemas em empresas de telecomunicações. Prever quais clientes têm maior probabilidade de cancelar permite **ações proativas de retenção**.  
Esse projeto aplica **Ciência de Dados e Machine Learning** para responder perguntas-chave:

- Quais clientes estão mais propensos a cancelar?  
- Quais fatores mais influenciam a evasão?  
- Como usar os dados para reduzir churn de forma estratégica?  

---

## 🔧 Desenvolvimento

### 1. 📥 ETL (Extract, Transform, Load)
- **Extração**: dados carregados da API em JSON.  
- **Transformação**:  
  - Tratamento de valores nulos e tipos.  
  - Conversão da variável `Churn` em binária.  
  - Criação de variáveis derivadas, como `avg_monthly_spend`.  
- **Carga**: dataset tratado salvo como `TelecomX_clean.csv`.  

---

### 2. 🔎 EDA (Exploração de Dados)
A análise exploratória revelou padrões importantes:  

**Distribuição de Churn**  
![Churn Distribution](assets/churn_dist.png)

**Churn por Tipo de Contrato**  
![Contrato vs Churn](assets/churn_contract.png)

**Mensalidade vs Churn (Boxplot)**  
![Mensalidade vs Churn](assets/churn_box.png)

**Churn por Método de Pagamento**  
![Pagamento vs Churn](assets/churn_payment.png)

**Principais insights:**  
- Contratos mensais → maior risco de churn.  
- Pagamento via **cheque eletrônico** → maior propensão à evasão.  
- Mensalidades altas e **tenure baixo (< 12 meses)** aumentam chance de cancelamento.  

---

### 3. 🤖 Modelagem Preditiva

#### Pré-processamento
- **OneHotEncoding** para variáveis categóricas.  
- **Normalização** para variáveis numéricas.  

#### Modelos testados
- **Regressão Logística** → baseline interpretável.  
- **Random Forest** → modelo mais robusto.  

#### Avaliação
- **Métricas**: AUC-ROC, Recall, F1-score.  
- **Visualizações**: Curva ROC, Matriz de Confusão, Importância de Variáveis.  

**Curvas ROC**  
![ROC Curves](assets/roc_curve.png)

**Importância das Variáveis (Random Forest)**  
![Feature Importance](assets/feature_importance.png)

---

## 📊 Resultados

| Modelo               | AUC-ROC | Recall | F1-score |
|----------------------|---------|--------|----------|
| Logistic Regression  | 0.82    | 0.68   | 0.64     |
| Random Forest        | 0.86    | 0.74   | 0.67     |

- **Random Forest** apresentou o melhor desempenho.  
- Variáveis-chave:  
  - **Tipo de contrato**  
  - **Método de pagamento**  
  - **Mensalidade**  
  - **Tenure (tempo de permanência)**  

---

## ✅ Conclusão

- O churn está fortemente associado a **contratos mensais** e **pagamento por cheque eletrônico**.  
- Clientes **novos e com mensalidades altas** são os mais propensos a cancelar.  
- O modelo preditivo permite identificar clientes em risco e agir proativamente.  

### Estratégias recomendadas
- Migrar clientes para **contratos anuais**.  
- Oferecer **descontos e benefícios** para novos clientes nos primeiros meses.  
- Incentivar **pagamentos automáticos** (cartão/crédito).  

---

## 📚 Teoria e Conceitos

- **ETL (Extract, Transform, Load)** → pipeline para preparar dados.  
- **EDA (Exploratory Data Analysis)** → explorar padrões e tendências.  
- **Churn Rate** → percentual de clientes que cancelam.  
- **Modelos de Classificação** → regressão logística e random forest.  
- **Métricas**:  
  - **AUC-ROC** (discriminação entre classes).  
  - **Recall** (prioridade: detectar clientes em risco).  
  - **F1-score** (equilíbrio entre precisão e recall).  

---

## 🛠️ Tecnologias Utilizadas

<p align="center">
  <img src="assets/tech_stack.png" width="500"/>
</p>

- **Python** → linguagem principal.  
- **Pandas & NumPy** → manipulação de dados.  
- **Plotly** → gráficos interativos.  
- **Scikit-Learn** → machine learning.  
- **Google Colab** → ambiente de execução.  

---

## 📌 Referências e Recomendações

### 📘 Documentação
- [Python](https://docs.python.org/3/)  
- [Pandas](https://pandas.pydata.org/docs/)  
- [NumPy](https://numpy.org/doc/stable/)  
- [Scikit-Learn](https://scikit-learn.org/stable/)  
- [Plotly](https://plotly.com/python/)  

### 📚 Cursos
- [Kaggle – Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning)  
- [Coursera – Machine Learning (Andrew Ng)](https://www.coursera.org/learn/machine-learning)  
- [DataCamp – Supervised Learning with scikit-learn](https://www.datacamp.com)  

### 💡 Boas práticas
- Versionamento com **Git/GitHub**.  
- Commits pequenos e descritivos.  
- Organização em pastas: `data/`, `notebooks/`, `src/`, `assets/`.  
- Documentação clara no `README.md`.  

---
