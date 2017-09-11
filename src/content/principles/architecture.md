---
title: Architecture diagrams
---



{{<mermaid>}}
sequenceDiagram
    participant Client
    participant Nhite
    participant Backend
    Note left of Client: calling the push command
    loop Zip
        Client->Client: Ziping the current directory
    end
  
    Client->>Nhite: gRPC sending pb.Message
{{< /mermaid >}}

