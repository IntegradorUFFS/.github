# Projeto Habitafort

## Integrantes
- Carlos Giovane Neu Nogueira (2311100010)
- Júlio Carvalho Gonçalves (2311100012)
- Marco Antônio Duz (2311100006)

## Visão Geral

Este projeto é uma iniciativa da *Habitafort*, uma construtora e incorporadora sediada em Chapecó, focada na construção de edifícios residenciais de pequeno a médio porte. A empresa tem como missão entregar imóveis acessíveis, com alta qualidade e ótimo padrão de acabamento, através de parcerias estratégicas com instituições financeiras e imobiliárias.

[https://github.com/IntegradorUFFS/requisitos/blob/main/Relato%CC%81rio%20-%20Projeto%20Integrador.pdf](https://github.com/IntegradorUFFS/requisitos/blob/main/Relat%C3%B3rio%20-%20Projeto%20Integrador.pdf)

## Objetivo do Projeto

O principal objetivo deste projeto é desenvolver um *sistema web intuitivo* que possibilite à Habitafort gerenciar de forma eficiente os insumos utilizados em suas obras. A equipe terá acesso rápido e fácil às informações sobre os materiais empregados, permitindo um controle rigoroso que evita desperdícios e otimiza o fluxo de trabalho.

## Expectativas do Produto

-  ⁠*Controle de Insumos*: O sistema permitirá que um profissional específico, responsável pelo controle de compras, gerencie os insumos restantes das obras de maneira totalmente digitalizada.
-  ⁠*Acesso Rápido*: A equipe terá acesso prático às informações em diversos dispositivos, garantindo que todos possam consultar os dados necessários a qualquer momento.

## Pré-requisitos

- Node.js (versão 14 ou superior)
- Go (versão 1.16 ou superior)
- PostgreSQL (instalado e rodando)

1. Clone os repositórios:
   
```bash
git clone https://github.com/IntegradorUFFS/back
git clone https://github.com/IntegradorUFFS/front
```

## Configurando o Frontend (React + Vite)

1. Acesse o diretório do projeto:

```bash
cd frontend
```

2. Instale as dependências do projeto:

```bash
npm install
```

3. Execute o projeto em ambiente de desenvolvimento:

```bash
npm run dev
```

O projeto React estará rodando em `http://localhost:5173`.

## Configurando o Backend (API em Go)

1. Acesse o diretório backend:

```bash
cd backend
```

2. Instale as dependências:

```bash
go mod tidy
```

2. Rode as migrações:

```bash
go install github.com/jackc/tern/v2@latest

go generate ./...
```

3. Configure o PostgreSQL e defina as variáveis de ambiente no arquivo `.env`:

```bash
DATABASE_PORT = 
DATABASE_HOST = 
DATABASE_USER = 
DATABASE_PASSWORD = 
DATABASE = 
JWT_SECRET = 
```

4. Execute a API:

```bash
 go run cmd/router/main.go
```

A API estará disponível em `http://localhost:8080`.

## Rodando o Projeto Completo

Com o frontend e o backend configurados e rodando, acesse `http://localhost:5173` para interagir com a aplicação React e fazer requisições para a API em Go.

## Scripts Disponíveis

### Frontend

- `npm run dev`: Executa o servidor de desenvolvimento do Vite.
- `npm run build`: Cria a versão de produção do aplicativo.
- `npm run preview`: Visualiza a versão de produção.

### Backend

- `go run cmd/router/main.go`: Executa o servidor da API Go.

## Tecnologias Usadas

- [React](https://reactjs.org/)
- [Vite](https://vitejs.dev/)
- [Go](https://golang.org/)
- [PostgreSQL](https://www.postgresql.org/)
