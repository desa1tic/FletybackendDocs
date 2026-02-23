
### Grafo Relacional
EL objetivo es mostrar como se encuentran distribuidas y asociadas las distintas colecciones de documentos en la base de datos Actual



A continuación se muestra la definición de las colecciones existentes en el esquema flety_dev 
 de la base de datos en Mongo del sistema.

### Settings - Collection
 
```json
//// Settings
{
  "_id": { "$oid": "64f1a2b3c4d5e6f7a8b90124" },
  "provider_timeout": 60,
  "countryname": "",
  "adminCurrencyCode": "",
  "adminCurrency": "",
  "adminTimeZone": "",
  "sms_notification": false,
  "email_notification": false,
  "push_notification": false,
  "get_referral_profit_on_card_payment": false,
  "get_referral_profit_on_cash_payment": false,
  "userEmailVerification": false,
  "providerEmailVerification": false,
  "userSms": false,
  "providerSms": false,
  "admin_phone": "",
  "contactUsEmail": "",
  "twilio_call_masking": false,
  "access_key_id": "",
  "secret_key_id": "",
  "aws_bucket_name": "",
  "is_use_aws_bucket": false,
  "image_base_url": "",
  "is_ride_share": false,
  "is_split_payment": false,
  "max_split_user": 5,
  "admin_email": "",
  "default_Search_radious": 100,
  "scheduled_request_pre_start_minute": 30,
  "scheduled_request_day_limit": 3,
  "number_of_try_for_scheduled_request": 1,
  "is_public_demo": false,
  "is_provider_initiate_trip": false,
  "stripe_secret_key": "",
  "stripe_publishable_key": "",
  "paystack_secret_key": "",
  "paystack_publishable_key": "",
  "payu_key": "",
  "payu_salt": "",
  "payment_gateway_type": 10,
  "email": "",
  "password": "",
  "domain": "",
  "provider_offline_min": 30,
  "smtp_host": "",
  "smtp_port": "",
  "is_show_estimation_in_provider_app": false,
  "is_show_estimation_in_user_app": false,
  "twilio_account_sid": "",
  "twilio_auth_token": "",
  "twilio_number": "",
  "twiml_url": "",
  "userPath": false,
  "providerPath": false,
  "android_client_app_url": "",
  "android_driver_app_url": "",
  "ios_client_app_url": "",
  "ios_driver_app_url": "",
  "find_nearest_driver_type": 1,
  "request_send_to_no_of_providers": 2,
  "android_user_app_gcm_key": "",
  "android_provider_app_gcm_key": "",
  "android_user_app_google_key": "",
  "android_provider_app_google_key": "",
  "ios_user_app_google_key": "",
  "ios_provider_app_google_key": "",
  "web_app_google_key": "",
  "road_api_google_key": "",
  "backend_google_key": "",
  "user_passphrase": "",
  "provider_passphrase": "",
  "ios_certificate_mode": "",
  "hotline_app_id": "",
  "hotline_app_key": "",
  "google_map_lic_key": "",
  "is_google_map_lic_key_expired": 0,
  "server_url": "",
  "app_name": "FLETY",
  "partner_panel_name": "",
  "dispatcher_panel_name": "",
  "hotel_panel_name": "",
  "corporate_panel_name": "",
  "is_tip": false,
  "is_toll": false,
  "timezone_for_display_date": "",
  "android_user_app_version_code": "",
  "android_user_app_force_update": false,
  "android_provider_app_version_code": "",
  "android_provider_app_force_update": false,
  "ios_user_app_version_code": "",
  "ios_user_app_force_update": false,
  "ios_provider_app_version_code": "",
  "ios_provider_app_force_update": false,
  "is_debug_log": true,
  "location": [0, 0],
  "firebase_apiKey": "",
  "firebase_authDomain": "",
  "firebase_databaseURL": "",
  "firebase_projectId": "",
  "firebase_storageBucket": "",
  "firebase_messagingSenderId": "",
  "user_terms_and_condition": "",
  "provider_terms_and_condition": "",
  "user_privacy_policy": "",
  "provider_privacy_policy": "",
  "android_places_autocomplete_key": "",
  "ios_places_autocomplete_key": "",
  "team_id": "",
  "key_id": "",
  "provider_bundle_id": "",
  "user_bundle_id": "",
  "type": "",
  "private_key_id": "",
  "private_key": "",
  "client_email": "",
  "client_id": "",
  "auth_uri": "",
  "token_uri": "",
  "auth_provider_x509_cert_url": "",
  "client_x509_cert_url": "",
  "is_user_social_login": true,
  "is_provider_social_login": true,
  "is_guest_token": false,
  "is_otp_verification_start_trip": false,
  "is_receive_new_request_near_destination": false,
  "near_destination_radius": 2000,
  "is_driver_go_home": false,
  "is_driver_go_home_change_address": false,
  "driver_go_home_radius": 2000,
  "is_allow_multiple_stop": false,
  "is_multiple_stop_waiting_free_on_each_stop": false,
  "multiple_stop_count": 3,
  "is_allow_ride_share": false,
  "ride_share_pickup_radius": 3,
  "ride_share_destination_radius": 3,
  "minimum_phone_number_length": 8,
  "maximum_phone_number_length": 14,
  "email_list_trip_notifiy": [],
  "base_url": "",
  "webpush_public_key": "",
  "webpush_private_key": "",
  "server_type": 2,
  "connectium_key": "",
  "connectium_base_url": "",
  "connectium_short_code": "",
  "connectium_dlr": "",
  "connectium_dlr_level": null,
  "connectium_dlr_webhook_url": "",
  "stop_threshold": 50,
  "emails_notify_registration_data": [],
  "tracking_link_sms": false,
  "landing_page_url": "",
  "user_app_insta_ad_url": "",
  "driver_app_insta_ad_url": "",
  "advertise_urls": []
}
```


