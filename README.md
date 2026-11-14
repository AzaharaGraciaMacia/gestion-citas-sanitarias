# Gestión de Citas Sanitarias

Aplicación web para gestionar las citas de un centro sanitario pequeño o mediano. Los pacientes solicitan citas en los horarios que ofrece el centro y el personal organiza la agenda de sus profesionales. Cada centro puede adaptar la interfaz a su identidad visual (nombre, logotipo y colores).

> Proyecto Intermodular de 2.º de DAW (curso 2026-2027) · Autora: Azahara Gracia Macia

## Problema que resuelve

Muchas clínicas pequeñas no pueden pagar un programa completo de gestión clínica y siguen gestionando las citas con hojas de cálculo o en papel. Esto provoca errores de citación (solapamientos, huecos perdidos), llamadas innecesarias y dependencia del horario de recepción. Esta aplicación cubre **solo la gestión de citas**, con un coste reducido y una imagen personalizada para cada centro.

## Usuarios

- **Paciente**: consulta la disponibilidad y solicita, modifica o cancela sus citas.
- **Atención al paciente**: confirma solicitudes y gestiona la agenda del centro.
- **Personal sanitario**: consulta y gestiona su agenda.
- **Administrador**: gestiona el personal, los profesionales, los horarios y la apariencia de la aplicación.

## Funcionalidades previstas

**Esenciales**

- Registro, inicio y cierre de sesión, con acceso diferenciado por rol.
- Gestión de profesionales, especialidades, horarios, duración de consultas y ausencias.
- Consulta de disponibilidad y solicitud, confirmación, modificación y cancelación de citas.
- Prevención de reservas simultáneas sobre el mismo horario.
- Agenda del centro filtrable por fecha, profesional y estado.
- Personalización del nombre, logotipo y tema de colores.
- Diseño adaptable a móvil, tableta y ordenador.

**Ampliaciones (si hay tiempo)**: confirmaciones y recordatorios por correo, justificantes de asistencia, estadísticas, más opciones de personalización, exportación de la agenda.

## Tecnologías previstas

PHP 8 (sin framework, estructura MVC) · MariaDB con PDO · HTML, CSS, Bootstrap 5 y JavaScript · PHPUnit · Git y GitHub.

## Estado actual

🟡 **Fase de planificación.** Se ha elaborado el plan de ejecución (Fase 3). Todavía no hay código de la aplicación.

| Hito | Descripción | Fecha prevista | Estado |
|---|---|---|---|
| H1 | Entrega de la Fase 3 (plan de ejecución) | 20/11/2026 | En curso |
| H2 | Diseño cerrado (modelo de datos, prototipos y temas) | 15/01/2027 | Pendiente |
| H3 | Autenticación y permisos operativos | 05/02/2027 | Pendiente |
| H4 | Gestión de citas completa en el servidor | 16/04/2027 | Pendiente |
| H5 | Versión mínima funcional integrada | 07/05/2027 | Pendiente |
| H6 | Versión desplegada y verificada | 28/05/2027 | Pendiente |
| H7 | Entrega final del proyecto | 04/06/2027 | Pendiente |

Próximo paso: preparar el entorno local y cerrar el diseño de la base de datos (bloques B1 y B2).

## Documentación

Toda la documentación del proyecto está en la carpeta [`docs/`](docs/):

- [Plan de ejecución y tareas](docs/plan-ejecucion.md)
- [Cronograma (Gantt)](docs/cronograma.md)
- [Procedimiento de trabajo](docs/procedimiento.md)
- [Registro de riesgos](docs/riesgos.md)
- [Registro de decisiones](docs/decisiones.md)
- [Seguimiento semanal](docs/seguimiento.md)
- [Entregas de cada fase (PDF)](docs/fases/)

## Seguridad

Este repositorio no contiene contraseñas, claves, tokens ni datos personales reales. La configuración local se guarda en `.env` (excluido por `.gitignore`). Usa `.env.example` como plantilla.
