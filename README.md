![](./resources/official_armmbed_example_badge.png)
# mbed-os-example-devicekey

Device key example for Mbed OS

## Getting started with DeviceKey ##

This is an example of an application that uses the DeviceKey APIs. 
The application injects a dummy root of trust (ROT) if true random number generator (TRNG) is not avalable. The application also invoke the derive key API several times in diffrent conditions and print the result. 

## Required hardware
* An mbed-os supported development board.
* A micro-USB cable.

## Mbed OS build tools

### Mbed CLI 2
Starting with version 6.5, Mbed OS uses Mbed CLI 2. It uses Ninja as a build system, and CMake to generate the build environment and manage the build process in a compiler-independent manner. If you are working with Mbed OS version prior to 6.5 then check the section [Mbed CLI 1](#mbed-cli-1).
1. [Install Mbed CLI 2](https://os.mbed.com/docs/mbed-os/latest/build-tools/install-or-upgrade.html).
1. From the command-line, import the example: `mbed-tools import mbed-os-example-devicekey`
1. Change the current directory to where the project was imported.

### Mbed CLI 1
1. [Install Mbed CLI 1](https://os.mbed.com/docs/mbed-os/latest/quick-start/offline-with-mbed-cli.html).
1. From the command-line, import the example: `mbed import mbed-os-example-devicekey`
1. Change the current directory to where the project was imported.

## Building and running

1. Connect a USB cable between the USB port on the target and the host computer.
1. Run the following command to build the example project and program the microcontroller flash memory:

    * Mbed CLI 2

    ```bash
    $ mbed-tools compile -m <TARGET> -t <TOOLCHAIN> --flash --sterm
    ```

    * Mbed CLI 1

    ```bash
    $ mbed compile -m <TARGET> -t <TOOLCHAIN> --flash --sterm
    ```

Your PC may take a few minutes to compile your code.

The binary is located at:

* **Mbed CLI 2** -
  `./cmake_build/<TARGET>/develop/<TOOLCHAIN>/mbed-os-example-devicekey.bin`

* **Mbed CLI 1** - `./BUILD/<TARGET>/<TOOLCHAIN>/mbed-os-example-devicekey.bin`.

You can manually copy the binary to the target, which gets mounted on the host
computer through USB, rather than using the `--flash` option.

You can also open a serial terminal separately, rather than using the `--sterm`
option, with the following command:

* Mbed CLI 2
    ```bash
    $ mbed-tools sterm
    ```

* Mbed CLI 1
    ```bash
    $ mbed sterm
    ```

The expected log can be found in [`tests/devicekey.log`](tests/devicekey.log).

## Troubleshooting

If you have problems, you can review the [documentation](https://os.mbed.com/docs/latest/tutorials/debugging.html) for suggestions on what could be wrong and how to fix it.

## License and contributions

The software is provided under Apache-2.0 license. Contributions to this project are accepted under the same license. Please see [contributing.md](./CONTRIBUTING.md) for more info.

This project contains code from other projects. The original license text is included in those source files. They must comply with our [license guide](https://os.mbed.com/docs/mbed-os/latest/contributing/license.html)
