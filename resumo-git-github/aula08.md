# ✍️ Resumo Aula 08
## Salvando Alterações No Repositório Local
No Git, salvar alterações significa adicionar os arquivos ao controle de versão e depois registrar essas mudanças no histórico com um commit.
## 1️⃣ Verificar o status dos arquivos

    git status

- O git status mostra a nossa arvore de trabalho e area de preparação de commits.
- Como ainda não adicionamos nenhuma alteração, ele sugere a criar ou clonar algum arquivo e utilizar o ```git add```
  
## 2️⃣ Adicionar arquivos ao staging area
    
    git add nome-do-arquivo

Ou adicionar todos os arquivos de uma vez:

    git add .

## 3️⃣ Registrar as alterações com um commit

    git commit -m "Mensagem descritiva da alteração"
    
💡 A mensagem do commit deve ser clara e resumir o que foi alterado.

## 4️⃣ Ver o histórico de commits

    git log
    
Exibe todos os commits feitos no repositório, mostrando autor, data e mensagem

## ✅ Resumo do fluxo:

git status → verificar alterações

git add → preparar arquivos

git commit → salvar no histórico

git log → conferir histórico
