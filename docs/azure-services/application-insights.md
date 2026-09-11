# Application Insights

Application Insights is the application performance monitoring part of Azure Monitor. In AI-103, it helps you understand how an AI app behaves in production by showing traces, failures, dependencies, and usage patterns.

## Role in AI-103

Use Application Insights when the scenario asks for app-level telemetry, request tracing, dependency tracking, or runtime diagnosis. It is especially useful for web apps, functions, and AI agents that need deeper observability.

## Key capabilities

- Request and dependency tracing: Shows how a request moves through the app and which downstream calls it makes.
- Failure and performance analysis: Highlights errors, slow paths, and latency spikes.
- Live metrics and availability checks: Gives near real-time health signals and simple uptime checks.
- OpenTelemetry-based instrumentation: Lets you send standard telemetry from your app into the service.

## Relationships to other services

| Service | Relationship |
| --- | --- |
| Azure Monitor | Hosts the broader observability platform. |
| Microsoft Foundry | Helps inspect agent and app behavior. |
| Azure OpenAI Service | Tracks the app behavior around model calls. |

## Security and identity

- Use Microsoft Entra ID for access.
- Limit who can read telemetry that may contain user data.
- Review whether prompt text or responses should be captured.

## Trade-offs and limits

| Consideration | Why it matters |
| --- | --- |
| Sampling | Sampling reduces volume, but it can hide rare issues. |
| Instrumentation choice | OpenTelemetry and automatic instrumentation suit different scenarios. |
| Data sensitivity | Telemetry can expose prompts, responses, or identifiers if you do not filter it. |

## Official references

- [Application Insights observability overview](https://learn.microsoft.com/azure/azure-monitor/app/app-insights-overview)
- [Create a resource](https://learn.microsoft.com/azure/azure-monitor/app/create-workspace-resource)
- [Enable OpenTelemetry](https://learn.microsoft.com/azure/azure-monitor/app/opentelemetry-enable)