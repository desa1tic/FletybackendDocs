La capa de **Controllers** (`controllers/`) actúa como el intermediario entre las rutas y la lógica de negocio. Su función principal es recibir las solicitudes del cliente (HTTP requests), procesar los parámetros de entrada y coordinar la respuesta adecuada, delegando la carga de trabajo pesada a los **Services**.

# 📂 Estructura del Directorio de Controladores

Esta tabla detalla la organización de los archivos del sistema, facilitando la localización de la lógica de negocio según su categoría.

| Categoría / Carpeta | Archivo                                                                             | Responsabilidad Principal                                      |
| :------------------ | :---------------------------------------------------------------------------------- | :------------------------------------------------------------- |
| **Core (Raíz)**     | [Admin.js](04%20Código/Controller-Principal/Admin.md)                               | Configuración global y gestión del panel administrativo.       |
|                     | [Bank_Detail.js](04%20Código/Controller-Principal/Bank_Detail.md)                   | Administración de cuentas bancarias                            |
|                     | [Card.js](04%20Código/Controller-Principal/Card.md)                                 | Ciclo de vida de métodos de pago                               |
|                     | [City.js](04%20Código/Controller-Principal/City.md)                                 | Catálogo maestro de ciudades operativas por país.              |
|                     | [CityType.js](04%20Código/Controller-Principal/CityType.md)                         | Definición de tipos de vehículos, servicios y tarifas locales. |
|                     | [Country.js](04%20Código/Controller-Principal/Country.md)                           | Gestión de configuración regional y jerarquía geográfica.      |
|                     | [Crons.js](04%20Código/Controller-Principal/Crons.md)                               | Automatización de tareas programadas                           |
|                     | [Emergency_Contact.js](04%20Código/Controller-Principal/Emergency_Contact.md)       | Gestión de contactos de emergencia.                            |
|                     | [Provider.js](04%20Código/Controller-Principal/Provider.md)                         | Gestión del perfil y estado del conductor.                     |
|                     | [Provider_Analytics.js](04%20Código/Controller-Principal/Provider_Analytics.md)     | Registro de métricas de desempeño del proveedor                |
|                     | [Provider_Document.js](04%20Código/Controller-Principal/Provider_Document.md)       | Validación y almacenamiento de documentación del proveedor.    |
|                     | [Provider_Earning.js](04%20Código/Controller-Principal/Provider_Earning.md)         | Cálculo diario de ingresos y reportes de ganancias.            |
|                     | [Shedule_Trip.js](04%20Código/Controller-Principal/Shedule_trip.md)                 | Lógica para la reserva y activación de viajes.                 |
|                     | [Trip.js](04%20Código/Controller-Principal/Trip.md)                                 | Gestion de viajes en tiempo real (Solicitud → Fin).            |
|                     | [User.js](04%20Código/Controller-Principal/User.md)                                 | Registro, autenticación y gestión del perfil del usuarios.     |
|                     | [User_document.js](04%20Código/Controller-Principal/UserDocument.md)                | Verificación de identidad y documentos de usuarios.            |
|                     | [Wallet_History.js](04%20Código/Controller-Principal/Wallet_History.md)             | Gestión de los movimientos de la billetera.                    |
| **Corporativo**     | [Corporate_Api.js](04%20Código/Corporate_Controller/Corporate_Api.md)               | Gestión de socios.                                             |
|                     | [Corporate_Payments.js](04%20Código/Corporate_Controller/Corporate_Payments.md)     | Métodos de pago, facturación y saldo                           |
|                     | [Corporate_Static_Api.js](04%20Código/Corporate_Controller/Corporate_Static_Api.md) | Dashboards y analítica para usuarios                           |
| **Administración**  | [Weekly_Earning.js](04%20Código/Admin_Controller/Weekly_Earning.md)                 | Liquidación  y dispersión de pagos.                            |











