# Projeto 1: Automação de Cadastro de Produtos

# Passo 1: Abrir o sistema da empresa;
# Passo 2: Fazer login no sistema;
# Passo 3: Importar a base de dados dos produtos;
# Passo 4: Cadastrar 1 produto;
# Passo 5: Repetir o passo 4 até acabarem os produtos. 

# Importando as bibliotecas necessárias
import pandas # Biblioteca para manipulação de dados 
import time # Biblioteca para lidar com tempo (pausas)
import pyautogui  # Biblioteca para automação de interface gráfica

# Passo 1: Abrir o sistema da empresa;
# Configuração inicial do pyautogui

pyautogui.PAUSE = 1 # Define um intervalo de 1 segundo entre cada comando do pyautogui

# Passo 1: Abrir o sistema da empresa (navegador)
pyautogui.press("Win") # Pressiona a tecla Windows (Menu Iniciar)
pyautogui.write("edge") # Digita "edge" (para abrir o Microsoft Edge)
pyautogui.press("enter") # Pressiona Enter

# Aguardar o navegador carregar
time.sleep(3)

# Passo 2: Fazer login no sistema
# Navegar até a página de login
pyautogui.write("https://dlp.hashtagtreinamentos.com/python/intensivao/login")
pyautogui.press("enter")
# Preencher os campos de login
# Localizar o campo de e-mail (ATENÇÃO: você precisa ajustar as coordenadas)
pyautogui.click(x=525, y=403)
pyautogui.write("pythonimpressionador@gmail.com") # Digitar o e-mail
pyautogui.press("tab") # Pressionar Tab para ir para o campo de senha
pyautogui.write("Sua senha") # Digitar a senha (substitua "Sua senha" pela senha real)
pyautogui.press("tab") # Pressionar Tab
pyautogui.press("enter") # Pressionar Enter para fazer login

# Passo 3: Importar a base de dados dos produtos
# Ler o arquivo CSV com os dados dos produtos
pandas.read_csv("Produtos.csv")
Tabela = pandas.read_csv("Produtos.csv")
print(Tabela) # Exibir a tabela (opcional - para verificar se foi lida corretamente)

# Aguardar o carregamento do sistema
time.sleep(2)

# Passo 4: Cadastrar um produto (repetir para cada produto na tabela)
for linha in Tabela.index:

    # Passo 5: Repetir o passo 4 até acabarem os produtos.
    # Clicar no campo de código do produto
    pyautogui.click (x=511, y=282)

    # Preencher os campos do formulário
    codigo = Tabela.loc[linha, "codigo"]
    pyautogui.write(str(codigo))
    pyautogui.press("tab")

    marca = Tabela.loc[linha, "marca"]
    pyautogui.write(str(marca))     
    pyautogui.press("tab")

    tipo = Tabela.loc[linha, "tipo"]
    pyautogui.write(str(tipo))
    pyautogui.press("tab")

    categoria = Tabela.loc[linha, "categoria"]
    pyautogui.write(str(categoria))
    pyautogui.press("tab")

    preco_unitario = Tabela.loc[linha, "preco_unitario"]
    pyautogui.write(str(preco_unitario))
    pyautogui.press("tab")  

    custo = Tabela.loc[linha, "custo"]
    pyautogui.write(str(custo))
    pyautogui.press("tab")

    obs = str(Tabela.loc[linha, "obs"])
    if obs != "nan": # Verificar se o campo "obs" está vazio (NaN)
        pyautogui.write(obs)
    pyautogui.press("tab")

    # Enviar o formulário
    pyautogui.press("enter")
    # Rolar a página para cima (para visualizar o próximo cadastro)
    pyautogui.scroll(10000)  

print("Cadastro de produtos concluído com sucesso!")
