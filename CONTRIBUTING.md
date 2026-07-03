# Contributing to Evship

## Before You Start

- Check existing issues and PRs to avoid duplicate work
- For large changes, open an issue first to discuss approach
- All contributions must follow the code standards below

## Development Setup

```bash
git clone https://github.com/Saifulhuq01/evship
cd evship
cp .env.example .env
docker compose -f infra/docker/docker-compose.yml up -d
mvn package
```

## Code Standards

- Java 21, Spring Boot 3.3, production-ready code only
- No TODOs or placeholder comments in merged code
- Every class must have a corresponding test
- All DB time calculations must use server NOW(), never JVM clock

## Pull Request Process

1. Branch from develop: `git checkout -b feature/your-feature develop`
2. Write code and tests
3. Run: `mvn verify` (must pass)
4. Open PR to develop (never directly to main)
5. Fill in the PR template completely

## Commit Message Format

```
feat: add EndpointClaimService with pod_id guard on release
fix: prevent Reaper from resetting IN_FLIGHT rows of live pods
docs: add ADR-009 for payload offload strategy
test: add DispatchIntegrationTest for double delivery scenario
```
