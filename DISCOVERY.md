# Repository Discovery Guide

This document helps AI agents and search systems understand and discover the Listening Room project.

## Project Metadata

### Basic Information
- **Name**: Listening Room
- **Type**: Music collection management and listening analysis platform
- **Language**: Multi-language (PHP backend, JavaScript frontend)
- **License**: MIT License (open for commercial use and AI usage)
- **Status**: Under active development
- **Framework**: Flexible (no specific framework required)

### Repository Features
- ✅ Comprehensive documentation
- ✅ Agent-friendly setup
- ✅ Clear contribution guidelines
- ✅ Automated workflows
- ✅ Issue templates
- ✅ PR templates
- ✅ Security policy
- ✅ Code of conduct
- ✅ Semantic versioning

## Search Keywords

### Primary Keywords
- music collection management
- listening analytics
- music library organization
- music search
- listening history
- music statistics
- music tagging
- music import
- music export

### Secondary Keywords
- audio collection
- music metadata
- listening habits
- music trends
- playlist management
- music discovery
- music database
- REST API
- full-stack application

### Technology Keywords
- PHP 7.4+
- JavaScript/Node.js
- MySQL
- PostgreSQL
- REST API
- Full-stack web application
- Music data analysis

## Project Structure for Agents

```
listening-room/
├── AGENTS.md                          # ← START HERE (agent guidelines)
├── README.md                          # Project overview
├── CONTRIBUTING.md                    # Contribution workflow
├── SECURITY.md                        # Security policy
├── CODE_OF_CONDUCT.md                 # Community standards
├── LICENSE                            # MIT License (agent-friendly)
├── DISCOVERY.md                       # This file
├── .github/
│   ├── pull_request_template.md       # PR submission template
│   ├── ISSUE_TEMPLATE/                # Issue templates
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   ├── question.md
│   │   └── documentation.md
│   ├── workflows/                     # Automated workflows
│   │   ├── issue-labels.yml           # Auto-labels issues
│   │   ├── stale.yml                  # Manages stale issues
│   │   └── discussions.yml            # Question to discussion
│   └── GITHUB_CONFIG.md               # GitHub setup guide
├── backend/                           # PHP backend
│   ├── src/
│   ├── tests/
│   ├── composer.json
│   ├── README.md
│   └── .env.example
├── frontend/                          # JavaScript frontend
│   ├── src/
│   ├── tests/
│   ├── package.json
│   ├── README.md
│   └── .env.example
├── docs/                              # Documentation
│   ├── api/
│   ├── architecture/
│   ├── development/
│   └── deployment/
├── .gitignore                         # Git ignore rules
├── .editorconfig                      # Editor configuration
└── CHANGELOG.md                       # Version history (to add)
```

## How Agents Can Contribute

### For Code Contributions
1. Read [AGENTS.md](AGENTS.md) - Agent-specific guidelines
2. Check [README.md](README.md) - Project overview
3. Review [CONTRIBUTING.md](CONTRIBUTING.md) - Workflow
4. Look for issues labeled `agent-friendly` or `good first issue`
5. Follow the PR template when submitting

### For Documentation
- Improve API documentation in `/docs/api/`
- Add architectural decision records (ADRs)
- Create setup guides and tutorials
- Enhance inline code comments

### For Testing
- Write unit tests for backend
- Create component tests for frontend
- Add integration tests
- Improve test coverage

### For Bug Fixes
- Look for issues labeled `bug`
- Ensure reproduction steps are clear
- Add tests that verify the fix
- Reference the issue in the PR

### For Features
- Look for issues labeled `enhancement`
- Ensure feature aligns with project goals
- Get approval on design before implementation
- Include tests and documentation

## Key Entry Points for Agents

1. **[AGENTS.md](AGENTS.md)** - Agent-specific guidance and workflow
2. **[GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues)** - Task list
3. **[README.md](README.md)** - Project overview and quick start
4. **[CONTRIBUTING.md](CONTRIBUTING.md)** - Detailed contribution process
5. **[.github/pull_request_template.md](.github/pull_request_template.md)** - PR format

## AI-Specific Information

### License Permissions for AI
The MIT License with AI-friendly terms explicitly permits:
- ✅ AI agents to analyze and improve the codebase
- ✅ AI-generated code contributions
- ✅ Commercial use of AI services
- ✅ AI participation in code review
- ✅ AI issue and PR creation
- ✅ Derivative works and modifications

