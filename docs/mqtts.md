# **Connecting S0 to Magistrala via MQTTS**

## **Running Magistrala**

Ensure that Magistrala is running.

Ensure also you are in the `embedded/targets/zephyr/mqtts` directory when executing the below steps

Modify the configuration file in `src/config.h`

Start with the WiFi credentials as S0 in this case is in Station Mode.

```code
#define WIFI_SSID "SSID"    // Replace `SSID` with WiFi ssid
#define WIFI_PSK "PASSWORD" // Replace `PASSWORD` with Router password
```

## **Configuring Magistrala variables**

## **Standard TLS**

```code
#define MOSQUITTO_BROKER_HOSTNAME "messaging.magistrala-beta.absmach.eu"
#define MOSQUITTO_BROKER_PORT 8883  // Encrypted, unauthenticated MQTTS port
#define MQTT_CLIENTID "zephyr_mqtts_client_new"  // Replace with unique client ID
#define CLIENT_SECRET "f6883013-af94-44c4-bdef-7188089c05fd" // Replace with your Client secret
#define CLIENT_ID "2fde3a36-e098-485c-8b83-314facaef903"         // Replace with your Client ID
```

## **Setting topic**

Use the `DOMAINID` AND `CHANNELID` to setup the topic in the required format shown below.

```bash
m/DOMAINID/c/CHANNELID/pub #for publishing
m/DOMAINID/c/CHANNELID/sub #for subscribing
```

Resulting topic looks like this:

```code
#define MQTT_PUBLISH_TOPIC "m/49baf6fe-2f7c-4748-8e99-2846346ef6ba/c/0ffc71bc-4a25-4e22-bfb8-b1a847ed50ab/pub"
#define MQTT_SUBSCRIBE_TOPIC "m/49baf6fe-2f7c-4748-8e99-2846346ef6ba/c/0ffc71bc-4a25-4e22-bfb8-b1a847ed50ab/sub"
```

## **Bulding and Flashing Code**

Once you update the configuration file, build and run the code:

```bash
west build -p always -b esp32c6_devkitc
west flash
west espressif monitor
```

To monitor Magistrala mqtts messages, check in Messages under Clients Management.

![Magistrala Messages](images/messages_magistrala.png)

---
