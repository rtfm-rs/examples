# STM32L4 RTIC Blink example

Working example of simple LED blinking application for STM32l4xx.

## How-to

### Terminal workflow

Rust embedded relies heavily on `terminal workflow`, you will enter commands in the terminal.
This can be strange at first, but this enables usage of great things like continuous integration tools.

For Mac OS X consider using `iTerm2` instead of Terminal application.
For Windows consider using `powershell` (win + r -> powershell -> enter -> cd C:\examples\rtic_v5\heartbeat_stm32l4)

### Build

Run `cargo build` to compile the code. If you run it for the first time,
it will take some time to download and compile dependencies. After that, you will see something like:

```bash
>cargo build
Finished dev [optimized + debuginfo] target(s) in 0.10s
```

If you see warnings, feel free to ask for help in chat or issues of this repo.

### Connect the board

You need to connect you Bluepill board to ST-Link and connect pins:

| BOARD |    | ST-LINK |
|-------|----|---------|
| GND   | -> | GND     |
| 3.3V  | -> | 3.3V    |
| SWCLK | -> | SWCLK   |
| SWDIO | -> | SWDIO   |

Plug in ST-Link to USB port and wait it to initialize.

### Flashing and running

Flashing with a standard STLink v2 is easy with `cargo-embed`:

```shell
$ cargo install cargo-embed
$ cargo embed --release
```

Please review the `.embed.toml` file to change your target IC among other options.
