# Suasor Development Guide

## Build Commands
- **Backend**: `cd backend && make build` (Go)
- **Frontend**: `cd frontend && npm run build` (SvelteKit)
- **Docker**: `cd backend && make docker-build && make docker-run`

## Run Commands
- **Backend**: `cd backend && make run`
- **Frontend**: `cd frontend && npm run dev`

## Test Commands
- **Backend**: `cd backend && go test ./... -v` or `make test`
- **Backend (single test)**: `cd backend && go test ./path/to/package -run TestName`
- **Integration Tests**: `cd backend && INTEGRATION=true go test ./... -v`
- **Pretty Tests**: `cd backend && make pretty-test` (requires gotestsome)
- **Frontend**: `cd frontend && npm run test`
- **Frontend (unit tests)**: `cd frontend && npm run test:unit`
- **Frontend (single test)**: `cd frontend && npm run test:unit -- -t "test name"`

## Lint/Format Commands
- **Backend**: No specific linter configured, follow Go standard practices
- **Frontend**: `cd frontend && npm run lint` and `npm run format`

## Code Style Guidelines
- **Naming**: Use CamelCase for exported/public members, lower camelCase for private members
- **Interfaces**: Define interfaces with method signatures, document with comments
- **Types**: Use strong typing with generics where appropriate, avoid interface{} when possible
- **Error Handling**: Always check errors in Go, use typed errors package for consistent responses
- **Context**: Pass context as first parameter to functions, especially in service/repository layers
- **Imports**: Group standard library, third-party, and local imports with blank lines
- **Dependencies**: Use dependency injection pattern with interfaces for testability
- **TypeScript**: Strong typing throughout, interfaces for models, avoid any type
- **Svelte**: Follow SvelteKit best practices, component files must have .svelte extension