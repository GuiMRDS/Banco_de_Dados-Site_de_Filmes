# 🎬 Desafio de Banco de Dados — Site de Filmes

![T-SQL](https://img.shields.io/badge/T--SQL-CC2927?style=flat&logo=microsoft-sql-server&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat&logo=microsoft-sql-server&logoColor=white)
![DIO](https://img.shields.io/badge/DIO-Trilha_.NET-512BD4?style=flat)

Desafio de projeto desenvolvido como parte da **Trilha .NET** da [Digital Innovation One (DIO)](https://www.dio.me/), módulo de **Banco de Dados**. O objetivo é aplicar conhecimentos em **modelagem relacional e consultas SQL** em um cenário realista de um site de filmes.

---

## 📋 Sobre o Desafio

Você foi designado como responsável pelo banco de dados de um site de filmes. O banco contém informações sobre filmes, atores e gêneros, com **relacionamentos muitos para muitos**, exigindo domínio de `JOIN`, filtros, agrupamentos e ordenações.

O desafio consiste em executar **12 consultas SQL** específicas que respondem a perguntas reais de negócio sobre os dados.

---

## 🗂️ Estrutura do Banco de Dados

O banco se chama **Filmes** e é composto pelas seguintes tabelas:

| Tabela | Descrição |
|---|---|
| `Filmes` | Dados dos filmes: ID, Nome, Ano, Duração |
| `Atores` | Dados dos atores: ID, PrimeiroNome, UltimoNome, Genero |
| `Generos` | Gêneros disponíveis: ID, Nome |
| `ElencoFilme` | Relaciona filmes e atores + Papel desempenhado |
| `FilmesGenero` | Relaciona filmes e seus gêneros |

### 🔗 Relacionamentos

```
Filmes ──< ElencoFilme >── Atores
Filmes ──< FilmesGenero >── Generos
```

- Um filme pode ter **vários gêneros** e um gênero pode pertencer a **vários filmes**
- Um filme pode ter **vários atores** e um ator pode participar de **vários filmes**

---

## 🎯 As 12 Consultas

| # | Descrição |
|---|---|
| 1 | Buscar o **nome e ano** dos filmes |
| 2 | Buscar o nome e ano dos filmes, ordenados por **ano crescente** |
| 3 | Buscar o filme **"De Volta para o Futuro"** com nome, ano e duração |
| 4 | Buscar os filmes lançados em **1997** |
| 5 | Buscar os filmes lançados **após o ano 2000** |
| 6 | Buscar os filmes com duração **entre 100 e 150 minutos**, ordenados pela duração |
| 7 | Buscar a **quantidade de filmes por ano**, agrupando e ordenando de forma decrescente |
| 8 | Buscar os **atores do gênero masculino** |
| 9 | Buscar as **atrizes do gênero feminino**, ordenando pelo primeiro nome |
| 10 | Buscar o **nome do filme e seu gênero** |
| 11 | Buscar o nome do filme e o gênero apenas do tipo **"Mistério"** |
| 12 | Buscar o **nome do filme, atores e o papel** desempenhado por cada um |

---

## 🗃️ Estrutura do Repositório

```
Banco_de_dados/
├── Imagens/                  # Prints dos resultados esperados de cada consulta
├── Script Desafio            # Scripts SQL com as 12 consultas resolvidas
├── Script Filmes.sql         # Script de criação e população do banco de dados
└── README.md
```

---

## 🚀 Como Executar

### Pré-requisitos

- [SQL Server](https://www.microsoft.com/pt-br/sql-server/sql-server-downloads) instalado
- [SSMS](https://learn.microsoft.com/pt-br/sql/ssms/download-sql-server-management-studio-ssms) (SQL Server Management Studio) ou [Azure Data Studio](https://azure.microsoft.com/pt-br/products/data-studio)

### Passo a passo

**1. Clone o repositório**
```bash
git clone https://github.com/GuiMRDS/Banco_de_dados.git
```

**2. Crie o banco e popule os dados**

Abra o SSMS, conecte ao seu servidor e execute:
```sql
-- Execute o arquivo Script Filmes.sql
-- Isso criará o banco "Filmes" com todas as tabelas e dados
```

**3. Execute as consultas do desafio**

Abra o arquivo `Script Desafio` e execute cada consulta individualmente para verificar os resultados.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| T-SQL (Transact-SQL) | Linguagem de consulta utilizada |
| SQL Server | Banco de dados relacional |
| SSMS / Azure Data Studio | Ferramentas de gerenciamento |
| Git / GitHub | Versionamento de código |

---

## 📚 Conceitos Praticados

- `SELECT` com múltiplas colunas e aliases
- `WHERE` com filtros simples e compostos (`AND`, `BETWEEN`, `>`, `<`)
- `ORDER BY` crescente e decrescente
- `GROUP BY` com `COUNT` para agrupamento de dados
- `JOIN` entre tabelas com chaves estrangeiras
- Relacionamentos **muitos para muitos** via tabelas intermediárias
- Consultas analíticas para responder perguntas de negócio

---

## 🎓 Contexto Acadêmico

> Projeto desenvolvido como desafio da **Trilha .NET** da **Digital Innovation One (DIO)**, módulo de Banco de Dados.
>
> Fork do repositório original: [digitalinnovationone/trilha-net-banco-de-dados-desafio](https://github.com/digitalinnovationone/trilha-net-banco-de-dados-desafio)

---

## 👨‍💻 Autor

**Guilherme Marinho**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-guilherme--marinho04-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/guilherme-marinho04/)
[![GitHub](https://img.shields.io/badge/GitHub-GuiMRDS-black?style=flat&logo=github)](https://github.com/GuiMRDS)
[![Email](https://img.shields.io/badge/Email-guimars22%40gmail.com-red?style=flat&logo=gmail)](mailto:guimars22@gmail.com)

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte de um desafio da DIO.
