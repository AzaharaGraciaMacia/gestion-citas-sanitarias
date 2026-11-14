# Plan de ejecución

Resumen del plan de la Fase 3. El documento completo (con recursos, permisos, riesgos y valoración económica) está en [fases/](fases/).

- **Periodo:** 16/11/2026 - 04/06/2027 (29 semanas).
- **Dedicación prevista:** unas 7 h por semana, 166 h planificadas y unas 20 h de reserva (Navidad y Pascua).
- **Seguimiento:** cada tarea es un issue de GitHub con su identificador; los hitos son milestones.

## Tareas

| ID | Tarea | Resultado esperado | Predecesoras | Horas | Inicio | Fin |
|---|---|---|---|---|---|---|
| **B1** | **Preparación y planificación** | | | **15** | | |
| T01 | Crear el repositorio GitHub | Repositorio accesible con la estructura inicial. | — | 2 | 16/11/2026 | 20/11/2026 |
| T02 | Elaborar el plan de ejecución | Documento F3 en PDF y copia en docs/. | — | 6 | 16/11/2026 | 20/11/2026 |
| T03 | Configurar el tablero de trabajo | Tablero con todas las tareas como issues. | T01, T02 | 2 | 23/11/2026 | 27/11/2026 |
| T04 | Preparar el entorno local | Entorno que ejecuta un «hola mundo» PHP conectado a MariaDB. | — | 2 | 23/11/2026 | 27/11/2026 |
| T05 | Crear el esqueleto del proyecto PHP | Proyecto que arranca y enruta una página de prueba. | T01, T04 | 3 | 23/11/2026 | 04/12/2026 |
| **B2** | **Diseño definitivo de la solución** | | | **11** | | |
| T06 | Cerrar reglas de negocio y permisos 🔴 | Documento docs/reglas-negocio.md aprobado. | T02 | 3 | 30/11/2026 | 04/12/2026 |
| T07 | Diseñar el modelo de datos 🔴 | Diagrama E-R y relacional en docs/. | T06 | 4 | 30/11/2026 | 11/12/2026 |
| T08 | Definir la estrategia de disponibilidad 🔴 | Decisión técnica registrada (ADR). | T07 | 2 | 07/12/2026 | 11/12/2026 |
| T09 | Definir rutas y endpoints | Tabla de rutas en docs/. | T06 | 2 | 07/12/2026 | 11/12/2026 |
| **B3** | **Diseño de la interfaz** | | | **8** | | |
| T10 | Mapa de navegación por rol | Diagrama de navegación. | T06 | 1 | 14/12/2026 | 18/12/2026 |
| T11 | Prototipos de pantallas | Prototipo navegable en Figma. | T10 | 5 | 14/12/2026 | 15/01/2027 |
| T12 | Temas visuales accesibles | Temas definidos como variables CSS. | T11 | 2 | 11/01/2027 | 15/01/2027 |
| **B4** | **Base de datos** | | | **7** | | |
| T13 | Script de creación de la BD 🔴 | database/schema.sql ejecutable sin errores. | T07, T08 | 4 | 14/12/2026 | 18/12/2026 |
| T14 | Datos ficticios de prueba | database/seed.sql con datos ficticios. | T13 | 2 | 04/01/2027 | 08/01/2027 |
| T15 | Conexión PDO y configuración 🔴 | Conexión funcionando en local. | T05, T13 | 1 | 04/01/2027 | 08/01/2027 |
| **B5** | **Autenticación y permisos** | | | **14** | | |
| T16 | Registro de pacientes 🔴 | Paciente registrado sin duplicados. | T15 | 4 | 18/01/2027 | 22/01/2027 |
| T17 | Inicio y cierre de sesión 🔴 | Login y logout operativos. | T16 | 3 | 18/01/2027 | 29/01/2027 |
| T18 | Control de acceso y protección 🔴 | Accesos no autorizados bloqueados. | T17 | 4 | 25/01/2027 | 29/01/2027 |
| T19 | Gestión de cuentas del personal | CRUD de personal operativo. | T18 | 3 | 01/02/2027 | 05/02/2027 |
| **B6** | **Backend: gestión del centro** | | | **17** | | |
| T20 | Profesionales y especialidades 🔴 | CRUD operativo con validación. | T18 | 4 | 08/02/2027 | 12/02/2027 |
| T21 | Horarios, duración y ausencias 🔴 | Horarios guardados y validados. | T20 | 6 | 08/02/2027 | 19/02/2027 |
| T22 | Cálculo de disponibilidad 🔴 | Huecos libres correctos para fecha y profesional. | T21, T08 | 7 | 15/02/2027 | 26/02/2027 |
| **B7** | **Backend: gestión de citas** | | | **23** | | |
| T23 | Solicitud de cita transaccional 🔴 | Imposible reservar dos veces el mismo hueco. | T22 | 6 | 01/03/2027 | 05/03/2027 |
| T24 | Confirmación y estados de la cita 🔴 | Cambios de estado registrados. | T23 | 3 | 08/03/2027 | 12/03/2027 |
| T25 | Mis citas: modificar y cancelar | El hueco anterior queda libre tras el cambio. | T23 | 5 | 15/03/2027 | 26/03/2027 |
| T26 | Agenda del centro 🔴 | Agenda filtrable para el personal. | T24 | 5 | 22/03/2027 | 16/04/2027 |
| T27 | Personalización visual | Cambios aplicados en todas las páginas. | T18, T12 | 4 | 12/04/2027 | 23/04/2027 |
| **B8** | **Frontend** | | | **22** | | |
| T28 | Plantilla base y navegación | Plantilla común reutilizable. | T05, T11 | 4 | 25/01/2027 | 05/02/2027 |
| T29 | Pantallas de registro y acceso | Formularios accesibles y validados. | T16, T28 | 2 | 01/02/2027 | 05/02/2027 |
| T30 | Pantalla de reserva | Reserva usable sin recargar la página. | T22, T28 | 5 | 22/02/2027 | 19/03/2027 |
| T31 | Pantallas «Mis citas» | Vistas del paciente completas. | T25 | 3 | 05/04/2027 | 09/04/2027 |
| T32 | Agenda y paneles de administración 🔴 | Vistas del personal y del administrador. | T26, T19, T21 | 5 | 12/04/2027 | 23/04/2027 |
| T33 | Revisión adaptable y de teclado | Lista de comprobación superada. | T29, T30, T31, T32 | 3 | 26/04/2027 | 30/04/2027 |
| **B9** | **Integración** | | | **6** | | |
| T34 | Integrar el flujo del paciente | Flujo completo sin errores. | T30, T31, T24 | 3 | 26/04/2027 | 30/04/2027 |
| T35 | Integrar flujos del personal y administrador 🔴 | Flujos completos sin errores. Hito: versión mínima funcional. | T32, T27, T34 | 3 | 03/05/2027 | 07/05/2027 |
| **B10** | **Pruebas** | | | **19** | | |
| T36 | Plan y registro de pruebas | docs/pruebas.md con los casos. | T06 | 2 | 11/01/2027 | 22/01/2027 |
| T37 | Pruebas automatizadas | Pruebas en verde. | T22, T23, T18 | 6 | 01/03/2027 | 23/04/2027 |
| T38 | Pruebas funcionales y de seguridad 🔴 | Registro de pruebas cumplimentado. | T35, T36 | 5 | 03/05/2027 | 14/05/2027 |
| T39 | Corrección y regresión 🔴 | Sin incidencias críticas abiertas. | T38 | 6 | 10/05/2027 | 21/05/2027 |
| **B11** | **Despliegue** | | | **7** | | |
| T40 | Preparar el alojamiento | Servidor listo con HTTPS. | T35 | 2 | 03/05/2027 | 07/05/2027 |
| T41 | Desplegar la aplicación 🔴 | Aplicación accesible en Internet. | T40, T39 | 3 | 17/05/2027 | 21/05/2027 |
| T42 | Verificar producción y copias 🔴 | Hito: versión desplegada verificada. | T41 | 2 | 24/05/2027 | 28/05/2027 |
| **B12** | **Documentación y entrega** | | | **17** | | |
| T43 | Documentación técnica continua | docs/ actualizado en cada hito. | T01 | 4 | 23/11/2026 | 28/05/2027 |
| T44 | Manual de instalación y de uso | docs/manual-*.md. | T35 | 4 | 17/05/2027 | 28/05/2027 |
| T45 | Memoria final 🔴 | Memoria en PDF. | T44 | 5 | 24/05/2027 | 04/06/2027 |
| T46 | Vídeo y defensa 🔴 | Vídeo y presentación. Hito: entrega final. | T45 | 4 | 31/05/2027 | 04/06/2027 |

🔴 = tarea del camino crítico.
