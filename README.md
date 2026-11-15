# Awesome-Oauth-2.0-Token-Authentication-Service

# Awesome OAuth 2.0 & Token Authentication Service

> A curated list of top OAuth 2.0 and Token Authentication Service platforms — both SaaS/Hosted commercial solutions and open-source alternatives for implementing standards-based authorization, token issuance, and identity federation.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Auth0](#auth0)
  - [Okta Customer Identity Cloud](#okta-customer-identity-cloud)
  - [Clerk](#clerk)
  - [Stytch](#stytch)
  - [FusionAuth Cloud](#fusionauth-cloud)
  - [Descope](#descope)
- [Open-Source Software](#-open-source-software)
  - [Keycloak](#keycloak)
  - [Ory Hydra](#ory-hydra)
  - [Casdoor](#casdoor)
  - [Zitadel](#zitadel)
  - [Authentik](#authentik)
  - [FusionAuth Community](#fusionauth-community)
  - [Hanko](#hanko)
  - [Duende IdentityServer](#duende-identityserver)
  - [OpenIddict](#openiddict)
  - [node-oidc-provider](#node-oidc-provider)
  - [Idenplane](#idenplane)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted OAuth 2.0 and Token Authentication Service platforms. These are not open-source but are included as reference points for feature comparison.

### Auth0
**Type:** Developer-first CIAM with extensive extensibility
Auth0 is the most widely adopted developer-focused identity platform, providing OAuth 2.0, OIDC, and SAML support with a vast ecosystem of SDKs, social providers, and extensibility through Rules and Actions. It is the primary commercial reference for open-source alternatives like Keycloak and Ory Hydra.

### Okta Customer Identity Cloud
**Type:** Enterprise CIAM with broad integration catalogue
Okta's Customer Identity Cloud (powered by Auth0) provides enterprise-grade CIAM with strong governance, compliance, and integration depth. It is positioned for organizations needing both workforce and customer identity in a unified platform.

### Clerk
**Type:** Developer-first authentication with polished UI components
Clerk provides drop-in authentication components for React, Next.js, and modern frameworks, with a strong focus on developer experience and pre-built UI. It is positioned for SaaS teams wanting to ship authentication quickly without building login screens from scratch.

### Stytch
**Type:** Passwordless-first authentication platform
Stytch focuses on passwordless authentication as a first-class experience, with full control over authentication UI. It is suited for development teams building consumer or B2B applications where authentication UX is a core product differentiator.

### FusionAuth Cloud
**Type:** Managed CIAM with same feature set as self-hosted
FusionAuth Cloud provides the same comprehensive CIAM capabilities as its self-hosted edition, with managed infrastructure. It is positioned for teams wanting a turnkey CIAM solution without the operational overhead of self-hosting.

### Descope
**Type:** No-code identity and user management
Descope offers visual workflow-based authentication and user management, with support for passwordless, MFA, and SSO. It is positioned for teams wanting to design authentication flows without deep identity protocol expertise.

---

## 🟩 Open-Source Software

Self-hosted, community-driven OAuth 2.0 and Token Authentication Service tools. The open-source ecosystem spans **full-featured IAM platforms**, **headless OAuth2 providers**, **Go-based single-binary solutions**, and **framework-specific libraries**.

### Keycloak
**Stack:** Java (Quarkus) | **License:** Apache-2.0
Keycloak is the most widely deployed open-source identity and access management platform, providing OAuth 2.0, OIDC, SAML, and WebAuthn support with LDAP/AD user federation . It is the most feature-complete general-purpose IdP, with the most extension points for Java developers through Service Provider Interfaces (SPIs) . Keycloak supports token exchange (RFC 8693), UMA 2.0, FAPI, and pushed authorization requests (PAR) for advanced OAuth profiles . It is a CNCF project with commercial support from Red Hat. **Trade-off:** Java/Quarkus architecture requires JVM tuning and Infinispan caching for clusters; resource footprint is higher than lighter Go alternatives.
**Best for:** Organizations needing a proven, standards-complete IAM platform with deep Java extensibility and broad protocol support, accepting the operational overhead of a JVM-based server.

### Ory Hydra
**Stack:** Go | **License:** Apache-2.0
Ory Hydra is a hardened, OpenID Certified OAuth 2.0 Authorization Server and OpenID Connect Provider, optimized for low latency and high throughput . It is **headless by design**—it does not provide a login UI or user management, instead implementing the OAuth2 layer over an existing user store . It supports token exchange, DPoP, and relationship-based authorization through Ory Keto . **Trade-off:** Requires you to build and operate the login and consent application yourself, making it a component rather than a complete solution.
**Best for:** Teams wanting a focused, high-performance OAuth2/OIDC layer to add to an existing identity system, accepting responsibility for the login and consent UI.

### Casdoor
**Stack:** Go / React | **License:** Apache-2.0
Casdoor is a UI-first open-source IAM platform with a single Go binary and React frontend, supporting OAuth 2.0, OIDC, SAML, CAS, LDAP, RADIUS, SCIM, and WebAuthn . It includes **70+ built-in social and enterprise providers** (WeChat, DingTalk, Lark, Alipay) and uses Casbin for authorization (ACL, RBAC, ABAC) . A key differentiator is **built-in MCP server and OAuth 2.1 authorization server for MCP**, treating AI agents as first-class clients . The login page is configured per-application in the admin console rather than deployed as code . **Trade-off:** Smaller community than Keycloak; some advanced OAuth profiles (UMA 2.0, FAPI, PAR) are not supported.
**Best for:** Teams wanting a modern, Go-based IAM with broad protocol coverage, extensive social providers, and built-in MCP support for AI agents.

### Zitadel
**Stack:** Go / TypeScript | **License:** AGPL-3.0
Zitadel is a cloud-native identity platform with a focus on **multi-tenancy and self-service**. It provides OIDC, SAML, MFA, passwordless, and user management with a modern API-first design . It supports **RFC 8693 token exchange** (since v2.49) and SCIM 2.0 server for receiving users from Entra ID or Okta . It is positioned for modern multi-tenant SaaS applications, with organizations built in as a first-class concept . **Trade-off:** AGPL licensing; smaller ecosystem than Keycloak.
**Best for:** Modern multi-tenant SaaS applications wanting organizations and self-service built in, accepting AGPL licensing.

### Authentik
**Stack:** Python / Go | **License:** MIT core / Enterprise
Authentik provides the **most flexible sign-in flow engine** among open-source IAM tools, with flows and stages edited in the admin interface and Python expression policies for custom logic . It supports OAuth 2.0, OIDC, SAML, LDAP outpost, RADIUS outpost, and SCIM source for syncing users from external directories . It also includes a proxy provider for Traefik, Caddy, Nginx, and Envoy. **Trade-off:** Enterprise features (including separate tenants) are gated to the paid tier; multi-tenancy is handled through "Brands" rather than true tenant isolation.
**Best for:** Teams needing highly customizable authentication flows with proxy-based access control, accepting the Python/Go stack and enterprise gating for full multi-tenancy.

### FusionAuth Community
**Stack:** Java | **License:** Source-available (Community edition free)
FusionAuth ships a broad CIAM feature set—registration, login, social sign-on, MFA, and user management—as a **single downloadable application**, with no user cap on the free Community edition . It is developer-friendly with strong APIs, webhooks, and localization, and supports multi-tenancy and multi-application setups . It is a common choice for companies with strict data-residency requirements needing to run CIAM on their own infrastructure . **Trade-off:** The Community edition is source-available rather than a permissive OSI license; advanced features and SLAs require paid editions .
**Best for:** Teams wanting a complete CIAM feature set in a single self-hosted download with no user cap, accepting the source-available licensing model.

### Hanko
**Stack:** Go | **License:** Open Source (self-hostable)
Hanko is an open-source authentication and user management solution focused on **moving beyond passwords** while being deployable today . It supports passkeys, social logins, SAML SSO, MFA (TOTP, security keys), and optional passwords . It provides **Hanko Elements** web components for embeddable login/registration and account profile UI, making integration fast . It is API-first with a small footprint and cloud-native architecture, available for self-hosting or on Hanko Cloud . **Trade-off:** Younger project with a smaller ecosystem than Keycloak; SDK coverage is still expanding.
**Best for:** Teams wanting a modern, passkey-first authentication solution with embeddable UI components, accepting a newer ecosystem.

### Duende IdentityServer
**Stack:** .NET / ASP.NET Core | **License:** Open Source (RPL for commercial)
Duende IdentityServer is an OpenID Connect and OAuth 2.0 framework for ASP.NET Core, listed in Microsoft's official community OSS authentication options . It is the most mature OAuth2/OIDC server implementation for the .NET ecosystem, with strong standards compliance and extensive documentation. **Trade-off:** Commercial use requires a paid license under the Reciprocal Public License; free for open-source and development use.
**Best for:** .NET teams needing a proven, standards-compliant OAuth2/OIDC server native to ASP.NET Core, accepting the commercial licensing terms for production.

### OpenIddict
**Stack:** .NET / ASP.NET Core | **License:** Apache-2.0
OpenIddict is an **Apache-2.0 licensed** OAuth 2.0/OpenID Connect server for ASP.NET Core and ASP.NET 4.x, providing a permissive alternative to Duende IdentityServer . It also functions as a client for 80+ external providers including Auth0, Microsoft Entra ID, GitHub, and Google . It is positioned for .NET teams wanting full control over their token server without commercial licensing restrictions.
**Best for:** .NET teams wanting a permissively licensed OAuth2/OIDC server with client capabilities for external providers, accepting a smaller ecosystem than Duende.

### node-oidc-provider
**Stack:** Node.js | **License:** Open Source
node-oidc-provider is a **certified** OpenID Connect Provider implementation for Node.js, listed in Microsoft's official community OSS authentication options . It provides a standards-compliant OIDC provider for Node.js applications, with certification from the OpenID Foundation. It is positioned for Node.js teams wanting a proven, certified OIDC implementation rather than building from scratch.
**Best for:** Node.js teams needing a certified OIDC provider, accepting a narrower focus than full IAM platforms.

### Idenplane
**Stack:** TypeScript / NestJS / PostgreSQL | **License:** Open Source
Idenplane is a lightweight open-source IAM server positioned as an alternative to Keycloak and Auth0, running in **~150 MB of RAM** (vs Keycloak's 1 GB+) . It supports OAuth 2.0, OIDC, SAML 2.0, WebAuthn/FIDO2, TOTP/MFA, SCIM 2.0, and Device Authorization (RFC 8628) . Key features include multi-tenancy via realms, organizations (B2B), RBAC + ABAC, hierarchical groups, LDAP federation, external IdP brokering, magic links, risk-based adaptive auth, and **migration importers for Auth0 and Keycloak configurations** . It is stateless and horizontally scalable, with 10 client SDKs and Prometheus metrics.
**Best for:** Teams wanting a lightweight, modern IAM with Keycloak/Auth0 migration paths and low resource footprint, accepting a newer project than established alternatives.

---

## 📊 Comparison at a Glance

| Software | License | Stack | OAuth2/OIDC | MCP Support | Resource Footprint | Self-Hosted | Best For |
|----------|---------|-------|-------------|-------------|---------------------|-------------|----------|
| **Auth0** | Proprietary | Cloud | ✅ | (Check) | N/A | ❌ | Developer-first CIAM |
| **Clerk** | Proprietary | Cloud | ✅ | ❌ | N/A | ❌ | Drop-in React auth |
| **Keycloak** | Apache-2.0 | Java/Quarkus | ✅ Full | ❌ | High (JVM) | ✅ | Complete IAM + Java SPIs |
| **Ory Hydra** | Apache-2.0 | Go | ✅ Headless | ❌ | Low | ✅ | OAuth layer over existing store |
| **Casdoor** | Apache-2.0 | Go/React | ✅ | ✅ Built-in | Moderate | ✅ | Go IAM + 70+ providers + MCP |
| **Zitadel** | AGPL-3.0 | Go/TS | ✅ | ❌ | Moderate | ✅ | Multi-tenant SaaS |
| **Authentik** | MIT core | Python/Go | ✅ | ❌ | Moderate | ✅ | Flexible sign-in flows |
| **FusionAuth** | Source-available | Java | ✅ | ❌ | Moderate | ✅ | Complete CIAM, no user cap |
| **Hanko** | Open Source | Go | ✅ | ❌ | Low | ✅ | Passkey-first + web components |
| **Idenplane** | Open Source | TS/NestJS | ✅ | ❌ | ~150 MB | ✅ | Lightweight Keycloak alternative |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source OAuth 2.0 or Token Authentication Service tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The OAuth2/OIDC landscape splits between **full IAM platforms** (Keycloak, Casdoor, Zitadel, Authentik, FusionAuth, Idenplane) that handle authentication, user management, and authorization in one system, and **headless OAuth layers** (Ory Hydra) that implement only the protocol layer over an existing user store. **Keycloak** remains the most feature-complete general-purpose option with the most advanced OAuth profile coverage (UMA 2.0, FAPI, PAR) and deep Java extensibility . **Casdoor** is the strongest modern alternative for teams wanting a Go-based single binary with broad social provider coverage and built-in MCP support for AI agents . **Ory Hydra** is the right choice when you already have a user store and need a hardened, high-performance OAuth2 layer without user management . For lightweight deployments, **Idenplane** offers Keycloak-like functionality at ~150 MB RAM with Auth0/Keycloak migration paths . .NET teams should evaluate **OpenIddict** (permissive Apache-2.0) versus **Duende IdentityServer** (mature but commercially licensed) .

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
