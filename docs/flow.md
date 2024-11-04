```mermaid
---
title: Tally to PowerBI Flow
---
flowchart TD
    A["Tally Companion"] -- Install Add In --> B("Tally Sync Add In")
    B --> C{"Sync Comany"}
    C -- First --> D["Sync all Data"]
    C -- After first --> E["Sync only changed or alttered data"]
    n1["Data Providers"] --> n2["SQLite"] & n3["SQL Server"]
    E --> n4["Database"]
    D --> n4
    n4 --> n6["Power BI or Excel"] & n10["Fabric"]
    n5["Fabric Semantic Model"] --> n8["Power BI"] & n9["Excel"]
    n10 --> n5

    n1@{ shape: rounded}
    n4@{ shape: rounded}
    n10@{ shape: text}
    n5@{ shape: rect}