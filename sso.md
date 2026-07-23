# Types of Single Sign-On (SSO)

Single Sign-On (SSO) allows users to access multiple applications using a single set of login credentials. Microsoft Entra ID supports several SSO methods based on application requirements and authentication protocols.

## Password-Based SSO
###  What is it?

Password-Based SSO stores the user's application credentials securely in Microsoft Entra ID. When the user signs in, Azure automatically enters the username and password for the application.

### Why do we use it?

It is used for legacy or web applications that do not support modern authentication protocols. It simplifies user access by eliminating the need to remember multiple passwords.

##  Linked SSO
### What is it?

Linked SSO provides users with a direct link to an external application after they sign in to Microsoft Entra ID. Azure does not authenticate the user to the application.

### Why do we use it?

It is used when an application manages its own authentication but administrators want users to access it easily from the Microsoft Entra portal.

## SAML-Based SSO
### What is it?

SAML (Security Assertion Markup Language) SSO uses the SAML 2.0 protocol to exchange authentication information between Microsoft Entra ID and the application. After a successful login, Azure sends a SAML assertion to the application.

### Why do we use it?

It is widely used for enterprise and SaaS applications because it provides secure authentication, supports Single Sign-On, and eliminates the need for separate application credentials.

## OpenID Connect (OIDC) SSO
### What is it?

OpenID Connect (OIDC) is an identity layer built on top of the OAuth 2.0 protocol. It allows applications to authenticate users through Microsoft Entra ID using JSON Web Tokens (JWT).

### Why do we use it?

It is commonly used by modern web and mobile applications because it is lightweight, secure, and easy to integrate with cloud-native applications.

## OAuth 2.0 SSO
### What is it?

OAuth 2.0 is an authorization framework that allows applications to securely access resources on behalf of a user without exposing their password. It uses access tokens to authorize API requests.

### Why do we use it?

It is primarily used for securing APIs and allowing applications to access Microsoft Graph or other protected services without requiring the user's credentials.

## Header-Based SSO
### What is it?

Header-Based SSO authenticates users by passing identity information through HTTP headers. It is commonly used with on-premises applications published through Azure Application Proxy.

### Why do we use it?

It is used to provide Single Sign-On for legacy web applications that rely on HTTP headers for authentication instead of modern protocols.
