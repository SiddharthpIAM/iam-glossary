# IAM Glossary

> A practical glossary of 153 Identity and Access Management (IAM) terms. Each entry has a concise definition and a link to a relevant standards or guidance source.

**Scope:** Identity lifecycle, authentication, authorization, federation, provisioning, governance, and cryptography.

**Note:** This is an educational reference, not a substitute for reading the linked standards. Definitions are paraphrased for quick learning; source links may be updated as standards evolve.

## Contents
- [Core Identity Concepts](#core-identity-concepts)
- [Authentication and MFA](#authentication-and-mfa)
- [Authorization and Access Control](#authorization-and-access-control)
- [Federation, SSO, and Protocols](#federation-sso-and-protocols)
- [Provisioning and Lifecycle](#provisioning-and-lifecycle)
- [Governance, Risk, and Compliance](#governance-risk-and-compliance)
- [Cryptography and Supporting Concepts](#cryptography-and-supporting-concepts)

---

## Core Identity Concepts

| Term | One-line meaning | Reference |
|---|---|---|
| **Identity** | A set of attributes that represents a person, service, device, or other entity. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Digital identity** | An online representation of an entity used to recognize it across digital systems. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Identifier** | A value used to distinguish an entity, such as a username, UUID, or email address. | [RFC 7643](https://www.rfc-editor.org/rfc/rfc7643) |
| **Identity lifecycle** | The processes for creating, updating, suspending, and deleting identities. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Identity proofing** | The process of establishing that an applicant is who they claim to be. | [NIST 800-63A-4](https://pages.nist.gov/800-63-4/sp800-63a.html) |
| **Identity provider (IdP)** | A system that authenticates users and may provide identity attributes to other systems. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Relying party (RP)** | A service that relies on an identity provider or verifier to make an authentication decision. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Subscriber** | An individual enrolled with a credential service provider and bound to one or more authenticators. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Credential** | Evidence, such as a password, certificate, or passkey, used to establish identity or prove control. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Authenticator** | Something a claimant possesses or controls and uses to prove identity during authentication. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Credential service provider (CSP)** | An entity that issues or manages subscriber credentials and related identity services. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Account** | A record that represents a user or service in a system and holds identity attributes and access settings. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Digital identity wallet** | A system that stores and presents digital credentials or identity information. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Identity governance** | Policies and processes that oversee identity lifecycle, access decisions, and compliance. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Identity repository** | A directory or database that stores identity records and attributes. | [RFC 7643](https://www.rfc-editor.org/rfc/rfc7643) |

## Authentication and MFA

| Term | One-line meaning | Reference |
|---|---|---|
| **Authentication** | Verifying that a claimant controls an authenticator associated with an identity. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Authorization** | Determining what an authenticated or identified subject is allowed to do. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Multi-factor authentication (MFA)** | Authentication requiring factors from at least two distinct factor categories. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Single-factor authentication** | Authentication that relies on one factor category, such as a password alone. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Knowledge factor** | An authentication factor based on something the claimant knows, such as a password or PIN. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Possession factor** | An authentication factor based on something the claimant possesses, such as a security key. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Inherence factor** | An authentication factor based on a physical characteristic, such as a fingerprint. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **One-time password (OTP)** | A short-lived code intended for one authentication attempt or a limited time window. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Time-based OTP (TOTP)** | An OTP generated from a shared secret and the current time. | [RFC 6238](https://www.rfc-editor.org/rfc/rfc6238) |
| **HMAC-based OTP (HOTP)** | An OTP generated from a shared secret and a counter value. | [RFC 4226](https://www.rfc-editor.org/rfc/rfc4226) |
| **Passkey** | A FIDO credential using public-key cryptography, typically designed for phishing-resistant sign-in. | [FIDO Alliance](https://fidoalliance.org/fido2/) |
| **WebAuthn** | A web standard for creating and using public-key credentials for strong authentication. | [W3C WebAuthn](https://www.w3.org/TR/webauthn-3/) |
| **FIDO2** | A set of standards including WebAuthn and CTAP for passwordless and multi-factor authentication. | [FIDO Alliance](https://fidoalliance.org/fido2/) |
| **Phishing-resistant authentication** | Authentication designed to prevent an attacker from successfully reusing a phished authenticator or response. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Passwordless authentication** | Authentication that does not require the user to enter a memorized password. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Biometrics** | Measurements of physical or behavioral traits used as part of an identity verification process. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Authenticator assurance level (AAL)** | A NIST category describing the strength of an authentication transaction. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Session** | A period of interaction in which a system maintains context after authentication. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Reauthentication** | Requiring a user to authenticate again during or after an existing session. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Step-up authentication** | Requesting stronger or additional authentication before a sensitive action. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Account recovery** | A process for restoring access when a user has lost access to their authenticators. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Credential stuffing** | An attack that tests stolen username-password pairs against other services. | [OWASP](https://owasp.org/www-community/attacks/Credential_stuffing) |
| **Brute-force attack** | Repeatedly trying possible secrets or credentials until one succeeds. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Risk-based authentication** | Adjusting authentication requirements based on contextual risk signals. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |

## Authorization and Access Control

| Term | One-line meaning | Reference |
|---|---|---|
| **Access control** | Mechanisms that allow or deny actions on resources according to policy. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Access control policy** | Rules that define which subjects may perform which actions on which resources. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Subject** | A user, service, process, or other actor requesting access to a resource. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Object / resource** | A file, application, API, database, or other asset that access is requested to. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Permission** | An allowed operation on a resource, such as read, write, or delete. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Entitlement** | A specific right, permission, or access package assigned to an identity. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Role** | A named collection of permissions associated with job functions or responsibilities. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Role-based access control (RBAC)** | An access model in which permissions are assigned to roles and users receive roles. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Attribute-based access control (ABAC)** | An access model that evaluates subject, resource, action, and environmental attributes. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Policy-based access control (PBAC)** | Access control in which decisions are evaluated against centrally defined policies. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Discretionary access control (DAC)** | An access model where resource owners can decide who receives access. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Mandatory access control (MAC)** | An access model where centrally enforced labels and rules govern access. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Least privilege** | Giving an identity only the permissions needed to perform its tasks. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Need to know** | Limiting information access to what is necessary for an assigned duty. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Separation of duties** | Dividing sensitive tasks among people or roles to reduce fraud and error risk. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Privileged access** | Access that can perform administrative or otherwise high-impact actions. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Privileged access management (PAM)** | Controls for securing, monitoring, and governing privileged accounts and sessions. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Just-in-time (JIT) access** | Granting access only when needed and typically for a limited duration. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Just-enough administration (JEA)** | Restricting administrative users to only the specific commands or actions required. | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/active-directory/) |
| **Access review / certification** | A periodic review to confirm that existing access remains appropriate. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Access request** | A formal request to obtain a role, permission, or resource entitlement. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Policy decision point (PDP)** | A component that evaluates a request against access-control policy. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Policy enforcement point (PEP)** | A component that enforces the decision made by an access-control policy system. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Policy information point (PIP)** | A source that provides attributes used in an access-control decision. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |
| **Policy administration point (PAP)** | A component used to create, manage, or distribute access-control policies. | [NIST 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) |

## Federation, SSO, and Protocols

| Term | One-line meaning | Reference |
|---|---|---|
| **Identity federation** | An arrangement that allows identities or authentication results to be trusted across separate domains. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Single sign-on (SSO)** | A capability that lets a user access multiple applications after one sign-in. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Federated authentication** | Authentication performed by one domain and trusted by another domain. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Security Assertion Markup Language (SAML)** | An XML-based standard for exchanging authentication and attribute assertions. | [OASIS SAML](https://www.oasis-open.org/standard/saml/) |
| **OpenID Connect (OIDC)** | An identity layer on top of OAuth 2.0 that enables clients to verify end-user identity. | [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html) |
| **OAuth 2.0** | An authorization framework that enables a client to obtain limited access to an HTTP service. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **OAuth 2.0 Security BCP** | Current best-practice guidance for securing OAuth 2.0 deployments. | [RFC 9700](https://www.rfc-editor.org/rfc/rfc9700) |
| **OpenID Provider (OP)** | An OIDC entity that authenticates end users and issues identity information to clients. | [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html) |
| **Relying party (OIDC)** | An OIDC client that relies on an OpenID Provider to authenticate an end user. | [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html) |
| **Authorization server** | A server that issues access tokens to clients after processing authorization grants. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Resource server** | A server that hosts protected resources and accepts access tokens. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Client** | An application that requests access to a protected resource on behalf of itself or a resource owner. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Access token** | A credential representing authorization to access protected resources. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Refresh token** | A credential used to obtain new access tokens without repeating the full authorization grant. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **ID token** | An OIDC token containing claims about an authentication event and end user. | [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html) |
| **Bearer token** | A token whose possession is sufficient to use it, without proof of possession of a separate key. | [RFC 6750](https://www.rfc-editor.org/rfc/rfc6750) |
| **JWT** | A compact format for representing claims transferred between parties, often signed or encrypted. | [RFC 7519](https://www.rfc-editor.org/rfc/rfc7519) |
| **JWS** | A format for protecting content with a digital signature or message authentication code. | [RFC 7515](https://www.rfc-editor.org/rfc/rfc7515) |
| **JWE** | A format for encrypting content for confidentiality. | [RFC 7516](https://www.rfc-editor.org/rfc/rfc7516) |
| **JWK** | A JSON data structure representing a cryptographic key. | [RFC 7517](https://www.rfc-editor.org/rfc/rfc7517) |
| **JWKS** | A JSON document containing a set of JSON Web Keys. | [RFC 7517](https://www.rfc-editor.org/rfc/rfc7517) |
| **PKCE** | An OAuth extension that protects authorization-code flows against code interception. | [RFC 7636](https://www.rfc-editor.org/rfc/rfc7636) |
| **Authorization code flow** | An OAuth flow in which a client exchanges a short-lived authorization code for tokens. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Client credentials grant** | An OAuth grant for a client accessing resources under its own authority. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Redirect URI** | The registered endpoint to which an authorization server sends a user-agent after authorization. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Scope** | A value used to specify the access range requested or granted to an OAuth client. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Claims** | Statements about an entity, such as a subject identifier, issuer, or authentication time. | [RFC 7519](https://www.rfc-editor.org/rfc/rfc7519) |
| **Issuer (iss)** | An identifier for the principal that issued a token or assertion. | [RFC 7519](https://www.rfc-editor.org/rfc/rfc7519) |
| **Audience (aud)** | The intended recipient or recipients of a token or assertion. | [RFC 7519](https://www.rfc-editor.org/rfc/rfc7519) |
| **Subject (sub)** | An identifier for the principal that is the subject of a token or assertion. | [RFC 7519](https://www.rfc-editor.org/rfc/rfc7519) |
| **SCIM** | A standard protocol for provisioning and managing identity data across domains. | [RFC 7644](https://www.rfc-editor.org/rfc/rfc7644) |
| **SCIM User resource** | A SCIM resource representing a person and that person's identity attributes. | [RFC 7643](https://www.rfc-editor.org/rfc/rfc7643) |
| **SCIM Group resource** | A SCIM resource used to represent a collection of users or other group members. | [RFC 7643](https://www.rfc-editor.org/rfc/rfc7643) |
| **LDAP** | A protocol for accessing and maintaining distributed directory information services. | [RFC 4511](https://www.rfc-editor.org/rfc/rfc4511) |
| **Kerberos** | A network authentication protocol that uses tickets and a trusted third party. | [RFC 4120](https://www.rfc-editor.org/rfc/rfc4120) |
| **X.509 certificate** | A digital certificate format commonly used to bind an identity to a public key. | [RFC 5280](https://www.rfc-editor.org/rfc/rfc5280) |
| **Public key infrastructure (PKI)** | Policies, roles, processes, and technology for managing public-key certificates and trust. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |

## Provisioning and Lifecycle

| Term | One-line meaning | Reference |
|---|---|---|
| **Provisioning** | Creating or configuring an account, identity, or access entitlement in a target system. | [RFC 7644](https://www.rfc-editor.org/rfc/rfc7644) |
| **Deprovisioning** | Disabling or removing accounts and entitlements when they are no longer needed. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Joiner-mover-leaver (JML)** | Lifecycle workflow for people joining, changing roles, and leaving an organization. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Account linking** | Associating two accounts or identifiers that represent the same person or entity. | [NIST 800-63-4](https://pages.nist.gov/800-63-4/sp800-63.html) |
| **Directory service** | A service that organizes and provides access to identity and resource information. | [RFC 4511](https://www.rfc-editor.org/rfc/rfc4511) |
| **Group management** | Managing membership in groups used to simplify access assignment and administration. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Birthright access** | Baseline access automatically assigned based on a person's attributes or employment status. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Dynamic group** | A group whose membership is calculated from rules or identity attributes. | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/active-directory/) |
| **Access recertification** | A recurring confirmation that users still require their current access. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Orphaned account** | An account that no longer has a valid owner or business justification. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Dormant account** | An account that has not been used for a defined period. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Service account** | A non-human account used by an application, service, or automated process. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Machine identity** | An identity assigned to a workload, device, application, or other non-human entity. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Workload identity** | An identity used by software workloads to authenticate to services or resources. | [NIST 800-207](https://csrc.nist.gov/pubs/sp/800/207/final) |
| **Secrets management** | Secure storage, access, rotation, and lifecycle management of passwords, keys, and tokens. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| **Credential rotation** | Replacing a credential or secret periodically or after a suspected compromise. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |

## Governance, Risk, and Compliance

| Term | One-line meaning | Reference |
|---|---|---|
| **Identity governance and administration (IGA)** | Capabilities for governing identity lifecycle, access requests, reviews, and compliance evidence. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Zero trust** | A security approach that does not grant implicit trust based solely on network location or ownership. | [NIST 800-207](https://csrc.nist.gov/pubs/sp/800/207/final) |
| **Continuous access evaluation** | Repeatedly reevaluating access as identity, device, session, or risk conditions change. | [NIST 800-207](https://csrc.nist.gov/pubs/sp/800/207/final) |
| **Conditional access** | Policy-based access decisions that consider signals such as user, device, location, or risk. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Segregation of duties (SoD) conflict** | A combination of permissions that could allow one person to perform incompatible tasks. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Toxic combination** | A set of entitlements that creates a high-risk SoD conflict when held together. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Access anomaly** | A pattern of access activity that deviates from expected behavior or policy. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Identity threat detection and response (ITDR)** | Security practices and tools focused on detecting and responding to identity-based threats. | [CISA](https://www.cisa.gov/) |
| **Audit trail** | A chronological record of security-relevant actions and events. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Non-repudiation** | Evidence that supports preventing a party from credibly denying an action or transaction. | [NIST 800-12](https://csrc.nist.gov/pubs/sp/800/12/r1/final) |
| **Risk assessment** | A process for identifying, estimating, and prioritizing risks to systems and information. | [NIST 800-30](https://csrc.nist.gov/pubs/sp/800/30/r1/final) |
| **Control** | A safeguard or countermeasure that manages security or privacy risk. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Policy exception** | An approved deviation from a standard access or security policy, usually with documented risk. | [NIST 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| **Data minimization** | Limiting collection and sharing of personal or sensitive data to what is necessary. | [NIST Privacy Framework](https://www.nist.gov/privacy-framework) |
| **Identity assurance level (IAL)** | A NIST category describing confidence in the identity-proofing process. | [NIST 800-63A-4](https://pages.nist.gov/800-63-4/sp800-63a.html) |
| **Federation assurance level (FAL)** | A NIST category describing security requirements for federation transactions. | [NIST 800-63C-4](https://csrc.nist.gov/pubs/sp/800/63/c/4/final) |
| **Phishing** | A deceptive attempt to obtain credentials or sensitive information by impersonating a trusted party. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Credential theft** | Unauthorized acquisition of passwords, tokens, keys, or other authentication material. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Session hijacking** | Taking over a valid authenticated session by stealing or abusing its session identifier or token. | [RFC 6750](https://www.rfc-editor.org/rfc/rfc6750) |
| **Token revocation** | Invalidating a token or making it unusable before its natural expiration. | [RFC 7009](https://www.rfc-editor.org/rfc/rfc7009) |
| **Certificate revocation** | Declaring a certificate untrusted before its scheduled expiration. | [RFC 5280](https://www.rfc-editor.org/rfc/rfc5280) |

## Cryptography and Supporting Concepts

| Term | One-line meaning | Reference |
|---|---|---|
| **Hash function** | A one-way function that maps input data to a fixed-length digest. | [NIST FIPS 180-4](https://csrc.nist.gov/pubs/fips/180-4/upd1/final) |
| **Salt** | Random or unique data added before password hashing to resist precomputed attacks. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Password hashing** | Applying a purpose-built one-way function to passwords before storing verifiers. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |
| **Digital signature** | A cryptographic value that helps verify data integrity and signer authenticity. | [RFC 7515](https://www.rfc-editor.org/rfc/rfc7515) |
| **Encryption** | Transforming information so it cannot be read without the required decryption capability. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| **Symmetric cryptography** | Cryptography that uses the same secret key, or related shared keys, for encryption and decryption. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| **Asymmetric cryptography** | Cryptography based on a public/private key pair. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| **Public key** | A cryptographic key that can be shared and used for verification or encryption, depending on the algorithm. | [RFC 7517](https://www.rfc-editor.org/rfc/rfc7517) |
| **Private key** | A secret cryptographic key used for signing or decryption and protected from disclosure. | [RFC 7517](https://www.rfc-editor.org/rfc/rfc7517) |
| **Mutual TLS (mTLS)** | TLS in which both client and server authenticate using certificates. | [RFC 8705](https://www.rfc-editor.org/rfc/rfc8705) |
| **TLS** | A protocol that provides confidentiality and integrity for data in transit and can authenticate peers. | [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446) |
| **Certificate authority (CA)** | An entity that issues and manages digital certificates under defined policies. | [RFC 5280](https://www.rfc-editor.org/rfc/rfc5280) |
| **Key rotation** | Replacing cryptographic keys according to a schedule or in response to risk. | [NIST 800-57](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| **Cryptographic nonce** | A value intended to be used once in a protocol or cryptographic operation. | [RFC 6749](https://www.rfc-editor.org/rfc/rfc6749) |
| **Replay attack** | An attack that reuses a previously captured valid message, token, or authentication response. | [NIST 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html) |

## Primary reference collections

- [NIST SP 800-63-4 Digital Identity Guidelines](https://pages.nist.gov/800-63-4/sp800-63.html) — identity proofing, authentication, and federation.
- [NIST SP 800-53 Rev. 5](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) — security and privacy controls.
- [NIST SP 800-162](https://csrc.nist.gov/pubs/sp/800/162/upd2/final) — attribute-based access control.
- [NIST SP 800-207](https://csrc.nist.gov/pubs/sp/800/207/final) — zero trust architecture.
- [RFC Editor](https://www.rfc-editor.org/) — IETF standards and best-current-practice documents.
- [OpenID Connect specifications](https://openid.net/developers/specs/) — OIDC standards.
- [W3C WebAuthn](https://www.w3.org/TR/webauthn-3/) — web authentication standard.

## Maintenance

- Prefer current NIST revisions and RFC Editor pages when updating references.
- Check whether a document has been superseded before describing it as current guidance.
- Open an issue or pull request to suggest corrections, additional terms, or better references.

## Disclaimer

This repository is an independent educational resource and is not affiliated with NIST, IETF, W3C, OASIS, FIDO Alliance, or other referenced organizations.