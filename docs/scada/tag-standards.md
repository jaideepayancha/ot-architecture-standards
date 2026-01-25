# Tag Modeling Standards

## UDT First Strategy

- No direct PLC tags in screens
- All equipment modeled as UDTs

## UDT Structure

Example: Pump

- Cmd.Start
- Cmd.Stop
- Status.Running
- Status.Fault
- Alarms.*

## Instance Naming

Format:

Area_Equipment_Function

Example:
PKG_P101_FeedPump

## Data Types

| Type | Use |
|--------|--------|
| Float | Process values |
| Int | Counts |
| Bool | States |

No Strings from PLC unless required.
