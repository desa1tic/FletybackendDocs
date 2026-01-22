# Archivo: `trip.js`
### Función: `create_trip` (Async)

**Descripción:**
Procesar la creación de solicitudes de viaje individuales o masivas.

|             | Campo             | Tipo     | Descripción                                                        |
| :---------- | :---------------- | :------- | :----------------------------------------------------------------- |
| **Entrada** | `user_data`       | Object   | Datos del usuario que solicita el servicio                         |
| **Entrada** | `trip_type`       | Number   | Tipo de viaje                                                      |
| **Entrada** | `service_type_id` | ObjectId | Identificador del tipo de servicio                                 |
| **Entrada** | `req_data`        | Object   | Detalles del viaje (coordenadas, direcciones, pago)                |
| **Entrada** | `req`             | Object   | Objeto de solicitud de Express                                     |
| **Entrada** | `response`        | Function | Call back para retornar resultados                                 |
| **Salida**  | `Objeto`          | Object   | **Promesa {** `success`, `trip`, `multiple_trips`, `message` **}** |

### Función: `upload_trip_images` (Async)

### Descripción:
Método que permite gestionar la carga y el almacenamiento de archivos.

|             | Campo                 | Tipo   | Descripción                                      |
| :---------- | :-------------------- | :----- | :----------------------------------------------- |
| **Entrada** | `user_id`             | String | id único de usuario                              |
| **Entrada** | `trip_id`             | String | id único de viaje                                |
| **Entrada** | `token`               | String | token de sesión                                  |
| **Entrada** | `user_type`           | Number | Tipo de usuario                                  |
| **Salida**  | `{ "success": true }` | Object | Indica que la operación se realizó correctamente |

## Función: `upload_trip_images` (Async)

### Descripción:
Método que permite gestionar la carga y el almacenamiento de archivos.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `provide_id` | String | Id de proveedor |
| **Entrada** | `trip_id` | String | Id de viaje |
| **Entrada** | `token` | String | Token de session |
| **Salida** | `{ "success": true }` | Object | |
## Función: `nearest_provider_list` (Async)

### Descripción:
Filtra y retorna una lista de proveedores (Conductores) que se encuentran físicamente cerca de una ubicación dada.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `cityType` | String | Id de proveedpr |
| **Entrada** | `req_data` | String | Datos de la solicitud: coordenadas, filtros de vehículo, preferencias y modo de pago. |
| **Entrada** | `response` | String | Callback para devolver la lista de proveedores o un error. |
| **Salida** | `{ "success": true, "message": "You get nearby driver list", "providers": [ ... ] }` | Object | |

## Función: `nearest_provider` (Async)

### Descripción:
Búsqueda y selección de proveedores disponibles.

|             | Campo                                                                   | Tipo      | Descripción                                          |
| :---------- | :---------------------------------------------------------------------- | :-------- | :--------------------------------------------------- |
| **Entrada** | `trip`                                                                  | Object    | Objeto de viaje o servicio                           |
| **Entrada** | `provider_id`                                                           | Object_id |                                                      |
| **Entrada** | `user_favourite_providers`                                              | Array     | Lista de IDs de proveedores                          |
| **Entrada** | `response`                                                              |           | Callback para retornar el resultado de la operación. |
| **Salida**  | `{ "success": true, "message": "Message code for nearby driver list" }` | Object    |                                                      |
## Función: `create` (Sync)

### Descripción:
Es una función controladora que gestiona el ciclo de vida inicial de una solicitud de viaje. Se realiza gestión de información de las paradas y direcciones de destino, se realizan validaciones al usuario, gestiona y aplica códigos promocionales, registra el viaje y se activa el algoritmo de búsqueda para encontrar al proveedor (conductor) más cercano.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | req.body con los siguientes campos: obligatorios {user_id, service_type_id, timezone} y campos opcionales {destination_addresses, destination_stops, promo_id, provider_id, created_by} |
| **Salida** | `{ "success": true, "trip": { ... }, "message": "" }` | Object | |
## Función: `provider_create` (Sync)

### Descripción:
Permite a un proveedor crear un viaje directamente vinculándolo a un número de teléfono. 

1) Verifica que el proveedor no tenga viajes activos.
2) Busca al usuario por su teléfono; la función registra un nuevo usuario automáticamente.
3) Al ser creado por el proveedor, el viaje se marca automáticamente como aceptado y el proveedor se asigna como confirmado con marcas de tiempo actuales.
4) Genera un número de factura único.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | req.body con los siguientes campos: {provider_id, phone, service_type_id, first_name, last_name, email, country_phone_code} |
| **Salida** | `{ "success": true, "message": "", "trip_id": "<id del viaje generado>", "user": <...> }` | Object | |
## Función: `send_request_from_dispatcher` (Sync)

### Descripción:
La función permite enviar una solicitud de un viaje existente a los proveedores cercanos.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | req.body con los siguientes campos: {trip_id, provider_id} |
| **Salida** | `{ "success": true, "message": "Message code for nearby driver list" }` | Object | |

## Función: get_near_provider (Sync)