### Admins - Collection

```json
/// Admins
{
  "_id": { "$oid": "65d7e8f2a1b2c3d4e5f6g7h8" },
  "username": "",
  "password": "",
  "email": "",
  "token": "",
  "type": 0,
  "url_array": [],
  "created_at": { "$date": "" },
  "updated_at": { "$date": "" },
  "uid": "",
  "country_phone_code": "",
  "country_id": { "$oid": "65d7e8f2a1b2c3d4e5f6g799" },
  "super_admin": 1
}

```

### Aiports - Collection

```json
/// airports
{
  "_id": { "$oid": "65d7f1a2b3c4d5e6f7a8b901" },
  "city_id": { "$oid": "65d7f1a2b3c4d5e6f7a8b902" },
  "title": "",
  "kmlzone": [],
  "styleUrl": "",
  "styleHash": "",
  "description": "",
  "stroke": "",
  "stroke_opacity": 0,
  "stroke_width": 0,
  "fill": "",
  "fill_opacity": 0,
  "created_at": { "$date": "" },
  "updated_at": { "$date": "" }
}
```

### Airport_to_cities - Collection

```json
//// Airports_to_cities
{
  "_id": { "$oid": "65d7f5b1e4b0a12345678901" },
  "city_id": { "$oid": "65d7f5b1e4b0a12345678902" },
  "airport_id": { "$oid": "65d7f5b1e4b0a12345678903" },
  "price": 0,
  "service_type_id": { "$oid": "65d7f5b1e4b0a12345678904" },
  "created_at": { "$date": "" },
  "updated_at": { "$date": "" }
}
```


### API Partners - Collections

```json
////api_partners
{
  "_id": { "$oid": "65d802a1b3c4d5e6f7a8b905" },
  "name": "",
  "token": "a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6",
  "createdAt": { "$date": "" },
  "updatedAt": { "$date": "" },
  "__v": 0
}

```


### Bank Details - Collections

```json
//// bank_details
{
  "_id": { "$oid": "65d80ba5c4d5e6f7a8b90200" },
  "bank_holder_type": 0,
  "bank_holder_id": { "$oid": "65d80ba5c4d5e6f7a8b90201" },
  "unique_id": 1001,
  "bank_name": "",
  "bank_branch": "",
  "bank_account_number": "",
  "bank_account_holder_name": "",
  "bank_beneficiary_address": "",
  "bank_unique_code": "",
  "bank_swift_code": "",
  "is_updated": 0,
  "created_at": { "$date": "" },
  "updated_at": { "$date": "" }
}

```

### Bank Code - Collections
```json

```

### Cards - Collections

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89012" },
  "payment_method": "",
  "card_type": "",
  "user_id": { "$oid": "65d80ba5c4d5e6f7a8b90201" },
  "last_four": "",
  "customer_id": "",
  "is_default": 0,
  "payment_gateway_type": 10,
  "type": 0,
  "created_at": "",
  "updated_at": ""
}

