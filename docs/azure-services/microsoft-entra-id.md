# Microsoft Entra ID

Microsoft Entra ID is the identity service for authentication and authorization in Azure apps. In AI-103, it is the default identity choice for securing users, services, and managed app access.

## Role in AI-103

Use Microsoft Entra ID when the scenario asks how users sign in, how services authenticate, or how one Azure resource accesses another without hard-coded secrets. It is a core part of secure AI app design.

## Key capabilities

- User and application authentication: Verifies people and apps before they access resources.
- Role-based access control: Gives each user or app only the permissions it needs.
- Managed identity support for Azure resources: Lets Azure resources sign in without secrets.
- App registration and consent flows: Defines apps in the directory and grants the access they need.

## Relationships to other services

| Service | Relationship |
| --- | --- |
| Azure OpenAI Service | Helps secure client and service access where supported. |
| Azure AI Search | Protects search resources and access to indexed content. |
| Azure Key Vault | Works with managed identities and roles to reduce secret use. |
| Microsoft Foundry | Secures the broader AI app or agent environment. |

## Security and identity

- Prefer Entra ID over long-lived shared secrets when possible.
- Use managed identities for Azure-hosted workloads.
- Assign the minimum roles needed for the task.
- Review consent and tenant boundaries in cross-tenant scenarios.

## Trade-offs and limits

| Consideration | Why it matters |
| --- | --- |
| Tenant scope | Identity decisions change across tenants and subscriptions. |
| Role design | Too many permissions make auditing harder. |
| Service support | Some endpoints still support keys, so know which authentication method fits the scenario. |

## Official references

- [Microsoft Entra ID documentation](https://learn.microsoft.com/entra/)
- [What is Microsoft Entra ID?](https://learn.microsoft.com/entra/fundamentals/what-is-microsoft-entra-id)
- [Managed identities for Azure resources](https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/overview)