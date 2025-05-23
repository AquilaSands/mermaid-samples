```mermaid
flowchart TD
  A[Employee Browser]

  subgraph Azure_Network
    AGW[App Gateway v2 - Public IP with WAF]
    VMPool[Web VMs in Private Subnet]
  end

  A -->|HTTPS| AGW
  AGW -->|HTTPS| VMPool
```
