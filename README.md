# 10_02_ASSI_Entity-Relationship
![Diagrama Borja Moll drawio (3)](https://github.com/Jooseruu/10_02_ASSI_Entity-Relationship/assets/120745808/d844a43c-d394-44d5-9d6c-a5f55c2748ff)




## Diagrama del Colegio Borja Moll
Este repositorio contiene el diagrama del Colegio Borja Moll. El diagrama incluye:

- Entidades
- Atributos, Clave Primaria
- Relaciones, relaciones con atributos.
- Roles en relaciones recursivas.
- Relaciones ternarias
- Atributos complejos. Atributos compuestos. Atributos multivalorados. Atributos derivados.
- Todas las cardinalidades posibles: uno a uno, uno a muchos, muchos a muchos.
- Participación total y parcial.

### Entidades
Tenemos varias entidades representadas en tablas como són Curso, Estudiante, telefonos(atributos multievaluados), Aula, Asignatura, Profesor, Calificación(entidad debil)

### Relaciones
1. **Estudiante - Curso**: La relación entre Estudiante y Curso es de tipo muchos a muchos, lo que significa que un Estudiante puede estar matriculado en uno o varios Cursos, y un Curso puede tener varios Estudiantes matriculados. La participación de ambas entidades en esta relación es total, ya que todos los estudiantes deben estar matriculados en un curso y todos los cursos deben tener al menos un estudiante.

2. **Curso - Asignatura**: La relación entre Curso y Asignatura es de tipo muchos a muchos, lo que significa que un Curso puede tener varias Asignaturas, y una Asignatura puede ser impartida en varios Cursos. La participación de ambas entidades en esta relación es total , ya todos los cursos deben tener al menos una asignatura y todas las asignaturas deben ser impartidas en al menos un curso.

3. **Profesor - Asignatura**: La relación entre Profesor y Asignatura es de tipo muchos a muchos, lo que significa que un Profesor puede impartir una o varias Asignaturas, y una Asignatura puede ser impartida por uno o varios Profesores. La participación de ambas entidades en esta relación es total , ya que todos los profesores deben impartir al menos una asignatura y todas las asignaturas deben ser impartidas por al menos un profesor.

4. **Asignatura - Aula**: La relación entre Asignatura y Aula es de tipo muchos a muchos, lo que significa que una Asignatura puede ser impartida en una o varias Aulas, y una Aula puede ser utilizada para impartir una o varias Asignaturas. La participación de ambas entidades en esta relación es total , ya que todas las asignaturas deben ser impartidas en al menos una aula y todas las aulas deben ser utilizadas para impartir al menos una asignatura.

5. **Profesor - Curso**: La relación entre Profesor y Curso es de tipo uno a muchos, lo que significa que un Profesor podría ser el tutor de uno o varios Cursos, pero un Curso solo podría tener un tutor (Profesor) asignado. La participación de la entidad Profesor en esta relación es parcial, ya que no todos los profesores deben ser tutores de un curso. La participación de la entidad Curso en esta relación es total ya que todos los cursos deben tener un tutor asignado.

6. **Curso - Calificación**: La entidad débil Calificación representa la nota obtenida en un Curso. Una Calificación no puede existir sin un curso asociado. Por lo tanto, la participación sería total

### Roles en relaciones recursiva
Este lo podemos ver en la tabla `Profesores` donde un Profesor puede ser mentor de otro convirtiendose así en mentor y mentorizado para asociar un mentor a un mentorizado el mentorizado debe tener el atributo `profesor_id` de su mentor en el atributo `mentor_id` de esa manera los relacionamos, la cardinalidad de la relación es de 1 a 1 ya que un profesor solo puede ser mentor de un mentorizado y un mentorizado solo puede tener un mentor, en cuanto a la participación es parcial ya que no todos los profesores deben ser mentores.

### Relaciones ternarias 
Tenemos la relación `Profesor-Aula-Asignatura` dividida en 2 y explicada en el apartado `Relaciones` (3-4)

### Atributos complejos
Tenemos 2:
El **atributo multivalorado** es aquel que contiene múltiples valores por cada instancia de un tipo de entidad. Por ejemplo, la entidad Estudiante con el atributo `telefonos`, cada empleado puede tener cero, uno o varios números de teléfono.

El **atributo derivado** es aquel cuyo valor puede derivarse de los valores de otros atributos o entidades relacionados en nuestro caso podemos obtener la edad de una persona con el atributo `fecha_nacimiento` .








