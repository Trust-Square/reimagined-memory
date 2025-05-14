# README.md

# Node.js Development Environment

This project provides a consistent development environment for Node.js applications using Visual Studio Code's devcontainers feature. It includes all essential tools and configurations needed for professional Node.js development.

## Features

- 📦 Node.js LTS (20.x) with npm
- 🛠️ Essential development tools (git, curl, wget)
- ✨ Code formatting with Prettier
- 🔍 Linting with ESLint
- 🧪 Testing setup with Jest
- 🔄 Live reload with Nodemon
- 🔒 Security best practices

## Getting Started

### Prerequisites

1. Install [Visual Studio Code](https://code.visualstudio.com/)
2. Install [Docker Desktop](https://www.docker.com/products/docker-desktop)
3. Install the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VS Code

### Setup

1. Clone this repository
2. Open the project in VS Code
3. When prompted, click "Reopen in Container"
4. Wait for the container to build and initialize

The development environment will be automatically configured with all necessary tools and extensions.

### Development

- `npm run dev`: Start the development server with hot reload
- `npm test`: Run tests
- `npm run lint`: Check code quality
- `npm run format`: Format code

## Project Structure

```
.
├── .devcontainer/          # Development container configuration
│   ├── devcontainer.json   # VS Code devcontainer settings
│   └── Dockerfile         # Container definition
├── src/                   # Source code
│   └── index.js          # Application entry point
├── package.json          # Project dependencies and scripts
├── .gitignore           # Git ignore patterns
└── README.md            # Project documentation
```

## Best Practices

- The container runs as non-root user 'node' for security
- Development tools are configured with recommended settings
- Code formatting and linting run automatically on save
- Container includes only essential tools to minimize size
- Environment variables should be stored in .env files (not in git)

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the ISC License.
