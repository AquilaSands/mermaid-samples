flowchart TD
  subgraph Internet
    A[Employee Browser]
  end

  subgraph Azure_Network
    direction TB
    AGW[App Gateway v2 (Public IP)  
        WAF Enabled]
    Subnet_Private[Private Subnet]
    VMPool[Web VMs]
  end

  A -- HTTPS --> AGW
  AGW -- HTTPS --> VMPool
