# Remote Access Architecture

## Principles

- No direct vendor access to control VLANs
- All access authenticated and logged

## Approved Methods

- VPN to DMZ jump host
- Session broker solutions
- Time-bound access

## Jump Hosts

Located in Industrial DMZ:

- Dual NIC
- Screen recording
- MFA

## Prohibited

- TeamViewer on HMIs
- Cellular modems on PLCs
- Split tunnel VPNs
