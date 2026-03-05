## Caso de Uso: CU-010-EST-HIT - Dashboard de Usuario - Historial de Viajes

Este caso de uso describe la funcionalidad de consulta global del histórico de servicios. A diferencia de las vistas segmentadas, el historial permite una auditoría completa de todos los estados de viaje (activos, completados, cancelados o futuros), sirviendo como la fuente central de verdad para la trazabilidad operativa y administrativa.

---

## 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-010-EST-HIT |
| **Caso de Uso** | Dashboard de usuario - historial de viajes |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Mostrar un listado con el historial de los viajes; monitoreo, clasificación y gestión de operaciones sobre los registros históricos. |
| **Prioridad** | Alta |

---

## 🛠️ Precondiciones del Sistema
* El usuario inició sesión de forma exitosa (**CU-001-ADM** / **CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes para auditoría de datos.
* Existe información transaccional y de viajes en la base de datos.

---

## 🔄 Flujo del Sistema



| Actor Principal (Usuario)                       | Actor Secundario (Sistema)                                                                                                                             |
| :---------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                                 | 1) El sistema ejecuta una consulta y muestra un listado con el historial total de los viajes.                                                          |
|                                                 | 2) Se visualiza: Item, Fecha de creación, Fecha de carga, Usuario, Unidad Asignada, Ruta, Detalle de viaje, Estatus, Detalle de pago, Chat y Opciones. |
| 3) Filtra resultados por ítems, fecha y rango   | 4) Actualiza la tabla dinámicamente según los parámetros de búsqueda.                                                                                  |
| 5) Hace click en **Ver Mapa**                   | 6) Redirige a la vista con carga visual de geolocalización (**CU-015-MAP**).                                                                           |
| 7) Selecciona **Cancelar viaje**                | 8) Muestra alerta de confirmación para anular o cancelar el servicio seleccionado.                                                                     |
| 9) Selecciona **Ver detalle**                   | 10) Muestra un popup con la ficha técnica y financiera detallada del viaje.                                                                            |
| 11) Selecciona **Editar información**           | 12) Redirige a la vista de edición de datos básicos (**CU-016-EDV**).                                                                                  |
| 13) Gestiona Pagos (Cliente/Aliado/Preliquidar) | 14) Muestra popups de confirmación para validar las transacciones.                                                                                     |
| 15) Selecciona **Reiniciar viaje** o **Nota**   | 16) Muestra popups para habilitar re-ejecución o agregar comentarios.                                                                                  |
| 17) Selecciona **Exportar CSV**                 | 18) Genera y descarga el archivo con los datos históricos filtrados.                                                                                   |

---

## 🔀 Flujo Alternativo

| Escenario | Resultado |
| :--- | :--- |
| **1) Sin Información Disponible** | El sistema muestra la tabla con valores por defecto (vacía). |
| **2) Interacción con módulos** | El usuario interactúa únicamente con las funciones habilitadas para su rol de visualización. |

---

## ✅ Post-Condiciones

| Escenario de Éxito | Escenario de Fallo |
| :--- | :--- |
| La vista de historial se muestra completamente renderizada con todas las opciones de gestión. | Se muestra mensaje de error en la consulta de datos. |
| El reporte CSV se genera íntegramente con el histórico solicitado. | La tabla muestra valores por defecto o ceros. |

---

## 🔗 Casos de Uso Relacionados
* [Estadísticas (CU-004)](02%20Casos%20de%20uso/CU-004%20-%20Dashboard.md)
* [CU-007-EST-VIAA](02%20Casos%20de%20uso/CU-007-EST-VIAA.md) 
* [CU-008-EST-VIAC](02%20Casos%20de%20uso/CU-008-EST-VIAC.md) 
* [CU-015-MAP](02%20Casos%20de%20uso/CU-015-MAP.md)
* [CU-016-EDV](02%20Casos%20de%20uso/CU-016-EDV.md)
* [CU-011-EST-RES](02%20Casos%20de%20uso/CU-011-EST-RES.md) 
* [CU-012-EST-MOC](02%20Casos%20de%20uso/CU-012-EST-MOC.md) 
* [CU-013-EST-BILL](02%20Casos%20de%20uso/CU-013-EST-BILL.md)