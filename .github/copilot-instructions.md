## Security

- Validate input sanitization practices.
- Search for risks that might expose user data.
- Prefer loading configuration and content from the database instead of hard coded content. If absolutely necessary, load it from environment variables or a non-committed config file.

## Code Quality

- Use consistent naming conventions.
- Try to reduce code duplication.
- Prefer maintainability and readability over optimization.
- If a method is used a lot, try to optimize it for performance.
- Prefer explicit error handling over silent failures.

---
applyTo: "*.html,*.css,*.js"
---

## Frontend Guidelines

- Use accessibility attributes (alt text, aria labels) and color schemes.
- Use responsive design for compatibility with mobile devices.
- Validate HTML structure and semantic elements


---
applyTo: "backend/**/*,*.py"
---

## Backend Guidelines

- All API endpoints must be defined in the `routers` folder.
- Load example database content from the `database.py` file.
- Error handling is only logged on the server. Do not propagate to the frontend.
- Ensure all APIs are explained in the documentation.
- Verify changes in the backend are reflected in the frontend (`src/static/**`). If possible breaking changes are found, mention them to the developer.

---
applyTo: "tests/**/**,docs/*.md"
---
## Testing Guidelines

- Write unit tests for all public functions and methods to ensure functionality.
- Use descriptive test names that explain the expected behavior.
- Include integration tests for API endpoints and database interactions.
- Aim for high code coverage (at least 80%) and run tests automatically in CI/CD pipelines.
- Mock external dependencies to isolate tests and avoid flaky results.
- Document test cases in comments for clarity and maintainability.

---
applyTo: "docs/*.md,README.md"
---
## Documentation Guidelines

- Keep all documentation up to date with code changes, including API endpoints and features.
- Use clear, concise language and include examples where helpful.
- Structure documents with headings, lists, and code snippets for readability.
- Include setup instructions, usage examples, and troubleshooting in README.md.
- Ensure accessibility by using alt text for images and semantic Markdown.
- Review and update documentation during code reviews to prevent outdated information.