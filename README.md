# battery_monitor_supervolt_to_vrm

Connect the Supervolt v3 Bely Battery Management System to a Raspberry Pi running Venus OS which can then be connected to the VRM portal. Available data can be used for monitoring, analysis, setting trigger conditions and notifications, both via web interface and app.

### Setup

[setup.pdf](https://github.com/user-attachments/files/16105433/setup.pdf)

![setup](https://github.com/koebiii/battery_monitor_supervolt_to_vrm/assets/22169369/851fab3e-e4f3-4a09-9f00-cc1caf64fdca)

### Hardware

- Supervolt v3 (launched in October 2023, with blue cover plate) XS LiFePO4 battery, featuring a three RJ45 port BMS.
- RJ45-1 provides always on ~12.8V DC OUT (pin 1: +, pin 4: -), max 1A. RJ45-1 also serves as hardware switch port. Interconnect / hot-wire pins 5, 6, 7, 8 to turn off (charging and discharging) the battery terminals.
- RJ45-2 and RJ45-3 are identically providing RS-485 and CAN capabilities (pin 5: CAN-H, pin 6: CAN-L).

- Raspberry Pi 3B running open source Victron Energy Venus OS large (including NodeRED), powered through the CAN HAT. The RPi 3B seems to be a good pick in terms of power consumption, performance and compatibility.
- Waveshare 17075 2-channel CAN FD HAT, featuring MCP2518FD CAN controller. Powered through RJ45-1, has onboard 8-28V DC IN delivering power to the RPi. There are recommendations to not use the lower spec MCP2515 controller.
- Waveshare 19964 LTE & GPS DTU, powered through RJ45-1, has onboard 7-36V DC IN.

- CAN BMS to VE.Can (CAN FD HAT) cable for port RJ45-2. Modify Supervolt cable or build your own (pin 5: CAN-H, pin 6: CAN-L).
- 120Ω terminator for port RJ45-3, shipped with the battery.
- Tool free custom configurable RJ45 connectors.
- Cabling (0.25mm2), 1A fuse.
- ModMyPi 3 Modular HAT case + 10mm spacer. Case needs to be modified (cut open) in order to be able to access the HAT wire terminals.

### Installation

- in work

### Note

This is a private project. Work in progress.

Don’t copy without challenging the details.

No liability for any correctness and proper functioning, and damage on your hardware.

Major changes are likely.

Review, comments and contribution welcome.
