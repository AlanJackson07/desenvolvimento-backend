# 📚 Resumo: Fundamentos de Backend e NestJS

## 1. O Ecossistema Web
O fluxo da internet baseia-se no modelo **Cliente-Servidor**.

* **Cliente (Frontend):** Quem consome o sistema e faz a requisição (ex: Navegador, App mobile).
* **Servidor (Backend):** Onde roda a aplicação. Recebe a requisição, processa regras de negócio, acessa o banco de dados e devolve uma resposta.
* **API (Application Programming Interface):** Conjunto de rotas que permite a comunicação entre o Cliente e o Servidor.
* **Banco de Dados:** Onde os dados são persistidos (ex: PostgreSQL, MongoDB).

> **Atenção:** O backend **não** cuida de telas, botões ou CSS. Ele lida com validações, autenticação, regras de negócio e persistência de dados.

---

## 2. Comunicação: HTTP e JSON

A comunicação Web ocorre via protocolo **HTTP**. Os dados geralmente trafegam no formato **JSON** (texto leve e estruturado).

### Métodos HTTP Principais
| Método | Ação | Exemplo de Uso |
|:---|:---|:---|
| `GET` | Buscar/Ler | Listar produtos ou buscar um aluno por ID |
| `POST` | Criar | Cadastrar um novo usuário |
| `PUT` | Atualizar (Tudo) | Atualizar o perfil completo do usuário |
| `PATCH` | Atualizar (Parte) | Atualizar apenas a senha |
| `DELETE` | Remover | Excluir um registro |

### Códigos de Status (Status Codes)
| Código | Categoria | Significado |
|:---|:---|:---|
| `200` | Sucesso | OK (Requisição processada com sucesso) |
| `201` | Sucesso | Created (Recurso criado, muito usado com POST) |
| `204` | Sucesso | No Content (Sucesso, mas sem corpo de resposta) |
| `400` | Erro Cliente | Bad Request (Requisição inválida/faltou dado) |
| `401` | Erro Cliente | Unauthorized (Usuário não autenticado) |
| `403` | Erro Cliente | Forbidden (Sem permissão de acesso) |
| `404` | Erro Cliente | Not Found (Rota ou recurso não existe) |
| `500` | Erro Servidor| Internal Server Error (Erro no código do backend) |

---

## 3. Node.js e a Necessidade de Frameworks

* **Node.js:** Ambiente de execução que permite rodar JavaScript/TypeScript no servidor (backend), fora do navegador. É assíncrono e orientado a eventos.
* **Por que usar um Framework?** Fazer tudo em Node.js puro gera código bagunçado e difícil de escalar. Frameworks trazem organização, padrões e ferramentas prontas.

---

## 4. O Framework NestJS

O **NestJS** é um framework backend para Node.js construído com TypeScript. Ele é modular e usa forte tipagem e injeção de dependências.

### Arquitetura Básica (Pilares do NestJS)
1. **Modules (`.module.ts`):** Agrupam a aplicação em blocos lógicos (ex: Módulo de Usuários, Módulo de Vendas).
2. **Controllers (`.controller.ts`):** Recebem as requisições HTTP e definem as rotas. Não devem conter lógica pesada.
3. **Services (`.service.ts`):** Contêm as regras de negócio. Fazem os cálculos e acessam o banco de dados.

### Fluxo de uma Requisição no NestJS
```mermaid
flowchart TD
    A[Request HTTP] --> B[Controller]
    B --> C[Service]
    C --> D[Banco de Dados]
    D --> C
    C --> B
    B --> F[Response HTTP]
