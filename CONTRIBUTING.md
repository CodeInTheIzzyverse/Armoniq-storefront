# Contributing to Armoniq Storefront

Thank you for contributing to Armoniq Storefront.

Armoniq is a fictional musical-instrument e-commerce project created for portfolio development and real-world software engineering practice. This repository contains the public customer-facing store.

## Development Setup

### Prerequisites

Before contributing, install:

- Node.js compatible with the project version.
- pnpm.
- Git.
- Required access to the Armoniq API for features that require backend integration.
- Required sandbox/test credentials for external integrations when applicable.

### Repository Setup

Clone the repository:

```bash
git clone https://github.com/Isa-Bedoya-UdeA/Armoniq-storefront.git
cd Armoniq-storefront
```

Install dependencies:

```bash
pnpm install
```

Create the local environment file from `.env.example`.

Never commit real credentials, API keys, tokens, private keys, or other secrets.

### Project Documentation

Before making architectural or feature changes, review:

- [Specification](SPEC.md)
- [Requirements](docs/REQUIREMENTS.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Testing](docs/TESTING.md)

## Branching Strategy

The project uses a feature-oriented branching strategy.

### Main Branch

`main` contains stable code suitable for integration, portfolio demonstrations, and releases.

Avoid direct commits to `main` for significant changes. Use a branch and Pull Request.

### Feature Branches

```text
feature/authentication
feature/product-management
feature/order-management
feature/address-management
feature/payment-integration
```

### Fix Branches

```text
fix/authentication-error
fix/product-filter
fix/order-status
fix/responsive-layout
```

### Documentation Branches

```text
docs/requirements
docs/architecture
docs/readme
```

### Branch Lifecycle

```text
main
  ↓
Create branch
  ↓
Implement change
  ↓
Run checks and tests
  ↓
Update documentation
  ↓
Pull Request
  ↓
Review
  ↓
Merge
```

## Commit Convention

Commits should be concise, descriptive, and focused on one logical change.

The project follows a Conventional Commits-inspired format:

```text
<type>: <description>
```

| Type | Purpose |
| --- | --- |
| `feat` | New functionality |
| `fix` | Bug fix |
| `refactor` | Code restructuring without behavior change |
| `docs` | Documentation |
| `test` | Tests |
| `build` | Build system or dependencies |
| `ci` | CI/CD |
| `style` | Formatting or non-functional style |
| `chore` | Maintenance |

Examples:

```text
feat: add product filtering
fix: correct order status transition
refactor: extract authentication service
docs: update API documentation
test: add product repository tests
ci: add integration test workflow
```

Keep commits focused. Avoid mixing unrelated changes.

## Pull Requests

Pull Requests should be used for significant changes.

A Pull Request should:

- Have a clear title.
- Reference the relevant GitHub issue when applicable.
- Describe the implementation.
- Explain important technical decisions.
- Include screenshots or recordings for relevant UI changes.
- Mention tests and checks performed.
- Identify updated documentation.
- Avoid unrelated changes.

### Pull Request Checklist

```text
[ ] Code builds successfully
[ ] Relevant tests pass
[ ] Lint and formatting checks pass
[ ] Type checking passes
[ ] No secrets are committed
[ ] Architecture rules are respected
[ ] Requirements are satisfied
[ ] Documentation is updated when necessary
[ ] UI changes were manually verified when applicable
```

## Issues and Milestones

GitHub Issues represent specific implementation tasks, bugs, improvements, or technical work.

Milestones group related issues into meaningful development increments, for example:

- Database Design
- Authentication
- Product Management
- Category Management
- Order Management
- Home and Content Management
- Checkout and Payments
- Testing
- Deployment and CI/CD

Issues should be small enough to implement and review independently.

An issue should contain:

- Clear title.
- Description and context.
- Expected behavior.
- Acceptance criteria.
- Related milestone.
- Screenshots, logs, or API examples when useful.
- Related issues when applicable.

Feature work must remain consistent with `SPEC.md` and `docs/REQUIREMENTS.md`.

## Code Style and Architecture

Armoniq is intentionally modular and follows separation of concerns.

### Frontend Organization

Keep responsibilities separated between:

- App Router pages and layouts.
- Reusable UI components.
- Feature components.
- Hooks.
- Services and API communication.
- State management.
- Constants.
- Types.
- Utilities.
- Tests.
- SCSS styles.

Keep business and data-access logic out of presentation components when it belongs in services, hooks, or state modules.

### Styling

The frontend uses SCSS exclusively.

Do not introduce Tailwind CSS or another styling system.

