# Penvire

An open-source platform for penetration testing consultancies, covering the day-to-day work from engagements to evidence and reporting.

> **Status:** early development. Nothing here is ready for production use yet.

## Two projects

**Penvire** is the product. It uses proven components for the security-critical parts, such as Keycloak or another OpenID provider for authentication, and never ships hand-written authentication.

**Penvire Lab** is a learning project. It implements those security-critical parts by hand (an OpenID provider, token exchange, tenant isolation, a tamper-evident audit trail) to learn where they fail. It never runs in production and never holds real data. Lab and product share no code.

## Repositories

| | Product | Lab |
| --- | --- | --- |
| Contracts (OpenAPI, AsyncAPI, Avro) | [penvire-contracts](https://github.com/Penvire/penvire-contracts) | [penvire-lab-contracts](https://github.com/Penvire/penvire-lab-contracts) |
| Backend services | [penvire-backend](https://github.com/Penvire/penvire-backend) | [penvire-lab-backend](https://github.com/Penvire/penvire-lab-backend) |
| Web UI and clients | [penvire-client](https://github.com/Penvire/penvire-client) | [penvire-lab-client](https://github.com/Penvire/penvire-lab-client) |
| Documentation | [penvire-docs](https://github.com/Penvire/penvire-docs) | in penvire-lab-backend |

Contracts are licensed under Apache-2.0, backend and clients under AGPL-3.0, and documentation under CC-BY-4.0.

## Contributing

Commits must be signed and follow [Conventional Commits](https://www.conventionalcommits.org/). Pull requests are merged with a merge commit, so every commit in a pull request ends up on `main`.

## Security

Please report vulnerabilities privately. See [SECURITY.md](https://github.com/Penvire/.github/blob/main/SECURITY.md).
