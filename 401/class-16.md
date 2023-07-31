# CF 401: Java // Reading Notes

## Class 16: Spring Security/Auth

## Readings

[Spring Security Overview](https://spring.io/guides/topicals/spring-security-architecture/)

### Questions

What does it mean to authenticate a user?
What does it mean to authorize a user?
What are the three possible outcomes of the AuthenticationManager’s authenticate() method?

### Answers

1. Authentication is the process of verifying the identity of a user or entity, ensuring that they are who they claim to be. It is the first step in the security process before granting access to a system, application, or resource. The authentication process typically involves the user providing some form of credentials (such as a username and password) to prove their identity. The system then compares the provided credentials with the stored ones (e.g., in a database) to validate the user's identity. If the provided credentials match the stored ones, the user is considered authenticated, and they are granted access to the system.
2. Authorization is the process of determining what actions and resources a user is allowed to access or perform after they have been successfully authenticated. It involves defining and enforcing access controls based on the authenticated user's role, permissions, or attributes. The system checks the user's authorization level against the specific resource or action they are trying to access. If the user is authorized for the requested resource or action, they are granted permission; otherwise, access is denied.
3. 3 possibilities:
* Return an `Authentication` (normally with an `authenticated=true`) if it can verify that the input represents a valid principal
* Throw an `AuthenticationException` if it believes that the input represents an invalid principal.
* Return `null` if it cannot decide

[Spring Auth Cheat Sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)

