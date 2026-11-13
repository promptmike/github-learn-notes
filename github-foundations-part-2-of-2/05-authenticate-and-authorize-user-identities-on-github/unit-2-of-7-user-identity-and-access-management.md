# User identity and access management

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

Enterprise security requires at least 2FA, if not more advanced methods such as passkeys or biometric authentication.
> We must use secure authentication methods to guard the enterprise.

## Modern Authentication in GitHub Enterprise

GitHub supports up-to-date methods that integrate with identity management systems.
> We must use up-to-date methods to authenticate users and guard the enterprise.

### Passkeys and WebAuthn

Passkeys are a passwordless method tied to a physical device, while WebAuthn supports biometric methods and hardware tokens.
> We must use secure authentication such as Passkeys or WebAuthn to resist phishing and credential-based attacks.

### GitHub Mobile for 2FA

GitHub Mobile supports push notifications for quick 2FA login.
> We must use secure authentication such as Passkeys, WebAuthn or 2FA with GitHub Mobile.

### OAuth and GitHub Apps

OAuth Apps use GitHub's OAuth 2.0 flow for external applications, while GitHub Apps authenticate as individual installations with fine-grained permissions.
> We must use secure methods and never rely on passwords alone.

### Enterprise Managed Users (EMU)

EMUs force all authentication to go through your IdP and can only be used by enterprise-managed accounts in GitHub Enterprise Cloud.
> Use the strongest possible methods to enforce secure login.

## Organization Management with SAML SSO

SAML links your IdP with GitHub, allowing users to sign in across services with a single set of credentials.
> We must use the strongest possible methods while keeping the sign in process convenient for users.

Users of SAML SSO can see the enterprises they belong to, but accessing repo data requires reauthentication by IdP.
> Use strong authentication methods while keeping sign in UX as smooth as possible.

Enterprise Admins must authorise access based on role and need-to-know, monitor and audit user activity, scope permissions and minimise the surface area for attacks.
> Admins have the responsibility to follow the principle of least privilege to secure assets.

![Insights: People - list of users with repo access](https://learn.microsoft.com/en-us/training/github/authenticate-authorize-user-identities-github/media/repository-permission-list-example.png)

To configure SAML SSO, integrate your IdP with GitHub.
> Admins have the responsibility to follow the principle of least privilege to secure assets and user identities.

==⚠️ **Note**==
==GitHub provides limited support for identity providers that implement the SAML 2.0 standard.==

## Enterprise Access and Authorization Controls

### Fine-Grained Personal Access Tokens (PATs)

Unlike classic Pats, fine-grained PATs restrict access to specific repos and scopes, support automatic expiration and offer enhanced traceability and compliance.
> Admins must provide secure, fine-grained access control to protect organisation assets and user identities.

### Custom Repository Roles

Admins can set custom roles that extend default permission sets to provide tailored access.
> Use secure, fine-grained methods and tailored permissions following the principle of least privilege.

### Security Policy Enforcement

You can set global rules such as enforcing 2FA, IP allowlists of approved networks only or blocking unverified OAuth Apps.
> Set global rules, then use fine-grained methods and custom roles to tailor permissions as needed for least privilege.

### Organizational and Enterprise-Level Controls

**Organization:**
- Default roles
- Team-based access
- Managing external collaborators

**Enterprise:**
- SAML
- IdP
- Global policy

> Use Enterprise, Organization and team controls to set roles and permissions following the principle of least privilege.

## Repository Visibility and Internal Access

Public repos are visible to everyone, private repos only to select users, and internal repos to everyone in an enterprise.
> Use modern, secure authentication methods at enterprise, organization and repository levels to protect user identities and reduce the attack surface.
