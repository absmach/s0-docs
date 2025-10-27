# Software

# S0 Software Overview

## Introduction

The **S0** is an IoT gateway board built around the **ESP32-C6** microcontroller, based on the **RISC-V** architecture. It is designed for versatile connectivity, efficiency, and secure communication with cloud-based IoT platforms.

The board runs on the **Zephyr Real-Time Operating System (RTOS)**, offering stability, modularity, and scalability for embedded applications. Zephyr provides extensive hardware abstraction and a unified development framework for ESP32-C6 and other architectures.

---

## Communication Protocols

The S0 board supports a variety of IoT communication protocols. These enable secure and efficient data transfer between the device and cloud services.

| Protocol       | Security | Description                                            | Reference                                                                      |
| -------------- | -------- | ------------------------------------------------------ | ------------------------------------------------------------------------------ |
| **MQTT**       | ✗        | Lightweight messaging protocol for IoT data exchange.  | [GitHub: MQTT Example](https://github.com/absmach/s0-mqtt-example)             |
| **MQTTS**      | ✓        | Secure MQTT communication over TLS (mTLS supported).   | [GitHub: MQTTS Example](https://github.com/absmach/s0-mqtts-example)           |
| **CoAP**       | ✗        | REST-based protocol optimized for constrained devices. | [GitHub: CoAP Example](https://github.com/absmach/s0-coap-example)             |
| **CoAP DTLS**  | ✓        | Secure CoAP communication using DTLS encryption.       | [GitHub: CoAP-DTLS Example](https://github.com/absmach/s0-coap-dtls-example)   |
| **HTTP**       | ✗        | Standard web communication protocol.                   | [GitHub: HTTP Example](https://github.com/absmach/s0-http-example)             |
| **HTTPS**      | ✓        | Secure version of HTTP over TLS.                       | [GitHub: HTTPS Example](https://github.com/absmach/s0-https-example)           |
| **WebSockets** | ✓        | Full-duplex communication protocol over TCP.           | [GitHub: WebSockets Example](https://github.com/absmach/s0-websockets-example) |

> Each communication example repository contains setup guides, sample code, and instructions for integration with Zephyr.

---

## Summary

The S0 board combines Zephyr’s robust RTOS capabilities with modern communication stacks and secure connectivity features. Its compatibility with **Magistrala**/**SuperMQ** enables seamless data flow between hardware and cloud, empowering developers to build scalable, secure, and efficient IoT systems.

---
