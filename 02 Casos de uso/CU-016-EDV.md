
## Caso de Uso: CU-016-EDV - Editar información del viaje

Este caso de uso describe el procedimiento para modificar los datos básicos de un viaje registrado. Se accede a esta vista desde los módulos de monitoreo para realizar ajustes administrativos o corregir información capturada durante la creación del servicio.

---

## 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-016-EDV |
| **Caso de Uso** | Editar información del viaje |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Redirigir a una vista donde se cargan los datos básicos del viaje y los mismos pueden ser editados. |
| **Prioridad** | Alta |

---

## 🛠️ Precondiciones del Sistema
* El usuario inició sesión de forma exitosa (**CU-001-ADM** / **CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes para la edición de registros.
* El usuario proviene de una acción de edición en: **CU-007-EST-VIAA**, **CU-008-EST-VIAC**, **CU-009-EST-VIAF** o **CU-014-EST-VIAE**, **CU-010-EST-HIT**

---

## 🔄 Flujo del Sistema

| Actor Principal (Usuario) | Actor Secundario (Sistema) |
| :--- | :--- |
| 1) Hace click sobre el botón/opción "Editar información" | 2) El sistema carga la vista de edición con los datos actuales del viaje. |
| 3) Modifica los campos necesarios (Datos básicos) | 4) El sistema valida la integridad de los nuevos datos ingresados. |
| 5) Confirma la edición | 6) El sistema actualiza el registro en la base de datos y confirma el éxito de la operación. |

---

## 🔀 Flujo Alternativo

| Escenario | Resultado |
| :--- | :--- |
| **1) Datos inválidos** | El sistema muestra un mensaje de error y no permite guardar los cambios. |
| **2) Cancelación de edición** | El usuario cancela la acción y el sistema lo devuelve a la vista de origen sin aplicar cambios. |

---

## ✅ Post-Condiciones

| Escenario de Éxito | Escenario de Fallo |
| :--- | :--- |
| Los datos del viaje son actualizados correctamente en el sistema. | El sistema mantiene la información original y muestra un error. |

---

## 🔗 Casos de Uso Relacionados
* [CU-007-EST-VIAA](02%20Casos%20de%20uso/CU-007-EST-VIAA.md)
* [CU-008-EST-VIAC](02%20Casos%20de%20uso/CU-008-EST-VIAC.md) 
* [CU-009-EST-VIAF](02%20Casos%20de%20uso/CU-009-EST-VIAF.md)
* [CU-014-EST-VIAE](02%20Casos%20de%20uso/CU-014-EST-VIAE.md)