Use mobile-first responsive design and the project's shared variables, mixins, utilities, and global styles.

### Reusable Components

Prefer reusable UI and feature components over duplicated markup.

Components should have clear responsibilities and avoid unnecessary coupling to pages or specific API responses.

### API Integration

Centralize API communication through the project's service/API layer.

Do not hard-code backend URLs, credentials, or environment-specific configuration.

### TypeScript

Use TypeScript throughout the project.

Prefer:

- Explicit domain and API types.
- Narrow types.
- Meaningful names.
- Small functions.
- Immutable data where practical.
- Reusable abstractions when justified.

Avoid:

- Unnecessary `any`.
- Dead code.
- Large functions or components with multiple responsibilities.
- Hard-coded secrets.
- Unnecessary duplication.

### General Engineering Principles

Follow these principles pragmatically:

- SOLID.
- Separation of Concerns.
- DRY.
- KISS.
- Dependency Inversion.
- Reusable components and services.
- Clear architectural boundaries.
- Consistent error handling.
- Accessibility and responsive design for frontend changes.

Do not introduce abstractions solely to make the code more complex.

## Documentation

Documentation is part of the implementation.

| Change | Documentation |
| --- | --- |
| Product scope | `SPEC.md` |
| Requirements | `docs/REQUIREMENTS.md` |
| Architecture | `docs/ARCHITECTURE.md` |
| Testing strategy | `docs/TESTING.md` |

Keep documentation synchronized with the implementation. Architectural decisions should not exist only in source code or commit messages.

## Testing

Testing is required for meaningful changes.

### Unit and Component Tests

Use Vitest and Testing Library for components, hooks, utilities, validation, state behavior, and important interactions.

### End-to-End Tests

Use Playwright for critical flows such as authentication, product browsing, search/filtering, favorites, cart, checkout, address management, and administrative CRUD where applicable.

### Before Merging

```text
[ ] Unit tests pass
[ ] Component tests pass when affected
[ ] E2E tests pass when affected
[ ] Type checking passes
[ ] Linting passes
[ ] Production build succeeds
[ ] Responsive behavior was checked for UI changes
```

## UI and Design

Figma is used for Armoniq's:

- Color palette.
- Typography.
- Logos and brand assets.
- UI references.
- Design decisions.

Significant UI changes should include appropriate screenshots and respect the mobile-first responsive design.

## Quality and CI/CD

The project uses:

- ESLint.
- Prettier.
- Husky.
- lint-staged.
- Commitlint.
- SonarCloud.
- GitHub Actions.

CI should validate relevant changes through dependency installation, linting, type checking, tests, and builds.

Do not bypass quality checks simply to merge a change. Document intentional changes to the quality pipeline.

## Security and Secrets

Never commit:

- `.env` files containing real credentials.
- API keys.
- Access tokens.
- Refresh tokens.
- Passwords.
- Private keys.
- Cloud provider credentials.
- Payment credentials.

Use `.env.example` to document required variables without exposing their values.

Use sandbox/test credentials for integrations whenever available.

## Scope and Project Context

Armoniq is a fictional musical-instrument e-commerce project created for portfolio development and real-world software engineering practice.

The project should prioritize:

1. Completing the defined MVP.
2. Maintaining a realistic e-commerce workflow.
3. Preserving the documented architecture.
4. Maintaining security and testability.
5. Keeping documentation synchronized.
6. Avoiding unnecessary scope expansion.

The project consists of three independent repositories:

- `Armoniq-api`: shared backend API.
- `Armoniq-admin`: administration application.
- `Armoniq-storefront`: customer-facing store.

Changes affecting contracts between repositories must be coordinated. API contract changes may require corresponding updates in both frontend applications.

Features outside the defined project scope should be discussed before implementation.

## Code of Conduct

Contributors are expected to maintain a respectful, professional, and constructive environment.

Communication should focus on:

- Technical reasoning.
- Evidence.
- Clear feedback.
- Respectful disagreement.
- Collaboration.

Harassment, discrimination, personal attacks, or intentionally disruptive behavior are not acceptable.

## Final Checklist

Before opening a Pull Request:

```text
[ ] Issue and milestone are identified
[ ] Branch follows the naming convention
[ ] Implementation follows the repository architecture
[ ] No secrets were committed
[ ] Tests were added or updated when appropriate
[ ] Linting and type checking pass
[ ] Project builds successfully
[ ] Documentation was updated
[ ] UI screenshots were added when appropriate
[ ] Pull Request clearly explains the change
```
