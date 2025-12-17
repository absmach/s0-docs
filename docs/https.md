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
#define DOMAIN_ID "DOMAIN_ID"         // Replace with your Domain ID
#define CLIENT_ID "CLIENT_ID"         // Replace with your Client ID
#define CLIENT_SECRET "CLIENT_SECRET" // Replace with your Client secret
#define CHANNEL_ID "CHANNEL_ID"       // Replace with your Channel ID
```

## **TLS Certificate**

Update `src/ca_cert.h` with [Magistrala CA certificate](https://github.com/absmach/magistrala/blob/main/docker/ssl/certs/ca.crt).

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
