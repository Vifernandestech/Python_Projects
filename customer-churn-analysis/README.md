# Projeto 2: Análise de Cancelamento de Clientes

Este projeto analisa uma base de dados de cancelamento de clientes (churn) para identificar padrões, entender as causas e propor soluções para reduzir a taxa de cancelamento.

## Descrição

O objetivo deste projeto é explorar um conjunto de dados de clientes de uma empresa fictícia, identificar os fatores que mais contribuem para o cancelamento de serviços e sugerir estratégias para melhorar a retenção de clientes. A análise é feita utilizando a linguagem Python e as bibliotecas `pandas`, `plotly` e `nbformat`.

## Etapas do Projeto

1. **Importação e Limpeza dos Dados:**
    *   Importar a base de dados (`cancelamentos.csv`) usando `pandas`.
    *   Remover a coluna `CustomerID`, considerada irrelevante para a análise.
    *   Tratar valores faltantes, removendo as linhas com dados incompletos.

2. **Análise Exploratória:**
    *   Calcular a taxa de cancelamento geral.
    *   Analisar a distribuição dos cancelamentos por diferentes variáveis, como:
        *   Duração do contrato (mensal, trimestral, anual)
        *   Tipo de assinatura (Basic, Standard, Premium)
        *   Idade
        *   Gênero
        *   Número de ligações para o call center
        *   Dias de atraso no pagamento
    *   Utilizar gráficos interativos da biblioteca `plotly` para visualizar os padrões e insights.

3. **Identificação das Causas de Cancelamento:**
    *   Com base na análise exploratória, identificar os principais fatores que contribuem para o cancelamento.
    *   Insights identificados:
        *   Clientes com contrato mensal têm uma taxa de cancelamento significativamente maior.
        *   Clientes com mais de 50 anos tendem a cancelar mais.
        *   O público feminino apresenta uma taxa de cancelamento ligeiramente superior.
        *   Clientes que ligam para o call center mais de 4 vezes têm alta probabilidade de cancelar.
        *   Clientes com mais de 20 dias de atraso no pagamento cancelam o serviço.

4. **Proposição de Soluções:**
    *   Com base nos insights, sugerir ações para reduzir a taxa de cancelamento, como:
        *   Oferecer incentivos para a migração de contratos mensais para trimestrais ou anuais.
        *   Desenvolver estratégias de retenção específicas para clientes com mais de 50 anos.
        *   Melhorar o atendimento no call center para reduzir a necessidade de múltiplas ligações.
        *   Implementar políticas mais flexíveis para lidar com atrasos no pagamento.

## Tecnologias Utilizadas

*   Python
*   `pandas`: Para manipulação e análise de dados.
*   `plotly`: Para criação de gráficos interativos.
*   `nbformat`: Para lidar com notebooks Jupyter.
*   Jupyter Notebook: Como ambiente de desenvolvimento.

## Pré-requisitos

*   Python 3
*   Jupyter Notebook ou Jupyter Lab
*   Bibliotecas: `pandas`, `plotly`, `nbformat`, `ipykernel`

## Como Executar

1. **Clone este repositório:**
    ```bash
    git clone <URL do seu repositório>
    ```
2. **Navegue até a pasta do projeto:**
    ```bash
    cd <pasta do projeto>/customer-churn-analysis
    ```
3. **Instale as dependências (caso ainda não estejam instaladas):**
    ```bash
    pip install pandas plotly nbformat ipykernel
    ```
4. **Abra o notebook `customer_churn_analysis.ipynb` no Jupyter Notebook ou VS Code:**
    ```bash
    jupyter notebook customer_churn_analysis.ipynb
    ```
    ou
    ```bash
   code customer_churn_analysis.ipynb
    ```
5. **Execute as células do notebook sequencialmente.**

## Considerações

*   Este projeto utiliza um conjunto de dados fictício para fins de demonstração.
*   As análises e conclusões são baseadas nos insights obtidos a partir deste conjunto de dados específico.
*   Em um cenário real, seria importante validar as conclusões com dados adicionais e considerar outros fatores contextuais.

## Melhorias Futuras

*   Realizar uma análise mais aprofundada da relação entre gênero e cancelamento, considerando outras variáveis.
*   Explorar a interação entre idade e outras variáveis para entender melhor o comportamento dos clientes com mais de 50 anos.
*   Segmentar os clientes em grupos com base em seu comportamento e características para desenvolver estratégias de retenção mais direcionadas.
*   Implementar um modelo preditivo para identificar clientes com alto risco de cancelamento.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* para reportar problemas ou sugerir melhorias, ou enviar um *pull request* com suas contribuições.
