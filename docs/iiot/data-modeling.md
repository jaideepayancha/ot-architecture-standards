# Data Modeling Standards

## Equipment Hierarchy

ISA-95 aligned:

Enterprise

- Site
  - Area
    - Line
      - Equipment

## Required Metadata

Each device must publish:

- Equipment ID
- Area
- Asset Class
- Engineering Units

## Tag Quality

- All data must include quality
- Bad quality must not be historized

## Naming

No free-text tag names in cloud pipelines.
