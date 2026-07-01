# Listening Room

A music collection management and listening analysis platform. Listening Room helps users organize their music libraries, track listening habits, and discover insights about their music consumption patterns.

[![License: CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
[![Open Issues](https://img.shields.io/github/issues/Furs-Tissue/listening-room)](https://github.com/Furs-Tissue/listening-room/issues)
[![Contributors](https://img.shields.io/github/contributors/Furs-Tissue/listening-room)](https://github.com/Furs-Tissue/listening-room/graphs/contributors)

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Development](#development)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)
- [Roadmap](#roadmap)

## Features

- 🎵 **Music Collection Management** - Organize and manage your music library
- 📊 **Listening Analytics** - Track and analyze your listening patterns
- 🔍 **Advanced Search** - Find songs, artists, and albums with powerful search filters
- 📈 **Statistics & Insights** - Discover trends in your music consumption
- 🏷️ **Smart Tagging** - Organize music with custom tags and collections
- 🔄 **Multi-format Support** - Import from various music sources
- 💾 **Data Export** - Export your listening history and collections

## Tech Stack

### Backend
- **Language**: PHP 7.4+
- **Framework**: Your choice (Laravel, Symfony, Slim, custom, etc.)
- **Database**: MySQL/PostgreSQL (flexible)
- **API**: RESTful architecture

### Frontend
- **Language**: JavaScript/TypeScript
- **Framework**: Your choice (React, Vue, Svelte, vanilla, etc.)
- **Styling**: CSS/SCSS/Tailwind CSS (flexible)
- **Build Tool**: Your choice (Webpack, Vite, etc.)

## Project Structure

```
listening-room/
├── backend/                    # PHP backend application
│   ├── src/                   # Source code
│   │   ├── API/              # API endpoints
│   │   ├── Models/           # Data models
│   │   ├── Services/         # Business logic
│   │   ├── Middleware/       # Middleware
│   │   └── Config/           # Configuration
│   ├── tests/                # Unit and integration tests
│   ├── migrations/           # Database migrations (if using migrations)
│   ├── composer.json         # PHP dependencies
│   ├── .env.example          # Environment template
│   └── README.md             # Backend-specific documentation
│
├── frontend/                  # JavaScript frontend application
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # Page components
│   │   ├── services/         # API service layer
│   │   ├── hooks/            # Custom hooks (if using React)
│   │   ├── store/            # State management
│   │   ├── styles/           # Global styles
│   │   ├── utils/            # Utility functions
│   │   └── App.js            # Root component
│   ├── public/               # Static assets
│   ├── tests/                # Unit and component tests
│   ├── package.json          # Node dependencies
│   ├── .env.example          # Environment template
│   └── README.md             # Frontend-specific documentation
│
├── docs/                      # Project documentation
│   ├── api/                  # API documentation
│   ├── architecture/         # Architecture decisions
│   ├── development/          # Development guides
│   ├── deployment/           # Deployment guides
│   └── CONTRIBUTING.md       # Contribution guidelines (also at root)
│
├── .github/                   # GitHub-specific configuration
│   ├── workflows/            # CI/CD workflows
│   ├── ISSUE_TEMPLATE/       # Issue templates
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   └── question.md
│   └── pull_request_template.md  # PR template
│
├── CONTRIBUTING.md           # How to contribute
├── README.md                 # This file
├── LICENSE                   # CC0 1.0 Universal License
├── .gitignore               # Git ignore rules
├── .editorconfig            # Editor configuration
└── AGENTS.md                # Guidance for AI agents

```

## Getting Started

### Prerequisites

- **PHP 7.4+** (for backend development)
- **Node.js 14+** and npm/yarn (for frontend development)
- **Git**
- **Database** (MySQL 5.7+ or PostgreSQL 10+)

### Quick Start

#### Backend Setup

```bash
# Clone the repository
git clone https://github.com/Furs-Tissue/listening-room.git
cd listening-room/backend

# Install dependencies
composer install

# Copy environment file
cp .env.example .env

# Generate application key (if applicable)
php artisan key:generate  # For Laravel

# Run database migrations
php artisan migrate  # Or appropriate migration command

# Start the development server
php artisan serve  # Or: php -S localhost:8000
```

#### Frontend Setup

```bash
# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install
# or
yarn install

# Start development server
npm run dev
# or
yarn dev

# Open browser to http://localhost:3000 (or configured port)
```

### Running Tests

```bash
# Backend tests
cd backend
phpunit
# or framework-specific command

# Frontend tests
cd frontend
npm test
# or
yarn test
```

### Verify Installation

1. Backend API should be running at `http://localhost:8000` (or configured port)
2. Frontend should be running at `http://localhost:3000` (or configured port)
3. Check the `/api/health` endpoint to verify backend is working
4. Run tests to ensure everything is set up correctly

## Development

### Code Style & Standards

We follow industry best practices for code quality:

**PHP:**
- [PSR-12](https://www.php-fig.org/psr/psr-12/) Coding Standard
- Use type hints and return types
- Follow SOLID principles

**JavaScript:**
- ES6+ standards
- Consistent formatting (see `.editorconfig`)
- Meaningful variable/function names
- JSDoc comments for exported functions

### Making Changes

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed contribution guidelines including:
- How to create a feature branch
- Code style requirements
- Testing procedures
- PR submission process

### Local Development Workflow

```bash
# 1. Create feature branch
git checkout -b feature/amazing-feature

# 2. Make your changes
# ... edit files ...

# 3. Run tests locally
cd backend && phpunit
cd ../frontend && npm test

# 4. Commit with descriptive message
git commit -m "feat: add amazing feature"

# 5. Push to your fork
git push origin feature/amazing-feature

# 6. Create Pull Request on GitHub
# (follow PR template in .github/pull_request_template.md)
```

### Environment Configuration

Create `.env` files in both backend and frontend directories:

**backend/.env:**
```
APP_ENV=local
APP_DEBUG=true
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=listening_room
DB_USERNAME=root
DB_PASSWORD=password
```

**frontend/.env:**
```
REACT_APP_API_URL=http://localhost:8000
REACT_APP_ENV=development
```

## API Documentation

### Base URL
- **Development**: `http://localhost:8000/api`
- **Production**: TBD

### Key Endpoints

#### Music Library
- `GET /api/music/search` - Search music library
- `GET /api/music/:id` - Get music details
- `POST /api/music/import` - Import music collection

#### Listening History
- `GET /api/listening-history` - Get user's listening history
- `POST /api/listening-history` - Record a listen event
- `GET /api/listening-history/stats` - Get listening statistics

#### Collections
- `GET /api/collections` - List user's collections
- `POST /api/collections` - Create collection
- `PUT /api/collections/:id` - Update collection
- `DELETE /api/collections/:id` - Delete collection

### Authentication
- Details available in `/docs/api/authentication.md`

### Full API Reference
See [docs/api/](docs/api/) for complete API documentation.

## Contributing

We welcome contributions from developers of all skill levels! 

### Quick Start for Contributors

1. **Fork** the repository
2. **Read** [CONTRIBUTING.md](CONTRIBUTING.md)
3. **Create** a feature branch (`git checkout -b feature/your-feature`)
4. **Make** your changes
5. **Test** your code
6. **Commit** with clear messages
7. **Push** to your fork
8. **Open** a Pull Request

### Types of Contributions

- 🐛 **Bug Reports** - Report issues you find
- ✨ **Features** - Suggest or implement new features
- 📚 **Documentation** - Improve docs and examples
- 🧪 **Tests** - Add test coverage
- 🎨 **UI/UX** - Improve user experience
- 🚀 **Performance** - Optimize code and speed

### Development Guidelines

- Follow the existing code style
- Write tests for new features
- Update documentation as needed
- Keep PRs focused and atomic
- Reference related issues in PRs

### Code Review Process

1. Submit a PR with your changes
2. Maintainers review within 1-3 days
3. Respond to feedback and make requested changes
4. PR is merged once approved

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## Project Roadmap

### Current Phase: Foundation
- [x] Core architecture setup
- [ ] Backend API development
- [ ] Frontend UI implementation
- [ ] Database schema finalization

### Next Phase: Features
- [ ] Advanced search filters
- [ ] Statistics dashboard
- [ ] Multi-format import support
- [ ] Data export functionality

### Future Enhancements
- [ ] Mobile app
- [ ] Real-time collaboration
- [ ] Machine learning recommendations
- [ ] Social features

See [GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues) for detailed task breakdown.

## Troubleshooting

### Common Issues

**Backend won't start**
- Check PHP version: `php -v` (should be 7.4+)
- Verify database connection in `.env`
- Run migrations: `php artisan migrate`

**Frontend won't compile**
- Clear node_modules: `rm -rf node_modules && npm install`
- Check Node version: `node -v` (should be 14+)
- Check for port conflicts (port 3000)

**Tests failing**
- Ensure database is running
- Run migrations first: `php artisan migrate:fresh --seed`
- Check `.env.testing` configuration

### Getting Help

- 📖 Check [docs/](docs/) directory
- 💬 Open a GitHub Discussion
- 🐛 Check existing [Issues](https://github.com/Furs-Tissue/listening-room/issues)
- 📝 Review [CONTRIBUTING.md](CONTRIBUTING.md)

## License

This project is licensed under the [Creative Commons Zero v1.0 Universal License](LICENSE) - effectively placing the work in the public domain. See LICENSE file for details.

## Acknowledgments

- Thanks to all [contributors](https://github.com/Furs-Tissue/listening-room/graphs/contributors)
- Built with modern, open-source technologies
- Inspired by the music community

---

**Status**: 🚧 Under Active Development

**Last Updated**: July 2026

For more information, see [docs/](docs/) or open an issue with questions!