### Descripción:
La función recupera una lista de proveedores cercanos basándose en la ubicación geográfica del usuario y el tipo de servicio seleccionado.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | req.body con los siguientes campos: {user_id, token, service_type_id, latitude, longitude, scheduled_request_time} |
| **Salida** | `{ "success": true, "providers": [....] }` | Object | |
## Función: `provider_get_trips` (Sync)

### Descripción:
La función recupera los detalles de los viajes vinculados a un proveedor.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `provider_id` | String | Id del proveedor |
| **Entrada** | `token` | String | token de sesion |
| **Salida** | `{ "success": true, "message": "", "providers": [....] }` | Object | |

# Archivo: `trip.js`

## Función: `provider_get_trip_details` (Sync)

### Descripción:
La función obtiene los detalles completos de los viajes asignados a un proveedor.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `rq` | Object | objeto req.body {provider_id, token} |
| **Salida** | `{ "success": true, "message": "MESSAGE_CODE_YOU_GET_TRIP", "trip_detail": [ { "user": {....} } ] }` | Object | |
## Función: `user_get_trip_status` (Sync)

### Descripción:
La función valida la sesión del usuario y busca un viaje activo o finalizado.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | objeto req.body {user_id, token, trip_id, type} |
| **Salida** | `{ "success": true, "message": "", "trip": {}, "city_detail": {}, "map_pin_image_url": "", "time_left_for_tip": "", "waiting_time_start_after_minute": "", "price_for_waiting_time": "", "total_wait_time": "", "isPromoUsed": "", "cancellation_fee": "", "payment_gateway": [...] }` | Object | |
## Función: `responds_trip` (Sync)

### Descripción:
Permite a un proveedor responder a una oferta de viaje. En este método, se verifica la identidad del proveedor mediante token, comprueba si el viaje aún está disponible y se procesa si el servicio es aceptado o rechazado.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | req.body: {provider_id, trip_id, is_provider_accepted, token, partner_id, is_request_timeout} |
| **Salida** | `{ "success": true, "message": "", "trip": {} }` | Object | |
## Función: `accept_trip` (Async)

### Descripción:
En la presente función se implementa la aceptación del servicio solicitado.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `provider` | Object | Objeto con información del proveedor |
| **Entrada** | `trip` | Object | Objeto con información del viaje |
| **Entrada** | `partner_id` | String | Identificador del partner |
| **Entrada** | `response` | Function | Callback para retornar el resultado de la operación. |
| **Salida** | `{ "success": true, "message": "MESSAGE_COD", "is_provider_accepted": 1 }` | Object | |
## Función: `reject_trip` (Sync)

### Descripción:
Función para procesar el rechazo de un viaje por parte de un proveedor.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `trip` | Object | Objeto con informacion del viaje. |
| **Entrada** | `provider_id` | String | Id de proveedor |
| **Entrada** | `is_request_timeout` | Boolean | Indica si el rechazo fue por falta de respuesta o por parte del usuario |
| **Entrada** | `response` | Function | Callback para enviar el resultado de la operación |
| **Salida** | `{ "success": true, "message": "", "is_provider_accepted": 0 }` | Object | |

## Función: `trip_cancel_by_user` (Sync)

### Descripción:
Cancela un viaje activo solicitado por un usuario. Se verifica el estado actual del viaje, se actualiza la disponibilidad del proveedor y mueve el registro del viaje a la tabla de históricos.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | request.body; req {user_id, trip_id, token, cancel_reason, type} |
| **Salida** | `{ "success": true, "message": "" }` | Object | |
## Función: `trip_cancel_by_provider` (Sync)

### Descripción:
Permite a un conductor cancelar un viaje activo. Se valida la identidad del proveedor, verifica que el viaje no haya sido cancelado previamente por otra parte y procede a liberar tanto al conductor como al vehículo.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | Dato con la informacion del viaje a cancelar, { provider_id, trip_id, token, cancel_reason } |
| **Salida** | `{ "success": true, "message": "" }` | Object | |

## Función: `scheduled_trip_cancel_by_admin` (Async)

### Descripción:
Detiene un viaje programado por intervención administrativa.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | objeto con inforamcion del viaje a cancelar; {trip_id, cancel_reason} |
| **Salida** | `{ "success": true }` | Object | |

## Función: `provider_set_trip_status` (Sync)

### Descripción:
Permite actualizar el estado de un viaje activo desde el lado del proveedor. Llegada al punto de origen y el inicio del viaje, captura coordenadas geográficas, marcas de tiempo y métricas de servicio.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | Object con información del viaje; {provider_id, is_provider_status, latitude, longitude, token} |
| **Salida** | `{ "success": true, "message": "", "is_provider_status": 6, "trip": {} }` | Object | |
## Función: `check_destination` (Sync)

### Descripción:
Valida los destinos de cara a sus coordenadas geográficas.

| | Campo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **Entrada** | `req` | Object | Objeto con información del destino; {user_id, token, latitude, longitude} |
| **Salida** | `{ "success": true, "message": "" }` | Object | |