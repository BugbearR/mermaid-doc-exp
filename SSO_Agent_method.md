```mermaid
sequenceDiagram
    participant Client
    participant Server
    participant Agent
    participant IdP
    Client->>IdP: Login
    IdP->>Client: token
    Client->>Server: request & token
    Server->>Agent: token
    Agent->>IdP: token
    IdP->>Agent: user info
    Agent->>Server: user info
    Server->>Client: response
```
