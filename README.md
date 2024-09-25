

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
