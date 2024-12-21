```mermaid
---
Django ER Diagram
---
erDiagram
genres {
    INTEGER id
    TEXT name
}

movies {
    INTEGER id
    TEXT name
    INTEGER genre_id
}

movies }|--> genres : id
```
