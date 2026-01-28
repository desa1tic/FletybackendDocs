La capa de **Controllers** (`controllers/`) actúa como el intermediario entre las rutas y la lógica de negocio. Su función principal es recibir las solicitudes del cliente (HTTP requests), procesar los parámetros de entrada y coordinar la respuesta adecuada, delegando la carga de trabajo pesada a los **Services**.

# 📂 Estructura del Directorio de Controladores

Esta tabla detalla la organización de los archivos del sistema, facilitando la localización de la lógica de negocio según su categoría.

| Categoría / Carpeta | Archivo                                                                                         | Responsabilidad Principal                                                        |
| :------------------ | :---------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------- |
| **Core (Raíz)**     | [Admin.js](04%20Código/Controller-Principal/Admin.md)                                           | Configuración global y gestión del panel administrativo.                         |
|                     | [Bank_Detail.js](04%20Código/Controller-Principal/Bank_Detail.md)                               | Administración de cuentas bancarias                                              |
|                     | [Card.js](04%20Código/Controller-Principal/Card.md)                                             | Ciclo de vida de métodos de pago                                                 |
|                     | [City.js](04%20Código/Controller-Principal/City.md)                                             | Catálogo maestro de ciudades operativas por país.                                |
|                     | [CityType.js](04%20Código/Controller-Principal/CityType.md)                                     | Definición de tipos de vehículos, servicios y tarifas locales.                   |
|                     | [Country.js](04%20Código/Controller-Principal/Country.md)                                       | Gestión de configuración regional y jerarquía geográfica.                        |
|                     | [Crons.js](04%20Código/Controller-Principal/Crons.md)                                           | Automatización de tareas programadas                                             |
|                     | [Emergency_Contact.js](04%20Código/Controller-Principal/Emergency_Contact.md)                   | Gestión de contactos de emergencia.                                              |
|                     | [Provider.js](04%20Código/Controller-Principal/Provider.md)                                     | Gestión del perfil y estado del conductor.                                       |
|                     | [Provider_Analytics.js](04%20Código/Controller-Principal/Provider_Analytics.md)                 | Registro de métricas de desempeño del proveedor                                  |
|                     | [Provider_Document.js](04%20Código/Controller-Principal/Provider_Document.md)                   | Validación y almacenamiento de documentación del proveedor.                      |
|                     | [Provider_Earning.js](04%20Código/Controller-Principal/Provider_Earning.md)                     | Cálculo diario de ingresos y reportes de ganancias.                              |
|                     | [Shedule_Trip.js](04%20Código/Controller-Principal/Shedule_trip.md)                             | Lógica para la reserva y activación de viajes.                                   |
|                     | [Trip.js](04%20Código/Controller-Principal/Trip.md)                                             | Gestion de viajes en tiempo real (Solicitud → Fin).                              |
|                     | [User.js](04%20Código/Controller-Principal/User.md)                                             | Registro, autenticación y gestión del perfil del usuarios.                       |
|                     | [User_document.js](04%20Código/Controller-Principal/UserDocument.md)                            | Verificación de identidad y documentos de usuarios.                              |
|                     | [Wallet_History.js](04%20Código/Controller-Principal/Wallet_History.md)                         | Gestión de los movimientos de la billetera.                                      |
| **Corporativo**     | [Corporate_Api.js](04%20Código/Corporate_Controller/Corporate_Api.md)                           | Gestión de socios.                                                               |
|                     | [Corporate.js](04%20Código/Corporate_Controller/Corporate.md)                                   | Gestión de socios.                                                               |
|                     | [Corporate_Payments.js](04%20Código/Corporate_Controller/Corporate_Payments.md)                 | Métodos de pago, facturación y saldo                                             |
|                     | [Corporate_Static_Api.js](04%20Código/Corporate_Controller/Corporate_Static_Api.md)             | Dashboards y analítica para usuarios                                             |
| **Administración**  | [Weekly_Earning.js](04%20Código/Admin_Controller/Weekly_Earning.md)                             | Liquidación  y dispersión de pagos.                                              |
|                     | [Admin_Partner_Weekly_Earning.js](04%20Código/Admin_Controller/Admin_Partner_Weekly_Earning.md) | Supervisa y gestiona la liquidación de las ganancias acumuladas de los asociados |
|                     | [Bank_Detail.js](04%20Código/Admin_Controller/Bank_Detail.md)                                   | Gestiona información de cuentas bancarias en la plataforma                       |
|                     | [City_Service.js](04%20Código/Admin_Controller/City_Service.md)                                 | Gestiona la lógica de configuración de servicios y tarifas por ciudad            |
|                     | [City.js](04%20Código/Admin_Controller/City.md)                                                 | Gestiona la creación de ciudades,                                                |
|                     | [Corporate_Admin.js](04%20Código/Admin_Controller/Corporate_Admin.md)                           | Gestiona  las cuentas corporativas                                               |
|                     | [Country.js](04%20Código/Admin_Controller/Country.md)                                           | Gestionar los países donde la plataforma opera.                                  |
|                     | [Daily_Earning.js](04%20Código/Admin_Controller/Daily_Earning.md)                               | gestiona las ganancias diarias                                                   |
|                     | [Dashboard.js](04%20Código/Admin_Controller/Dashboard.md)                                       | Gestiona la visualización de estadísticas globales                               |
|                     | [Dispatcher.js](04%20Código/Admin_Controller/Dispatcher.md)                                     | Gestiona la asignación de viajes manualmente                                     |
|                     | [Documents.js](04%20Código/Admin_Controller/Documents.md)                                       | Gestión de documentos de usuarios en la plataforma                               |
|                     | [Email_Detail.js](04%20Código/Admin_Controller/Email_Detail.md)                                 | Gestiona las plantillas y envio de corre                                         |
|                     | [Ferry_Ticket.js](04%20Código/Admin_Controller/Ferry_Ticket.md)                                 | Gestión y validación de tickets                                                  |
|                     | [Guest_Token.js](04%20Código/Admin_Controller/Guest_Token.md)                                   | Gestión de token de invitados.                                                   |
|                     | [Inbox_Notifications.js](04%20Código/Admin_Controller/Inbox_Notifications.md)                   | Gestión de Notificaciones                                                        |
|                     | [Languages.js](04%20Código/Admin_Controller/Languages.md)                                       | Gestión de idiomas                                                               |
|                     | [Map_View.js](04%20Código/Admin_Controller/Map_View.md)                                         | Proporciona los datos de una vista panorámica del estado de la flota             |
|                     | [Partner_Earning.js](04%20Código/Admin_Controller/Partner_Earning.md)                           | Gestión financiera desde de los asociados                                        |
|                     | [Partner_Payments.js](04%20Código/Admin_Controller/Partner_Payments.md)                         | Gestiona la pasarela de pagos y la billetera digital                             |
|                     | [Partner.js](04%20Código/Admin_Controller/Partner.md)                                           | Gestiona el ciclo de vida completo de los asociados                              |
|                     | [Promo_Code.js](04%20Código/Admin_Controller/Promo_Code.md)                                     | Gestiona el ciclo de vida de los códigos promocionales.                          |
|                     | [Provider_Daily_Earning.js](04%20Código/Admin_Controller/Provider_Daily_Earning.md)             | Permite gestionar  el desglose de las ganancias diarias de los conductores       |
|                     | [Provider_Earning.js](04%20Código/Admin_Controller/Provider_Earning.md)                         | Gestiona la visualización de ganancias diarias de los proveedores                |
|                     | [Provider_Weekly_Earning.js](04%20Código/Admin_Controller/Provider_Weekly_Earning.md)           | Gestiona la visualización de ganancias semanales de los proveedores              |
|                     | [Provider.js](04%20Código/Admin_Controller/Provider.md)                                         | Gestiona  ciclo de vida del proveedor.                                           |
|                     | [Request.js](04%20Código/Admin_Controller/Request.md)                                           | Gestión de las solicitudes                                                       |
|                     | [Review.js](04%20Código/Admin_Controller/Review.md)                                             | Gestiona las reseñas                                                             |
|                     | [Shedule.js](04%20Código/Admin_Controller/Shedule.md)                                           | Gestión de los viajes futuros                                                    |
|                     | [Send_Mass_Notifications.js](04%20Código/Admin_Controller/Send_Mass_Notifications.md)           | Gestiona las notificaciones masivas                                              |
|                     | [Service_Specifications.js](04%20Código/Admin_Controller/Service_Specifications.md)             | Gestiona los detalles de servicio                                                |
|                     | [Service_Type.js](04%20Código/Admin_Controller/Service_Type.md)                                 | Gestión de modelos de vehículos por servicio                                     |
|                     | [Setting.js](04%20Código/Admin_Controller/Setting.md)                                           | Gestiona el panel de configuración global del sistema                            |
|                     | [Sms_Detail.js](04%20Código/Admin_Controller/Sms_Detail.md)                                     | Gestiona las plantillas de mensajes del sistema.                                 |
|                     | [Transaction_History.js](04%20Código/Admin_Controller/Transaction_History.md)                   |                                                                                  |
|                     | [Trip_Earning.js](04%20Código/Admin_Controller/Trip_Earning.md)                                 |                                                                                  |
|                     | [Truck.js](04%20Código/Admin_Controller/Truck.md)                                               |                                                                                  |
|                     | [Type_Capacity.js](04%20Código/Admin_Controller/Type_Capacity.md)                               |                                                                                  |
















