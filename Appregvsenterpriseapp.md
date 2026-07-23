# Azure App Registration
## Introduction

Azure App Registration is a feature in Microsoft Entra ID (formerly Azure Active Directory) that allows applications to be registered with Azure for identity and access management. It creates a unique identity for an application, enabling it to authenticate users, access Microsoft services, and securely interact with APIs. Every registered application receives a unique Application (Client) ID and can be configured with authentication methods, API permissions, certificates, and client secrets.

App Registration is commonly used for web applications, mobile applications, APIs, background services, and automation scripts that need secure authentication with Microsoft Entra ID.

### Key Features
* Provides a unique identity for an application.
* Supports user authentication using Microsoft Entra ID.
* Enables secure access to Microsoft Graph and other APIs.
* Supports OAuth 2.0 and OpenID Connect authentication protocols.
* Allows creation of Client Secrets and Certificates.
* Supports Single Sign-On (SSO) and Multi-Factor Authentication (MFA).
* Can define Redirect URIs for web and mobile applications.
* Allows configuration of API permissions and application roles.
### Benefits
* Secure authentication and authorization.
* Simplifies API access using Microsoft Entra ID.
* Supports enterprise-grade security features.
* Enables integration with Microsoft 365 and Azure services.
* Centralized identity management for applications.

# Enterprise Applications
## Introduction

An Enterprise Application in Microsoft Entra ID represents an application's service principal within a tenant. It is created automatically when an application is registered in the same tenant or when an external (third-party) application is added from the Microsoft Entra Gallery. Enterprise Applications are used to manage how users and groups access an application after it has been registered.

Unlike App Registration, which defines the application itself, an Enterprise Application represents the application's instance within an organization and is responsible for authentication, authorization, user assignments, and access policies.

### Key Features
* Represents the application's Service Principal in the tenant.
* Manages user and group assignments.
* Supports Single Sign-On (SSO).
* Allows configuration of Conditional Access policies.
* Enables Multi-Factor Authentication (MFA).
* Provides sign-in logs and audit logs.
* Supports third-party SaaS applications from the Microsoft Entra Gallery.
* Controls application permissions within the organization.
### Benefits
* Centralized management of application access.
* Improved security through Conditional Access and MFA.
* Simplified user provisioning and access control.
* Easy integration with cloud and SaaS applications.
* Detailed monitoring through sign-in and audit logs.
