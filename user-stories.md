# User Stories

## História 1 - Cadastro

Como usuário,
quero me cadastrar no sistema,
para poder acessar minha conta.

### Critérios de Aceitação:
- O email deve ser válido
- A senha deve ter no mínimo 8 caracteres
- Não deve permitir email duplicado
- Após cadastro válido, deve retornar status 201

---

## História 2 - Login

Como usuário,
quero fazer login,
para acessar minha conta.

### Critérios de Aceitação:
- Login deve aceitar email e senha válidos
- Deve retornar mensagem de erro para senha incorreta
- Deve retornar mensagem de erro para usuário inexistente
