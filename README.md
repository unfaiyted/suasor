# Suasor

Suasor is a comprehensive media management and AI integration platform that provides a unified interface for interacting with various media services and AI tools.

## Features

- **Media Server Integration**: Connect to Plex, Jellyfin, Emby, and Subsonic to access and manage your media libraries
- **AI-Powered Recommendations**: Use AI models (Claude, OpenAI, Ollama) to generate personalized recommendations based on your viewing/listening history
- **Automation Integration**: Support for Radarr, Sonarr, and Lidarr for automated media management
- **Unified API**: Interact with all connected services through a single interface
- **User Management**: Authentication, roles, and user-specific configurations

## Architecture

- **Backend**: Go-based API and service integrations
- **Frontend**: SvelteKit with TailwindCSS and Skeleton UI

## Getting Started

### Prerequisites

- Go 1.20+
- Node.js 18+
- Docker (optional)

### Installation

#### Backend

```bash
cd backend
make build
make run
```

#### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Docker

```bash
docker-compose up
```

## Development

### Build Commands
- **Backend**: `cd backend && make build`
- **Frontend**: `cd frontend && npm run build`
- **Docker**: `cd backend && make docker-build && make docker-run`

### Run Commands
- **Backend**: `cd backend && make run`
- **Frontend**: `cd frontend && npm run dev`

### Test Commands
- **Backend**: `cd backend && go test ./... -v` or `make test`
- **Frontend**: `cd frontend && npm run test`

### Lint/Format Commands
- **Backend**: Follow Go standard practices
- **Frontend**: `cd frontend && npm run lint` and `npm run format`

## API Documentation

API documentation is available at `/docs` when running the backend server.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with [Go](https://golang.org/)
- Frontend powered by [SvelteKit](https://kit.svelte.dev/)
- UI components from [Skeleton UI](https://www.skeleton.dev/)