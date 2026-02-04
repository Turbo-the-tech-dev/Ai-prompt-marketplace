# CLAUDE.md — AI Assistant Guide for Ai-prompt-marketplace

## Project Overview

**Ai-prompt-marketplace** is a marketplace platform for AI prompts with strict schema validation. The system enforces structured prompt definitions including inputs, constraints, safety tags, expected outputs, versioning, and pricing tiers.

**Current Status:** Pre-development / planning phase. The repository contains only the initial README with the project vision. No source code, dependencies, or infrastructure have been set up yet.

## Repository Structure

```
Ai-prompt-marketplace/
├── CLAUDE.md          # This file — AI assistant guide
└── README.md          # Project description and vision
```

As the project grows, this section should be updated to reflect the actual directory layout.

## Core Domain Concepts

These are the key domain entities described in the project vision:

- **Prompt**: A structured AI prompt listing in the marketplace
- **Schema Validation**: Strict validation rules applied to all prompt definitions
- **Inputs**: Defined input parameters a prompt accepts
- **Constraints**: Rules and limitations on prompt usage
- **Safety Tags**: Labels indicating content safety classifications
- **Expected Outputs**: Descriptions of what the prompt should produce
- **Versioning**: Prompt version management (creation, updates, deprecation)
- **Pricing Tiers**: Monetization levels for prompt access

## Development Guidelines

### General Conventions

- Keep code simple and focused — avoid over-engineering
- Prefer explicit over implicit patterns
- Write self-documenting code; only add comments where logic is non-obvious
- Follow the principle of least surprise in API and schema design
- Validate at system boundaries (user input, external APIs), trust internal code

### Git Workflow

- **Branch naming:** Feature branches should use descriptive names (e.g., `feature/prompt-schema`, `fix/validation-bug`)
- **Commits:** Use clear, concise commit messages focused on "why" not "what"
- **Main branch:** Keep main stable; all work happens on feature branches
- **Pull requests:** Include a summary and test plan

### Code Style (to be enforced once tech stack is chosen)

- Use a linter and formatter from day one
- Consistent naming conventions: camelCase for variables/functions, PascalCase for types/classes
- Keep functions small and single-purpose
- Prefer composition over inheritance

### Schema and Validation Patterns

Since schema validation is central to this project:

- Define schemas declaratively (e.g., JSON Schema, Zod, Pydantic)
- Separate validation logic from business logic
- Provide clear, actionable error messages on validation failure
- Version schemas alongside prompt versions
- Never trust client-side validation alone — always validate server-side

### Security Considerations

- Never commit secrets, API keys, or credentials (use `.env` files excluded via `.gitignore`)
- Sanitize all user inputs to prevent injection attacks
- Implement proper authentication and authorization for marketplace operations
- Safety tags must be validated and cannot be bypassed by end users
- Rate-limit API endpoints to prevent abuse

### Testing Strategy

When testing is set up:

- Write tests alongside features, not as an afterthought
- Unit tests for schema validation logic and business rules
- Integration tests for API endpoints and database operations
- Test both valid inputs and edge cases / invalid inputs for all schemas

## Build and Run

No build system or dependencies are configured yet. This section should be updated when the tech stack is established. Expected entries:

```bash
# Install dependencies
# (e.g., npm install, pip install -r requirements.txt)

# Run development server
# (e.g., npm run dev, python manage.py runserver)

# Run tests
# (e.g., npm test, pytest)

# Build for production
# (e.g., npm run build)
```

## Architecture Notes

The marketplace will likely require:

- **Backend API**: REST or GraphQL endpoints for CRUD operations on prompts, users, and transactions
- **Database**: Storage for prompts, user accounts, purchase records, and version history
- **Validation Layer**: Schema validation engine for prompt definitions
- **Authentication**: User registration, login, and access control
- **Frontend**: UI for browsing, purchasing, and managing prompts (if applicable)

## For AI Assistants

When working on this codebase:

1. **Read before writing.** Always read existing files before proposing changes.
2. **Respect existing patterns.** Match the style and conventions already in use.
3. **Minimal changes.** Only modify what is necessary to accomplish the task.
4. **No speculative features.** Don't add functionality that wasn't requested.
5. **Update this file.** When significant structural changes are made (new directories, new tech stack choices, new conventions), update CLAUDE.md to reflect the current state.
6. **Security first.** Never introduce vulnerabilities — validate inputs, escape outputs, protect secrets.
7. **Test your work.** Run existing tests after changes; add tests for new functionality.
