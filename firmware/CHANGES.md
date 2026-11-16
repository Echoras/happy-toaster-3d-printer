# Happy Toaster: Marlin 2.1.2 configuration changes

These four files replace the matching files in a stock
[Marlin 2.1.2](https://github.com/MarlinFirmware/Marlin/tree/2.1.2) checkout
(`Marlin/Configuration.h`, `Marlin/Configuration_adv.h`, `Marlin/_Bootscreen.h`,
`Marlin/_Statusscreen.h`). Everything below is a change from the stock defaults.

## Board and drivers
- `MOTHERBOARD BOARD_RAMPS_14_EFB` (Arduino Mega 2560 + RAMPS 1.4)
- A4988 drivers on all axes, plus `Z2_DRIVER_TYPE A4988` for dual Z lead-screw motors

## Motion
- Steps/mm: X 83.7, Y 80.4, Z 400, E 95.2 (stock: 80, 80, 400, 500)
- Max feedrate X/Y lowered to 200 mm/s (stock 300)
- Print and travel acceleration lowered to 500 mm/s² (stock 3000)
- `CLASSIC_JERK` with X/Y jerk 8 mm/s and E jerk 12 mm/s
- `INVERT_X_DIR` to match motor wiring

## Temperature
- Heated bed thermistor enabled (`TEMP_SENSOR_BED 1`)
- `PIDTEMPBED` with tuned values Kp 115.57, Ki 18.81, Kd 473.37

## Endstops, probe and leveling
- Endstops inverted for this switch wiring; `ENDSTOP_INTERRUPTS_FEATURE` enabled
- Fixed-mount inductive Z probe (`FIX_MOUNTED_PROBE`, `USE_PROBE_FOR_Z_HOMING`)
- Measured probe offset: `NOZZLE_TO_PROBE_OFFSET { 40, 10, -0.85 }`
- `Z_SAFE_HOMING` and `AUTO_BED_LEVELING_BILINEAR`
- `Z_MIN_PROBE_REPEATABILITY_TEST` (M48) for checking probe accuracy

## Machine size and features
- Bed 310 × 310 mm (stock 200 × 200), Z max 230 mm
- `EEPROM_SETTINGS`, `SDSUPPORT`, RepRapDiscount full graphic LCD
- Custom boot and status screens, machine name "Happy Toaster"
