# Procedimiento de trabajo

## Tareas

- Cada tarea del plan es un **issue** con su identificador en el título (`T23 Solicitud de cita transaccional`), su etiqueta de bloque y su milestone (H1-H9).
- Tablero de GitHub Projects con las columnas **Pendiente → En curso → En revisión → Hecho**. Como máximo 2 tareas en curso a la vez.

## Ciclo semanal

1. **Inicio de semana:** elegir las tareas según el cronograma, priorizando el camino crítico.
2. **Durante la semana:** trabajar en una rama por tarea; commit y push en cada sesión.
3. **Fin de semana:** anotar en [seguimiento.md](seguimiento.md) las horas reales, los avances, los problemas y los siguientes pasos.
4. **En cada hito:** revisar el cronograma, los riesgos y el README; crear la etiqueta de versión.

## Ramas

- `main`: siempre funcional.
- `feature/Txx-descripcion`, `fix/Txx-descripcion`, `docs/Txx-descripcion`.
- Fusión mediante pull request enlazado al issue (`Closes #xx`), tras revisar el diff y ejecutar las pruebas.
- Etiquetas: `v0.1` (H5), `v0.5` (H7), `v1.0` (H9).

## Commits

Formato [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/) con el identificador de la tarea:

```
feat(T23): bloquear hueco al confirmar la reserva
fix(T25): liberar horario al cancelar
test(T37): casos de solapamiento parcial
docs(T43): actualizar README
```

## Incidencias

Issue con la etiqueta `bug` y la plantilla «Incidencia»: pasos, resultado esperado, resultado obtenido, requisito afectado y gravedad (crítica, alta o menor). Las incidencias críticas tienen prioridad sobre cualquier tarea nueva.

## Criterio de terminado

- [ ] Se obtiene el resultado esperado y se ha comprobado manualmente.
- [ ] Las pruebas automatizadas relacionadas pasan (si afecta a reglas críticas).
- [ ] Los permisos y las validaciones se comprueban en el servidor.
- [ ] El código está fusionado en main, sin credenciales ni código de depuración.
- [ ] La documentación afectada está actualizada.

## Copias de seguridad

- Código y docs: GitHub (push en cada sesión).
- BD local: `database/schema.sql` y `seed.sql` versionados, más un `mysqldump` semanal fuera del repositorio.
- Documentos de trabajo: OneDrive educativo y copia mensual en un disco externo.
- Producción: copias del hosting y una copia manual antes de cada despliegue.
