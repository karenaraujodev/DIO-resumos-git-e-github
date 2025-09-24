# ✍️ Resumo Aula 09
## ↩️Desfazendo alterações no repositório local

#### 1️⃣ Remover um repositório criado por engano

      rm -rf .git
      
👉 Apaga toda a pasta oculta .git e desfaz o versionamento.

#### 2️⃣ Restaurar um arquivo da árvore de trabalho

      git restore nome-do-arquivo
      
👉 Restaura o arquivo para o último estado salvo no repositório.

### 3️⃣ Alterar a mensagem do último commit

      git commit --amend -m "nova mensagem"
      
👉 Substitui a mensagem do commit anterior (sem criar um novo commit).

4️⃣ Desfazer o último commit, mas manter as alterações na staging area

      git reset --soft <hash-do-commit>
  
👉 O commit é desfeito, mas os arquivos continuam prontos para um novo commit.

5️⃣ Desfazer o último commit e voltar os arquivos para a área de trabalho

    git reset --mixed <hash-do-commit>

👉 O commit é desfeito e os arquivos voltam para a área de trabalho (precisam ser adicionados novamente).

### ✅ Resumo rápido:

- 🗑️ Apagar versionamento → rm -rf .git

- 🔄 Restaurar arquivo → git restore nome-do-arquivo

- ✏️ Renomear último commit → git commit --amend -m "nova mensagem"

- ♻️ Desfazer commit (mantendo staging) → git reset --soft

- 🔙 Desfazer commit (voltando para working dir) → git reset --mixed
 
