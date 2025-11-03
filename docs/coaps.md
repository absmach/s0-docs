# **Connecting S0 to Magistrala via CoAP Secure**

## **Running Magistrala**

Ensure that Magistrala is running.

Ensure also you are in the `embedded/targets/zephyr/coaps` directory when executing the below steps

Modify the configuration file in `src/config.h`

Start with the WiFi credentials as S0 in this case is in Station Mode.

```code
#define WIFI_SSID "SSID"    // Replace `SSID` with WiFi ssid
#define WIFI_PSK "PASSWORD" // Replace `PASSWORD` with Router password
```

## **Configuring Magistrala variables**

```code
#define MAGISTRALA_HOSTNAME "MAGISTRALA_HOSTNAME" // Replace with your Magistrala instance hostname or IP
#define MAGISTRALA_COAPS_PORT 5684
#define DOMAIN_ID "DOMAIN_ID"         // Replace with your Domain ID
#define CLIENT_ID "CLIENT_ID"         // Replace with your Client ID
#define CLIENT_SECRET "CLIENT_SECRET" // Replace with your Client secret
#define CHANNEL_ID "CHANNEL_ID"       // Replace with your Channel ID
```

## **DTLS Certificate**

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
