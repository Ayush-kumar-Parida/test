---
title : 'Single Sign On'
date : 2023-10-05T21:06:50+05:30
draft : false
---

## What is SSO?

**Single Sign-On (SSO)** is an authentication mechanism that allows users to **access multiple applications** and systems **with a single set of login credentials**. By implementing SSO, Maersk can enable seamless experiences for users across different domains, ensuring a unified login experience. This means that once a user logs in to one application or domain, they can seamlessly navigate to other interconnected applications without needing to provide their credentials again. This unified experience not only enhances user satisfaction but also simplifies the user journey, streamlining interactions and improving customer productivity. Maersk SSO is currently in development and can be seen on our **cdt.maersk.com**

![SSO](sso-diag.png)

Here we see that many sites like Fleetrisk, Supplier Connect, Maersk.com, Maersk Line all are redirected to the same login page i.e. **accounts.maersk.com** where user can login with a single set of credentials.

## Fundamental principles and Benefits of Single Sign-On (SSO)

**1. User Convenience:** SSO significantly improves the user experience by reducing the number of times users have to enter their credentials. This simplifies their interactions with various applications and services, leading to higher user satisfaction.

**2. Productivity:** SSO enhances productivity as users spend less time on authentication-related tasks. They can quickly access the tools they need, increasing overall efficiency.

**3. Security:** SSO can enhance security by centralizing user authentication and enforcing strong authentication methods. It also allows for centralized monitoring and control of user access, reducing the risk of unauthorized access.

**4. Centralized Management:** SSO solutions often provide centralized user management and access control. Administrators can easily add or remove users, control access permissions, and track user activity from a central location.

**5. Reduced Password Fatigue:** Users are less likely to resort to weak passwords or password reuse when they have fewer credentials to manage, improving overall security.

**6. Integration:** SSO can be integrated into various applications and services, including web applications, mobile apps, and cloud services, making it a versatile solution for organizations with diverse IT environments.

**7. Federation:** SSO can extend authentication across organizational boundaries through federated identity systems. This allows users to access resources from partner organizations without needing separate accounts.

**8. Single Log-Out:** Users can be logged out of all connected services simultaneously with a single log-out action, enhancing security and ensuring complete session termination.

**9. Compliance:** SSO can help organizations comply with security and privacy regulations by enforcing strong authentication and access controls.

Common SSO protocols and standards include SAML (Security Assertion Markup Language), OAuth 2.0, and OpenID Connect (OIDC). These protocols define the mechanics of how authentication and authorization are handled in an SSO environment.

Security and compliance benefits of SSO reduces the number of attack surfaces because users only log in once each day and only use one set of credentials. Reducing login to one set of credentials improves enterprise security. When employees have to use separate passwords for each app, they usually don't.
