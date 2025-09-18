# ✍️Resumo Aula 04

## ⚙️ Configurando o Git
 Com o Git instalado, precisamos fazer algumas configurações iniciais. Para isso, vamos abrir o Git Bash(terminal) e digitar alguns comandos. 

```
git config
```
- O comando git config permite visualizar e definir variáveis de configuração do Git. Essas configurações podem ser aplicadas em três níveis:

### 🔧 Níveis de configuração

--system → Vale para todo o computador
👉 Todo usuário que usar o Git nesse PC vai herdar essa configuração.
(É como colocar uma regra geral para a máquina inteira).

--global → Vale apenas para o usuário do computador
👉 Todos os repositórios que você criar ou clonar vão usar essa configuração.
(É como definir preferências pessoais).

--local → Vale somente para o repositório em que estamos
👉 Se um projeto precisar de nome ou e-mail diferente, configuramos apenas nele.
(É como uma regra feita só para aquela pasta/projeto).

### 🔑 Configurações comuns no Git
- 📝 Definir nome do usuário 
```
git config --global user.name "Seu Nome"
```
- 📧 Definir e-mail do usuário
```
git config --global user.email "seuemail@exemplo.com"
```
- 🔍 Verificar branch padrão configurada
```
git config init.defaultBranch
```
- 🌿 Definir main como branch padrão
```
git config --global init.defaultBranch main
```
- 📋 Listar todas as configurações já definidas
```
git config --list
```
