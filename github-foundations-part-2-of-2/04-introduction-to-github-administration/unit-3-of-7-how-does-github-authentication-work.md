# How does GitHub authentication work?

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We must authenticate users in GitHub.
> Authentication is one of the most common administrative tasks in GitHub.

## GitHub's authentication options

**GitHub provides several authentication options:**

### Username and password

Administrators can allow users to continue with basic HTTP authentication.
> Admins must make careful choices with authentication methods.

==⚠️ Note==
==GitHub no longer supports password authentication for Git operations or API usage. We strongly recommend using one (or several) of the other options listed in this unit.==

### Personal access tokens

![Personal Access Tokens admin page](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/personal-access-token.png)

Users can generate a Personal Access Token (PAT) for access to a particular org or repo.
> Basic HTTP method is no longer universally supported and should be replaced with more secure methods such as PATs.

### SSH keys

SSH keys can authenticate a user to remote servers and services.
> Basic HTTP should be replaced with PATs or SSH keys where possible.

Generate an SSH key, add it to ssh-agent and add it to your GitHub account.
> PATs and SSH keys can provide secure remote access to services.

An organisation with SAML single sign-on (SSO) can provide SSH certificates to access repos.
> Use personal PATs or SSH keys, or use and organisation's SSH certs with SAML SSO.

### Deploy keys

Deploy keys are SSH keys for a single repo that holds the public key, while the private is on the user's server.
> Use personal PATs and SSH keys, SAML SSO for organisations or deploy keys for a single repo.

**Configure Fork Settings:**
1. Go to repo *Settings*
2. Left Sidebar -> *Security* -> *Deploy keys*
3. *Add deploy key*

![Add deploy key interface](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/deployment-keys.png)

## GitHub's added security options

**GitHub provides a range of security options:**

### Two-factor authentication

![Require 2FA option](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/2-factor-authentication.png)

With 2FA you sign in with your username and password, then provide a second form of authentication.
> 2FA or MFA is better than single sign-in, while PATs and SSH are better than basic HTTP authentication.

GitHub has several MFA options, such as authenticator apps, hardware security keys, passkeys and SMS codes.
> Use MFA options and PATs or SSH where possible for best security practices.

Organisations on GitHub Team and Enterprise Cloud can require 2FA for personal accounts of members, while admins of EMUs and Enterprise Server can only require 2FA for enterprise-managed accounts.
> Require MFA, PATs and SSH within the scope of your authority.

Enforcing 2FA strengthens security.
> Strengthen security by enforcing best practices such as MFA and SSH.

### SAML SSO

With SAML SSO, authentication requests are redirected to the organisation's IdP.
> Enforce best practices such as MFA and SSH, while providing a single IdP if required.

GitHub supports all providers that implement SAML 2.0.
> GitHub provides support for best practices such as MFA, SSH, Idp and SAML 2.0.

### LDAP (GitHub Enterprise Server)

Lightweight Directory Access Protocol is widely used for managing user directory information.
> GitHub supports MFA, PATs, SSH, IdP, SAML 2.0 and LDAP.

GitHub Enterprise Server supports LDAP integration to authenticate users against the existing company directory (e.g. Active Directory).
> GitHub supports many best practices such as MFA, PATs, SSH, Idp, SAML SSO and LDAP, so we should use them to maximise security for our users.
