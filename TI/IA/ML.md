---
markmap:
  initialExpandLevel: 2
---

# 🧠 **Machine Learning**

## 🎯 **Visão Geral**
- Subárea da **IA**
- Aprende com dados (*sem programação explícita*)
- Base para ==predição==, ==classificação== e tomada de decisão

## 🧬 **Tipos de Aprendizado**

### ✅ **Supervisionado**
- Aprendizado com **dados rotulados**
- Objetivo: ==predição== de saída conhecida
- Técnicas: **classificação**, **regressão**

#### 📌 *Algoritmos*
- **Regressão Linear**
  - 📎 `y = ax + b`, erro quadrático mínimo
- **Regressão Logística**
  - 📎 *Classificação binária*, saída entre `0` e `1`
- **Naive Bayes**
  - 📎 *Probabilidade condicional*, independência entre atributos
- **KNN**
  - 📎 `distância euclidiana`, vizinhos mais próximos
- **SVM**
  - 📎 `hiperplano ótimo`, `kernel`, `margens máximas`
- **Árvores de Decisão**
  - 📎 Estrutura `SE...ENTÃO`, entropia, índice de Gini
- **Random Forest**
  - 📎 `bagging`, várias árvores, reduz overfitting
- **LDA**
  - 📎 **Separação máxima entre classes**, redução de dimensão
- **LVQ**
  - 📎 Proximidade de `vetores protótipos`, supervisão
- **SVR**
  - 📎 Regressão com `margens`, versão do SVM

### 🚫 **Não Supervisionado**
- Não usa rótulos
- Descobre ==padrões ocultos== nos dados

#### 🧩 *Clusterização*
- **K-Means**
  - 📎 `centroides`, número `K`, distância
- **Hierarchical Clustering**
  - 📎 `dendrogramas`, métodos aglomerativo/divisivo
- **DBSCAN**
  - 📎 `densidade`, detecta outliers
- **Mean Shift**
  - 📎 desloca média até convergência

#### 🧾 *Associação*
- **Apriori**
  - 📎 `se A então B`, suporte, confiança, lift
- **Eclat**
  - 📎 Interseção de conjuntos, melhor desempenho
- **FP-Growth**
  - 📎 Árvore de padrões, evita candidatos

#### 📉 *Redução de Dimensionalidade*
- **PCA**
  - 📎 `variância máxima`, autovalores
- **T-SNE**
  - 📎 `visualização`, projeção 2D/3D
- **UMAP**
  - 📎 mais rápido que T-SNE, preserva estrutura local

### ⚖️ **Semisupervisionado**
- Dados parcialmente rotulados
- Útil quando rotulagem é ==cara==

#### 📌 Técnicas
- **Label propagation**
  - 📎 Expande rótulos por `grafo`
- **Autoencoder com fine-tuning**
  - 📎 Pré-treino não supervisionado + ajuste supervisionado

### 🧠 **Aprendizado por Reforço**
- Agente aprende com interação com o ambiente
- Baseado em ==recompensas== e penalidades

#### 📌 Conceitos
- **Q-Learning**
  - 📎 Tabela `Q`, aprendizado por `recompensa`
- **SARSA**
  - 📎 Atualiza Q com a **ação atual**
- **DQN**
  - 📎 Deep Q-Network, usa `rede neural`
- **Exploração x Exploração**
  - 📎 `explore` ou `exploit`

## 🧪 **Outros / Híbridos**

### 🔀 Redes Neurais
- **ANN**
  - 📎 `Perceptrons`, aprendizado supervisionado
- **CNN**
  - 📎 `convolução`, imagens
- **RNN**
  - 📎 `feedback interno`, séries temporais

### 🔄 Geração de dados
- **Autoencoders**
  - 📎 Compactação + reconstrução
- **GANs**
  - 📎 Duas redes: `geradora` e `discriminadora`

### 🎯 Ensemble Learning
- **Bagging**
  - 📎 Subconjuntos de dados → modelos paralelos (`Random Forest`)
- **Boosting**
  - 📎 Correção sequencial de erros (`AdaBoost`, `XGBoost`)
- **Stacking**
  - 📎 Combina previsões de modelos

## ⚠️ **Problemas Comuns**

### **Overfitting**
- 📎 Modelo *memoriza*, não generaliza
- 📎 ==Alta variância==, maior complexidade
- 📎 Erro baixo em treino, alto em teste

### **Underfitting**
- 📎 Modelo *aprende pouco*
- 📎 ==Alto viés (bias)==, estrutura simples
- 📎 Erro alto em treino e teste

### *Soluções*
- 📎 Regularização (`L1`, `L2`)
- 📎 Cross-validation
- 📎 Aumentar base de dados
- 📎 Modelos mais adequados

## 🛠️ **Processo de Construção**

### 1. **Pré-processamento**
- 📎 `Limpeza`, `normalização`, `codificação`, `divisão treino/teste`

### 2. **Treinamento**
- 📎 Algoritmo aprende `padrões` dos dados

### 3. **Validação**
- 📎 Métricas: `acurácia`, `precisão`, `recall`, `F1`

### 4. **Teste**
- 📎 Avaliação com dados não vistos

### 5. **Otimização**
- 📎 Ajuste de `hiperparâmetros`: Grid Search, Random Search
