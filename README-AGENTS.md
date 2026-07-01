# Getting Started as an AI Agent

Welcome! This is a quick reference guide for AI agents contributing to Listening Room.

## TL;DR - Quick Start

1. **Read**: [AGENTS.md](AGENTS.md) (5 min read)
2. **Understand**: Project structure and tech stack from [README.md](README.md)
3. **Find**: A task labeled `agent-friendly` or `good first issue` in [Issues](https://github.com/Furs-Tissue/listening-room/issues)
4. **Do**: Fork → Create branch → Implement → Test → PR
5. **Disclose**: Mention AI involvement in your PR description

## Essential Files

| File | Purpose | For Agents |
|------|---------|------------|
| [AGENTS.md](AGENTS.md) | Agent guidelines | **START HERE** |
| [README.md](README.md) | Project overview | Understanding the project |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Workflow and standards | How to contribute |
| [LICENSE](LICENSE) | MIT License | You have permission! |
| [SECURITY.md](SECURITY.md) | Security guidelines | Keep it secure |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Community standards | Be respectful |

## Quick Reference

### Project Info
- **Type**: Music collection management and listening analysis
- **Backend**: PHP 7.4+ (any framework)
- **Frontend**: JavaScript (any framework)
- **Database**: MySQL or PostgreSQL
- **License**: MIT (agent-friendly!)

### Tech Stack
```
Backend:   PHP → API → Database
Frontend:  JavaScript → UI → API
```

### Key Directories
```
backend/      PHP backend code
frontend/     JavaScript frontend code
docs/         Documentation
.github/      GitHub configuration
```

### Development Commands

**Backend**
```bash
cd backend
composer install          # Install dependencies
cp .env.example .env      # Setup environment
phpunit                   # Run tests
```

**Frontend**
```bash
cd frontend
npm install              # Install dependencies
cp .env.example .env     # Setup environment
npm test                 # Run tests
npm run dev              # Start dev server
```

## Finding Tasks

Good tasks for AI agents have labels:
- ✅ `agent-friendly` - Optimized for AI
- ✅ `good first issue` - Beginner-friendly
- ✅ `help wanted` - Actively seeking help
- ✅ `test`, `docs` - Specific task types

**Find tasks**: [https://github.com/Furs-Tissue/listening-room/issues](https://github.com/Furs-Tissue/listening-room/issues)

## Contribution Workflow

```bash
# 1. Fork the repo
# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/listening-room.git
cd listening-room

# 3. Create a feature branch
git checkout -b feature/issue-description

# 4. Make your changes
# (edit files as needed)

# 5. Test your changes
cd backend && phpunit
cd ../frontend && npm test

# 6. Commit with clear message
git commit -m "feat(scope): description"

# 7. Push to your fork
git push origin feature/issue-description

# 8. Create Pull Request on GitHub
# (use the PR template, link the issue, describe changes)

# 9. Respond to feedback
# (make requested changes, commit, push)
```

## Commit Message Format

```
type(scope): description

Examples:
- feat(api): add music search endpoint
- fix(frontend): resolve player pause bug
- docs(contributing): update setup instructions
- test(backend): add unit tests for music service
```

**Types**: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`

## Code Standards

### PHP
- Follow [PSR-12](https://www.php-fig.org/psr/psr-12/)
- Use type hints and return types
- Write docstrings for public methods
- Use prepared statements (security!)
- Validate all input

### JavaScript
- Use ES6+ features
- Write JSDoc comments for exported functions
- Use `const`/`let` (not `var`)
- Follow `.editorconfig` for formatting
- Sanitize output (XSS prevention)

### General
- Write tests for new code (80%+ coverage goal)
- Keep commits atomic and logical
- Update documentation
- No hardcoded secrets
- Consider security implications

## Testing Checklist

- [ ] Run backend tests: `phpunit`
- [ ] Run frontend tests: `npm test`
- [ ] Test manually (if UI-related)
- [ ] Check code style
- [ ] Verify no console errors
- [ ] Test with edge cases

## When You Get Stuck

**Need Help?**
1. Check [AGENTS.md](AGENTS.md) "Common Issues" section
2. Review similar completed PRs
3. Comment on the issue with your question
4. Check [README.md](README.md) troubleshooting section

**Ask Questions Like**:
```
@maintainers - I'm working on feature X. 
Should I implement Y in the service layer or API layer?
Please advise before I proceed.
```

## Important Reminders

✅ **DO**
- Read the guidelines before starting
- Write tests for your code
- Keep PRs focused and atomic
- Reference issues in PRs
- Respond to feedback promptly
- **Disclose AI involvement** in your PR
- Follow code standards
- Validate and sanitize input

❌ **DON'T**
- Work on issues without recent activity
- Create huge PRs (break into smaller ones)
- Hardcode secrets or credentials
- Ignore code review feedback
- Work on blocked/on-hold issues
- Merge your own PRs
- Make breaking changes without discussion

## PR Template Tips

When creating a PR:
```markdown
## Description
Clear description of what this PR does

## Type of Change
- [x] Bug fix / Feature / Docs / Refactor / Test

## Related Issue
Closes #123

## Testing
How to test the changes

## Disclosure
This PR was created with AI assistance from [Tool].
Human review has been completed.
```

## Key Links

- 🤖 **Agent Guidelines**: [AGENTS.md](AGENTS.md)
- 📖 **Project README**: [README.md](README.md)
- 🤝 **Contributing**: [CONTRIBUTING.md](CONTRIBUTING.md)
- 📋 **Issues**: [GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/Furs-Tissue/listening-room/discussions)
- 🔐 **Security**: [SECURITY.md](SECURITY.md)
- 📜 **License**: [LICENSE](LICENSE)
- 🎯 **This Guide**: [README-AGENTS.md](README-AGENTS.md)

## Next Steps

1. ✅ Read [AGENTS.md](AGENTS.md)
2. ✅ Check [GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues)
3. ✅ Pick a task labeled `agent-friendly`
4. ✅ Fork and create a branch
5. ✅ Start coding!

---

**Questions?** Open a discussion or comment on an issue.

**Ready?** Let's build Listening Room together! 🎵
