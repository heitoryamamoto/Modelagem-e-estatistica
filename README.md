# 📘 Projeto – Modelagem Estatística & Machine Learning (2º Bimestre)
## **Análise, Modelagem e Predição de Ratings de Séries Web**

Este projeto tem como objetivo aplicar técnicas de Estatística, EDA e Modelagem Preditiva para entender e prever o **rating de séries** a partir de variáveis como popularidade, votos, gênero, idioma, ano e mês de estreia.

O trabalho segue rigorosamente os itens solicitados na **lauda oficial da disciplina**, incluindo:
- EDA completo  
- Testes estatísticos  
- Regressão  
- Classificação  
- Tuning de modelos  
- Diagnóstico de resíduos  

---

# 🗂 Conteúdo do Projeto

## **1. Introdução**
Inclui:
- Motivação  
- Objetivo do projeto  
- Hipóteses analisadas  
- Fonte e licença do dataset  

---

## **2. EDA – Análise Exploratória dos Dados**

Foram realizadas:
- Tratamento de dados ausentes  
- Histogramas e boxplots  
- Correlação entre variáveis  
- Distribuições temporais (ano e mês de estreia)  
- Teste **ANOVA** para verificar se o rating difere entre gêneros  
- Insights explicativos após cada visualização  

Testes estatísticos exigidos na lauda:
- **Jarque-Bera** (normalidade dos resíduos)  
- **ANOVA F-test** (diferenças entre grupos)  

---

## **3. Modelagem – Regressão**

Modelos explorados:
- Regressão Linear Simples  
- Regressão Linear Múltipla (via *statsmodels*)  
- Regressão Polinomial  

Métricas avaliadas:
- **MAE**  
- **RMSE**  
- **R²**  

### Diagnóstico de Resíduos
- Histograma + QQ-Plot  
- Homocedasticidade (Breusch–Pagan + gráfico de resíduos vs fitted)  
- Multicolinearidade via **VIF**  

> **Conclusão:** modelos lineares não capturam bem a variação do rating devido ao baixo desvio do target.

---

## **4. Modelagem – Classificação**

Conversão do rating em faixas:
- **Baixo**
- **Médio**
- **Alto**

Modelos utilizados:
- **Naive Bayes**  
- **Regressão Logística**

Inclui:
- Classification Report  
- Matriz de Confusão  
- Acurácia, Precisão, Recall e F1-Score  

> **Resultado:** Regressão Logística apresentou o melhor desempenho, com aproximadamente **95% de acurácia**.

---

## **5. Tuning dos Modelos & AutoML (PyCaret)**

O PyCaret foi usado para:
- Comparação automática de modelos de Regressão  
- Tuning do melhor modelo (**CatBoost Regressor**)  
- Validação cruzada k-fold (k = 10)  

> **Conclusão:** CatBoost obteve o menor erro e maior estabilidade entre os modelos testados.

---

## **6. Conclusões Gerais do Projeto**

- Popularidade e número de votos têm correlação moderada com o rating.  
- O rating possui variação muito baixa, limitando o desempenho de modelos de regressão.  
- Modelos lineares não explicam bem o comportamento do rating.  
- Modelos de **classificação** tiveram ótimo desempenho, especialmente a Regressão Logística.  
- Modelos avançados como **CatBoost** se destacaram, mas ainda limitados pela baixa variabilidade do target.  

---

# 📁 Dataset

- **Fonte:** Kaggle  
- **Licença:** Creative Commons CC BY-NC-SA 4.0  
- O dataset contém **2000 séries** com variáveis numéricas e categóricas.

---

# 🛠️ Tecnologias Utilizadas

- Python 3.10  
- Pandas  
- Seaborn / Matplotlib  
- Scikit-Learn  
- Statsmodels  
- PyCaret  
- SciPy  

---

# 📌 Como executar o projeto

### **Google Colab (recomendado)**

Execute:

```bash
pip install pycaret[full]
