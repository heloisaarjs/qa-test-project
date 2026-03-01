# Bug Report

## Título
Cadastro permite email inválido

## Ambiente
Homologação

## Passos para Reproduzir
1. Acessar tela de cadastro
2. Inserir email sem @
3. Inserir senha válida
4. Clicar em cadastrar

## Resultado Atual
Usuário é cadastrado com sucesso

## Resultado Esperado
Sistema deve bloquear cadastro com email inválido

## Evidência (simulada)
Request:
POST /users

Payload:
{
  "email": "heloisaemail.com",
  "password": "12345678"
}

Response:
Status Code: 201
Body:
{
  "id": 15,
  "email": "heloisaemail.com"
}
O sistema deveria bloquear email inválido, mas permitiu o cadastro.
