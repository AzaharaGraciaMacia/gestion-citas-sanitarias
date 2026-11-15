# Registro de decisiones (ADR)

Formato: contexto, decisión, alternativas y consecuencias. Las decisiones no se borran: si cambian, se añade una nueva que sustituye a la anterior.

## ADR-001 · PHP sin framework con estructura MVC

- **Fecha:** 25/10/2026 (Fase 2)
- **Contexto:** el alcance es acotado y el tiempo de aprendizaje es limitado.
- **Decisión:** PHP sin framework, separando controladores, lógica de negocio, acceso a datos (PDO) y vistas.
- **Alternativas:** Laravel (descartado por la curva de aprendizaje en el tiempo disponible).
- **Consecuencias:** hay que implementar y probar la autenticación, el CSRF y la validación.

## ADR-002 · MariaDB y reservas transaccionales

- **Fecha:** 25/10/2026 (Fase 2). Se concretará en T08.
- **Contexto:** dos pacientes no pueden reservar el mismo horario de un profesional.
- **Decisión:** la confirmación de una reserva será una transacción. El mecanismo de bloqueo y las restricciones se decidirán en T08.
- **Alternativas:** comprobar y luego insertar sin protección (descartado: no evita las condiciones de carrera).

## ADR-003 · Flujo de trabajo con GitHub Flow simplificado

- **Fecha:** 15/11/2026 (Fase 3)
- **Decisión:** rama main estable, una rama por tarea y pull requests enlazados a issues.
- **Consecuencias:** historial ordenado y trazabilidad entre tareas, código y documentación.
