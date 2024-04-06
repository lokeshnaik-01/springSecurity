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
