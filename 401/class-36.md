# CF 401: Java // Reading Notes

## Class 36: Cognito

## Readings

[Amplify and Cognito](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)

### Questions

1. Where in your application should you check the current auth session?
2. what is the command that is used to push your changes to the cloud?
3. What does Amplify Auth do for your application?

### Answers

1. Checking the Current Auth Session:

* You should check the current auth session in your application where authentication-related operations need to be performed. Common scenarios include checking if the user is authenticated before allowing access to certain parts of your app or checking if the user's session has expired and requires reauthentication.
* To check the current auth session, you can use Amplify Auth's methods, such as `Amplify.Auth.fetchAuthSession()`, to retrieve the current authentication session. You can then inspect the session's state to determine the user's authentication status.
Example code snippet to check the current auth session:

```java
Amplify.Auth.fetchAuthSession(
    result -> {
        if (result.isSignedIn()) {
            // User is signed in
        } else {
            // User is not signed in
        }
    },
    error -> {
        // Handle the error
    }
);
```

2. `amplify push`
3. Amplify Auth in Your Application:

* Amplify Auth is a part of the AWS Amplify library that provides authentication and user management capabilities for your Android app. It simplifies the integration of AWS Cognito into your application for user authentication.
* Here's what Amplify Auth does for your application:
    * User Authentication: Amplify Auth enables user registration, sign-in, and sign-out functionalities.
    * Identity Verification: It allows you to verify user identities through methods like email or phone number confirmation.
    * Session Management: Amplify Auth handles user sessions and provides methods to check if a user is signed in or fetch the current auth session.
    * User Attributes: You can manage user attributes like profile information.
    * Password Management: Amplify Auth allows users to change their passwords and reset forgotten passwords.
    * Multi-Factor Authentication (MFA): You can enable MFA for added security.
    * Integration with Social Identities: It supports social identity providers like Google and Facebook for user sign-in.
    * Custom Authentication: You can implement custom authentication flows when needed.

Essentially, Amplify Auth provides a high-level API to manage user authentication and identity in your Android app, making it easier to integrate AWS Cognito's authentication services into your application.

To use Amplify Auth, you'll need to configure it in your app, which involves setting up authentication providers, configuring user pools, and customizing the authentication experience to fit your application's requirements.
