# Spring Security
- add dependency `spring-boot-starter-security` will secure all the end points
- passwords are stored in specific format `{id}encodedPassword`\
  - `{noop}test123`, `noop` is encrypting algo used `test123` is the password
- `@Cofiguration` bean is used to 
- There are multiple ways to authenticate
  - In memory
  - JDBC etc
## Declarative Security
- Define application's security constraints in configuration
  - `@Configuration`
- Provides separation of concerns b/w application code and security
## Programing Security
- Spring Security provides an API for custom app conding
- Provides greater customization for specific app req

# Cross-Site Request Forgery (CSRF)
- Spring Security can protect against CSRF attacks
- Embed additional authentication data/token into all HTML forms
- On subsequent requests, web app will verify token before processing
- primary use case is traditional web apps
- Can be used for any normal browser web requests
- CSRF can be disabled for non-browser clients
- CSRF not required for stateless APIs that use POST, PUT, DELETE, PATCH
# JDBC authentication
- Default Spring Security Database Schema consist of two tables `users` and `authorities`
  - users table has below fields
    - username, password, enabled
  - authorities table has below fields
    - username, authority
- Internally Spring Security uses "ROLE_" prefix for the authority in authorities table
- Spring will automatically read data from the database if we follow spring conventions and create tables in that way
- 