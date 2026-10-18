# Health BlackBerry Mock

Static mock endpoints for BlackBerry application development and connectivity testing.

## Overview

`health-bb-mock` provides static HTTP response payloads hosted on GitHub Pages. It is intended for testing HTTP connectivity, response parsing, and basic health-check workflows from Java applications running on legacy BlackBerry devices.

This repository is part of the **PrimoCLI** development project and serves as an initial mock endpoint for a future self-hosted Health Server.

## Endpoints

| Endpoint | Description |
|---|---|
| `/health.txt` | General health-check response |
| `/server.txt` | Mock server status |
| `/services.txt` | Mock infrastructure services status |

## Example Responses

### Health Check

```text
STATUS=OK
SERVICE=PRIMO-HEALTH-MOCK
VERSION=1.0
```

### Server Status

```text
SERVER=DITTO
STATUS=ONLINE
MODE=MOCK
```

### Services Status

```text
PROXMOX=ONLINE
STORAGE=ONLINE
VPN=OFFLINE
```

## Technology

- GitHub Pages
- Static text files
- Java ME / BlackBerry Java applications
- HTTP response parsing

## Limitations

- Responses are static and do not reflect actual infrastructure status.
- GitHub Pages serves content over HTTPS; plain HTTP is not supported as an independently configurable endpoint.
- TLS compatibility depends on the BlackBerry OS version and Java networking implementation.
- No backend processing, authentication, or dynamic health monitoring is provided.

## Security

This repository is public. All endpoint responses must contain non-sensitive test data only.

Do not store credentials, access tokens, internal server details, or other confidential information.

## Future Development

- Validate connectivity from physical BlackBerry devices.
- Test HTTP response parsing in PrimoCLI.
- Record compatibility across different BlackBerry OS versions.
- Replace static responses with a self-hosted Health Server when infrastructure connectivity is available.

## Disclaimer

This repository is intended exclusively for development and testing. Reported statuses are simulated and must not be used for operational monitoring.
