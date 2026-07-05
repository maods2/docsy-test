---
title: Diagrams with Mermaid
linkTitle: Diagrams
weight: 30
description: Flowcharts, sequence diagrams, and more using Mermaid
---

Docsy supports [Mermaid](https://mermaid.js.org/) out of the box. Put diagram code in a fenced code block tagged `mermaid` and it renders automatically in the browser.

## Flowchart

```mermaid
flowchart LR
    A[Write Markdown] --> B[Hugo builds site]
    B --> C[GitHub Pages]
    C --> D[Readers see diagrams]
```

## Sequence diagram

```mermaid
sequenceDiagram
    participant User
    participant Hugo
    participant Browser

    User->>Hugo: Add ```mermaid``` block
    Hugo->>Browser: HTML + Mermaid JS
    Browser->>Browser: Render SVG diagram
```

## Class diagram

```mermaid
classDiagram
    class Documentation {
        +String title
        +render()
    }
    class MermaidDiagram {
        +String source
        +draw()
    }
    Documentation --> MermaidDiagram : includes
```

## State diagram

```mermaid
stateDiagram-v2
    [*] --> Draft
    Draft --> Review : submit
    Review --> Published : approve
    Review --> Draft : changes requested
    Published --> [*]
```

## Gantt chart

```mermaid
gantt
    title Sample project timeline
    dateFormat YYYY-MM-DD
    section Build
    Setup Docsy site   :done, a1, 2026-01-01, 3d
    Add content        :done, a2, after a1, 5d
    Deploy to Pages    :active, a3, after a2, 2d
```

## Pie chart

```mermaid
pie title Docs content types
    "Guides" : 45
    "API reference" : 30
    "Tutorials" : 25
```

## Tips

- Mermaid loads only on pages that contain a `mermaid` code block.
- Configure global diagram styling in `hugo.yaml` under `params.mermaid`.
- See the [Docsy diagrams guide](https://www.docsy.dev/docs/content/diagrams-and-formulae/) for PlantUML, KaTeX, and more.
