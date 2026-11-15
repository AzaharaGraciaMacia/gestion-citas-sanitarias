# Cronograma

Diagrama de Gantt de la planificación inicial. GitHub lo muestra directamente. Para actualizarlo, modifica las fechas y vuelve a hacer commit. Las tareas marcadas como `crit` forman el camino crítico.

Las fechas siguen el calendario de 2.º curso 2026-2027. La semana del 28/12/2026 (Navidad) y la del 29/03/2027 (Pascua) no tienen tareas asignadas: son la reserva de contingencia. Las semanas de preparación y exámenes de evaluación (23/11-04/12 y 01/02-12/02) y la Formación en Empresa (01/03-09/05/2027) tienen la carga reducida.

```mermaid
gantt
    title Gestión de Citas Sanitarias - Plan de ejecución
    dateFormat YYYY-MM-DD
    axisFormat %d/%m
    section B1 Preparación y planificación
    T01 Crear el repositorio GitHub :T01, 2026-11-16, 2026-11-21
    T02 Elaborar el plan de ejecución :T02, 2026-11-16, 2026-11-21
    T03 Configurar el tablero de trabajo :T03, 2026-11-23, 2026-11-28
    T04 Preparar el entorno local :T04, 2026-11-23, 2026-11-28
    T05 Crear el esqueleto del proyecto PHP :T05, 2026-11-30, 2026-12-05
    section B2 Diseño definitivo de la solución
    T06 Cerrar reglas de negocio y permisos :crit, T06, 2026-12-07, 2026-12-12
    T07 Diseñar el modelo de datos :crit, T07, 2026-12-07, 2026-12-19
    T08 Definir la estrategia de disponibilidad :crit, T08, 2026-12-14, 2026-12-19
    T09 Definir rutas y endpoints :T09, 2026-12-14, 2026-12-19
    section B3 Diseño de la interfaz
    T10 Mapa de navegación por rol :T10, 2026-12-14, 2026-12-19
    T11 Prototipos de pantallas :T11, 2027-01-04, 2027-01-23
    T12 Temas visuales accesibles :T12, 2027-01-25, 2027-01-30
    section B4 Base de datos
    T13 Script de creación de la BD :crit, T13, 2026-12-21, 2026-12-26
    T14 Datos ficticios de prueba :T14, 2027-01-04, 2027-01-09
    T15 Conexión PDO y configuración :crit, T15, 2027-01-04, 2027-01-09
    section B5 Autenticación y permisos
    T16 Registro de pacientes :crit, T16, 2027-01-11, 2027-01-16
    T17 Inicio y cierre de sesión :crit, T17, 2027-01-18, 2027-01-23
    T18 Control de acceso y protección :crit, T18, 2027-01-25, 2027-01-30
    T19 Gestión de cuentas del personal :T19, 2027-02-01, 2027-02-06
    section B6 Backend: gestión del centro
    T20 Profesionales y especialidades :crit, T20, 2027-02-08, 2027-02-20
    T21 Horarios, duración y ausencias :crit, T21, 2027-02-15, 2027-02-27
    T22 Cálculo de disponibilidad :crit, T22, 2027-02-22, 2027-03-06
    section B7 Backend: gestión de citas
    T23 Solicitud de cita transaccional :crit, T23, 2027-03-08, 2027-03-20
    T24 Confirmación y estados de la cita :crit, T24, 2027-03-22, 2027-03-27
    T25 Mis citas modificar y cancelar :T25, 2027-04-05, 2027-04-17
    T26 Agenda del centro :crit, T26, 2027-04-12, 2027-04-24
    T27 Personalización visual :T27, 2027-04-19, 2027-05-01
    section B8 Frontend
    T28 Plantilla base y navegación :T28, 2027-01-18, 2027-01-30
    T29 Pantallas de registro y acceso :T29, 2027-02-01, 2027-02-06
    T30 Pantalla de reserva :T30, 2027-03-01, 2027-03-27
    T31 Pantallas Mis citas :T31, 2027-04-26, 2027-05-01
    T32 Agenda y paneles de administración :crit, T32, 2027-05-03, 2027-05-08
    T33 Revisión adaptable y de teclado :T33, 2027-05-03, 2027-05-15
    section B9 Integración
    T34 Integrar el flujo del paciente :T34, 2027-05-03, 2027-05-08
    T35 Integrar flujos del personal y administrador :crit, T35, 2027-05-10, 2027-05-15
    section B10 Pruebas
    T36 Plan y registro de pruebas :T36, 2027-01-11, 2027-01-16
    T37 Pruebas automatizadas :T37, 2027-03-15, 2027-05-01
    T38 Pruebas funcionales y de seguridad :crit, T38, 2027-05-10, 2027-05-22
    T39 Corrección y regresión :crit, T39, 2027-05-10, 2027-05-22
    section B11 Despliegue
    T40 Preparar el alojamiento :T40, 2027-05-10, 2027-05-15
    T41 Desplegar la aplicación :crit, T41, 2027-05-17, 2027-05-22
    T42 Verificar producción y copias :crit, T42, 2027-05-24, 2027-05-29
    section B12 Documentación y entrega
    T43 Documentación técnica continua :T43, 2026-11-23, 2027-05-29
    T44 Manual de instalación y de uso :T44, 2027-05-10, 2027-05-22
    T45 Memoria final :crit, T45, 2027-05-17, 2027-05-29
    T46 Vídeo y defensa :crit, T46, 2027-05-24, 2027-05-29
    section Hitos
    H1 Entrega de la Fase 1 :milestone, H1, 2026-10-18, 0d
    H2 Entrega de la Fase 2 :milestone, H2, 2026-11-01, 0d
    H3 Entrega de la Fase 3 :milestone, H3, 2026-11-15, 0d
    H4 Diseño cerrado :milestone, H4, 2027-01-29, 0d
    H5 Autenticación y permisos operativos :milestone, H5, 2027-02-05, 0d
    H6 Gestión de citas completa en el servidor :milestone, H6, 2027-04-30, 0d
    H7 Versión mínima funcional integrada :milestone, H7, 2027-05-14, 0d
    H8 Versión desplegada y verificada :milestone, H8, 2027-05-25, 0d
    H9 Entrega final del proyecto :milestone, H9, 2027-05-28, 0d
```

## Hitos

| Hito | Descripción                                                 | Fecha prevista |
| ---- | ----------------------------------------------------------- | -------------- |
| H1   | Entrega de la Fase 1 (Análisis de la necesidad y propuesta) | 18/10/2026     |
| H2   | Entrega de la Fase 2 (Diseño y viabilidad)                  | 01/11/2026     |
| H3   | Entrega de la Fase 3 (plan de ejecución)                    | 15/11/2026     |
| H4   | Diseño cerrado (modelo de datos, prototipos y temas)        | 29/01/2027     |
| H5   | Autenticación y permisos operativos                         | 05/02/2027     |
| H6   | Gestión de citas completa en el servidor                    | 30/04/2027     |
| H7   | Versión mínima funcional integrada                          | 14/05/2027     |
| H8   | Versión desplegada y verificada                             | 25/05/2027     |
| H9   | Entrega final del proyecto                                  | 28/05/2027     |

## Historial de cambios del cronograma

| Fecha      | Cambio                | Motivo |
| ---------- | --------------------- | ------ |
| 15/11/2026 | Planificación inicial | Fase 3 |
