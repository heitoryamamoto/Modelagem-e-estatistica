📘 Projeto – Modelagem Estatística & Machine Learning (2º Bimestre)
Análise, Modelagem e Predição de Ratings de Séries Web

Este projeto tem como objetivo aplicar técnicas de Estatística, EDA e Modelagem Preditiva para entender e prever o rating de séries a partir de variáveis como popularidade, votos, gênero, idioma, ano e mês de estreia.

O trabalho segue rigorosamente os itens solicitados na lauda oficial da disciplina, incluindo:
EDA completo, testes estatísticos, regressão, classificação, tuning de modelos e diagnóstico de resíduos.

🗂 Conteúdo do Projeto

O notebook inclui:

1. Introdução

Motivação

Objetivo do projeto

Hipóteses analisadas

Fonte e licença do dataset

2. EDA – Análise Exploratória dos Dados

Foram realizadas:

Tratamento de dados ausentes

Histogramas e boxplots

Correlação entre variáveis

Distribuições temporais (ano e mês de estreia)

Teste ANOVA para verificar se o rating difere entre gêneros

Insights explicativos após cada visualização

Inclui também testes estatísticos exigidos na lauda:

Jarque-Bera (normalidade dos resíduos)

ANOVA F-test (diferenças entre grupos)

3. Modelagem – Regressão

Modelos explorados:

Regressão Linear Simples

Regressão Linear Múltipla (via statsmodels)

Regressão Polinomial

Métricas: MAE, RMSE, R²

Foi realizado também:

Diagnóstico de resíduos

Histograma + QQ-Plot

Homocedasticidade (Breusch–Pagan + gráfico resíduos vs fitted)

Multicolinearidade via VIF

Conclusão: modelos lineares não capturam bem a variação do rating devido ao baixo desvio no target.

4. Modelagem – Classificação

Conversão do rating em faixas:

Baixo, Médio e Alto

Modelos usados:

Naive Bayes

Regressão Logística

Inclui:

Classification Report

Matriz de Confusão

Acurácia, Precisão, Recall, F1-Score

Resultados:
A Regressão Logística apresentou o melhor desempenho (≈95% de acurácia).

5. Tuning dos Modelos & AutoML (PyCaret)

Foi utilizado o PyCaret para:

Comparação automática de modelos de Regressão

Tuning do modelo campeão (CatBoost Regressor)

Validação cruzada (k-fold = 10)

Conclusão:
O CatBoost obteve o menor erro e melhor estabilidade.

6. Conclusões Gerais do Projeto

Popularidade e votos têm correlação moderada com o rating.

O rating possui variação muito baixa, o que limita desempenho de modelos de regressão.

Modelos lineares não foram suficientes para explicar o comportamento do rating.

Para classificação, o desempenho foi excelente, especialmente com Regressão Logística.

Modelos avançados como CatBoost se destacaram na regressão, mas ainda limitados pelo baixo desvio do target.

📁 Dataset

Fonte: Kaggle

Licença: Creative Commons CC BY-NC-SA 4.0

O dataset contém 2000 séries com variáveis numéricas e categóricas.

🛠️ Tecnologias Utilizadas

Python 3.10

Pandas

Seaborn / Matplotlib

Scikit-Learn

Statsmodels

PyCaret

SciPy

📌 Como executar o projeto
Google Colab (recomendado)

Abra o notebook e execute:

pip install pycaret[full]


Em seguida, rode todas as células em ordem.

🧠 Próximos Passos (Limitações e Melhorias)

Incluir variáveis textuais (ex: descrição da série) usando embeddings.

Testar modelos de deep learning.

Criar modelos de recomendação baseados em similaridade.

Aumentar o número de features para enriquecer o poder preditivo.

✒️ Autores

Heitor Yamamoto e Gustavo Nishimura
