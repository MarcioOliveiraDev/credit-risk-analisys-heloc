# Análise de Risco de Crédito com Dataset HELOC 🏠💳

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Concluído-success)

## 📋 Sobre o Projeto

Este projeto foi desenvolvido como parte da disciplina de **Aprendizagem de Máquina** do programa de Pós-Graduação em Ciência da Computação do **Centro de Informática (CIn) - UFPE**.

O objetivo é aplicar a metodologia **CRISP-DM** para prever o risco de crédito (variável `is_at_risk`) utilizando o dataset **HELOC (Home Equity Line of Credit)**. O projeto explora desde a análise exploratória até a otimização de hiperparâmetros e explicabilidade do modelo (XAI).

### 👥 Equipe
* Lucas Matheus dos Santos Gonçalves
* Márcio Oliveira de Brito
* Maria Luiza de França Duda

---

## 🛠️ Metodologia e Ferramentas

O projeto segue o ciclo de vida CRISP-DM:
1.  **Entendimento dos Dados:** Análise estatística, correlações e identificação de outliers.
2.  **Preparação:** Tratamento de valores nulos, *Feature Engineering*, balanceamento de classes (**SMOTE**) e padronização.
3.  **Modelagem:** Teste de múltiplos algoritmos (Random Forest, XGBoost, LightGBM, MLP, etc.).
4.  **Otimização:** Uso de **Random Search** e **Optuna** para ajuste fino de hiperparâmetros.
5.  **Avaliação:** Métricas como Recall, F1-Score, ROC-AUC e Matriz de Confusão.
6.  **Explicabilidade:** Uso de **SHAP** (Shapley Additive Explanations) para interpretar as decisões do modelo (Black Box).

**Principais Bibliotecas:**
* `scikit-learn`, `imbalanced-learn`
* `xgboost`, `lightgbm`
* `optuna` (para otimização bayesiana)
* `shap` (para XAI)
* `pandas`, `seaborn`, `matplotlib`

---

## 📊 Principais Resultados

Abaixo, apresentamos as métricas obtidas. O modelo **XGBoost** foi o escolhido para a implantação devido ao seu melhor equilíbrio entre a identificação de clientes de risco (Recall) e a precisão geral (ACSA), especialmente após a otimização com Optuna.

| Modelo | Recall (Risco) | F1-Score | Acurácia (ACSA) |
| :--- | :---: | :---: | :---: |
| **XGBoost (Tuned)** | **71,92%** | **73,96%** | **72,79%*** |
| LightGBM | 71,67% | 73,50% | 62,83% |
| Random Forest | 71,47% | 71,50% | 61,61% |

> \* **Nota:** A Acurácia (ACSA - Average Class Specific Accuracy) do XGBoost subiu de ~63% para **72,79%** após a otimização com Optuna (Seção 6.2 do relatório), demonstrando a eficácia do ajuste fino de hiperparâmetros.
> Consulte a pasta `docs/` para ler o **Relatório Técnico Completo** e a **Apresentação de Slides**.

---

## 📂 Estrutura do Repositório

* `notebooks/01_data_understanding.ipynb`: Análise exploratória inicial.
* `notebooks/02_data_preparation.ipynb`: Limpeza e preparação (SMOTE).
* `notebooks/03_modeling_...ipynb`: Treinamento, validação cruzada e otimização (Optuna).
* `docs/`: Relatórios em PDF gerados durante a disciplina.

---

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/credit-scoring-heloc.git](https://github.com/seu-usuario/credit-scoring-heloc.git)

