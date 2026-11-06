**Sergei Ivanov**  
**Go Developer**  
Belarus (open to hybrid/on-site in Belarus, remote, or relocation)  
ivanov.sergei.dev@gmail.com | [GitHub](https://github.com/s-588) | [LinkedIn](https://www.linkedin.com/in/ivanousiarhiej)

## Summary

Go developer who has built an AODV-style multi-interface mesh routing node (userspace UDP), a full UDP/TCP DNS server with PostgreSQL, protobuf HTTP API, JWT+RBAC and Prometheus, and a type-safe transport management system. Seeking a trainee or junior Go backend role (APIs, services or infrastructure). Available immediately.

## Skills

- **Languages**: Go, SQL  
- **Backend & APIs**: REST, protobuf, gRPC, JWT, Prometheus  
- **Databases**: PostgreSQL, sqlc, Goose  
- **Testing**: Testcontainers, testify  
- **Networking**: UDP, TCP, DNS, WebSockets  
- **Other**: Docker Compose, Templ, HTMX
- **Languages (Spoken)**: English (B2), Russian (native)

## Projects

### AODV Mesh Node  
**Go | UDP | Bubble Tea | Docker Compose** | [GitHub](https://github.com/s-588/mesh-network)

- Implemented an AODV-style on-demand mesh routing node (RREQ, RREP, RERR, HELLO) running in userspace over UDP/IP with multi-interface support.
- Built an interactive Bubble Tea TUI and CLI that communicate with a local HTTP IPC server, allowing operators to inspect neighbours/routes, send messages.
- Created a ready-to-run 11-node Docker Compose topology spanning four networks for end-to-end protocol testing without physical hardware.

### DNS Server  
**Go | PostgreSQL | chi | sqlc | protobuf | Prometheus** | [GitHub](https://github.com/s-588/dns-server)

- Implemented a DNS server that answers both UDP and TCP queries using resource records stored in PostgreSQL.
- Delivered a complete protobuf HTTP CRUD API with JWT cookie authentication and admin/user RBAC; Goose migrations.
- Added Prometheus metrics (query latency, login outcomes, record operations) and real-time JSON log streaming over WebSocket.
- Built CLI and Bubble Tea TUI so operators can manage records and watch live logs without direct database access.
- Wrote unit tests for HTTP handlers with testify, mockery and httptest and integration tests for the repository layer with Testcontainers.

### Transport Management System  
**Go | PostgreSQL | sqlc | Templ | HTMX** | [GitHub](https://github.com/s-588/tms)

- Built a transport order management system for vehicles, clients, employees and orders with end-to-end type safety provided by sqlc and Templ.
- Implemented dynamic order pricing based on PostGIS distance calculations, weight, fuel consumption and client loyalty discounts.
- Added integration tests using Testcontainers that cover CRUD operations and database logic.
- Implemented soft-delete and full audit logging via database triggers on every table; generated contracts and Excel reports from templates for completed orders.
- Added gRPC API alongside the main HTTP/Templ + HTMX web UI. Packaged the full stack with Docker Compose and Taskfile.

## Education

**Gomel State Agrarian and Economic College**  
Specialty: Software of Information Technologies  
Qualification: Technician-Programmer