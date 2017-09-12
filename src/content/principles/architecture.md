---
title: Architecture diagrams
---



{{<mermaid>}}
sequenceDiagram
    participant Client
    participant Nhite
    participant Backend
    participant Terraform-Lib
    Client->>Nhite: push
    Nhite->>Backend: push
    Nhite->>Client: ID
    Client->>Nhite: plan ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>Terraform-Lib: commands/plan.go
    Nhite->>Client: result
    Client->>Nhite: apply ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>Terraform-Lib: commands/apply.go
    Nhite->>Client: result
{{< /mermaid >}}

