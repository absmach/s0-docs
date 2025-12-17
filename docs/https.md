# **Connecting S0 to Magistrala via HTTPS**

## **Running Magistrala**

Ensure that Magistrala is running.

Ensure also you are in the `embedded/targets/zephyr/https` directory when executing the below steps.

Modify the configuration file in `src/config.h`

Start with the WiFi credentials as S0 in this case is in Station Mode.

```code
#define WIFI_SSID "SSID"    // Replace `SSID` with WiFi ssid
#define WIFI_PSK "PASSWORD" // Replace `PASSWORD` with Router password
```

## **Configuring Magistrala variables**

## **Standard TLS**

```code
#define MAGISTRALA_HOSTNAME "messaging.magistrala.absmach.eu" // Replace with your Magistrala instance hostname
#define MAGISTRALA_HTTPS_PORT 443
#define DOMAIN_ID "49baf6fe-2f7c-4748-8e99-2846346ef6ba"         // Replace with your Domain ID
#define CLIENT_ID "2fde3a36-e098-485c-8b83-314facaef903"         // Replace with your Client ID
#define CLIENT_SECRET "f6883013-af94-44c4-bdef-7188089c05fd" // Replace with your Client secret
#define CHANNEL_ID "0ffc71bc-4a25-4e22-bfb8-b1a847ed50ab"       // Replace with your Channel ID
```

## **TLS Certificate**

Update `src/ca_cert.h` with your Magistrala server's CA certificate.

## **Bulding and Flashing Code**

Once you update the configuration file, build and run the code:

```bash
west build -p always -b esp32c6_devkitc
west flash
west espressif monitor
```

To monitor Magistrala coap messages, check in Messages under Clients Management.

![Magistrala Messages](images/messages_magistrala.png)

---