```

### Cities - Collections

```json
//// cities
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89033" },
  "countryid": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "countryname": "",
  "full_cityname": "",
  "timezone": "",
  "cityname": "",
  "is_use_city_boundary": false,
  "city_locations": [],
  "payment_gateway": [0, 0],
  "unit": 1,
  "is_payment_mode_cash": 1,
  "is_payment_mode_card": 1,
  "is_payment_mode_apple_pay": 0,
  "isPromoApplyForCash": 1,
  "isPromoApplyForCard": 1,
  "isBusiness": 1,
  "airport_business": 1,
  "city_business": 1,
  "zone_business": 1,
  "isCountryBusiness": 1,
  "destination_city": [
    { "$oid": "65d80ba5c4d5e6f7a8b90206" },
    { "$oid": "65d80ba5c4d5e6f7a8b90207" }
  ],
  "citycode": "",
  "cityLatLong": [0, 0],
  "cityRadius": 50,
  "is_ask_user_for_fixed_fare": false,
  "provider_min_wallet_amount_set_for_received_cash_request": 0,
  "is_check_provider_wallet_amount_for_received_cash_request": false,
  "is_provider_earning_set_in_wallet_on_cash_payment": false,
  "is_provider_earning_set_in_wallet_on_other_payment": false,
  "is_caracas": false,
  "main_city": 0,
  "daily_cron_date": "",
  "created_at": "",
  "updated_at": ""
}

```

### City to Cities - Collections

```json
/// city_to_cities
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89044" },
  "city_id": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "destination_city_id": { "$oid": "65d80ba5c4d5e6f7a8b90233" },
  "price": 0,
  "service_type_id": { "$oid": "63482780ec17be54c98e9082" },
  "created_at": "",
  "updated_at": ""
}

```

### City Types - Collections

```json
/// city_types
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89055" },
  "countryid": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "is_hide": 1,
  "surge_multiplier": 0,
  "surge_start_hour": 0,
  "surge_end_hour": 0,
  "is_surge_hours": 0,
  "is_zone": 0,
  "rich_area_surge": [],
  "surge_hours": [
    { "is_surge": false, "day": "0", "day_time": [] },
    { "is_surge": false, "day": "1", "day_time": [] },
    { "is_surge": false, "day": "2", "day_time": [] },
    { "is_surge": false, "day": "3", "day_time": [] },
    { "is_surge": false, "day": "4", "day_time": [] },
    { "is_surge": false, "day": "5", "day_time": [] },
    { "is_surge": false, "day": "6", "day_time": [] }
  ],
  "is_business": 1,
  "countryname": "",
  "cityid": { "$oid": "65d8f1e2a3c4b5d6e7f89033" },
  "cityname": "",
  "typeid": { "$oid": "63482593ec17be54c98e8ebd" },
  "type_image": "",
  "min_fare": 0,
  "provider_profit": 0,
  "typename": "",
  "city_id": { "$oid": "65d8f1e2a3c4b5d6e7f89033" },
  "is_car_rental_business": 0,
  "car_rental_ids": [],
  "base_price_distance": 0,
  "base_price_time": 0,
  "base_price": 0,
  "price_per_unit_distance": 0,
  "price_for_total_time": 0,
  "waiting_time_start_after_minute": 0,
  "price_for_waiting_time": 0,
  "waiting_time_start_after_minute_multiple_stops": 0,
  "price_for_waiting_time_multiple_stops": 0,
  "tax": 0,
  "max_space": 0,
  "cancellation_fee": 0,
  "user_miscellaneous_fee": 0,
  "provider_miscellaneous_fee": 0,
  "user_tax": 0,
  "provider_tax": 0,
  "is_ride_share": 0,
  "model_pricing_ids": [],
  "modelid": [],
  "serviceid": [],
  "capacityid": [],
  "price_per_km_a": 0,
  "price_per_km_b": 0,
  "price_per_km_c": 0,
  "price_per_km_d": 0,
  "price_per_km_e": 0,
  "price_per_km_f": 0,
  "price_per_km_g": 0,
  "price_per_km_h": 0,
  "price_per_km_i": 0,
  "price_per_km_j": 0,
  "price_per_km_k": 0,
  "price_per_km_l": 0,
  "price_per_km_m": 0,
  "price_per_km_n": 0,
  "price_per_km_o": 0,
  "price_per_km_p": 0,
  "price_per_km_q": 0,
  "price_per_km_r": 0,
  "price_per_km_s": 0,
  "price_per_km_t": 0,
  "price_per_km_u": 0,
  "price_per_km_v": 0,
  "price_per_km_w": 0,
  "price_per_km_y": 0,
  "cost_per_stop_inside_city": 0,
  "cost_per_stop_outside_city": 0,
  "cost_per_helper": 0,
  "cost_travel_insurance": 0,
  "fixed_fees": 0,
  "model_type": 0,
  "user_type_id": { "$oid": "67bc7581c8895882f94bcfc0" },
  "user_type": 0,
  "free_stops": 2,
  "corporate_partner_profit_fees": 0,
  "ti_internal_transit": 0,
  "ferry_ticket_price": 0,
  "ferry_flety_cost": 0,
  "created_at": "",
  "updated_at": "",
  "zone_ids": [],
  "night_shift": 0,
  "boat_ticket": 0
}

