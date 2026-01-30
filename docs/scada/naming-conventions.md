# Naming Conventions

Consistent naming across all plants and systems is critical for searchability, portability, and enterprise-wide reporting.

## Equipment Hierarchy (ISA-95)

Follow this structure for all tag and device naming:
`[Enterprise].[Site].[Area].[Line].[Cell].[Device]`

**Example**: `Tyson.PlantA.Processing.Line1.Filler.Motor01`

## Tag Naming Standards

1. **No Spaces**: Use CamelCase or Underscores.
2. **Standard Suffixes**: Use ISA-S5.1 standard abbreviations:
    - `_PV`: Process Value
    - `_SP`: Setpoint
    - `_ST`: Status
    - `_ALM`: Alarm
3. **Case Sensitivity**: Consistent use of UpperCase for acronyms (e.g., `PLC_Run_ST`).

## PLC / Device Naming

Devices must be named based on their primary function and location:
`[Site]-[Area]-[Function]-[ID]`

**Example**: `PTA-PROB1-PLC-01` (Plant A, Processing Building 1, PLC #1)

## Ignition Project Naming

- **Perspective Pages**: `/lines/filling/overview`
- **User Groups**: `[Site]_Operators`, `[Site]_Engineers`
- **Naming Style**: kebab-case for URLs and folders.
