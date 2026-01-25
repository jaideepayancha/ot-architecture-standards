# Ignition Project Structure Standard

## Naming

Project Name Format:

plantcode_area_function

Example:
bg_packaging_dashboards

## Folder Structure

### Vision

- Templates/
- Windows/
- Shared/

### Perspective

- Views/
- Params/
- Shared/

## Script Organization

- project.util
- project.tags
- project.db
- project.alarm

No scripting in event handlers beyond function calls.

## Libraries

All business logic must be in shared scripts.
