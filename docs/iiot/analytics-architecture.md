# Analytics Architecture

## Layers

1. Ingestion
2. Stream processing
3. Storage
4. Analytics
5. Visualization

## Approved Tools

- Databricks
- Power BI
- Tableau
- Custom ML pipelines

## Separation of Concerns

No analytics workloads on:

- SCADA servers
- Historians

## Latency Classes

| Use Case | Latency |
|--------|--------|
| Operator dashboards | < 1 sec |
| Ops analytics | < 5 min |
| Business reporting | Hourly |
