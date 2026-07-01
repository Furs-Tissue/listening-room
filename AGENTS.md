# Agents.md - Agent Guidelines for Listening Room

## Overview

This document provides guidance for AI agents, language models, and automated systems contributing to the Listening Room project. Agents are welcome and encouraged to contribute!

## Quick Start for Agents

### Before You Begin

1. **Read the documentation**:
   - [README.md](README.md) - Project overview and quick start
   - [CONTRIBUTING.md](CONTRIBUTING.md) - Detailed contribution guidelines
   - [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Community standards

2. **Understand the architecture**:
   - Backend: PHP with flexible framework choice
   - Frontend: JavaScript with flexible framework choice
   - Database: MySQL or PostgreSQL
   - API: RESTful architecture

3. **Check existing issues**:
   - Look for issues labeled `good first issue` or `help wanted`
   - Check `agent-friendly` label for tasks optimized for AI agents
   - Avoid duplicate work by checking open PRs

## Agent-Specific Tasks

### Well-Suited for Agents

✅ **Code Generation & Implementation**
- Writing API endpoints
- Creating UI components
- Database schema and migrations
- Unit and integration tests
- Documentation improvements
- Code refactoring and optimization
- Bug fixes with clear reproduction steps

✅ **Analysis & Optimization**
- Code review and suggestions
- Performance analysis
- Security vulnerability scanning
- Dependency updates
- Dead code elimination
- Architecture improvements

✅ **Documentation**
- API documentation
- Setup guides
- Architecture decision records (ADRs)
- Code comments and explanations
- Examples and tutorials
- Migration guides

### Requires Human Oversight

⚠️ **Use Caution**
- Breaking changes (discuss first)
- Database migrations affecting production
- Security-critical code
- Major architectural decisions
- User-facing features (may need design input)
- License or legal matters

❌ **Not Recommended**
- Issues requiring subjective user feedback
- Design decisions without specifications
- Community management tasks
- Release/deployment decisions
- Issues marked as "blocked" or "on-hold"

## Development Workflow for Agents

### Step 1: Analyze the Issue

```
1. Read the issue carefully
2. Understand requirements and acceptance criteria
3. Review related code and documentation
4. Check for dependencies on other work
5. Identify tests that need to pass
```

### Step 2: Plan Your Approach

```
1. Identify affected files and components
2. Plan the solution architecture
3. List dependencies that might be needed
4. Plan test coverage
5. Estimate scope and complexity
```

### Step 3: Implement the Solution

```
1. Create a feature branch: git checkout -b feature/issue-description
2. Write code following project standards
3. Add tests for new functionality
4. Run tests locally
5. Commit with clear messages
```

### Step 4: Create a Pull Request

```
1. Push to your fork
2. Create PR using the template in .github/pull_request_template.md
3. Link the related issue using "Closes #123"
4. Fill out all relevant sections
5. Wait for review
```

### Step 5: Respond to Feedback

```
1. Read reviewer comments carefully
2. Make requested changes
3. Explain decisions if needed
4. Commit with clear messages
5. Re-request review
```

## Code Quality Standards

### For All Submissions

- **Readability**: Code should be clear and self-documenting
- **Comments**: Complex logic should be explained
- **Tests**: All new code should have tests (aim for 80%+ coverage)
- **Style**: Follow language-specific conventions (PSR-12 for PHP, ES6+ for JS)
- **Security**: No hardcoded credentials, validate inputs, use prepared statements
- **Documentation**: Update relevant docs, add docstrings/JSDoc comments
- **Commits**: One logical change per commit with clear messages

### Backend (PHP)

```php
// ✅ GOOD
public function searchMusic(string $query, int $limit = 20): array
{
    // Validate input
    if (empty($query) || strlen($query) > 200) {
        throw new InvalidArgumentException('Invalid search query');
    }
    
    // Use prepared statements for security
    $results = $this->db->prepare(
        'SELECT * FROM music WHERE title LIKE ? LIMIT ?'
    )->execute(["%{$query}%", $limit]);
    
    return $results;
}
```

### Frontend (JavaScript)

```javascript
// ✅ GOOD
/**
 * Fetches music from the API and updates the store
 * @param {string} query - The search query
 * @param {number} limit - Maximum results to return
 * @returns {Promise<Array>} Array of music objects
 * @throws {Error} If the request fails
 */
async function searchMusic(query, limit = 20) {
  if (!query || query.length > 200) {
    throw new Error('Invalid search query');
  }
  
  const response = await fetch(
    `/api/music/search?q=${encodeURIComponent(query)}&limit=${limit}`
  );
  
  if (!response.ok) {
    throw new Error(`Search failed: ${response.statusText}`);
  }
  
  return response.json();
}
```

## Testing Requirements

### Unit Tests

- Write tests for new functions/methods
- Aim for >80% code coverage
- Test both happy paths and error cases
- Use descriptive test names

### Integration Tests

- Test API endpoints work correctly
- Test database operations
- Test authentication/authorization
- Test error handling

### Running Tests Locally

```bash
# Backend
cd backend
phpunit

# Frontend
cd frontend
npm test
```

## Commit Message Format

Use conventional commits for clear history:

```
<type>(<scope>): <description>

<optional body>

<optional footer>
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Code style (formatting, missing semicolons, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding tests
- `chore`: Maintenance tasks

### Examples

```
feat(api): add music search endpoint
fix(frontend): resolve player pause bug
docs(contributing): update setup instructions
test(backend): add unit tests for music service
refactor(api): simplify music filtering logic
```

## Security Considerations for Agents

When writing code, always consider:

- **Input Validation**: Validate and sanitize all user input
- **SQL Injection**: Use prepared statements
- **XSS Prevention**: Escape output in frontend code
- **CSRF Protection**: Include CSRF tokens in forms
- **Authentication**: Verify user identity
- **Authorization**: Check permissions before allowing actions
- **Secrets**: Never hardcode API keys, passwords, or tokens
- **Dependencies**: Keep dependencies up to date

## When to Ask for Help

If you're unsure about something, create a comment in the issue:

```
@maintainers - I'm implementing feature X and have a question about the architecture.
Should component Y be in the service layer or the API layer? 
Please advise before I proceed.
```

## Common Issues and Solutions

### Database Connection Fails
- Check `.env` file is configured
- Verify database is running
- Check credentials are correct
- Review `SECURITY.md` for best practices

### Tests Fail Locally
- Run migrations: `php artisan migrate:fresh`
- Clear cache: `php artisan cache:clear`
- Check Node/PHP versions match requirements
- Review test output for specific errors

### Code Style Issues
- PHP: Run `php-cs-fixer` or appropriate formatter
- JavaScript: Run `eslint --fix`
- Check `.editorconfig` for formatting rules

### PR Review Feedback
- Read feedback carefully
- Ask clarifying questions if needed
- Make changes requested
- Commit with clear messages
- Respond to all feedback before requesting re-review

## Disclosing AI Involvement

**When creating a PR or commit:**

Please clearly indicate AI involvement in the PR description or commit message:

```
## Disclosure
This PR was generated with assistance from [AI Tool Name].
Human review and testing have been completed.
```

Or in commit message:
```
feat(api): add music search endpoint (AI-assisted, human-reviewed)
```

**This is important for:**
- Transparency with the community
- Understanding code provenance
- Ensuring proper review
- Meeting project standards

## Resources

- 📖 [README.md](README.md) - Project overview
- 🤝 [CONTRIBUTING.md](CONTRIBUTING.md) - Contribution guidelines
- 🛡️ [SECURITY.md](SECURITY.md) - Security policy
- 📋 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Community standards
- 🏗️ [.github/GITHUB_CONFIG.md](.github/GITHUB_CONFIG.md) - GitHub setup
- 🔄 [LICENSE](LICENSE) - MIT License with AI permissions

## Getting Started

**Ready to contribute?**

1. Fork the repository
2. Check [GitHub Issues](https://github.com/Furs-Tissue/listening-room/issues) for tasks
3. Look for `good first issue` or `agent-friendly` labels
4. Read the issue requirements
5. Create a branch and start implementing
6. Follow the workflow above
7. Submit your PR!

## Questions?

If you have questions:
- Check existing documentation
- Review similar completed PRs
- Comment on the issue with specific questions
- Open a discussion if more general

---

**Thank you for helping improve Listening Room!** 🎵
