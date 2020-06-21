```
rustup target add thumbv6m-none-eabi thumbv7m-none-eabi thumbv7em-none-eabi thumbv7em-none-eabihf
cargo build --target thumbv7m-none-eabi
openocd
 arm-none-eabi-objcopy --output-target=binary blink blinky.bin
arm-none-eabi-gdb(windows)/gdb-multiarch(linux)
file ./target/thumbv7m-none-eabi/debug/blink
target remote :3333
monitor reset halt
load
continue
```
