# 🏦 Modelo Preditivo de Crédito com Explainable AI (LIME)

## 📌 Contextualização do Problema

No cenário de análise de crédito bancário, modelos de Machine Learning vêm sendo amplamente utilizados para avaliar o risco de clientes e automatizar a concessão de crédito.  
Embora esses modelos possam atingir altos níveis de **precisão**, sua **opacidade** dificulta o entendimento sobre **por que** determinada decisão foi tomada — especialmente nos casos de **negação de crédito**.

Essa falta de transparência pode gerar problemas como:
- Dúvidas e insatisfação de clientes.
- Questionamentos de gerentes e equipes comerciais.
- Riscos de **não conformidade** com órgãos reguladores.

Para lidar com essa demanda, este projeto aplica técnicas de **Explainable AI (XAI)** utilizando a biblioteca **LIME** (*Local Interpretable Model-agnostic Explanations*), com o objetivo de explicar **decisões individuais** de um modelo de classificação para crédito.

---

## 🎯 Objetivos

1. Treinar um **modelo preditivo** de classificação binária para análise de risco de crédito.
2. Aplicar **LIME** para gerar explicações locais para **cada cliente analisado**.
3. Interpretar quais características (ex.: idade, renda, histórico de inadimplência) mais influenciaram nas decisões.
4. Discutir **limitações** e **boas práticas** no uso de modelos explicáveis em crédito.

---

## 📂 Dataset Utilizado

**Statlog (German Credit Data)** – UCI Machine Learning Repository  
📎 [Link para o Dataset](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)

**Descrição:**
- **Amostras:** 1.000 clientes.
- **Atributos:** 20 variáveis, incluindo idade, tipo de conta, histórico de crédito, propósito do empréstimo, valor solicitado, entre outros.
- **Variável alvo:** Risco de crédito (`good` ou `bad`).
- **Formato:** CSV numérico.

---

## 🛠️ Metodologia

1. **Pré-processamento**
   - Carregamento do dataset.
   - Tratamento de valores categóricos via *One-Hot Encoding*.
   - Normalização dos dados numéricos.
   - Divisão em treino e teste (80/20).

2. **Treinamento do Modelo**
   - Algoritmo escolhido: **Random Forest Classifier**
   - Justificativa:
     - Alta performance em problemas de classificação tabular.
     - Boa capacidade de modelar interações entre variáveis.
     - Funciona bem com dados categóricos codificados.
   - Métricas avaliadas:
     - Acurácia
     - Precisão
     - Recall
     - F1-Score
