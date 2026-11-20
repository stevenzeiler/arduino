# Status

_Last reviewed 2026-11-20 (audit pass 02, docs only)._ Historical repo, `legacy` profile.

## Works
- Nothing was run. No hardware, no Arduino toolchain was used in this review.

## Likely fine (read, not run)
- The three sketches are short and read as complete; the temperature maths is the standard MLX90614 formula.

## Broken or out of date
- `serial_server.js` uses the pre-1.0 `serialport` API (`serialport.SerialPort`, `parsers.readline`); there is no `package.json`, so no dependency is declared.
- The serial port name is hard-coded to a macOS device (`/dev/cu.usbmodem1411`).
- `i2cmaster.h` and `twimaster.cpp` date from 2005 (AVR-GCC 3.4); they may need changes for current Arduino cores. **(inference)**

## Unknown
- Whether the sketches compile on a current Arduino IDE (2.x) and board package.
- The exact LCD part. The code does not name it.

## Next (only if revived)
- Compile with `arduino-cli`, add a `package.json` and update `serial_server.js` to current `serialport`, add a wiring diagram, choose a licence.

## Not yet from the standard
Baseline tier only. Missing and waiting for revival: CONTRIBUTING, SECURITY, CHANGELOG, CI, CloudEvents catalog, API docs. LICENSE is a decision for Steven (the vendored library is GPLv3).
