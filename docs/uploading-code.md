# Uploading Code

Before uplaoding any code, be sure to have activated a virtual environment as guided in the [Zephyr documentation](https://docs.zephyrproject.org/latest/develop/getting_started/index.html).

Download and install the binary blobs that the Espressif HAL needs by running:

```bash
west blob fetch hal_espressif
```

After cloning the embedded Repository, move to the directory with the Zephyr code for all the protocols.

```bash
cd /embedded/targets/zephyr
ls
```

Choose the protocol you want to communicate over by moving into that directory.

Make sure to observe these files in your current directory:

```bash
CMakeLists.txt
prj.conf
src
```

Change the variable in config file in `src/config.h` to be same with your SuperMQ environment variables ie `CLIENTID`, `CLIENTSECRET`, `DOMAINID`, `CHANNELID`.

Do this for all the variables in the config file.

Build the code using the command:

```bash
west build -p always -b esp32c6_devkitc
```

The board parameter can be changed to whichever board you are using as long as it is recognized by Zephyr.
For more information, check [Zephyr supported boards](https://docs.zephyrproject.org/latest/boards/index.html#)

To upload code to the S0 and monitor the serial output:

```bash
west flash
west espressif monitor
```
