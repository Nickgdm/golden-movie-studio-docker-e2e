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
4. Acompanhe os logs e confirme que frontend e backend iniciaram corretamente.
5. Consulte a configuração do Cypress e a pasta `tests/` para executar os cenários. Se os testes estiverem fora dos containers, instale as dependências correspondentes antes de executá-los.

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
Consulte o `docker-compose.yml` para verificar portas, nomes de serviços e volumes. Não presuma que os testes estejam executando automaticamente apenas porque os containers iniciaram.

---

## 🎓 Formação
Atividade desenvolvida durante a formação profissionalizante em **Quality Assurance (QA) pela EBAC — Escola Britânica de Artes Criativas e Tecnologia**.