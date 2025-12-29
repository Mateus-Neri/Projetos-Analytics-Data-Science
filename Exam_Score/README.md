# 📊 Student Exam Score Prediction

Este projeto tem como objetivo **analisar fatores que influenciam o desempenho acadêmico** de estudantes e **construir um modelo de regressão** capaz de prever a nota final (`exam_score`) com base em variáveis comportamentais, educacionais e contextuais.

O foco está tanto na **análise exploratória** quanto na **qualidade do modelo preditivo**, utilizando boas práticas de ciência de dados.

---

## 🎯 Objetivo do Projeto

- Identificar **quais variáveis realmente impactam o desempenho dos alunos**
- Avaliar relações lineares entre presença, horas de estudo e nota
- Construir e avaliar um **modelo de regressão** para prever a nota final
- Aplicar **seleção de features baseada em estatística**
- Comparar métricas de erro para validar a qualidade do modelo

---

## 🧠 Perguntas Respondidas

- Alunos que **frequentam mais aulas tiram notas maiores?**
- **Horas de estudo** são mais importantes que o tipo de curso?
- Variáveis demográficas como **gênero e curso** influenciam o desempenho?
- Qual é o **erro médio real** do modelo ao prever notas?

---

## 🗂️ Dataset

O dataset contém informações como:

- `age`
- `study_hours`
- `class_attendance`
- `sleep_hours`
- `sleep_quality`
- `study_method`
- `facility_rating`
- `exam_difficulty`
- `exam_score` (variável alvo)

📌 Dataset usado apenas para fins educacionais.

---

## ⚙️ Metodologia

### 🔹 Pré-processamento
- Tratamento de variáveis categóricas:
  - Binárias → mapeamento `0 / 1`
  - Baixa cardinalidade → One-Hot Encoding
  - Ordinais → Ordinal Encoding
- Remoção de variáveis irrelevantes com base em estatística

---

### 🔹 Seleção de Features
Foram utilizados dois critérios:

- **p-values (significância estatística)**
- **F-score (ANOVA – `f_regression`)**

Variáveis como `gender` e `course` foram removidas por não apresentarem relação estatisticamente relevante com o target.

---

### 🔹 Modelo
- **XGBRegressor**
- Ajuste de hiperparâmetros com `GridSearchCV`
- Avaliação em conjunto de teste

---

## 📈 Métricas de Avaliação

| Métrica | Resultado |
|------|----------|
| MAE | **8.64** |
| MSE | **115.38** |
| RMSE | **≈ 10.7** |
| R² | **≈ 0.67** |

### Interpretação
- O modelo erra, em média, **~9 pontos** na nota final
- Explica cerca de **67% da variância** das notas
- Performance consistente para um problema educacional realista

---

## 📊 Visualizações

- Relação entre presença em aula e nota
- Comparação entre valores reais e previstos
- Importância estatística das variáveis
- Distribuição das notas por método de estudo

---

## 🧪 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Seaborn / Matplotlib
- Scikit-learn
- XGBoost

---

## 📁 Estrutura do Repositório
