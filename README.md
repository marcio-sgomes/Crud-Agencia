# Crud-Agencia

> 📦 Projeto de estudo — não recebe mais atualizações.

Trabalho de CRUD feito com Java (fevereiro de 2022): cadastro, busca, edição e exclusão de clientes de uma agência, usando Servlets, JSP e JDBC com MySQL.

## Contexto

Faz parte de uma série de repositórios do mesmo trabalho (agência de viagens com CRUD de clientes, 2022):

| Repositório | Data | O que é |
|---|---|---|
| [projeto-agencia](https://github.com/marcio-sgomes/projeto-agencia) | fev/2022 | Primeira landing page em React (tema Start Bootstrap Grayscale) |
| **Crud-Agencia** | fev/2022 | Primeiro CRUD de clientes em Java (este repositório) |
| [front-back](https://github.com/marcio-sgomes/front-back) | mar/2022 | Versão intermediária: API Spring Boot + front React |
| [agencia-plus](https://github.com/marcio-sgomes/agencia-plus) | mar/2022 | **Versão final**, com diagramas e script do banco |

## Tecnologias

- Java com Servlets (`javax.servlet`) e JSP/JSTL.
- JDBC + MySQL Connector 8.0.28 (o `.jar` está em `WEB-INF/lib`).
- HTML, Bootstrap 3 e o tema [Start Bootstrap Grayscale](https://startbootstrap.com/theme/grayscale/) nas páginas.

## Estrutura

```
src/main/java/controllers/   Servlets: /CreateAndFind, /ClienteUpdate, /ClienteDestroy
src/main/java/dao/           Acesso ao banco (ClienteDao)
src/main/java/db/            Conexão JDBC (MySqlConnection)
src/main/java/model/         Classe Cliente
src/main/webapp/             Páginas (index.html, lista.jsp, formUpdate.jsp) e estáticos
```

## Como abrir

1. Importe a pasta no Eclipse como *Dynamic Web Project* e configure um Tomcat 9 (usa `javax.servlet`).
2. Crie no MySQL o banco `java` com a tabela `clientes` (colunas `id`, `nome`, `cpf`, `nascimento`, `situacao`).
3. Copie `.env.example` para `.env` como referência e defina as variáveis `DB_URL` (padrão `jdbc:mysql://localhost:3306/java`), `DB_USER` (padrão `root`) e `DB_PASSWORD` na configuração do servidor (o Tomcat não lê o `.env` sozinho).
4. Rode no Tomcat e acesse a página inicial do projeto.
