# **Getting Started**

## **Development Environment**

To program and build firmware for the S0 board, you need to install **Zephyr OS**.  
Zephyr can be downloaded and set up from the official website:

👉 [https://zephyrproject.org](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)

Zephyr provides:

- Hardware abstraction for ESP32-C6 peripherals
- Real-time task scheduling
- Networking and protocol stacks
- Secure communication and TLS support

Once Zephyr is installed, you can build and flash applications directly to the S0 board using standard Zephyr tools such as `west`.

## **Codebase Setup**

Zephyr code for the various protocols can be accessed by cloning [Embedded Repository](https://github.com/absmach/embedded)

## **Magistrala Setup**

- Start by navigating to [Magistrala](https://cloud.magistrala.absmach.eu) and signing up.

- Create a domain, channel and client.

- Connect the client to the channel you created.
  
- From these will you get the `CHANNELID`, `DOMAINID`, `CLIENTID` and `CLIENTSECRET`
  
---
