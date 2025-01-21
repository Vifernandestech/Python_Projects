# Projeto 1: Automação de Cadastro de Produtos

Este projeto automatiza o processo de cadastro de produtos em um sistema web, utilizando Python e as bibliotecas `pandas` e `pyautogui`.

## Descrição

O objetivo deste projeto é automatizar uma tarefa repetitiva e propensa a erros: o cadastro manual de produtos em um sistema. Ao utilizar a biblioteca `pyautogui`, o script simula as ações de um usuário, como abrir o navegador, navegar até a página de cadastro, preencher os campos do formulário e clicar em botões. Os dados dos produtos são lidos de um arquivo CSV usando a biblioteca `pandas`.

## Funcionalidades

*   Abre o navegador e navega até a URL do sistema.
*   Realiza o login no sistema, preenchendo os campos de e-mail e senha.
*   Lê os dados dos produtos a partir de um arquivo CSV (`Produtos.csv`).
*   Preenche os campos do formulário de cadastro para cada produto, incluindo:
    *   Código
    *   Marca
    *   Tipo
    *   Categoria
    *   Preço Unitário
    *   Custo
    *   Observações (se aplicável)
*   Clica no botão para enviar o formulário.
*   Repete o processo para todos os produtos no arquivo CSV.

## Tecnologias Utilizadas

*   Python
*   `pandas`: Para manipulação de dados (leitura do CSV).
*   `pyautogui`: Para automação da interface gráfica do usuário.
*   `time`: Para adicionar pausas entre as ações.

## Pré-requisitos

*   Python 3 instalado.
*   Bibliotecas necessárias instaladas: `pip install pandas pyautogui`
*   Arquivo `Produtos.csv` com os dados dos produtos, seguindo o formato especificado.
*   Navegador Microsoft Edge (o código atualmente está configurado para Edge, mas pode ser adaptado).

## Como Executar

1. **Clone este repositório:**
    ```bash
    git clone <URL do seu repositório>
    ```
2. **Navegue até a pasta do projeto:**
    ```bash
    cd <pasta do projeto>/product-registration-automation
    ```
3. **Instale as dependências:**
    ```bash
    pip install pandas pyautogui
    ```
4. **Configure o script:**
    *   Modifique a URL do sistema no script `product-registration-automation.py` ou `automated-product-cadastro.py`, se necessário.
    *   Ajuste as coordenadas dos cliques e campos de texto no script, utilizando o script auxiliar `pegar_posição.py` para obter as posições corretas do mouse na sua tela.
5. **Execute o script:**
    ```bash
    python product-registration-automation.py ou python automated-product-cadastro.py
    ```

## Script Auxiliar: `pegar_posição.py`

Este script é uma ferramenta auxiliar para obter as coordenadas (x, y) do mouse na tela. Isso é necessário para configurar corretamente os cliques e a digitação nos campos do formulário do sistema.

**Como usar:**

1. Execute o script: `python pegar_posição.py`
2. Posicione o mouse sobre o elemento desejado na tela (por exemplo, um campo de texto).
3. Anote as coordenadas exibidas no terminal.
4. Atualize as coordenadas no script principal (`product-registration-automation.py`).

## Considerações Importantes

*   **Configuração Específica do Sistema:** Este projeto foi desenvolvido para um sistema web específico. As coordenadas dos elementos na tela e a estrutura do formulário de cadastro podem variar em outros sistemas. Portanto, é necessário ajustar o script de acordo com as características do sistema alvo.
*   **Tratamento de Erros:** O script atual não possui um tratamento de erros robusto. Em um ambiente de produção, seria importante adicionar mecanismos para lidar com exceções, como falhas de conexão, elementos não encontrados na página ou erros no preenchimento do formulário.
*   **Segurança:** As credenciais de login (e-mail e senha) estão atualmente fixas no código. Para um uso mais seguro, considere armazená-las em um arquivo de configuração separado ou utilizar variáveis de ambiente.

## Melhorias Futuras

*   Implementar tratamento de erros para lidar com situações inesperadas.
*   Tornar o script mais configurável, permitindo que o usuário especifique a URL do sistema, o arquivo de dados e as coordenadas dos elementos por meio de um arquivo de configuração ou parâmetros de linha de comando.
*   Adicionar logs para registrar as ações realizadas e eventuais erros.
*   Modularizar o código, separando as diferentes funcionalidades em funções para melhor organização e reutilização.
*   Utilizar uma abordagem baseada em identificadores de elementos HTML em vez de coordenadas absolutas, se o sistema alvo permitir, para tornar o script menos dependente da resolução da tela.

## Contribuições

Contribuições são bem-vindas! Se você encontrar algum erro ou tiver sugestões de melhorias, por favor, abra uma *issue* ou envie um *pull request*.

---
