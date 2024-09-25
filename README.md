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
        int Creditos
    }
    MATRICULA {
        string ID_Matricula PK
        date Fecha_Matricula
        string ID_Alumno FK
        string ID_Materia FK
    }
    
    ALUMNOS ||--o{ MATRICULA : "matricula"
    MATERIA ||--o{ MATRICULA : "ofrecida en"


# Modelo Entidad-Relación (MER)

## Entidades

### Alumnos
- **ID_Alumno** (PK)
- Nombre
- Apellido
- Fecha_Nacimiento

### Materia
- **ID_Materia** (PK)
- Nombre_Materia
- Creditos

### Matricula
- **ID_Matricula** (PK)
- Fecha_Matricula
- **ID_Alumno** (FK)
- **ID_Materia** (FK)

## Relaciones
- Un **Alumno** puede estar matriculado en varias **Materias** (1:N).
- Una **Materia** puede tener varios **Alumnos** matriculados (1:N).