```

### City Zones - Collelctions

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89066" },
  "cityid": { "$oid": "65d8f1e2a3c4b5d6e7f89033" },
  "title": "",
  "cityname": "",
  "styleUrl": "",
  "styleHash": "",
  "description": "",
  "stroke": "",
  "stroke_opacity": 0,
  "stroke_width": 0,
  "fill": "",
  "fill_opacity": 0,
  "total_provider_in_zone_queue": [
    { "$oid": "65d80ba5c4d5e6f7a8b90501" },
    { "$oid": "65d80ba5c4d5e6f7a8b90502" }
  ],
  "kmlzone": [
    [ -66.9036, 10.4806 ],
    [ -66.9040, 10.4810 ],
    [ -66.9036, 10.4806 ]
  ],
  "created_at": "",
  "updated_at": ""
}
```

### Corporates - Collections

```json
//// corporates
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89077" },
  "unique_id": 1,
  "company_name": "",
  "rif": "",
  "name": "",
  "password": "",
  "email": "",
  "country_phone_code": "",
  "phone": "",
  "address": "",
  "country_id": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "country_name": "",
  "wallet_currency_code": "",
  "customer_id": "",
  "stripe_doc": "",
  "account_id": "",
  "bank_id": "",
  "token": "",
  "is_approved": 0,
  "wallet": 0,
  "refferal_code": "",
  "last_transferred_date": "",
  "is_own_service_type": 0,
  "picture": "",
  "rif_url": "",
  "document_2": "",
  "alt_phone": "",
  "uid": "",
  "corporate_type_id": { "$oid": "65d80ba5c4d5e6f7a8b90900" },
  "corporate_type_userid": { "$oid": "65d80ba5c4d5e6f7a8b90901" },
  "url_array": [],
  "is_trip_approve": 0,
  "is_subcorporate_admin": 0,
  "is_hide_amount": 0,
  "mass_notifications": [],
  "preliquidation": 0,
  "is_use_fixed_partner_profit": 0,
  "is_damasco": 0,
  "allow_edit_trip": 0,
  "created_at": "",
  "updated_at": "",
  "active_api": false,
  "api_key": ""
}
```

### Countries - Collections

```json
{
  "_id": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "countryname": "",
  "countrycode": "",
  "alpha2": "",
  "currency": "",
  "flag_url": "",
  "currencycode": "",
  "currencysign": "",
  "countrytimezone": "",
  "country_all_timezone": [],
  "payment_gateways": [],
  "countryphonecode": "",
  "isBusiness": 1,
  "referral_bonus_to_user": 0,
  "bonus_to_providerreferral": 0,
  "referral_bonus_to_provider": 0,
  "bonus_to_userreferral": 0,
  "phone_number_min_length": 8,
  "phone_number_length": 10,
  "is_referral": true,
  "userreferral": 0,
  "is_provider_referral": true,
  "providerreferral": 0,
  "default_selected": false,
  "is_auto_transfer": true,
  "auto_transfer_day": 7,
  "daily_cron_date": "",
  "created_at": "",
  "updated_at": "",
  "coordinates": {
    "latitude": "0.0",
    "longitude": "0.0"
  }
}
```


### Country Datas - Collections

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89088" },
  "alpha2": "",
  "alpha3": "",
  "code": "",
  "currency_code": "",
  "decimals": 2,
  "name": "",
  "sign": "",
  "timezones": [],
  "timezones_detail": {
    "key": {
      "rawOffsetInMinutes": 0,
      "abbreviation": "",
      "rawFormat": ""
    }
  },
  "active": false
}
```

### Dispatchers - Collections

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89099" },
  "unique_id": 1,
  "first_name": "",
  "last_name": "",
  "password": "",
  "token": "",
  "email": "",
  "country_phone_code": "",
  "phone": "",
  "country": "",
  "countryid": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "city": "",
  "cityid": { "$oid": "65d8f1e2a3c4b5d6e7f89033" },
  "created_at": "",
  "updated_at": ""
}

```

### Documents - Collections

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89110" },
  "unique_id": 1,
  "countryid": { "$oid": "65d80ba5c4d5e6f7a8b90205" },
  "title": "",
  "type": 8,
  "option": 0,
  "expired_date": "",
  "issue_date": "",
  "is_issue_date": false,
  "is_degree": false,
  "degree": "",
  "is_unique_code": false,
  "is_expired_date": false,
  "document_for": 0,
  "created_at": "",
  "updated_at": ""
}
```

### Helpers - Collections

```json
{
  "_id": { "$oid": "65d8f1e2a3c4b5d6e7f89122" },
  "unique_id": 1,
  "name": "",
  "cedula": "",
  "phone": "",
  "country_phone_code": "",
  "helper_type_id": { "$oid": "65d80ba5c4d5e6f7a8b90301" },
  "created_at": "",
  "updated_at": ""
}
```