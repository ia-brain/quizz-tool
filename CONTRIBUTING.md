# Contributing to Quizz Tool

Thank you for your interest in contributing to Quizz Tool! This document provides guidelines and instructions for contributing to the project.

## 🤝 How to Contribute

### Reporting Issues

1. **Search existing issues** first to avoid duplicates
2. **Use the issue templates** provided in the repository
3. **Provide detailed information** including:
   - Clear description of the issue
   - Steps to reproduce
   - Expected vs actual behavior
   - Environment details (browser, OS, etc.)
   - Screenshots or videos if applicable

### Suggesting Features

1. **Check the roadmap** and existing feature requests
2. **Use the feature request template**
3. **Explain the use case** and provide context
4. **Include mockups or examples** if possible

## 🚀 Development Process

### Setting Up Development Environment

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:

   ```bash
   git clone https://github.com/YOUR_USERNAME/quizz-tool.git
   cd quizz-tool
   ```

3. **Install dependencies**:

   ```bash
   npm install
   ```

4. **Set up environment variables**:
   ```bash
   cp .env.example .env.local
   # Edit .env.local with your configuration
   ```

### Branch Strategy

We follow GitFlow branching model:

- **`main/master`**: Production-ready code
- **`develop`**: Integration branch for features
- **`feature/*`**: New features (e.g., `feature/quiz-builder-ui`)
- **`bugfix/*`**: Bug fixes (e.g., `bugfix/login-validation`)
- **`hotfix/*`**: Critical production fixes

### Creating a Feature Branch

```bash
git checkout develop
git pull origin develop
git checkout -b feature/your-feature-name
```

## 📝 Coding Standards

### Code Style

- **TypeScript**: All new code must be written in TypeScript
- **ESLint**: Follow the configured ESLint rules
- **Prettier**: Code is automatically formatted on commit
- **Naming conventions**:
  - Components: PascalCase (e.g., `QuizBuilder`)
  - Files: kebab-case (e.g., `quiz-builder.tsx`)
  - Variables/functions: camelCase (e.g., `createQuiz`)
  - Constants: UPPER_SNAKE_CASE (e.g., `API_BASE_URL`)

### File Organization

```
src/
├── app/                    # Next.js App Router pages
│   ├── (dashboard)/       # Route groups
│   └── api/               # API routes
├── components/            # Reusable UI components
│   ├── ui/               # Base UI components
│   └── features/         # Feature-specific components
├── hooks/                # Custom React hooks
├── lib/                  # Utility functions
├── stores/               # Zustand stores
├── types/                # TypeScript definitions
└── utils/                # Helper functions
```

### Component Guidelines

1. **Use functional components** with hooks
2. **Implement proper TypeScript types** for all props
3. **Follow the component structure**:

   ```tsx
   // Imports
   import React from "react";
   import { SomeType } from "@/types";

   // Types
   interface ComponentProps {
     title: string;
     onClick: () => void;
   }

   // Component
   export function Component({ title, onClick }: ComponentProps) {
     // Implementation
   }
   ```

4. **Use proper prop destructuring**
5. **Implement proper error boundaries** where needed

## 🧪 Testing Requirements

### Testing Strategy

- **Unit tests**: Test individual components and functions
- **Integration tests**: Test component interactions
- **E2E tests**: Test complete user workflows

### Writing Tests

1. **Create tests alongside components**:

   ```
   components/
   ├── quiz-builder.tsx
   └── quiz-builder.test.tsx
   ```

2. **Use descriptive test names**:

   ```typescript
   test("should create a new quiz when form is submitted with valid data");
   ```

3. **Follow AAA pattern** (Arrange, Act, Assert)

### Running Tests

```bash
# Run all tests
npm run test

# Run unit tests
npm run test:unit

# Run E2E tests
npm run test:e2e

# Run tests in watch mode
npm run test:watch
```

## 📋 Commit Guidelines

### Conventional Commits

We use [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

#### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, semicolons, etc.)
- **refactor**: Code refactoring
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **build**: Build system changes
- **ci**: CI configuration changes
- **chore**: Other changes (dependencies, etc.)

#### Examples

```bash
feat(quiz): add multiple choice question type
fix(auth): resolve login validation error
docs: update API documentation
test(quiz): add unit tests for quiz creation
```

## 🔄 Pull Request Process

### Before Submitting

1. **Sync with develop branch**:

   ```bash
   git checkout develop
   git pull origin develop
   git checkout your-branch
   git rebase develop
   ```

2. **Run the complete test suite**:

   ```bash
   npm run test
   npm run lint
   npm run type-check
   ```

3. **Build the project**:
   ```bash
   npm run build
   ```

### Pull Request Checklist

- [ ] Code follows project coding standards
- [ ] All tests pass
- [ ] New features include appropriate tests
- [ ] Documentation is updated (if applicable)
- [ ] Commit messages follow conventional commits
- [ ] PR title follows conventional commits format
- [ ] PR description explains the changes clearly

### PR Review Process

1. **Automated checks** must pass (CI/CD pipeline)
2. **Code review** by at least one maintainer
3. **Manual testing** for significant changes
4. **Approval** from project maintainers

## 🎯 Code Quality

### Pre-commit Hooks

The project uses Husky to run pre-commit hooks:

- **ESLint**: Checks code quality
- **Prettier**: Formats code
- **Type checking**: Validates TypeScript

### Quality Standards

- **Test coverage**: Maintain >80% test coverage
- **Performance**: No unnecessary re-renders or memory leaks
- **Accessibility**: Follow WCAG 2.1 AA guidelines
- **Security**: No hardcoded secrets or vulnerabilities

## 🏷 Versioning

We use [Semantic Versioning](https://semver.org/):

- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (backward compatible)

## 📞 Getting Help

- **GitHub Discussions**: For questions and ideas
- **GitHub Issues**: For bug reports and feature requests
- **Discord**: For real-time chat and community support

## 📄 License

By contributing to Quizz Tool, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to Quizz Tool! 🎉
