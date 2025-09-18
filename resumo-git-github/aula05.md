# ✍️ Resumo Aula 05
## 🔑 Autentificação via token
O token funciona como uma “senha alternativa”, só que mais segura. Ele é gerado no GitHub e pode ter permissões específicas (ex: só leitura, só escrita, acesso total, etc). Além disso, pode ter uma data de expiração ou podemos revoga-lo quando quisermos.

## ⚙️ Como gerar um Token no GitHub

- Vá até: Settings → Developer settings → Personal Access Tokens.

- Clique em Tokens (classic) → Generate new token.

- Escolha as permissões (para uso com Git normalmente é repo).

- Defina uma data de expiração ou deixe sem expiração.

- Copie o token gerado(não dá pra ver de novo).
  
## 🔐 Como usar o Token no Git

Quando fazemos operações que pedem autenticação utilizamos o token.

#### Exemplo: ao  clonar um repositório do github
    
     git clone https://github.com/usuario/repositorio.git

     
- Git pede login → digite seu usuário do GitHub

- Git pede senha → cole o token
    
## 🗃️ Armazenamento de credenciais 

O armazenamento de credenciais(usuario + token) é um recurso do Git para não precisarmos estar fazendo essa validação sempre.

### ⚙️ Modos de armazenamento

- ```cache``` → Armazena temporariamente em memória (padrão: 15 minutos).
```
  git config --global credential.helper cache
```

- ```store``` → Salva em arquivo de texto no computador(guarda permanentemente)
```
git config --global credential.helper store
```

- ```manager``` → Usa o Git Credential Manager, integrando com o Windows (mais seguro).
```
git config --global credential.helper manager
```

### 📋 Comandos úteis

- Ver qual helper está configurado
```
git config --global credential.helper
```
