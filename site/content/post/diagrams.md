---
date: 2016-12-24T20:04:40.407Z
title: Diagrams
description: "How to use Mermaid diagrams"
tags: ["diagrams", "docs"]
---

## Flowchart

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Sequence Diagram

```mermaid
sequenceDiagram
  participant Alice
  participant Bob
  Alice->>John: Hello John, how are you?
  loop Healthcheck
    John->>John: Fight against hypochondria
  end
  Note right of John: Rational thoughts <br/>prevail!
  John-->>Alice: Great!
  John->>Bob: How about you?
  Bob-->>John: Jolly good!
```

# Gantt diagram

```mermaid
gantt
  dateFormat YYYY-MM-DD
  title Adding GANTT diagram to mermaid
  excludes weekdays 2014-01-10

  section A section
  Completed task :done, des1, 2014-01-06,2014-01-08
  Active task :active, des2, 2014-01-09, 3d
  Future task : des3, after des2, 5d
  Future task2 : des4, after des3, 5d
```

## Class diagram - experimental

```mermaid
classDiagram
  Class01 <|-- AveryLongClass : Cool
  Class03 _-- Class04
  Class05 o-- Class06
  Class07 .. Class08
  Class09 --> C2 : Where am i?
  Class09 --_ C3
  Class09 --|> Class07
  Class07 : equals()
  Class07 : Object[] elementData
  Class01 : size()
  Class01 : int chimp
  Class01 : int gorilla
  Class08 <--> C2: Cool label
```

# Entity Relationship Diagram - experimental

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

## User Journey Diagram

```mermaid
journey
  title My working day
  section Go to work
  Make tea: 5: Me
  Go upstairs: 3: Me
  Do work: 1: Me, Cat
  section Go home
  Go downstairs: 5: Me
  Sit down: 5: Me
```

And that is how what you can do.
