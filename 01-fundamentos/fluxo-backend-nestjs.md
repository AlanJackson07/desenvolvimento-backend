# 🚀 Fundamentos de Backend, HTTP e NestJS

## 🎯 Objetivo
Compreender o funcionamento do backend, o fluxo cliente-servidor e a base do NestJS.

---

# 🧠 O que é Backend?

Backend é a parte do sistema responsável por:

- processar regras de negócio;
- receber requisições;
- validar dados;
- acessar banco de dados;
- integrar serviços externos;
- retornar respostas ao cliente.

---

## ⚙️ Fluxo do Backend

1. Cliente envia requisição
2. Backend recebe
3. Valida dados
4. Executa lógica
5. Acessa banco
6. Retorna resposta

---

# 🌐 Cliente x Servidor

## 📱 Cliente
Quem consome o sistema:
- navegador
- app mobile
- outro sistema

## 🖥 Servidor
Onde roda o backend.

---

# 🔗 API (Application Programming Interface)

Conjunto de rotas que permitem comunicação entre sistemas.

### Exemplos:
- GET /produtos
- POST /usuarios
- POST /auth/login

---

# 🌍 HTTP (Protocolo Web)

HTTP define como cliente e servidor se comunicam.

---

## 📬 Métodos HTTP

| Método | Função |
|------|--------|
| GET | Buscar dados |
| POST | Criar |
| PUT | Atualizar |
| PATCH | Atualizar parcialmente |
| DELETE | Remover |

---

## 📊 Status Code

| Código | Significado |
|------|-------------|
| 200 | OK |
| 201 | Criado |
| 400 | Erro do cliente |
| 401 | Não autenticado |
| 403 | Sem permissão |
| 404 | Não encontrado |
| 500 | Erro interno |

---

# 📦 JSON

Formato de troca de dados.

### Exemplo:
```json
{
  "nome": "Alan",
  "idade": 20
}
