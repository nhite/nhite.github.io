
---
title: Architecture diagrams
---



{{<mermaid>}}
sequenceDiagram
    participant Client
    participant Nhite
    participant Backend
    participant TerraformLib
    Client->>Nhite: push
    Nhite->>Backend: push
    Nhite->>Client: ID
    Client->>Nhite: plan ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>TerraformLib: commands/plan.go
    Nhite->>Client: result
    Client->>Nhite: apply ID
    Nhite->>Backend: Get ID
    Nhite->>Nhite: cd ID
    Nhite-->>TerraformLib: commands/apply.go
    Nhite->>Client: result
{{< /mermaid >}}
