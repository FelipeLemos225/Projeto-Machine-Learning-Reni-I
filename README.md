# Projeto Individual (PI1) – Aprendizado de Máquina Supervisionado

Este projeto apresenta a aplicação de duas técnicas de aprendizado de máquina supervisionado:
- **Regressão Linear**  
- **Regressão Logística**

O objetivo é demonstrar a construção completa de experimentos em Machine Learning, desde a etapa de ETL até a avaliação e interpretação dos resultados obtidos pelos modelos.

---

## 📂 Estrutura do Projeto

Projeto Reni I/
├── data/ # Dados (vazio – dataset carregado do sklearn)
├── figures/ # Gráficos gerados pelos notebooks
├── models/ # Modelos treinados salvos em .pkl
├── notebooks/
│ ├── 01_regressao_linear_california.ipynb
│ └── 02_logistica_cancer_mama.ipynb
├── src/ # Scripts auxiliares (se necessário)
├── requirements.txt
├── .gitignore
└── README.md

## 🧠 Regressão Linear – *California Housing*

Modelo utilizado para prever o valor mediano de casas em diferentes distritos da Califórnia.

### 🔎 **Métricas obtidas no conjunto de teste**
- **MAE:** 0.533  
- **RMSE:** 0.746  
- **R²:** 0.576  

O modelo explica cerca de **57,6% da variabilidade** do valor das casas. Os erros médios (MAE e RMSE) permanecem em valores coerentes para um modelo linear simples, considerando as múltiplas variáveis socioeconômicas presentes no dataset.

### 🔄 **Validação Cruzada (5 folds)**
- **R² médio:** 0.601  
- **Desvio padrão:** 0.017  

Esses números indicam que o modelo apresenta boa estabilidade e não sofre de overfitting significativo.

### 📊 **Gráficos gerados**
- Distribuição de variáveis (histogramas)  
- Matriz de correlação  
- Gráfico Real vs Previsto  
- Distribuição dos resíduos  

Todos os gráficos estão disponíveis na pasta `figures/`.

---

## 🧬 Regressão Logística – *Breast Cancer Wisconsin*  
A Regressão Logística foi utilizada para classificar tumores como **malignos** ou **benignos**, utilizando variáveis morfológicas do conjunto de dados.

### 🔎 **Métricas no conjunto de teste**
- **Acurácia:** 0.982  
- **Precisão:** 0.986  
- **Revocação:** 0.986  
- **F1-Score:** 0.986  
- **AUC-ROC:** 0.995  

Os resultados indicam **excelente desempenho**, com baixíssimas taxas de erros.  
A alta precisão e revocação tornam o modelo especialmente adequado para cenários de saúde, onde falsos negativos são críticos.

### 🔄 **Validação Cruzada (5 folds)**
- **AUC-ROC médio:** 0.995  
- **Desvio padrão:** 0.005  

A consistência entre os folds confirma um comportamento estável e generalizável.

### 📊 **Gráficos gerados**
- Matriz de confusão  
- Curva ROC  

Ambos disponíveis na pasta `figures/`.


---

## 🚀 Como executar o projeto

### 1. Ativar o ambiente virtual

```bash
.venv\Scripts\Activate.ps1

### 2. Abrir os notebooks

jupyter notebook

🛠 Tecnologias utilizadas

Python 3

NumPy

Pandas

Scikit-learn

Matplotlib

Seaborn

Jupyter Notebook

📝 Observações

Os datasets utilizados são carregados diretamente da biblioteca sklearn.datasets, eliminando a necessidade de arquivos externos.
Os modelos são salvos no diretório models/ para reuso ou deploy futuro.