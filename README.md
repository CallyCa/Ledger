# Ledger

API para gerenciamento de informações financeiras.

> O projeto está em fase inicial de estruturação. A definição detalhada da arquitetura e dos principais módulos será realizada posteriormente.

## Tecnologias e versões

- .NET SDK 10 LTS
- ASP.NET Core 10
- PostgreSQL 18
- Entity Framework Core

As versões foram fixadas conforme a ADR [`001-definir-versoes-dotnet-postgresql`](docs/adr/001-definir-versoes-dotnet-postgresql.md).

## Pré-requisitos

Antes de executar o projeto, instale:

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)
- [PostgreSQL 18](https://www.postgresql.org/download/)
- Git

Verifique as instalações com:

```powershell
dotnet --version
psql --version
git --version
```

## Clonando o projeto

```powershell
git clone https://github.com/CallyCa/Ledger.git
cd Ledger
```

## Restaurando as dependências

```powershell
dotnet restore Ledger.slnx
```

## Compilando o projeto

```powershell
dotnet build Ledger.slnx
```

## Executando os testes

```powershell
dotnet test Ledger.slnx
```

## Executando a API

A partir da raiz do repositório:

```powershell
dotnet run --project src/Ledger.Api/Ledger.Api.csproj
```

Por padrão, a API estará disponível em:

- HTTPS: `https://localhost:5000`


## Estrutura de diretórios

```text
.
├── docs/
│   └── adr/
│       └── 001-definir-versoes-dotnet-postgresql.md
├── src/
│   └── Ledger.Api/
│       ├── Properties/
│       │   └── launchSettings.json
│       ├── appsettings.json
│       ├── Ledger.Api.csproj
│       └── Program.cs
├── tests/
│   └── Ledger.Api.Tests/
│       └── Ledger.Api.Tests.csproj
├── .editorconfig
├── .gitignore
├── Ledger.slnx
└── README.md
```

- `docs/adr/`: registros de decisões de arquitetura (ADRs).
- `src/Ledger.Api/`: projeto principal da API.
- `tests/Ledger.Api.Tests/`: projeto de testes automatizados.
- `Program.cs`: ponto de entrada e configuração inicial da aplicação.
- `appsettings.json`: configurações da aplicação.
- `Ledger.slnx`: arquivo da solução.
- `README.md`: documentação básica para configuração e execução do projeto.

## Banco de dados

A configuração de conexão, o modelo de dados e as migrações ainda serão definidos conforme a arquitetura e os requisitos funcionais forem estabelecidos.

## Arquitetura

A arquitetura da aplicação ainda será definida em uma etapa posterior. A estrutura atual representa apenas a base inicial da API, da solução e do projeto de testes.
