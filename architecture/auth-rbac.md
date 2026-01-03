# Authentication & RBAC

## Authentication Methods
- Email + Password
- Employee Code

## Authentication Flow
1. Frontend sends credentials
2. Backend validates credentials
3. Backend issues JWT token
4. Frontend stores token securely
5. Token attached to every API request

## Roles
- admin → full access
- manager → manage employees & departments
- employee → access own data only

## Enforcement
RBAC is enforced strictly in backend via:
- Middleware
- Policies / Gates

Frontend uses role only for UI rendering.