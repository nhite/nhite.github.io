---
title: Architecture diagrams
---



{{<mermaid>}}
sequenceDiagram
    participant Client
    participant Nhite
    participant Backend
    participant Terraform
    Client->>Nhite: push
    Nhite->>Backend: push
    Nhite->>Client: ID
    Client->>Nhite: plan ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>Terraform: commands/plan.go
    Nhite->>Client: result
    Client->>Nhite: apply ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>Terraform: commands/apply.go
    Nhite->>Client: result
{{< /mermaid >}}

