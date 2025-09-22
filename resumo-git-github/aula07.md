# ✍️ Resumo Aula 07
## Criando e Clonando Repositórios

Existem duas formas de obter um repositório Git na nossa maquina

### 1️⃣ Criando um repositório local → transformar um diretório existente em um repositório Git.

1. Para isso, vamos criar uma pasta através do git bash e entrar nela utilizando os seguintes comandos:

        mkdir nomeDaPasta
   
        cd nomeDaPasta

2. Por fim, inicializar o versionamento local:

        git init
    

### 2️⃣ Clonando um repositório existente.

1. Para isso, temos duas formas de clonar o repositório:
   
    - Clonar usando SSH
  
          git clone git@github.com:usuario/repositorio.git

    - Ou usando HTTPS
  
          git clone https://github.com/usuario/repositorio.git

2. Depois de clonado, podemos acessar a pasta assim:
  
       cd nomeDaPasta
  
### 🔍 Verificando as configurações do repositório

Dentro do repositório, podemos usar:

      cat config

- Esse comando mostra o conteúdo do arquivo de configuração do Git local ```(.git/config)```. Ele contém informações importantes, como:

💻 Core → configurações básicas do repositório (permissões, formato, histórico).

🌐 Remote "origin" → endereço do repositório remoto e como buscar os branches.

🌿 Branch "main" → branch padrão e informações de merge/push.

