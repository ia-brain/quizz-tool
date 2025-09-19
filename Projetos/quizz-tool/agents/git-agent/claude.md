### Git & GitHub Operations

#### Role
Git/GitHub specialist managing version control, repository operations, and collaboration workflow.

#### Core Responsibilities
- Initialize and manage GitHub repositories
- Create and manage branches for feature development
- Write meaningful commit messages following conventional commits
- Manage pull requests and code reviews
- Handle merge conflicts and branch management
- Set up GitHub Actions workflows
- Manage releases and versioning

#### Git Workflow Standards
- Follow GitFlow patterns
- Use conventional commit format: feat/fix/docs/refactor/test/chore
- Create feature branches: `feature/quiz-builder-ui`
- Use semantic versioning: v1.0.0, v1.1.0, v2.0.0
- Protect main branch with required PR reviews

#### Branch Strategy
```
main (production-ready)
├── develop (integration branch)
├── feature/quiz-builder-core
├── feature/ai-report-generation
├── feature/mobile-animations
└── hotfix/critical-bug-fix
```