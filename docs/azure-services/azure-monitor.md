# Azure Monitor

Azure Monitor collects and analyzes telemetry from Azure resources and applications. In AI-103, it helps you measure reliability, performance, and usage across the AI solution.

## Role in AI-103

Use Azure Monitor when the scenario asks how to observe an AI solution in production, detect failures, or review operational trends. It is the broader monitoring plane that contains logs, metrics, alerts, and Application Insights.

## Key capabilities

- Metrics and logs: Collects the data you need to inspect app and resource health.
- Alerts and action groups: Notifies people or automation when a condition changes.
- Workbooks and dashboards: Presents telemetry in visual reports and charts.
- Diagnostic settings for Azure resources: Sends platform logs and metrics to monitoring targets.

## Relationships to other services

| Service | Relationship |
| --- | --- |
| Application Insights | Provides application-focused observability inside Azure Monitor. |
| Microsoft Foundry | Tracks AI app and agent health signals. |
| Azure OpenAI Service | Lets you observe usage and operational behavior around the app that calls the model. |

## Security and identity

- Use Microsoft Entra ID for access control.
- Restrict who can read logs and modify alerts.
- Keep monitoring data aligned with the data classification of the workload.

## Trade-offs and limits

| Consideration | Why it matters |
| --- | --- |
| Data volume | More telemetry improves insight but can increase cost. |
| Signal choice | Too many alerts create noise; too few hide failures. |
| Scope | Azure Monitor covers more than one app, so the data model can be broad. |

## Official references

- [Azure Monitor documentation](https://learn.microsoft.com/azure/azure-monitor/)
- [What is Azure Monitor?](https://learn.microsoft.com/azure/azure-monitor/fundamentals/overview)
- [Azure Monitor alerts](https://learn.microsoft.com/azure/azure-monitor/alerts/alerts-overview)