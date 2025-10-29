# 🚀 Minimal API com .NET 7 e MySQL

Este projeto é uma **Minimal API** desenvolvida em **.NET 7**, com integração ao **MySQL**, seguindo boas práticas de arquitetura em camadas.  
A aplicação implementa endpoints para gerenciamento de **administradores** e **veículos**, utilizando **Entity Framework Core** para persistência de dados.

## 📂 Estrutura do Projeto

```

minimal-api/
└── Api/
├── Program.cs
├── Startup.cs
├── appsettings.json
├── Dominio/
│   ├── DTOs/
│   ├── Entidades/
│   ├── Enuns/
│   ├── Interfaces/
│   ├── ModelViews/
│   └── Servicos/
├── Infraestrutura/
│   └── Db/DbContexto.cs
├── Migrations/
└── Properties/

````

**Principais diretórios:**
- `Dominio/` → Regras de negócio, DTOs, entidades, serviços e interfaces.  
- `Infraestrutura/` → Configuração de acesso ao banco e contexto do Entity Framework.  
- `Migrations/` → Scripts de migração do banco de dados.  
- `Program.cs` e `Startup.cs` → Inicialização e configuração da aplicação.

## 🧠 Tecnologias Utilizadas

- [.NET 7](https://dotnet.microsoft.com/)
- [Entity Framework Core](https://docs.microsoft.com/ef/)
- [MySQL](https://www.mysql.com/)
- [Swagger UI](https://swagger.io/) (para documentação e testes de endpoints)
- [C#](https://learn.microsoft.com/dotnet/csharp/)

## ▶️ Como Executar o Projeto

1. **Clonar o repositório:**

   ```bash
   git clone https://github.com/seuusuario/minimal-api.git
   cd minimal-api/Api
   ```

2. **Restaurar dependências:**

   ```bash
   dotnet restore
   ```

3. **Executar a API:**

   ```bash
   dotnet run
   ```

4. **Acessar no navegador:**

   ```
   http://localhost:5004/swagger
   ```

---

## 🧩 Endpoints Principais

### 🔐 Administradores

| Método | Endpoint                     | Descrição                      |
| ------ | ---------------------------- | ------------------------------ |
| `POST` | `/api/administradores/login` | Realiza login do administrador |
| `GET`  | `/api/administradores`       | Lista todos os administradores |
| `POST` | `/api/administradores`       | Cria um novo administrador     |

### 🚗 Veículos

| Método   | Endpoint             | Descrição                     |
| -------- | -------------------- | ----------------------------- |
| `GET`    | `/api/veiculos`      | Lista todos os veículos       |
| `POST`   | `/api/veiculos`      | Cadastra um novo veículo      |
| `PUT`    | `/api/veiculos/{id}` | Atualiza um veículo existente |
| `DELETE` | `/api/veiculos/{id}` | Remove um veículo             |
