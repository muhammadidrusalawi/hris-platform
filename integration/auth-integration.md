# Authentication Integration

## Token Handling
- JWT token attached via Authorization header
- Token injected automatically in API client

## React Query Integration
- Queries depend on authentication state
- Cache cleared on logout
- Unauthorized responses trigger logout flow

## Error Handling
- 401 → Unauthorized (force logout)
- 403 → Forbidden (show access denied UI)