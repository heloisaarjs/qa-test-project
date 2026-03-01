# Casos de Teste – Cadastro e Login

## Funcionalidade: Cadastro de Usuário

| ID   | Cenário | Pré-condição | Passos | Resultado Esperado | Tipo |
|------|----------|--------------|--------|--------------------|------|
| CT01 | Cadastro válido | Usuário não cadastrado | 1. Inserir email válido<br>2. Inserir senha com 8+ caracteres<br>3. Clicar em cadastrar | Usuário criado com sucesso (Status 201) | Funcional |
| CT02 | Email inválido | - | 1. Inserir email sem @<br>2. Inserir senha válida<br>3. Clicar em cadastrar | Sistema deve exibir mensagem de erro | Negativo |
| CT03 | Senha menor que 8 caracteres | - | 1. Inserir email válido<br>2. Inserir senha curta<br>3. Clicar em cadastrar | Sistema deve bloquear cadastro | Negativo |
| CT04 | Email já existente | Usuário já cadastrado | 1. Inserir email já existente<br>2. Inserir senha válida<br>3. Clicar em cadastrar | Sistema deve retornar erro de duplicidade | Negativo |

---

## Funcionalidade: Login

| ID   | Cenário | Pré-condição | Passos | Resultado Esperado | Tipo |
|------|----------|--------------|--------|--------------------|------|
| CT05 | Login válido | Usuário cadastrado | 1. Inserir email válido<br>2. Inserir senha correta<br>3. Clicar em login | Login realizado com sucesso (Status 200) | Funcional |
| CT06 | Senha incorreta | Usuário cadastrado | 1. Inserir email válido<br>2. Inserir senha incorreta<br>3. Clicar em login | Sistema deve retornar 401 Unauthorized | Negativo |
| CT07 | Usuário inexistente | - | 1. Inserir email não cadastrado<br>2. Inserir senha qualquer<br>3. Clicar em login | Sistema deve retornar 404 Not Found | Negativo |
