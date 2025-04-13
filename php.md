# LLM Code Generation Context: Modern PHP

**Core Philosophy:** Generate readable, simple, maintainable, and modern PHP code. Prioritize native PHP features and coding standards. Use Composer packages for common tasks.

**Technology Stack & Priorities:**

1.  **PHP:**
    *   **Version:** PHP 8.3+ (unless otherwise specified).
    *   **Coding Standards:** Follow PSR-12 coding standards.
    *   **Error Handling:** Use exceptions for error handling.
    *   **Type Declarations:** Use strict type declarations (`declare(strict_types=1);`).
    *   **Modern Features:** Embrace modern PHP features like arrow functions, null coalescing operator, match expression, etc.

2.  **Composer:**
    *   **Dependency Management:** Use Composer for managing dependencies.
    *   **Autoloading:** Rely on Composer's autoloader.

4.  **Database:**
    *   **PDO:** Use PDO for database interactions when not using Laravel's Eloquent ORM.
    *   **Prepared Statements:** Always use prepared statements to prevent SQL injection.

**Coding Guidelines:**

*   **Simplicity:** Always prefer the simplest, most straightforward implementation.
*   **Readability & Maintainability:** Write code that is easy to read, understand, and extend. Use verbose and descriptive naming.
*   **Structure:** For simple scripts, aim for a single file. Refactor into classes and functions as complexity grows.
*   **No Hardcoding:** Never hardcode sensitive information (PII, URLs, API keys) or configuration values. Use environment variables (`.env` files) or configuration files.
*   **Logging:** Implement comprehensive logging for all significant steps. Use a logging library like Monolog.
*   **Documentation:** Document code thoroughly using docblocks and comments. Follow PHPDoc standards.
*   **Security:** Implement relevant OWASP Top Ten security recommendations pragmatically.

**Specific Instructions:**

*   **Single-File Scripts:** For simple tasks, create single PHP files that can be run from the command line. Use Composer for dependency management.
*   **Web Applications:** For web applications, use also a single file with a simple server, such as PHP's built-in web server. Ensure proper routing and handling of requests, including error handling and response formatting, and implement proper security measures such as CSRF protection and XSS prevention, including input validation and output encoding.
*   **Input Validation:** Always validate user input to prevent security vulnerabilities.
*   **Output Encoding:** Encode output properly to prevent XSS vulnerabilities.
*   **Error Reporting:** Configure error reporting appropriately for development and production environments.

**Exclusions (Unless explicitly requested):**

*   **Legacy Code:** Avoid using deprecated features or outdated coding practices.
*   **Over-Engineering:** Don't over-engineer solutions. Keep it simple and focused.
*   **Unnecessary Dependencies:** Avoid using unnecessary dependencies. Use native PHP features when possible.

**Goal:** Generate code that is immediately understandable, follows modern PHP standards, leverages the specified stack effectively, and integrates seamlessly with existing projects. Prioritize simplicity and directness.
