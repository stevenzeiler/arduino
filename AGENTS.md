# AGENTS.md

Historical repo (2014), `legacy` profile of the repo standard. Docs-only changes unless Steven revives it.

## Stack
Arduino C++ sketches (`.ino`), a vendored AVR I2C library, and one Node script (`serial_server.js`).

## Layout
- `lcd_screen/main_cpp/` LCD demo
- `ift/` MLX90614 thermometer sketches (`MLX90614.ino` to serial, `infared_thermometer/` to LCD)
- `vendor/I2Cmaster/` third-party library by Peter Fleury (GPLv3). Do not edit; keep its `License.txt`.
- `docs/` banner and STATUS

## Commands
No build system. As it would have been done: open a sketch in the Arduino IDE 1.x and upload. Today, `arduino-cli compile --fqbn arduino:avr:uno <sketch dir>` would be the way to try (untested). `node serial_server.js` needs an old `serialport`.

## Rules
- Docs-only changes unless the repo is revived. Do not change sketches or vendored code.
- Never commit secrets.
- Use Conventional Commits (`docs:`, `fix:`, `chore:`).
- Update `docs/STATUS.md` whenever you learn what works.
- Mark guesses as **(inference)**.
