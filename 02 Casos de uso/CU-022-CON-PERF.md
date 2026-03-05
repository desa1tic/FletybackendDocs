## Caso de Uso: CU-022-CON-PERF - Editar Perfil del Conductor

Este caso de uso describe el proceso mediante el cual un administrador puede modificar la información personal o de contacto asociada a un conductor registrado en la plataforma, asegurando que los datos se mantengan actualizados en el sistema.

### 📋 Información General

| Sección | Descripción |
| :--- | :--- |
| **ID** | CU-022-CON-PERF |
| **Caso de Uso** | Editar Perfil del Conductor |
| **Actor Principal** | Usuario |
| **Actor Secundario** | Software |
| **Objetivo** | Permite modificar la información personal o de contacto asociados al conductor. |
| **Prioridad** | Alta |

---

### 🛠️ Precondiciones del Sistema
* El usuario inicia sesión de forma exitosa (**CU-001-ADM / CU-001-CLI**).
* El usuario cuenta con el rol y los permisos pertinentes.
* El usuario hizo clic en editar desde **CU-021-CON-ENLI**.

---

### 🔄 Flujo del Sistema

| Actor Principal (Usuario)                                                                                                     | Actor Secundario (Sistema)                                              |
| :---------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------- |
|                                                                                                                               | 1) El sistema carga los datos actuales del conductor.                   |
| 2) Modifica los datos del conductor; Nombre, Apellido, Email, Teléfono, Dirección, Contraseña y Fecha de creación (creado en) |                                                                         |
| 3) Guarda los datos.                                                                                                          | 4) El sistema deja persistencia de la modificación en la base de datos. |
| **Fin**                                                                                                                       |                                                                         |

---

### 🔀 Flujo Alternativo

| Actor Principal (Usuario) | Actor Secundario (Sistema) |
| :--- | :--- |
| 1) El usuario puede interactuar con otros módulos del sistema, aquellos que su rol le permita. | |
| 2) Regresa a **CU-021-CON-VEHÍ**. | |

---

### ✅ Post-Condiciones

| Escenario | Resultado Esperado |
| :--- | :--- |
| **Carga de Datos** | Los datos se cargaron correctamente para su edición. |
| **Éxito en Modificación** | La acción de modificar los datos fue exitosa y se refleja en el perfil. |
| **Fallo en Guardado** | La acción de guardar los datos no fue satisfactoria (error de conexión o validación). |

---

### 🔗 Casos de Uso Relacionados
* [Conductor (CU-021)](02%20Casos%20de%20uso/CU-021-Conductor.md)
* [CU-027-CON-APRO](02%20Casos%20de%20uso/CU-027-CON-APRO.md)
* [CU-028-CON-NPRO](02%20Casos%20de%20uso/CU-028-CON-NPRO.md)