# zephyrBlinky
>**Important:** DO NOT clone this repository using Git. ONLY use west command to clone this repository, refer to [Section "Clone the project and initiate west"](#clone-the-project-and-initiate-west).

## Getting Started
***
These are exercises to build custom Zephyr project from scratch. See the [Introduction to Zephyr](https://docs.zephyrproject.org/latest/introduction/index.html) for high-level overview, and [Getting Started Guide](https://docs.zephyrproject.org/latest/getting_started/index.html) in the documentation to start developing.

1. Custom Manifest to build Blinky.
2. GPIO.

## Setup The Environment
***

## Build
***
To build the application, you need following steps to initialize your project root.

### Clone the project and initialize west
Let west clone and initialized the repository for you. After this step you will get a folder named `nucleoBlinky` containing a folder named `zephyrBlinky` (this repository). The `nucleoBlinky` is called the *Project Root*.

west init
~~~
west init -m https://github.com/weisheik/zephyrBlinky.git nucleoBlinky
~~~
Change to the created directory (Project Root) and use west to clone the required modules. This command will checkout every repository specified in the *Manifest* file, `west.yml`. Run the `west update` command whenever something has changed in the Manifest. 

west update
~~~bash
cd nucleoBlinky
west update
~~~

### Build the Blinky
You will find the build instructions for each target in their respective directories. This is the example for the blinky directory.

west build
~~~json
west build -b <board_name> zephyrBlinky/app