# Azure Key Vault

Azure Key Vault stores secrets, keys, and certificates outside application code. In AI-103, it helps keep model keys, endpoint values, and other sensitive settings out of source files.

## Role in AI-103

Use Azure Key Vault whenever an AI solution needs secure storage for connection strings, API keys, certificates, or other secrets. It is a common companion service for model, search, and monitoring setups.

## Key capabilities

- Secret storage: Keeps sensitive values out of application code.
- Key management: Stores and manages cryptographic keys for protected workflows.
- Certificate storage: Holds certificates for secure app and service access.
- Access control through Azure roles and policies: Limits who can read or manage vault content.

## Relationships to other services

| Service | Relationship |
| --- | --- |
| Azure OpenAI Service | Stores endpoint values and access credentials when needed. |
| Azure AI Search | Stores indexing or admin credentials when the scenario requires them. |
| Microsoft Foundry | Stores connection values for the broader AI app or agent workflow. |

## Security and identity

- Use Microsoft Entra ID and role-based access control.
- Prefer private access where the deployment requires it.
- Rotate secrets and remove unused credentials.
- Keep application code free of embedded secrets.

## Trade-offs and limits

| Consideration | Why it matters |
| --- | --- |
| Access model | Too much access weakens the value of the vault. |
| Secret lifecycle | Expired or stale secrets can break model and data access. |
| Operational overhead | Secure storage still needs rotation and review. |

## Official references

- [Azure Key Vault documentation](https://learn.microsoft.com/azure/key-vault/general/)
- [Basic concepts](https://learn.microsoft.com/azure/key-vault/general/basic-concepts)
- [Use Azure RBAC for access control](https://learn.microsoft.com/azure/key-vault/general/rbac-guide)