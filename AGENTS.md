# Temp Mail development rules

## Project baseline

- Build a modern temporary email SaaS as a modular monolith targeting Laravel 13 and PHP 8.5.
- Use Blade, Tailwind CSS, Alpine.js, and Vite. Support MySQL, MariaDB, PostgreSQL, and SQLite.
- Follow the shared Balanced Premium SaaS design system with Zinc neutrals, Indigo accents, and Comfortable density. Support Light, Dark, and System appearance. Default to System.
- Target WCAG 2.2 AA. Use English for product UI, source code, identifiers, comments, and documentation.

## Workflow

- Inspect the repository and Git status before editing. Preserve unrelated work. Read the relevant [project documentation](docs/) before implementing a module, as those documents become available.
- Treat unresolved product decisions as open. Do not invent features or permissions.
- Add or update relevant automated tests when functionality changes. Run available checks and report any that could not run.
- Update relevant documentation when architecture or behavior changes. Record significant decisions in [the decision log](docs/decisions/).

## Implementation

- Respect module boundaries and keep dependencies between modules minimal. Prefer small, maintainable classes and reusable Blade components. Avoid monolithic controllers, views, JavaScript, and CSS.
- Use the shared design system for Installer, Authentication, Dashboard, Profile, and future modules. Module-specific themes are prohibited.
- Use semantic HTML, keyboard interactions, focus management, responsive layouts, and reduced-motion support.
- Apply Laravel validation, authorization, CSRF protection, secure sessions, rate limiting, and safe error handling where applicable. Keep secrets out of logs, output, browser storage, commits, and documentation.
- Protect existing installations and data. Never use the existence of `.env` alone to determine installation state. Support initial browser installation on localhost, VPS, and supported shared hosting without requiring SSH.

## Git and handoff

- Follow Conventional Commits and commit only validated work. Never force-push, overwrite unrelated changes, or commit credentials.
- Push to the configured remote only when authenticated and authorized. Report commit and push success only after Git confirms it.
- Before completing a task, report changed files, tests and checks, known limitations, and Git status.
