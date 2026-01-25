# Database and Historian Standards

## Historian

- All critical tags must be historized
- Use deadband where applicable
- Enable store-and-forward

## Databases

- Separate historian and transactional DBs
- No direct PLC writes to DB

## Queries

- Named queries only
- No inline SQL in bindings

## Retention

| Data | Retention |
|--------|---------|
| Raw | 90 days |
| Aggregates | 3 years |
