"Smart" Immersion Controller

See https://www.notion.so/niallgormley/Smart-Domestic-Immersion-Heater-Controller-AquaHeatIQ-cdcf95fe5f9b4179aaec39e1e94fd0bb

# Notes

## 11/11/2023 - Initial Prototype Iteration

### Results from assembly and first tests.

- Incorrect Footprint for choke (L2)
- 3.3v Power has some high freq (~20kHz) noise, and some voltage drop when relays activated.
- Relay configuration. Insufficient capacity (10A, needs ~13A) on relay NC config that I used to ensure only one relay activates at any one time.
- I wired all the temp sensors onto one jack, this kinda worked okay, and am getting temp readings, but getting "Sensor CRC errors" so its missing readings intermittently

### Ideas for v2 prototype iteration

- Change layout to match back mount for existing Horstmann mounting box. Remove earth terminal and align wiring.
- Redesign relay control circuit so that control circuit ensures that only is activated rather than relay wiring.
- Move indicator LEDs to MCU board.
- Add some capacitors/inductors to reduce PSU noise and voltage drop upon relay activation.
- Add support for a SCT-013-000 Current Sensor to measure power.
- Fix third-party KiCad libraries in projects/git.
- Find a better way of connecting the temp sensors?
