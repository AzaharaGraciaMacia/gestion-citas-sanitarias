# Registro de riesgos

Se revisa en cada hito. Estados posibles: **Abierto** (vigilado), **Controlado** (ya no es probable), **Ocurrido** (se ha aplicado la actuación; anotar fecha y resultado).

## Riesgos del desarrollo

| ID | Riesgo | Prob. | Impacto | Medida preventiva | Actuación si aparece | Estado |
|---|---|---|---|---|---|---|
| R01 | Retraso por coincidir con entregas y exámenes de otros módulos | Alta | Medio | Carga semanal de 5-8 h; semanas de reserva en Navidad y Pascua; seguimiento semanal de horas | Usar la reserva; reducir alcance no crítico; aplazar ampliaciones | Abierto |
| R02 | Dificultad en el cálculo de disponibilidad o en el control de concurrencia | Media | Alto | Diseñar la estrategia antes de programar (T08); pruebas PHPUnit desde el principio (T37) | Simplificar a franjas fijas con restricción UNIQUE (profesional, inicio); consultar al profesorado | Abierto |
| R03 | Estimaciones optimistas en tareas nuevas (sesiones, CSRF, subida de archivos) | Media | Medio | Tareas pequeñas; consultar primero la documentación oficial; registrar horas reales | Reajustar el Gantt en el siguiente hito y usar la reserva | Abierto |
| R04 | Problemas de integración frontend-backend | Media | Medio | Definir rutas y formato JSON en T09; integración progresiva por flujos | Probar los endpoints por separado con DevTools; corregir el contrato y documentarlo | Abierto |
| R05 | Pérdida de código o documentos | Baja | Alto | Push en cada sesión; OneDrive y disco externo (apartado 6.8) | Restaurar desde GitHub o desde la copia más reciente | Abierto |
| R06 | Corrupción o pérdida de la base de datos local | Media | Medio | Scripts schema/seed versionados; mysqldump semanal | Recrear la base de datos con los scripts en minutos | Abierto |
| R07 | Problemas de despliegue (versión de PHP, permisos, HTTPS) | Media | Alto | Comprobar requisitos antes de contratar; preparar el hosting antes de las pruebas (T40); documentar versiones | Ajustar configuración; alojamiento alternativo; demostración en local como respaldo | Abierto |
| R08 | Caída de un servicio externo (GitHub, hosting) | Baja | Medio | Copia local completa; funcionalidad esencial sin servicios externos | Trabajar en local y sincronizar después; demo local | Abierto |
| R09 | Publicar credenciales en el repositorio | Media | Alto | .env en .gitignore; revisar el diff antes de cada commit | Cambiar inmediatamente las credenciales y limpiar el historial | Abierto |
| R10 | Crecimiento del alcance durante el desarrollo | Media | Medio | Ampliaciones solo después del hito H5 | Registrar la idea como issue «ampliación» y posponerla | Abierto |
| R11 | Enfermedad o indisponibilidad personal | Baja | Alto | Margen de contingencia en el calendario | Replanificar y comunicarlo al profesorado | Abierto |

## Prevención de riesgos laborales

| ID | Riesgo | Prob. | Impacto | Medida preventiva | Actuación si aparece | Estado |
|---|---|---|---|---|---|---|
| R12 | Molestias musculoesqueléticas por postura prolongada | Media | Medio | Silla regulable; pantalla a la altura de los ojos y a 50-70 cm; pies apoyados; teclado y ratón externos con el portátil | Corregir el puesto; estiramientos; consulta médica si persisten | Abierto |
| R13 | Fatiga visual | Alta | Bajo | Pausa de 5-10 min cada hora; regla 20-20-20; iluminación difusa sin reflejos; brillo adecuado | Aumentar las pausas; revisión oftalmológica si persiste | Abierto |
| R14 | Fatiga mental y estrés por plazos | Media | Medio | Planificación realista; sesiones de 2 h como máximo; no acumular trabajo antes de las entregas | Replanificar y priorizar; descansar antes de seguir | Abierto |
| R15 | Riesgo eléctrico o sobrecarga de enchufes | Baja | Alto | Regleta con interruptor y protección contra sobretensiones; cables ordenados | Desconectar el equipo y revisar la instalación | Abierto |

## Revisiones

| Fecha | Hito | Cambios |
|---|---|---|
| 16/11/2026 | H1 | Registro inicial |
