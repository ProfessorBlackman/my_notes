- [x] JwtAuthenticationFIlter
- [x] OrganizationAuthenticationFilter
- [x] Organization data access check

## Roles:
- [x] Get roles form kafka
- [x] Clean data from kafka into usable data
- [x] Save roles and permissions into db
- [x] On Application start load these roles and permissions into redis
- [x] Use roles for authentication

Role Partition:
pk = ORG#{OrganizationId}Role#{RoleId}
sk = ORG#{OrganizationId}Role#{RoleId}

### Role Table
| id | role_name | description | permissions | is_system | number_of_users |
| -- |------------ | ------------ | ------------- | ----------- | -------- |
|73|publisher|no need|[view users, admin]|true|0|

## Roles data structure for redis
roles = {role - permissions}
permissions = [permission 1, permission 2, permission 3]