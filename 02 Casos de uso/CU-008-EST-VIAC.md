## Caso de Uso: CU-008-EST-VIAC - Dashboard de Usuario - Viajes Completados

Este caso de uso describe la funcionalidad de consulta y auditoría de los servicios que han finalizado su ciclo operativo. Permite al administrador revisar el histórico de rutas, pagos y detalles técnicos de viajes concluidos, manteniendo las mismas capacidades de gestión administrativa y exportación de datos.

---

## 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-008-EST-VIAC |
| **Caso de Uso** | Dashboard de usuario - Viajes completados |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Mostrar la lista de todos los viajes completados; monitoreo, clasificación y gestión de operaciones sobre el historial de servicios. |
| **Prioridad** | Alta |

---

## 🛠️ Precondiciones del Sistema
* El usuario inició sesión de forma exitosa (**CU-001-ADM** / **CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes para auditoría y gestión de viajes.
* Existe información de estadísticas y registros de viajes con estatus "Completado" en la base de datos.
* Los servicios de consulta y geolocalización están operativos.

---

## 🔄 Flujo del Sistema



| Actor Principal (Usuario)                             | Actor Secundario (Sistema)                                                                                                                                                                                                |
| :---------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|                                                       | 1) Ejecuta una consulta y muestra un listado de viajes completados con columnas: item, Fecha de creación, Fecha de carga,  Usuario, Unidad Asignada, Ruta, Detalle del viaje, , Estatus Detalle del pago Chat y  opciones |
| 2) Filtra resultados por ítems, fecha o rango         | 3) Actualiza la tabla dinámicamente según los criterios de búsqueda.                                                                                                                                                      |
| 4) Hace click en **Ver Mapa**                         | 5) Redirige a la vista de carga visual de la ruta en mapa (**CU-015-MAP**).                                                                                                                                               |
| 6) Selecciona **Cancelar/Anular viaje**               | 7) Muestra alerta de confirmación para revertir o anular el registro.                                                                                                                                                     |
| 8) Selecciona **Ver Detalle**                         | 9) Despliega un popup con el desglose técnico y financiero del viaje.                                                                                                                                                     |
| 10) Selecciona **Editar Información**                 | 11) Redirige a la vista de edición de datos básicos (**CU-016-EDV**).                                                                                                                                                     |
| 12) Gestiona Pagos (Cliente/Aliado/Preliquidar)       | 13) Muestra popups de confirmación para la validación de cierres de caja.                                                                                                                                                 |
| 14) Selecciona **Reiniciar viaje** o **Agregar nota** | 15) Muestra popups para habilitar re-ejecución o añadir comentarios de auditoría.                                                                                                                                         |
| 16) Selecciona **Exportar CSV**                       | 17) Genera y descarga el archivo con los datos históricos en formato CSV.                                                                                                                                                 |

---

## 🔀 Flujo Alternativo

| Escenario | Resultado |
| :--- | :--- |
| **1) Sin Información Disponible** | El sistema muestra la tabla con valores por defecto (vacía). |
| **2) Interacción con módulos** | El usuario puede navegar pero solo interactúa con las acciones permitidas por su rol. |

---

## ✅ Post-Condiciones

| Escenario de Éxito | Escenario de Fallo |
| :--- | :--- |
| La vista de viajes completados se muestra completamente renderizada con todas las opciones de gestión. | Se muestra mensaje de error y valores por defecto. |
| Los reportes CSV se generan con la data filtrada correctamente. | La tabla no carga o muestra errores de sincronización de datos. |

---

## 🔗 Casos de Uso Relacionados
* [Estadísticas (CU-004)](02%20Casos%20de%20uso/CU-004%20-%20Dashboard.md)
* [CU-007-EST-VIAA](02%20Casos%20de%20uso/CU-007-EST-VIAA.md)
* [CU-015-MAP](02%20Casos%20de%20uso/CU-015-MAP.md)
* [CU-016-EDV](02%20Casos%20de%20uso/CU-016-EDV.md)
* [CU-009-EST-VIAF](02%20Casos%20de%20uso/CU-009-EST-VIAF.md) 
* [CU-010-EST-HIT](02%20Casos%20de%20uso/CU-010-EST-HIT.md)  
* [CU-013-EST-BILL](02%20Casos%20de%20uso/CU-013-EST-BILL.md)