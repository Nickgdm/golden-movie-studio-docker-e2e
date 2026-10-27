<pre>
╔═════════════════════════════════════════════════════════════════════════════════════════════════════════╗
║                                  GOLDEN MOVIE STUDIO — DOCKER E TESTES E2E                              ║
╚═════════════════════════════════════════════════════════════════════════════════════════════════════════╝
</pre>
Aplicação de treinamento de QA que integra frontend, backend, persistência SQLite e testes end-to-end com Cypress, utilizando Docker Compose para organizar os serviços.

## Sobre o projeto

O repositório permite estudar a inicialização coordenada de uma aplicação web e a execução de testes E2E em um ambiente baseado em containers.

## Objetivos

- Preparar um ambiente reproduzível usando containers.
- Integrar frontend e backend de uma aplicação de exemplo.
- Executar testes end-to-end com Cypress.
- Consultar logs, vídeos e capturas de tela para auxiliar a análise.

## Tecnologias e ferramentas

- Docker e Docker Compose
- Node.js
- API REST
- SQLite
- Cypress
- HTML, CSS e JavaScript

## Pré-requisitos

- Docker Engine e Docker Compose instalados.
- Git instalado.
- Portas utilizadas pelos serviços disponíveis no computador.

## Como executar

1. Clone o repositório e acesse o diretório do projeto.
2. Confira as variáveis e as portas definidas em `docker-compose.yml`.
3. Inicie os serviços:

```bash
docker compose up --build
```

4. O serviço `cypress` está definido no Compose para executar `npx cypress run` após a inicialização dos serviços da aplicação. Acompanhe os logs para verificar o resultado.
5. Os vídeos e as capturas de tela são montados nos diretórios locais `cypress-videos/` e `cypress-screenshots/`, conforme a configuração do Compose.

Para encerrar os serviços:

```bash
docker compose down
```

## Estrutura do projeto

```text
atividade-docker/
├── .github/
├── golden-movie-studio-backend/
├── golden-movie-studio-frontend/
├── tests/
├── cypress.config.js
├── docker-compose.yml
└── README.md
```

## Desafios práticos

- Coordenar serviços que dependem uns dos outros.
- Configurar portas e variáveis de ambiente.
- Verificar a persistência de dados quando aplicável.
- Executar testes contra o ambiente inicializado.

## Boas práticas

- Definir o ambiente por meio do Docker Compose.
- Separar frontend, backend e testes.
- Consultar logs para auxiliar o diagnóstico.
- Confirmar o resultado dos testes nos logs do container `gms-cypress`.

## Aprendizados

A atividade permite praticar a containerização de uma aplicação web e compreender como frontend, backend, banco de dados e testes E2E se integram em um ambiente de desenvolvimento e validação.

## Considerações finais

Consulte `docker-compose.yml` para verificar portas, nomes de serviços e volumes. Embora o serviço de testes seja definido no Compose, o resultado da execução deve ser confirmado nos logs do container `gms-cypress`.
<pre>
╔═════════════════════════════════════════════════════════════════════════════════════════════════════════╗
║       Atividade desenvolvida durante a formação profissionalizante em Quality Assurance (QA) pela       ║
║                     EBAC — Escola Britânica de Artes Criativas e Tecnologia                             ║
╚═════════════════════════════════════════════════════════════════════════════════════════════════════════╝
</pre>
