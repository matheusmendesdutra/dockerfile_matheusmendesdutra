Automação de Build, Testes e Deploy com Docker e GitHub Actions
Este projeto automatiza o processo de build, testes e deploy de uma aplicação web composta por React (front-end), Node.js/Express (back-end) e PostgreSQL (banco de dados) usando Docker e GitHub Actions.

Estrutura
Frontend: Aplicação React (porta 3000).
Backend: API Node.js/Express (porta 5000).
Banco de Dados: PostgreSQL (porta 5432).
Como Funciona
Dockerfiles: Cada componente da aplicação (front-end, back-end e banco de dados) tem seu próprio Dockerfile para construir imagens Docker.
GitHub Actions: Dois workflows principais:
Build and Test: Constrói as imagens Docker e executa os testes.
Deploy: Publica as imagens no Docker Hub e realiza o deploy (simulado) para produção.
Configuração
GitHub Secrets: Configure os secrets DOCKER_USERNAME e DOCKER_PASSWORD no GitHub para autenticação com o Docker Hub.
Automação: Os workflows são acionados automaticamente em cada push para a branch main.
Rodando Localmente
Clone o repositório e construa as imagens Docker para cada componente.
Execute os containers localmente:
Frontend: docker run -p 3000:3000 my-react-app
Backend: docker run -p 5000:5000 my-node-app
Banco de dados: docker run -p 5432:5432 my-postgres-db
Objetivo
O objetivo é automatizar todo o processo de desenvolvimento e deploy usando Docker e GitHub Actions, garantindo que as imagens Docker sejam construídas, testadas e publicadas automaticamente sempre que houver atualizações no código.