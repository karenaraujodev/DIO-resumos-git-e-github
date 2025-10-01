# ✍️ Resumo Aula 12
## ⚡ Comandos Úteis no Dia a Dia

Esses são alguns dos comandos Git mais usados no dia a dia de desenvolvimento:
    
#### 📌 Verificando o status do repositório

Mostra os arquivos modificados, adicionados ou não rastreados:

    git status

#### 📌 Verificando o histórico de commits

Lista os commits realizados na branch atual:

    git log

#### 📌 Visualizando diferenças

Ver mudanças em arquivos antes de adicionar:

    git diff

Ver mudanças já adicionadas (git add):

    git diff --cached

#### 📌 Trabalhando com arquivos

Remover arquivo do repositório e do diretório:

    git rm nome-do-arquivo


Renomear ou mover arquivos/pastas:

    git mv nome-antigo nome-novo

#### 📌 Atualizando repositório local

Baixar alterações do repositório remoto (sem mesclar):

    git fetch


Baixar e mesclar as alterações da branch remota:

    git pull

#### 📌 Enviando alterações

Enviar commits para o repositório remoto:

    git push

#### 📌 Mesclando branches

Mesclar uma branch na branch atual (exemplo: trazer alterações da feature para a main):

    git checkout main
    git merge feature


Se não houver conflitos → o Git faz o merge automaticamente.

Se houver conflitos → será necessário resolvê-los manualmente, depois usar:
    
    git add nome-do-arquivo
    git commit -m "Resolvendo conflitos de merge"


### ✅ Resumo rápido dos mais usados:

- git status → ver situação atual

- git log --oneline → histórico rápido

- git diff → ver mudanças

- git add . + git commit -m "" → salvar alterações

- git pull → atualizar

- git push → enviar alterações

- git merge → unir branches
