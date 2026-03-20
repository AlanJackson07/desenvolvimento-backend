# 🚀 Encontro 01 — Backend, HTTP, Node.js e NestJS (Guia Completo)

---

# 🎯 Objetivos

- Entender o que é backend
- Compreender cliente-servidor
- Dominar HTTP e JSON
- Introdução ao Node.js
- Introdução ao NestJS

---

# 🧠 O QUE É BACKEND?

Backend é a parte da aplicação responsável por:

- Processar regras de negócio
- Validar dados
- Receber requisições
- Acessar banco de dados
- Retornar respostas
- Integrar serviços externos

---

## ⚙️ Exemplo real (Login)

1. Usuário digita email e senha
2. Frontend envia para o backend
3. Backend valida os dados
4. Backend consulta o banco
5. Backend retorna resposta (sucesso ou erro)

---

# 🌐 CLIENTE X SERVIDOR

## 📱 Cliente
- Navegador
- Aplicativo mobile
- Sistema externo

## 🖥 Servidor
- Onde roda o backend
- Processa requisições

---

# 🔗 API (Application Programming Interface)

API é a interface que permite comunicação entre sistemas.

---

## 📌 Exemplos de rotas

```http
GET /produtos
POST /usuarios
POST /auth/login
DELETE /usuarios/1