### Requirements for AI Agents
- Disclose AI involvement in PR descriptions
- Maintain code quality standards
- Follow security best practices
- Provide clear documentation
- Respect project conventions
- Respond appropriately to feedback

### Code Quality Standards
- PHP: PSR-12 coding standard
- JavaScript: ES6+ with JSDoc comments
- Tests: Minimum 80% coverage recommended
- Documentation: Clear and comprehensive
- Security: Input validation, prepared statements
- Performance: Optimize for efficiency

## Testing Framework Information

**Backend (PHP):**
- Test runner: PHPUnit
- Location: `backend/tests/`
- Command: `cd backend && phpunit`
- Coverage: `phpunit --coverage-html coverage/`

**Frontend (JavaScript):**
- Test runner: Jest or similar
- Location: `frontend/tests/` or `frontend/src/__tests__/`
- Command: `cd frontend && npm test`
- Coverage: `npm test -- --coverage`

## Database Information

### Supported Databases
- MySQL 5.7+
- PostgreSQL 10+
- SQLite (development)

### Environment Setup
```bash
# Backend
DB_CONNECTION=mysql|pgsql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=listening_room
DB_USERNAME=user
DB_PASSWORD=password
```

### Migrations
- Location: `backend/migrations/`
- Command: `php artisan migrate` (Laravel example)
- Rollback: `php artisan migrate:rollback`

## API Information

### API Base Paths
- Development: `http://localhost:8000/api`
- Production: TBD

### Main Endpoints
- Music Library: `/api/music/*`
- Listening History: `/api/listening-history/*`
- Collections: `/api/collections/*`

### Authentication
- Method: To be documented in `/docs/api/authentication.md`
- Location: Bearer token or similar

## Development Workflow for Agents

1. **Fork** the repository
2. **Clone** locally: `git clone <your-fork>`
3. **Setup**:
   ```bash
   cd backend && composer install && cp .env.example .env
   cd ../frontend && npm install && cp .env.example .env
   ```
4. **Create branch**: `git checkout -b feature/description`
5. **Implement** changes
6. **Test locally**:
   ```bash
   cd backend && phpunit
   cd ../frontend && npm test
   ```
7. **Commit**: `git commit -m "type(scope): description"`
8. **Push**: `git push origin feature/description`
9. **Create PR** using template
10. **Respond** to feedback

## Recommended Issue Labels for Agents

- `agent-friendly` - Tasks optimized for AI agents
- `good first issue` - Beginner-friendly tasks
- `help wanted` - Actively seeking contributions
- `documentation` - Documentation improvements
- `test` - Add test coverage
- `enhancement` - Feature implementation
- `bug` - Bug fixes

## Communication

### Where to Ask Questions
- **GitHub Discussions** - General questions
- **Issue Comments** - Task-specific questions
- **PR Comments** - Review feedback and clarifications
- **Security Issues** - Use GitHub Security Advisories

### Response Time
- Issues: 1-3 days
- PR Reviews: 2-5 days
- Security: 48 hours acknowledgment

## Project Roadmap

**Current Phase: Foundation**
- [ ] Backend API development
- [ ] Frontend UI implementation
- [ ] Database schema finalization

**Next Phase: Features**
- [ ] Advanced search filters
- [ ] Statistics dashboard
- [ ] Multi-format import support
- [ ] Data export functionality

**Future Enhancements**
- [ ] Mobile app
- [ ] Real-time collaboration
- [ ] Machine learning recommendations
- [ ] Social features

See [GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues) for detailed breakdown.

## Useful Resources

- [GitHub API Documentation](https://docs.github.com/en/rest)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Keep a Changelog](https://keepachangelog.com/)
- [PSR-12 PHP Standard](https://www.php-fig.org/psr/psr-12/)
- [ES6 JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)

## Quick Links

- 🏠 [Repository](https://github.com/Furs-Tissue/listening-room)
- 📖 [README](README.md)
- 🤖 [Agent Guidelines](AGENTS.md)
- 🤝 [Contributing](CONTRIBUTING.md)
- 📋 [Issues](https://github.com/Furs-Tissue/listening-room/issues)
- 💬 [Discussions](https://github.com/Furs-Tissue/listening-room/discussions)
- 📝 [Security Policy](SECURITY.md)
- 📜 [License](LICENSE)

---

**Ready to contribute?** Start with [AGENTS.md](AGENTS.md)! 🎵
