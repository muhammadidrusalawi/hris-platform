# Frontend Architecture

- Repository: https://github.com/muhammadidrusalawi/hris-web
- Framework: React (TypeScript)

## State Management Strategy

### Server State
Handled by **React Query**:
- Data fetching
- Caching
- Background refetching
- Synchronization with backend

### Client / Global State
Handled by **React Context**:
- Authentication state
- User identity
- Role information

React Context is NOT used for server data.

## Validation
Client-side validation is handled using **Zod**:
- Form validation
- Type-safe schemas
- Shared validation logic

## Key Rules
- Frontend never enforces authorization rules
- Role-based UI rendering depends on backend response
- Backend remains the source of truth