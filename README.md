# Renan Rohers

Desenvolvimento backend com Java e Spring Boot. Meu foco está em sistemas distribuídos, autorização contextual e rastreabilidade: entender como os serviços se comunicam, tomam decisões e preservam o histórico necessário para explicar seu comportamento.

Meu principal projeto está reunido na organização **[Consent & Audit Architecture](https://github.com/consent-audit-arch)**. Lá você encontra os serviços, a documentação e o caminho para executar a demonstração.

## Projeto em destaque

### [Consent & Audit Architecture](https://github.com/consent-audit-arch/infra#readme)

**Quem pode usar um dado pessoal, para qual finalidade — e como investigar essa decisão depois?**

Um projeto pessoal que nasceu no meu TCC e conecta gerenciamento de consentimento, políticas de autorização e auditoria em uma arquitetura de microsserviços. O console permite conceder consentimento, executar uma consulta protegida, revogar a autorização e investigar as decisões na linha do tempo.

- **Autorização:** Keycloak para identidade, Open Policy Agent para decisões e uma biblioteca Spring compartilhada para aplicar o controle nos serviços.
- **Histórico:** Event Sourcing para registrar mudanças de consentimento, com projeção síncrona para as consultas de autorização.
- **Integração:** outbox e Kafka para propagar eventos às visões de auditoria e métricas.
- **Exploração:** console React com cenários de cobrança, promoções e investigação histórica.

[Arquitetura e diagramas](https://github.com/consent-audit-arch/infra/blob/main/docs/architecture.md) · [Executar localmente](https://github.com/consent-audit-arch/infra#executar-localmente) · [Roteiro de demonstração](https://github.com/consent-audit-arch/infra/blob/main/docs/demo.md)

## Tecnologias usadas no projeto

| Área | Tecnologias |
| --- | --- |
| Backend | Java 21, Spring Boot, Maven |
| Identidade e autorização | Spring Security, OAuth2/JWT, Keycloak, OPA/Rego |
| Dados e mensageria | PostgreSQL, MongoDB, Apache Kafka |
| Frontend | React, TypeScript, Vite, Tailwind CSS |
| Ambiente local | Docker, Docker Compose, Bash |

## Componentes para conhecer

- [Security Starter](https://github.com/consent-audit-arch/tcc-security-starter): enforcement reutilizável e publicação das decisões de autorização.
- [Consent Command](https://github.com/consent-audit-arch/consent-command-service): eventos, projeção e outbox na transação do comando.
- [Audit Service](https://github.com/consent-audit-arch/audit-service): decisões correlacionadas ao histórico do consentimento.
- [Console](https://github.com/consent-audit-arch/consent-frontend): interface para explorar os fluxos e inspecionar os registros.
