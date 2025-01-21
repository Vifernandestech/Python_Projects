# Projeto 3: Previsão de Score de Crédito com Machine Learning

Este projeto utiliza algoritmos de Machine Learning para prever o score de crédito de clientes com base em um histórico de dados.

## Descrição

O objetivo deste projeto é construir um modelo preditivo capaz de estimar o score de crédito de um cliente, que é uma medida de sua capacidade de honrar compromissos financeiros. O modelo é treinado usando um conjunto de dados históricos e, em seguida, aplicado a novos clientes para prever seu score.

## Etapas do Projeto

1. **Importação e Preparação dos Dados:**
    *   Importar a base de dados (`Aula03 - clientes.csv`) usando `pandas`.
    *   Remover a coluna `id_cliente`, irrelevante para a modelagem.
    *   Transformar variáveis categóricas ("profissao", "mix\_credito", "comportamento\_pagamento") em numéricas usando Label Encoding.

2. **Divisão dos Dados:**
    *   Separar a variável alvo (`score_credito`) das variáveis preditoras.
    *   Dividir os dados em conjuntos de treino e teste usando `train_test_split` (72% para treino, 28% para teste).

3. **Treinamento dos Modelos:**
    *   Utilizar dois algoritmos de classificação:
        *   `RandomForestClassifier`
        *   `KNeighborsClassifier`
    *   Treinar cada modelo com os dados de treino.

4. **Avaliação dos Modelos:**
    *   Fazer previsões nos dados de teste usando os modelos treinados.
    *   Avaliar o desempenho dos modelos usando a métrica de acurácia (`accuracy_score`).
    *   Resultados de acurácia:
        *   Random Forest: ~84%
        *   KNN: ~74%

5. **Previsão com Novos Clientes:**
    *   Importar um novo conjunto de dados com informações de novos clientes (`Aula03 - novos_clientes.csv`).
    *   Aplicar as mesmas transformações (Label Encoding) realizadas nos dados de treinamento.
    *   Utilizar o modelo com melhor desempenho (Random Forest) para prever o score de crédito dos novos clientes.

## Tecnologias Utilizadas

*   Python
*   `pandas`: Para manipulação de dados.
*   `scikit-learn`: Para Machine Learning (Label Encoding, treinamento de modelos, avaliação).

## Pré-requisitos

*   Python 3
*   Bibliotecas: `pandas`, `scikit-learn`

## Como Executar

1. **Clone este repositório:**
    ```bash
    git clone <URL do seu repositório>
    ```
2. **Navegue até a pasta do projeto:**
    ```bash
    cd <pasta do projeto>/credit-scoring-prediction
    ```
3. **Instale as dependências:**
    ```bash
    pip install pandas scikit-learn
    ```
4. **Execute o script:**
    ```bash
    python credit_scoring_prediction.py
    ```

## Considerações

*   Este projeto utiliza um conjunto de dados para fins de demonstração.
*   O desempenho do modelo pode variar dependendo do conjunto de dados utilizado.
*   Em um cenário real, seria importante realizar uma validação mais robusta do modelo, usando técnicas como validação cruzada, e explorar outras métricas de avaliação, como precisão, recall, F1-score e AUC.

## Melhorias Futuras

*   **Tratamento de Valores Nulos:** Implementar tratamento de valores nulos (caso existam).
*   **Exploração de Outros Modelos:** Testar outros algoritmos de classificação, como Regressão Logística, SVM, Gradient Boosting, etc.
*   **Otimização de Hiperparâmetros:** Ajustar os hiperparâmetros dos modelos usando técnicas como `GridSearchCV` ou `RandomizedSearchCV` para melhorar o desempenho.
*   **Validação Cruzada:** Utilizar validação cruzada para uma avaliação mais confiável do modelo.
*   **Normalização/Padronização:** Aplicar normalização ou padronização nas features numéricas, se necessário.
*   **Feature Engineering:** Criar novas features a partir das existentes para tentar melhorar a capacidade preditiva do modelo.
*   **Avaliar outras Métricas:** Além da acurácia, calcular e analisar outras métricas de desempenho, como precisão, recall, F1-score e AUC.

## Contribuições

Contribuições são sempre bem-vindas! Se você identificar erros, tiver sugestões ou quiser contribuir com o código, por favor, abra uma *issue* ou envie um *pull request*.
