# Teste de Regressão (simulado)

## Contexto

Foi identificado um bug onde o sistema permitia cadastro com email inválido.
Após correção pela equipe de desenvolvimento, foi realizada regressão para validar a estabilidade da aplicação.

---

## Cenários de Regressão Executados

| ID   | Cenário | Objetivo | Resultado Esperado |
|------|----------|----------|--------------------|
| RG01 | Cadastro com email inválido | Validar correção do bug | Sistema deve bloquear cadastro |
| RG02 | Cadastro com email válido | Garantir que a correção não afetou cadastro válido | Status 201 Created |
| RG03 | Login com novo usuário | Validar fluxo completo | Login realizado com sucesso |
| RG04 | Login com senha incorreta | Garantir que regras de autenticação continuam funcionando | Status 401 Unauthorized |

---

## Tipo de Regressão

Regressão parcial focada nas funcionalidades impactadas (Cadastro e Login).
