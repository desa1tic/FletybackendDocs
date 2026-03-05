## Caso de Uso: CU-007-EST-VIAA - Dashboard de Usuario - Viajes Activos

Este caso de uso describe la funcionalidad de monitoreo y gestión operativa de los servicios en curso. Es la herramienta principal de despacho y control, permitiendo supervisar desde la geolocalización hasta la edición administrativa de los viajes que aún no han finalizado.

---

## 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-007-EST-VIAA |
| **Caso de Uso** | Dashboard de usuario - Viajes activos |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Mostrar la lista en tiempo real de todos los viajes en curso; monitoreo, clasificación y gestión de operaciones sobre viajes activos. |
| **Prioridad** | Alta |

---

## 🛠️ Precondiciones del Sistema
* El usuario inició sesión de forma exitosa (**CU-001-ADM** / **CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes para la gestión de tráfico.
* Existen viajes registrados con estatus activo o en curso en la base de datos.
* Los servicios de geolocalización (Google Maps/Mapbox) se encuentran disponibles.

---

## 🔄 Flujo del Sistema



| Actor Principal (Usuario)                             | Actor Secundario (Sistema)                                                                                                                                                                                          |
| :---------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|                                                       | 1) Ejecuta una consulta y muestra un listado de viajes activos con columnas: Item, Fecha de craciòn, Fecha de carga, Usuario, Unidad asignada, Ruta, Detalle del viaje, Estatus, detalle del Pago, Chat y Opciones. |
| 2) Filtra resultados por ítems, fecha o rango         | 3) Actualiza la tabla dinámicamente según los criterios de búsqueda.                                                                                                                                                |
| 4) Hace click en **Ver Mapa**                         | 5) Redirige a la vista de geolocalización (**CU-015-MAP**).                                                                                                                                                         |
| 6) Selecciona **Cancelar Viaje**                      | 7) Muestra alerta de confirmación antes de procesar la baja.                                                                                                                                                        |
| 8) Selecciona **Ver Detalle**                         | 9) Despliega un Popup con la información técnica completa del viaje.                                                                                                                                                |
| 10) Selecciona **Editar Información**                 | 11) Redirige al formulario de edición de datos básicos (**CU-016-EDV**).                                                                                                                                            |
| 12) Gestiona Pagos (Cliente/Aliado/Preliquidar)       | 13) Muestra Popups de confirmación para cada acción financiera.                                                                                                                                                     |
| 14) Selecciona **Reiniciar Viaje** o **Agregar Nota** | 15) Muestra Popups para re-ejecución o registro de comentarios.                                                                                                                                                     |
| 16) Selecciona **Exportar CSV**                       | 17) Genera y descarga el archivo con la data filtrada.                                                                                                                                                              |

---

## 🔀 Flujo Alternativo

| Escenario | Resultado |
| :--- | :--- |
| **1) Sin Información Disponible** | El sistema muestra la tabla vacía con valores por defecto. |
| **2) Permisos Insuficientes** | El usuario puede visualizar pero no ejecutar acciones (Cancelar, Editar, Pagos). |

---

## ✅ Post-Condiciones

| Escenario de Éxito | Escenario de Fallo |
| :--- | :--- |
| La vista de viajes activos se muestra completamente renderizada con todas las opciones de gestión. | Se muestra mensaje de error en la consulta. |
| Las acciones administrativas impactan los modelos de datos correspondientes. | Los valores se muestran en cero o por defecto. |

---

## 🔗 Casos de Uso Relacionados
* [Estadísticas (CU-004)](02%20Casos%20de%20uso/CU-004%20-%20Dashboard.md)
* [CU-015-MAP](02%20Casos%20de%20uso/CU-015-MAP.md)
* [CU-016-EDV](02%20Casos%20de%20uso/CU-016-EDV.md)
* [CU-008-EST-VIAC](02%20Casos%20de%20uso/CU-008-EST-VIAC.md)  
* [[CU-009-EST-VIAF]] 
* [CU-010-EST-HIT](02%20Casos%20de%20uso/CU-010-EST-HIT.md) 