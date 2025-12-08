```mermaid
erDiagram
    Pupil {
        INTEGER id
        TEXT last_name
        TEXT first_name
        TEXT gender
        TEXT birth
        REAL height
        INTEGER squad_id 
    }

    Squad {
        INTEGER id
        TEXT name
    }


    Pupil }|--|| Squad : squad
```