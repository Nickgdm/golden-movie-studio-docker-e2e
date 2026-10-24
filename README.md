# Golden Movie Studio — Docker e Testes E2E

Aplicação de treinamento de QA que integra frontend, backend, persistência SQLite e testes end-to-end com Cypress, com serviços containerizados por Docker Compose.

## Objetivos
- Preparar um ambiente reproduzível usando containers.
- Integrar frontend e backend de uma aplicação de exemplo.
- Executar testes end-to-end com Cypress.

## Tecnologias
- Docker e Docker Compose
- Node.js
- API REST
- SQLite
- Cypress
- HTML, CSS e JavaScript

## Pré-requisitos
- Docker Engine e Docker Compose instalados.
- Git.
- Portas usadas pelos serviços disponíveis no computador.

## Como executar
1. Clone o repositório e acesse a pasta.
2. Confira as variáveis e portas definidas no `docker-compose.yml`.
3. Inicie os serviços:
```bash
docker compose up --build
```
4. O serviço `cypress` está definido no `docker-compose.yml` e executa `npx cypress run` após os serviços de aplicação iniciarem. Acompanhe os logs para conferir o resultado dos testes.
5. Os vídeos e screenshots são montados nos diretórios locais `cypress-videos/` e `cypress-screenshots/`, conforme a configuração do Compose.

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
Coordenar serviços que dependem uns dos outros, configurar portas e variáveis, garantir persistência quando aplicável e executar testes contra o ambiente inicializado.

## Boas práticas adotadas
- Definição do ambiente com Docker Compose.
- Separação de frontend, backend e testes.
- Logs disponíveis para auxiliar o diagnóstico.

## 📚 Aprendizados
A atividade permitiu praticar containerização de uma aplicação web e compreender como frontend, backend, banco de dados e testes E2E se integram em um ambiente de desenvolvimento e validação.

## Considerações finais
Consulte o `docker-compose.yml` para verificar portas, nomes de serviços e volumes. O serviço de testes é iniciado pelo Compose, mas a conclusão e o resultado dos testes devem ser confirmados nos logs do container `gms-cypress`.

---

## 🎓 Formação
Atividade desenvolvida durante a formação profissionalizante em **Quality Assurance (QA) pela EBAC — Escola Britânica de Artes Criativas e Tecnologia**.