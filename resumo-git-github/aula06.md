# ✍️ Resumo Aula 06
## 🔑 Autenticação Via SSH
SSH (Secure Shell) é um protocolo seguro que cria uma conexão criptografada entre o computador e o GitHub.

Diferente da autenticação via HTTPS (que usa login + token), o SSH usa um par de chaves:

🔒 Chave privada → fica no computador.

🔑 Chave pública → é cadastrada no GitHub.

Assim, quando tentamos acessar um repositório, o GitHub confere se a chave privada do seu PC corresponde à chave pública registrada na sua conta.

## ⚙️ Como configurar autenticação via SSH

### 1- Verificar se já existe uma chave SSH
   
   ```
   ls -al ~/.ssh
   ```
 Se aparecer arquivos como id_rsa e id_rsa.pub, significa que já tem uma chave criada. se já existir chave, basta pegar a pública ```cat ~/.ssh/id_ed25519.pub``` e cadastrar no GitHub. Não precisa criar outra.
 
 ### 2- Gerar uma nova chave SSH (se não tiver)
  
  ```
  ssh-keygen -t ed25519 -C "seu-email-do-github@example.com"
  ```
***👉 Ele vai pedir:***

- Local para salvar (podemos só apertar Enter)

- Uma senha

Isso vai gerar dois arquivos:

  chave privada → id_ed25519

  chave pública → id_ed25519.pub

### 3- Adicionar a chave privada ao SSH Agent

O ssh-agent mantém a chave em memória enquanto a sessão estiver ativa. Essa etapa é importante para estarmos armazenando a nossa chave de maneira segura

       eval "$(ssh-agent -s)"
       
O ssh-add adiciona a chave privada no agente.

    ssh-add ~/.ssh/id_ed25519

***👉 Ele vai pedir:***

- passphrase  (senha que criamos)

### 4- Adicionar a chave pública a conta do Github
Utilizamos o comando abaixo para exibir a chave pública e podermos copia-la
  
    cat ~/.ssh/id_ed25519.pub
    
Vamos em Settings → SSH and GPG keys → New SSH key.

Por fim, colamos a chave pública e salvamos.

### 5- Testar conexão

    ssh -T git@github.com
    
## 🚀 Usando SSH no Git
Quando formos clonar um repositório, usamos o link SSH (e não o HTTPS).
Exemplo:

    git clone git@github.com:usuario/repositorio.git

Depois disso, ```git push``` e ```git pull``` já vão funcionar sem precisar digitar token ou senha.
