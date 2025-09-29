# ✍️ Resumo Aula 11
## 🌿 Trabalhando com Branches
Branches (ou ramificações) permitem trabalhar em linhas paralelas de desenvolvimento sem afetar diretamente a branch principal (main).

### 1️⃣ Criando e navegando entre branches

Criando uma nova branch:

    git branch nome-da-branch

Listar branches existentes:

    git branch

Mudar para outra branch:

    git checkout nome-da-branch

Criar e já trocar para a nova branch:

    git checkout -b nome-da-branch

### 2️⃣ Mesclando branches
Depois de concluir o trabalho em uma branch, podemos mesclar com a main:
    
    git checkout main
    
    git merge nome-da-branch

Isso junta o histórico da branch escolhida na branch principal.

### 3️⃣ Deletando branches

Após mesclar ou quando não for mais necessária:

    git branch -d nome-da-branch

### 4️⃣ Tratando conflitos

Se dois commits modificarem a mesma parte de um arquivo, o Git não sabe qual versão manter → ocorre um conflito

- O Git marca os trechos conflitantes no arquivo:
  
- Devemos editar o arquivo manualmente, escolhendo qual versão manter (ou mesclando as duas).
  
- Depois, confirmamos a resolução do conflito:
  
      git add nome-do-arquivo
      git commit -m "Resolvendo conflito"
