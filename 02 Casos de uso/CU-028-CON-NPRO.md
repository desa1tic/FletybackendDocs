## Caso de Uso: CU-028-CON-NPRO - Conductores no aprobados

Este caso de uso describe la funcionalidad que permite gestionar a los conductores que se encuentran en estatus de "No Aprobados". El sistema centraliza su información para que el administrador pueda auditar los motivos, revisar documentación pendiente o ejecutar acciones de reactivación.

### 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-028-CON-NPRO |
| **Caso de Uso** | Conductores No Aprobados |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Permite obtener una visión completa de los conductores que están actualmente "No Aprobados" (disponibles o activos en la aplicación). Permite revisar su rendimiento histórico (Solicitudes, Completados, Cancelados), verificar su documentación y estado de aprobación, y tomar acciones de gestión inmediata (editar, rechazar, ver documentos). |
| **Prioridad** | Alta |

---

### 🛠️ Precondiciones del Sistema
* El usuario inicia sesión de forma exitosa (**CU-001-ADM / CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes.
* Existen conductores registrados y actualmente con el estatus "Aprobados".

---

### 🔄 Flujo del Sistema

| Actor Principal (Usuario)                                    | Actor Secundario (Sistema)                                                                                                                                                                       |
| :----------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                                              | 1) Carga la información de los conductores en línea; item, nombre, email, teléfono, dirección, ciudad (city), país (country), versión de la app, fecha registro, creado desde, aliado y opciones |
| 2) Consulta la información mostrada.                         |                                                                                                                                                                                                  |
| 3) El usuario puede filtrar los datos mostrados en pantalla. |                                                                                                                                                                                                  |
| **Fin**                                                      |                                                                                                                                                                                                  |

---

### 🔀 Flujo Alternativo (Acciones de Gestión)

| Acción del Usuario | Reacción del Sistema |
| :--- | :--- |
| El usuario puede acceder a otros módulos de Conductor. | Permite la navegación según permisos. |
| El usuario puede editar los detalles. | Redirige a **CU-022-CON-PERF**. |
| Puede consultar la información de vehículo. | Redirige a **CU-023-CON-VEHI**. |
| Puede consultar el historial. | Redirige a **CU-024-CON-HIST**. |
| Puede consultar el historial de referencias. | Redirige a **CU-025-CON-HISR**. |
| Puede consultar documentación. | Redirige a **CU-026-CON-DOC**. |
| Permite el rechazo del conductor. | Muestra mensaje con resultado de la operación. |
| Permite reactivar un conductor. | Muestra mensaje con resultado de la operación. |

---

### ✅ Post-Condiciones

| Escenario | Resultado Esperado |
| :--- | :--- |
| **Gestión Informativa** | El administrador tiene una comprensión clara del estado operativo y el rendimiento de los conductores. |
| **Exportación** | Se ha generado un archivo de reporte si se usó la función Exportar. |
| **Acciones Realizadas** | Si se realizaron acciones de gestión (Editar, Rechazar), el estatus del conductor ha sido actualizado. |

---

### 🔗 Casos de Uso Relacionados
* [CU-022-CON-PERF](02%20Casos%20de%20uso/CU-022-CON-PERF.md)
* [CU-023-CON-VEHI](02%20Casos%20de%20uso/CU-023-CON-VEHI.md)
* [CU-024-CON-HIST](02%20Casos%20de%20uso/CU-024-CON-HIST.md)
* [CU-025-CON-HISR](02%20Casos%20de%20uso/CU-025-CON-HISR.md)
* [CU-026-CON-DOC](02%20Casos%20de%20uso/CU-026-CON-DOC.md)
* [CU-027-CON-APRO](02%20Casos%20de%20uso/CU-027-CON-APRO.md)
* [Conductor (CU-021)](02%20Casos%20de%20uso/CU-021-Conductor.md)