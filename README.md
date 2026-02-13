# Family Travel Tracker

> Um dashboard web para registrar países visitados por diferentes membros da família, acompanhar progresso de viagens e visualizar histórico de forma simples e intuitiva.

## Visão Geral
O **Family Travel Tracker** é uma aplicação full stack construída para centralizar o controle de viagens por usuário.  
Com ela, cada pessoa pode manter seu próprio mapa de países visitados, alternar perfis facilmente e adicionar novos destinos em poucos cliques.  
O projeto demonstra integração entre backend em Node.js, persistência relacional com PostgreSQL e renderização server-side com EJS.  

## Impacto e Resultado
- Permite acompanhamento individual do histórico de viagens por membro da família.
- Reduz atrito no registro de novos países com busca por nome.

## Aprendizados Técnicos Destacados
- Implementação de **CRUD parcial** com Express e PostgreSQL.
- Uso de **consultas SQL relacionais** com `JOIN` para consolidar dados por usuário.
- Organização de interface dinâmica com **EJS templates** e assets estáticos.
- Gerenciamento de configuração segura via variáveis de ambiente (`dotenv`).

## Stack Tecnológica
- **Node.js**
- **Express.js**
- **EJS**
- **PostgreSQL**
- **SQL**
- **dotenv**

## Funcionalidades Principais
- Seleção de usuário ativo para visualizar dados personalizados.
- Registro de países visitados por usuário.
- Cadastro de novos usuários com nome e cor de destaque no mapa.
- Contagem total de países visitados no perfil selecionado.

## Diferenciais do Projeto
- **Arquitetura simples e escalável** para evoluir com autenticação e multiusuário real.
- **Modelo relacional objetivo** (`users` + `visited_countries`) com boa base para crescimento.
- **Experiência prática de produto**: o sistema resolve um caso real de acompanhamento familiar de viagens.

## Preview
> _Adicione aqui um GIF ou screenshot da aplicação rodando para aumentar conversão com recrutadores._

![Preview do projeto](https://via.placeholder.com/1200x650.png?text=Family+Travel+Tracker+Preview)

## Como Rodar Localmente

### 1) Clone o repositório
```bash
git clone <URL_DO_REPOSITORIO>
cd family-travel-tracker-project
```

### 2) Instale as dependências
```bash
npm install
```

### 3) Configure as variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
PG_USER=seu_usuario
PG_HOST=localhost
PG_DATABASE=nome_do_banco
PG_PASSWORD=sua_senha
PG_PORT=5432
```

### 4) Crie as tabelas e dados iniciais
Execute o script SQL:
```bash
psql -U seu_usuario -d nome_do_banco -f queries.sql
```

### 5) Inicie a aplicação
```bash
nodemon index.js
```
A aplicação ficará disponível em: `http://localhost:3000`

## Estrutura do Projeto
```bash
family-travel-tracker-project/
├── index.js                # Servidor Express e regras de negócio
├── queries.sql             # Estrutura e seed inicial do banco PostgreSQL
├── package.json            # Dependências e metadados do projeto
├── public/
│   └── styles/             # Estilos CSS da interface
└── views/
    ├── index.ejs           # Tela principal com mapa/estatísticas
    └── new.ejs             # Tela de criação de usuário
```

<!--
## Melhorias Futuras
- Implementar autenticação real (login/sessão) por usuário.
- Adicionar validação de formulários e mensagens de erro amigáveis.
- Criar testes automatizados (unitários e integração).
- Disponibilizar deploy com CI/CD (ex.: Render, Railway ou Fly.io).
- Exibir métricas avançadas (continentes, últimos países adicionados, ranking familiar). 
-->

## 👨‍💻 Autor
Feito por **Henrique Costa**.  
Se este projeto te interessou, fique à vontade para conectar no LinkedIn e trocar ideias sobre backend, dados e produtos digitais.
