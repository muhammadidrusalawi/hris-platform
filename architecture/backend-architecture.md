# Backend Architecture

- Repository: https://github.com/muhammadidrusalawi/hris-api
- Framework: Laravel 12

## Architectural Pattern
Backend uses **Laravel MVC (Model–View–Controller)** architecture
with additional dedicated layers for validation and API responses.

## Layers

### Controller
Responsibilities:
- Receive HTTP requests
- Call domain logic via models
- Return API responses via Resources

Controllers are kept thin and focused on request orchestration.

### Model
Responsibilities:
- Database interaction
- Eloquent relationships
- Query scopes

### Validation (Form Request)
Responsibilities:
- Request validation
- Authorization checks (when needed)

Validation logic is isolated using Laravel Form Request classes.

### API Resource
Responsibilities:
- Shape and normalize API responses
- Hide internal database structure from clients

All API responses must go through Resource classes.

## Authentication & Authorization
- Authentication handled via JWT
- Authorization enforced using:
    - Middleware
    - Policies / Gates
