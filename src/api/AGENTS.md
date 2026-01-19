# Agent Instructions — API Component

## Scope
Applies only to `src/api`.

## API rules
- Do not introduce breaking changes without versioning plan.
- Keep controller endpoints thin; business logic stays in services.
- Validate inputs explicitly; return consistent error shapes.
- Ensure auth/authorization is preserved; do not relax policies.

## Tests
- Add/adjust unit tests for services.
- Add/adjust integration tests if endpoints or auth behavior changes.

## Observability
- Use structured logging; never log request bodies if they may contain PII.
