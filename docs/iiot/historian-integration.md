# Historian Integration Standards

Standardizing how process data is archived and retrieved ensures data integrity and supports enterprise-wide analytics.

## Approved Historian Platforms

1. **Site Level**: Ignition Tag Historian (SQL-based) for short-term trending and local recovery.
2. **Enterprise Level**: Aveva PI System (Asset Framework) for long-term archiving and complex calculations.
3. **Cloud Level**: Azure Data Lake / AWS S3 for Big Data and AI/ML applications.

## Connectivity Standards

### SCADA to Site Historian
- **Protocol**: Native Ignition SQL Driver.
- **Storage**: Minimum 1-year local retention on high-performance storage.
- **Redundancy**: Use Store-and-Forward to prevent data loss during database outages.

### Site to Enterprise Historian (PI)
- **Protocol**: PI Connector for OPC UA or PI Interface for RDBMS.
- **Data Flow**: Unidirectional from Level 3 to Level 4 via IDMZ.
- **Asset Framework (AF)**: All data must be mapped to a standardized AF template following the ISA-95 equipment hierarchy.

### OT to Cloud Ingestion
- **Protocol**: MQTT Sparkplug B.
- **Standard**: Data is streamed in real-time to the cloud ingestion layer. Batch exports (CSV/Parquet) are permitted only for legacy systems.

## Data Governance

- **Compression**: Use "Exception and Compression" settings to minimize storage without losing process resolution.
- **Timestamps**: All data must use **UTC timestamps** at the source.
- **Deadbands**: Standard deadbands must be applied to prevent "noise" storage (e.g., 0.1% of span for analog values).
