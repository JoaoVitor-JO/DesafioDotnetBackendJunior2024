# 📇 Projeto Backend – enContact API

🚀 Projeto backend desenvolvido em **.NET / C#**, baseado no desafio técnico da **enContact**, com foco em **boas práticas, arquitetura limpa e consultas eficientes**.

Mais do que apenas “fazer funcionar”, o objetivo foi **entender as decisões técnicas**, lidar com problemas reais de backend e construir uma API organizada, extensível e bem documentada.

---

## 🧩 Sobre o desafio

O desafio proposto pela enContact simula situações comuns do dia a dia no desenvolvimento backend, incluindo:

- Código com pontos de melhoria
- Possíveis bugs e problemas de performance
- Necessidade de refatoração
- Implementação correta de regras de negócio
- Uso eficiente de SQL e banco de dados

A aplicação consiste em uma **API REST para cadastro, importação e consulta de contatos em agendas**, com vínculo opcional a empresas.

🔗 Desafio original:  
https://github.com/EnkiGroup/DesafioDotnetBackendJunior2024

---

## 🛠️ Tecnologias utilizadas

- **C# / .NET**
- **ASP.NET Core (Web API)**
- **SQLite**
- **Dapper / Dapper.Contrib**
- **Swagger (OpenAPI)**
- **SQL (JOINs, filtros dinâmicos, paginação)**

---

## 🏗️ Arquitetura e conceitos aplicados

- Repository Pattern
- Service Layer
- Separação de responsabilidades (Domínio, Persistência e API)
- DTOs / DAOs para mapeamento de dados
- Tratamento de erros e nulls
- Contratos bem definidos com interfaces
- Consultas SQL performáticas e legíveis

---

## ✅ Funcionalidades implementadas

### 📒 Agendas
- Criar, editar, excluir e listar agendas

### 🏢 Empresas
- Criar, editar, excluir e listar empresas

### 📥 Importação de contatos via CSV
- Leitura de arquivos `.csv`
- Importação registro a registro
- Erros em um contato não interrompem a importação
- Contato deve obrigatoriamente estar vinculado a uma agenda
- Empresa informada no CSV deve existir previamente
- Contato pode ser criado sem empresa

### 🔍 Pesquisa de contatos
- Busca em qualquer campo do contato:
  - Nome
  - Email
  - Telefone
  - Endereço
  - Nome da empresa
- Entrada única de texto (estilo Google)
- Paginação com `page` e `pageSize`

### 🗂️ Pesquisa de contatos agrupados por agenda
- Pesquisa por nome ou parte do nome do contato
- Retorno agrupado por agenda

Exemplo de resposta:
```json
[
  {
    "contactBookId": 1,
    "contactBookName": "Agenda Pessoal",
    "contacts": [
      {
        "id": 10,
        "name": "João Silva",
        "email": "joao@email.com"
      }
    ]
  }
]
```

---

## 📑 Documentação da API

A API é totalmente documentada com **Swagger**, permitindo:

- Testar endpoints diretamente pelo navegador
- Visualizar parâmetros de busca e paginação
- Validar contratos de entrada e saída

Após executar o projeto, acesse:
```
http://localhost:{porta}/swagger
```

---

## 🧠 Aprendizados

Durante o desenvolvimento, este projeto reforçou conceitos importantes como:

- A importância da separação entre domínio, persistência e transporte de dados
- Como pequenos erros de rota ou mapeamento podem quebrar uma API
- Uso consciente de SQL ao invés de abstrações excessivas
- Como paginação e agrupamento impactam diretamente a performance
- Benefícios de contratos claros usando interfaces

---

## 🚀 Próximos passos (evoluções possíveis)

- Testes automatizados
- Autenticação e autorização
- Cache para consultas frequentes
- Paginação com metadados (total de registros, total de páginas)
- Versionamento da API

---

## 👨‍💻 Autor

Projeto desenvolvido por **João Vitor**  
📌 Backend | .NET | SQL | Automação | 

