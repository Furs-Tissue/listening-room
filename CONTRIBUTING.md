# Contributing to Listening Room

Thank you for your interest in contributing to Listening Room! We're building a music collection management and listening analysis platform, and we welcome contributions from developers of all skill levels. Whether you prefer PHP, JavaScript, or any modern framework, there's a place for your work here.

## Getting Started

### Prerequisites
- **Backend**: PHP 7.4+ (any modern framework of your choice - Laravel, Symfony, custom, etc.)
- **Frontend**: JavaScript/Node.js 14+ (React, Vue, Svelte, vanilla JS, or any framework you prefer)
- Git
- A GitHub account

### Initial Setup

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/listening-room.git
   cd listening-room
   ```

3. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or for bug fixes:
   git checkout -b fix/issue-description
   ```

## Project Overview

**Listening Room** is a music collection management and listening analysis platform. The project is framework-agnostic, meaning contributors have the freedom to choose their preferred technology stack.

### Project Structure (Expected)

```
listening-room/
├── backend/               # PHP backend (any framework)
│   ├── src/              # Source code
│   ├── tests/            # Backend tests
│   ├── config/           # Configuration files
│   └── composer.json     # PHP dependencies (if using Composer)
├── frontend/             # JavaScript frontend (any framework)
│   ├── src/              # Source code
│   ├── tests/            # Frontend tests
│   ├── public/           # Static assets
│   └── package.json      # Node dependencies (if using npm/yarn)
├── docs/                 # Documentation
├── README.md             # Project overview
├── AGENTS.md             # Agent guidelines
└── LICENSE               # CC0 1.0 Universal
```

## Development Workflow

### 1. Before You Start

