# Pending Client Decisions

| ID | Decision | Current Default | Status |
|----|----------|-----------------|--------|
| PD-001 | Invoice Paper Size | Standard A4 Printer | Confirmed  |
| PD-002 | Product Attributes for Carpets | Confirmed | Closed |
| PD-003 | Customer Payment Allocation | Confirmed | Closed |

# Confirmed Client Decisions

## User Permissions

**Decision Date:** 2026-07-19

### Decision

- Version 1.0 supports multiple authenticated users.
- Each user has an individual username and password.
- All users have identical system permissions.
- Role-Based Authorization is out of scope for Version 1.0.
- Additional users can be created without changing the permission model.

### Impact

- No Roles table.
- No Permissions table.
- Authentication only.
- Future versions may introduce role-based authorization if required.
