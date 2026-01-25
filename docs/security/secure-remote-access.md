# Secure Remote Access

## Principles

- No always-on vendor access
- Time-bound sessions only

## Approved Architecture

Vendor → VPN → DMZ Jump Host → OT

## Controls

- MFA required
- Session recording
- Approval workflow

## Prohibited

- Direct VPN to control VLAN
- Cellular modems on PLCs
- Cloud remote desktop tools
