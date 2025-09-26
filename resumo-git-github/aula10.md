# ✍️ Resumo Aula 10
## 🔄 Enviando e baixando alterações com o Github
Anteriormente, vimos como salvar alterações no repositório local (git add + git commit). Agora, precisamos enviar essas mudanças para o repositório remoto no GitHub.

### 🚀 Conectando repositório local ao GitHub

1. Criar um repositório no GitHub.

2. Conectar ao repositório local:

       git remote add origin <link do repositório do github aqui>
   
       git push -u origin main

### 📤 Enviar alterações para o GitHub 

Depois de criar novos commits:
      
      git push origin main

- push → envia os commits locais para o repositório remoto.

### ⬇️ Baixar alterações do GitHub
Se o repositório remoto foi atualizado, podemos sincronizar:

      git pull origin main

- pull → baixa e mescla as alterações do GitHub no repositório local.

### ✅ Resumo rápido:

Conectar repositório local ao GitHub → git remote add origin <url>

Enviar alterações → git push origin main

Baixar alterações → git pull origin main
