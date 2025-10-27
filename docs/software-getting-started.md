## Development Environment

To program and build firmware for the S0 board, you need to install **Zephyr OS**.  
Zephyr can be downloaded and set up from the official website:

👉 [https://zephyrproject.org](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)

Zephyr provides:

- Hardware abstraction for ESP32-C6 peripherals
- Real-time task scheduling
- Networking and protocol stacks
- Secure communication and TLS support

Once Zephyr is installed, you can build and flash applications directly to the S0 board using standard Zephyr tools such as `west`.

## Codebase Setup

Zephyr code for the various protocols can be found by cloning [Embedded Repository](https://github.com/absmach/embedded)

## SuperMQ Setup

Start by cloning the [SuperMQ repository](https://github.com/absmach/supermq)

Follow the documentation on how to start off SuperMQ via he CLI [SuperMQ startup](https://docs.supermq.absmach.eu/cli)
---
