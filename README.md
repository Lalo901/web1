```mermaid
erDiagram
    ALUMNOS {
        string ID_Alumno PK
        string Nombre
        string Apellido
        date Fecha_Nacimiento
    }
    MATERIA {
        string ID_Materia PK
        string Nombre_Materia
        int Créditos
    }
    MATRICULA {
        string ID_Matricula PK
        date Fecha_Matricula
        string ID_Alumno FK
        string ID_Materia FK
    }
    
    ALUMNOS ||--o{ MATRICULA : "matricula"
    MATERIA ||--o{ MATRICULA : "ofrecida en"