- **Check existing issues** at [listening-room/issues](https://github.com/Furs-Tissue/listening-room/issues) to avoid duplicate work
- **For major features**, open an issue first to discuss your approach with maintainers
- **For bug fixes**, look for existing issues or create one with clear reproduction steps
- **Review AGENTS.md** for agent-specific guidelines and requirements

### 2. Setting Up Your Development Environment

#### Backend (PHP)

If contributing to the backend:

```bash
# Navigate to backend directory
cd backend

# Install dependencies (example for Composer)
composer install

# Set up environment (create .env file from template if provided)
cp .env.example .env

# Run any setup scripts
php artisan migrate  # if using Laravel
# or appropriate command for your framework
```

#### Frontend (JavaScript)

If contributing to the frontend:

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install
# or
yarn install

# Start development server
npm run dev
# or
yarn dev
```

### 3. Making Changes

#### Code Style Guidelines

**PHP:**
- Follow PSR-12 coding standards
- Use meaningful variable and function names
- Add PHPDoc comments for public methods
- Keep functions focused and single-responsibility

**JavaScript:**
- Follow ES6+ conventions
- Use consistent indentation (2 or 4 spaces, document your choice)
- Add JSDoc comments for exported functions
- Use const/let over var

**General:**
- Write clear, descriptive commit messages
- Keep commits atomic (one logical change per commit)
- Comment complex business logic
- Write tests for new features

#### Example Commit Messages

```bash
# Feature commits
git commit -m "feat: add music library search functionality"
git commit -m "feat(api): implement listening history analysis endpoint"

# Bug fixes
git commit -m "fix: correct date formatting in collection display"
git commit -m "fix(db): resolve duplicate entry issue in music import"

# Documentation
git commit -m "docs: add API documentation for listening endpoints"

# Testing
git commit -m "test: add unit tests for collection filtering"

# Refactoring
git commit -m "refactor: simplify music analysis algorithm"
```

### 4. Testing

Before submitting your changes:

**Backend Tests:**
```bash
cd backend
# Run tests (command depends on your framework)
phpunit
# or
vendor/bin/phpunit
```

**Frontend Tests:**
```bash
cd frontend
npm test
# or
yarn test
```

**Manual Testing:**
- Test your changes in the browser/application
- Verify both happy path and edge cases
- Check for console errors
- Test on different screen sizes (if frontend)

### 5. Submitting Your Contribution

#### Push Your Changes

```bash
git push origin feature/your-feature-name
```

#### Open a Pull Request

On GitHub, create a Pull Request with:

1. **Clear Title**: Describe what you changed
   - ✅ Good: "Add music library search with filters"
   - ❌ Bad: "Update stuff"

2. **Description**: Include:
   - What problem does this solve?
   - How does it work?
   - Any relevant issue numbers: `Closes #123`
   - Screenshots/examples if applicable
   - Testing instructions if needed

3. **Example PR Description:**
   ```markdown
   ## Description
   Implements a search feature for the music library with filter options.

   ## Problem Solved
   Users couldn't easily find songs in large collections.

   ## Changes Made
   - Added search API endpoint (`/api/music/search`)
   - Created search UI component with filters
   - Added tests for search functionality

   ## Testing Instructions
   1. Import a music collection (100+ songs)
   2. Use search bar to find a song
   3. Apply filters by artist/genre
   4. Verify results are accurate

   Closes #42
   ```

## Pull Request Guidelines

- **Link related issues** using `Closes #123` to auto-close when merged
- **Keep PRs focused** - one feature or fix per PR
- **Include tests** for new features or bug fixes
- **Update documentation** if needed
- **Respond to review feedback** promptly
- **Keep commits clean** - rebase if necessary before merge
- **Follow code style** guidelines for the language
- **Request review** from maintainers when ready

## Reporting Issues

When reporting bugs or suggesting features:

1. **Use descriptive titles**
   - ✅ "Search fails when collection has 1000+ songs"
   - ❌ "Search broken"

2. **Provide context**
   - Operating system and browser (if frontend)
   - PHP/Node version
   - Steps to reproduce
   - Expected vs. actual behavior
   - Error messages or logs

3. **Include examples**
   - Screenshots
   - Code snippets
   - Database queries (if relevant)
   - Network requests (if API-related)

## Architecture & Design Decisions

When proposing architectural changes:

1. **Open an issue first** to discuss the approach
2. **Explain the rationale** - why this change is needed
3. **Consider alternatives** - what other solutions exist?
4. **Document trade-offs** - what are the pros and cons?
5. **Get maintainer feedback** before implementing

## Documentation

Good documentation helps agents and humans alike:

- **README.md**: Project overview and quick start
- **API Documentation**: Document all endpoints and parameters
- **Code Comments**: Explain "why", not "what"
- **Setup Guides**: Clear instructions for local development
- **CHANGELOG**: Track major changes between versions

## Framework Flexibility

This project welcomes contributions using any modern framework:

**Backend (PHP):**
- Laravel, Symfony, Slim, Yii, or custom
- Document your framework choice in relevant files
- Ensure dependencies are clearly listed

**Frontend (JavaScript):**
- React, Vue, Svelte, Angular, or vanilla JS
- Document your framework choice
- Maintain consistency with existing code

**Consistency note:** If the project already has established code, try to match the style and approach for easier integration.

## Getting Help

- **Questions about setup?** Open a GitHub Discussion
- **Unsure about a feature?** Comment on the related issue
- **Need clarification?** Ask in your PR comments
- **Check existing documentation** in `/docs` folder

## Code of Conduct

By participating in this project, you agree to:
- Treat all contributors with respect
- Maintain a welcoming and inclusive environment
- Provide constructive feedback
- Report inappropriate behavior to maintainers

## License

By contributing to Listening Room, you agree that your contributions are licensed under the [Creative Commons Zero v1.0 Universal](LICENSE) license, which dedicates your work to the public domain.

---

## Quick Reference

| Task | Command |
|------|---------|
| Create feature branch | `git checkout -b feature/name` |
| Run backend tests | `cd backend && phpunit` |
| Run frontend tests | `cd frontend && npm test` |
| Start dev server | `npm run dev` (in frontend dir) |
| Push changes | `git push origin feature/name` |
| Create PR | Visit GitHub and create from your branch |

---

**Thank you for contributing to Listening Room!** 🎵

Your work helps build a better music collection management platform for everyone.
