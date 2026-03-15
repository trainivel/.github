# Copilot Instructions

## Purpose
This is a Laravel 12 modular application with **account-based isolation** and strict workspace separation. Copilot must follow all project standards for DTOs, migrations, transformers, and tests.

## Mandatory Rules

1. **Account isolation**
   - Queries and API calls must only access records for the authenticated user's accounts.
   - Unauthorized access must return empty results or deny access.

2. **DTOs**
   - No constructors.
   - Use named static constructors.
   - Fluent getters and setters.
   - Transformations must go through a Transformer class.
   - Immutable unless set via setter.
   
3. **Database**
   - No JSON columns.
   - No ENUM columns in migrations.
   - Use PHP enums for all domain states, types, and statuses.
   
4. **Transformers / Adapters**
   - All API ↔ DTO ↔ destination conversions go through Transformers.
   - No direct API requests in controllers or services.
   
5. **Testing**
   - Use `it_should_*` naming for all PHPUnit tests.
   - Always test happy path + 5 failure modes.
   - Include validation, authorization, business rules, destructive action safeguards.
   - Fixtures loaded from JSON, converted to DTOs.

6. **Coding Conventions**
   - Early returns.
   - Small, clear methods.
   - No commented-out code.
   - Keep documentation synchronized with module names and behaviors.
