# Electronic Components Guide

Welcome to our electronics components inventory and reference guide! This document covers the various electronic components available in the workshop, their uses, and how to get started with them.

## Table of Contents
- [Small Computers (Single Board Computers)](#small-computers)
- [Microcontrollers](#microcontrollers)
- [Sensors](#sensors)
- [Discrete Components](#discrete-components)
- [Power Supplies and Regulators](#power-supplies-and-regulators)
- [Communication Modules](#communication-modules)
- [Storage and Organization](#storage-and-organization)
- [Getting Started](#getting-started)
- [Resources](#resources)

---

## Small Computers (Single Board Computers)

### Raspberry Pi Family

The **Raspberry Pi** is a very common small form factor Linux computer perfect for projects requiring full operating system capabilities.

#### Advantages
- **Huge ecosystem**: Massive community support with existing software libraries and hardware add-ons (called "HATs")
- **Full OS**: Run Linux distributions, browse the web, run complex applications
- **Rich connectivity**: Most models have Ethernet, HDMI, USB, and WiFi
- **Powerful**: Can handle multimedia, databases, web servers, etc.
- **GPIO pins**: Interface with electronics projects
- **Well documented**: Extensive tutorials and project examples

#### Models Available
- **Raspberry Pi Zero / Zero W**: 
  - Ultra-compact ($5-15)
  - Zero W includes WiFi and Bluetooth
  - Great for embedded projects
  - Single-core 1GHz processor
  
- **Raspberry Pi 3/4**: 
  - More powerful ($35-45)
  - Quad-core processors
  - 1-8GB RAM options (Pi 4)
  - Multiple USB ports
  - Gigabit Ethernet (Pi 4)
  - Best for projects needing performance

- **Raspberry Pi 5** (Latest):
  - Most powerful option (~$60-80)
  - Significant performance improvements
  - PCIe support
  - Better I/O capabilities

#### Best Use Cases
- Home automation hubs
- Media centers (Kodi, Plex)
- Retro gaming (RetroPie)
- Web servers
- Network attached storage (NAS)
- Computer vision (with camera module)
- Learning Linux and programming
- Projects requiring multiple USB devices

#### Getting Started
1. Get a microSD card (16GB+ recommended)
2. Install Raspberry Pi OS (formerly Raspbian)
3. Connect keyboard, mouse, monitor via HDMI
4. Follow online tutorials for your specific project

#### Common HATs (Hardware Attached on Top)
- **Sense HAT**: Environmental sensors, LED matrix, joystick
- **Camera Module**: HD video recording and photography
- **Power supply HATs**: Clean power delivery, UPS functionality
- **Motor control**: For robotics projects
- **PoE HAT**: Power over Ethernet

### Other Single Board Computers

#### Arduino with Linux Shields
Some Arduino boards can run Linux with appropriate shields, bridging the gap between microcontrollers and full computers.

#### Orange Pi / Banana Pi
Budget alternatives to Raspberry Pi with varying capabilities and compatibility.

---

## Microcontrollers

Microcontrollers are single-chip computers designed for embedded applications. Unlike Raspberry Pi, they run a single program repeatedly without an operating system.

### ESP8266 - "The Swiss Army Chainsaw"

The **ESP8266** revolutionized IoT projects by combining a capable microcontroller with built-in WiFi at an incredibly low price point.

#### Specifications
- **Processor**: 80/160 MHz Tensilica L106
- **Memory**: 32KB instruction, 80KB user data
- **WiFi**: 802.11 b/g/n (2.4GHz)
- **GPIO**: 9-11 usable pins (depending on module)
- **Price**: $2-5 (incredibly cheap!)
- **Power**: 3.3V operation

#### Popular Modules
- **ESP-01**: Minimal, 8-pin module
- **NodeMCU**: Development board with USB, voltage regulator
- **Wemos D1 Mini**: Compact, Arduino-compatible
- **ESP-12E/F**: Most common module for custom PCBs

#### Programming Options
- **Arduino IDE**: Easiest for beginners, huge library support
- **NodeMCU (Lua)**: Scripting language, rapid prototyping
- **MicroPython**: Python on microcontrollers
- **ESP-IDF**: Native ESP SDK for advanced users
- **PlatformIO**: Professional development environment

#### Best Use Cases
- WiFi-connected sensors (temperature, humidity, motion)
- Home automation controllers
- IoT devices (smart switches, monitors)
- Web servers (simple status pages)
- MQTT clients for messaging
- WiFi-controlled LED strips
- Remote monitoring systems

#### Limitations
- Limited GPIO pins
- 3.3V only (needs level shifters for 5V devices)
- Limited memory for complex programs
- WiFi only (no Bluetooth on original ESP8266)

#### Where to Buy
- AliExpress: ~$2-3 each (bulk discounts available)
- Amazon: ~$5-8 for faster shipping
- Adafruit/SparkFun: $7-10 with better documentation

### ESP32 - The Powerful Successor

The **ESP32** takes everything great about the ESP8266 and adds significantly more capabilities.

#### Specifications
- **Processor**: Dual-core 240MHz Tensilica LX6
- **Memory**: 520KB SRAM, 4MB+ Flash
- **Connectivity**: 
  - WiFi 802.11 b/g/n
  - Bluetooth 4.2 and BLE
- **GPIO**: 34 pins (many with special functions)
- **ADC**: 18 channels, 12-bit resolution
- **DAC**: 2 channels, 8-bit
- **Touch sensors**: 10 capacitive touch pins
- **Price**: $4-10 depending on module

#### Popular Modules
- **ESP32-DEVKIT**: Standard development board
- **ESP32-CAM**: Includes camera module
- **ESP32-WROVER**: Extra PSRAM for memory-intensive tasks
- **M5Stack**: Complete development system with display
- **Wemos LOLIN32**: Compact with battery charging

#### Improvements Over ESP8266
- Much more RAM (critical for complex applications)
- Dual-core processor (can run tasks simultaneously)
- More GPIO pins
- Bluetooth and BLE support
- Better ADC (more channels, better accuracy)
- Hardware cryptography acceleration
- More PWM channels
- CAN bus support

#### Best Use Cases
- Bluetooth Low Energy (BLE) devices
- Battery-powered projects (deep sleep modes)
- Audio projects (I2S support)
- Projects needing many sensors
- Real-time data processing
- Camera/video applications (ESP32-CAM)
- Complex automation systems
- Wearable devices

#### Programming
Same options as ESP8266 plus:
- **ESP-WHO**: Face detection/recognition
- **ESP-ADF**: Audio development framework
- Better multitasking support with dual cores

### Arduino Boards

Traditional microcontroller development boards with excellent beginner support.

#### Arduino Uno
- **Classic choice** for learning electronics
- ATmega328P processor (16MHz)
- 5V operation
- 14 digital I/O pins, 6 analog inputs
- Huge library ecosystem
- Perfect for: Learning, basic projects, shields

#### Arduino Nano
- Compact version of Uno
- Breadboard-friendly
- Same ATmega328P chip
- Great for permanent installations

#### Arduino Mega
- Many more pins (54 digital, 16 analog)
- More memory
- For projects needing lots of I/O
- Great with TFT displays, complex robotics

#### Arduino Leonardo/Pro Micro
- Native USB support
- Can act as keyboard/mouse
- ATmega32u4 processor
- Perfect for: USB HID projects, custom game controllers

### Other Microcontrollers

#### STM32 "Blue Pill"
- ARM Cortex-M3 processor (72MHz)
- Very cheap ($2-4)
- More powerful than Arduino
- Steeper learning curve

#### Teensy
- Powerful ARM-based boards
- Excellent for audio projects
- High-speed USB
- More expensive but very capable

#### ATtiny Series
- Tiny, cheap microcontrollers
- 8-pin chips (ATtiny85)
- Limited pins but great for simple projects
- Can be programmed via Arduino

---

## Sensors

We stock a wide variety of sensors for different measurement needs. Here's what's typically available:

### Environmental Sensors

#### Temperature & Humidity
- **DHT11**: Basic, ±2°C accuracy, cheap ($1-2)
- **DHT22 (AM2302)**: Better accuracy (±0.5°C), wider range ($3-5)
- **BME280**: Temp, humidity, barometric pressure, I2C/SPI ($5-8)
- **DS18B20**: Waterproof temperature sensor, 1-Wire protocol ($2-4)
- **SHT31**: High accuracy, I2C ($7-10)

#### Air Quality
- **MQ-2**: Smoke, LPG, propane detection ($1-3)
- **MQ-135**: Air quality, CO2 sensing ($2-4)
- **CCS811**: eCO2 and TVOC sensor with I2C ($10-15)
- **PMS5003**: Particulate matter sensor (PM2.5, PM10) ($15-25)

#### Light
- **LDR (Photoresistor)**: Simple light detection ($0.10-0.50)
- **BH1750**: Digital ambient light sensor, I2C ($1-3)
- **TSL2561**: Luminosity sensor with IR rejection ($5-8)
- **VEML7700**: High accuracy lux sensor ($4-6)

#### Pressure & Altitude
- **BMP180**: Barometric pressure, altitude ($2-4)
- **BMP280**: Improved version, better accuracy ($3-5)
- **BME680**: Temp, humidity, pressure, gas sensor ($10-15)

### Motion & Position Sensors

#### Accelerometers & Gyroscopes
- **MPU6050**: 6-axis (3-axis gyro + 3-axis accelerometer), I2C ($2-5)
- **MPU9250**: 9-axis (adds magnetometer) ($5-10)
- **ADXL345**: 3-axis accelerometer, popular choice ($3-6)
- **LSM6DS3**: Low power 6-axis IMU ($5-8)

#### Distance & Proximity
- **HC-SR04**: Ultrasonic distance sensor (2cm-4m), cheap ($1-3)
- **VL53L0X**: Time-of-flight laser ranging, I2C ($5-12)
- **GP2Y0A21YK**: Sharp IR distance sensor (10-80cm) ($8-12)
- **JSN-SR04T**: Waterproof ultrasonic ($5-8)

#### PIR (Motion Detection)
- **HC-SR501**: Passive infrared motion detector ($1-3)
- **AM312**: Mini PIR sensor, low power ($1-2)

### Position & Navigation

#### GPS
- **NEO-6M**: Basic GPS module, UART ($8-15)
- **NEO-7M**: Improved acquisition time ($10-18)
- **NEO-M8N**: Better accuracy and reliability ($15-25)

#### Magnetometers (Compass)
- **HMC5883L**: 3-axis digital compass, I2C ($2-5)
- **QMC5883L**: Compatible alternative ($1-3)

### Optical Sensors

#### Color & Gesture
- **TCS34725**: RGB color sensor, I2C ($7-10)
- **APDS-9960**: RGB, gesture, proximity sensor ($5-8)

#### Line Followers
- **TCRT5000**: IR reflective sensor ($0.50-1)
- **QTR sensor arrays**: Multiple sensors for line following ($5-15)

### Current & Voltage

#### Current Sensors
- **ACS712**: Hall effect current sensor (5A/20A/30A versions) ($2-5)
- **INA219**: High-side current/voltage monitor, I2C ($5-10)

#### Voltage Sensors
- **Voltage divider modules**: Step down for ADC reading ($1-2)
- **INA3221**: Triple-channel voltage/current monitor ($8-12)

### Other Sensors

#### Sound
- **MAX4466**: Electret microphone with adjustable gain ($3-6)
- **KY-038**: Simple sound detection module ($1-2)
- **INMP441**: I2S digital microphone ($3-5)

#### Vibration
- **SW-420**: Vibration detection module ($1-2)

#### Gas/Flame
- **MQ series**: Various gas sensors (MQ-2, MQ-3, MQ-4, etc.) ($1-4 each)
- **Flame sensor**: IR-based flame detection ($1-2)

#### Touch
- **TTP223**: Capacitive touch sensor ($0.50-1)
- **MPR121**: 12-channel capacitive touch, I2C ($5-8)

### Sensor Communication Protocols

Understanding how sensors communicate:

- **Analog**: Simple voltage output, read with ADC
- **Digital GPIO**: High/low signals
- **I2C**: Two-wire protocol, multiple devices on same bus
- **SPI**: Faster serial protocol, requires more pins
- **UART/Serial**: Asynchronous communication
- **1-Wire**: Single wire for data (like DS18B20)

---

## Discrete Components

Basic electronic components available in the workshop.

### Resistors

#### Standard Values
We stock resistors in E12 or E24 series, common values:
- **10Ω - 1MΩ** range
- Common values: 220Ω, 330Ω, 1kΩ, 4.7kΩ, 10kΩ, 100kΩ
- **Power ratings**: 1/4W (most common), 1/2W, 1W
- **Types**: Through-hole and SMD

#### Special Resistors
- **Potentiometers**: Variable resistors (10kΩ most common)
- **Trimpots**: Small adjustable resistors for calibration
- **Thermistors (NTC)**: Temperature-dependent resistors
- **LDRs**: Light-dependent resistors (photoresistors)

### Capacitors

#### Ceramic Capacitors
- **Range**: 1pF to 10µF
- **Voltage**: 50V typical
- **Uses**: Decoupling, filtering, timing
- **Common values**: 0.1µF (100nF), 10nF, 1µF

#### Electrolytic Capacitors
- **Range**: 1µF to 1000µF+
- **Voltage**: 16V, 25V, 50V common
- **Polarized**: Must observe polarity!
- **Uses**: Power supply filtering, bulk storage
- **Common values**: 10µF, 100µF, 220µF, 470µF, 1000µF

#### Tantalum Capacitors
- Higher capacitance in smaller package
- More expensive
- Polarized

### Inductors

- **Range**: 1µH to 1mH
- **Uses**: Power supplies, filtering, RF circuits
- Common in DC-DC converters

### Diodes

#### Standard Diodes
- **1N4001-1N4007**: General purpose rectifier (1A, varying voltages)
- **1N5817-1N5819**: Schottky diodes, low voltage drop
- Uses: Reverse polarity protection, rectification

#### Zener Diodes
- **Common values**: 3.3V, 5.1V, 12V
- Uses: Voltage regulation, reference voltages

#### LEDs (Light Emitting Diodes)
- **Colors**: Red, green, blue, yellow, white, RGB
- **Sizes**: 3mm, 5mm, 10mm through-hole; various SMD
- **Special**: WS2812B addressable RGB LEDs
- **Forward voltage**: Red ~2V, Blue/White ~3.2V
- Always use current-limiting resistor!

### Transistors

#### BJT (Bipolar Junction Transistors)
- **NPN**: 2N3904, 2N2222 (common switching transistors)
- **PNP**: 2N3906 (complement to 2N3904)
- Uses: Switching, amplification
- Typical ratings: 200mA, 40V

#### MOSFETs
- **N-channel**: 2N7000 (small signal), IRLZ44N (logic level, high current)
- **P-channel**: FQP27P06 (high-side switching)
- Better for switching higher currents than BJTs
- Lower power dissipation

### Integrated Circuits (ICs)

#### Op-Amps
- **LM358**: Dual op-amp, general purpose
- **TL072**: Low-noise, good for audio
- **LM741**: Classic single op-amp (mostly for learning)

#### Comparators
- **LM393**: Dual comparator
- **LM339**: Quad comparator

#### Timers
- **555**: Classic timer IC, countless applications
  - Astable mode: oscillator
  - Monostable mode: one-shot timer

#### Logic ICs
- **74HC series**: CMOS logic gates
  - 74HC00: Quad NAND
  - 74HC02: Quad NOR
  - 74HC04: Hex inverter
  - 74HC08: Quad AND
  - 74HC32: Quad OR
  - 74HC74: Dual D flip-flop
  - 74HC595: Shift register (serial to parallel)

### Connectors & Headers

- **Pin headers**: 2.54mm pitch, male/female, various lengths
- **Dupont connectors**: Pre-crimped jumper wires
- **JST connectors**: 2-pin for batteries, various sizes
- **Screw terminals**: For permanent wire connections
- **Barrel jacks**: DC power input
- **USB connectors**: Type A, Micro-B, Type-C

### Switches & Buttons

- **Tactile switches**: Momentary push buttons
- **Toggle switches**: SPST, SPDT, DPDT
- **Slide switches**: For power on/off
- **DIP switches**: Multiple small switches in one package
- **Rotary encoders**: For menu navigation, volume control

### Miscellaneous

- **Buzzers**: Active (with oscillator) and passive
- **Relays**: Electromechanical switches (5V, 12V common)
- **Optocouplers**: Optical isolation between circuits
- **Crystals**: 16MHz, 32.768kHz for timing
- **Fuses**: Various ratings for overcurrent protection

---

## Power Supplies and Regulators

### Linear Regulators

#### 78xx Series (Positive Voltage)
- **7805**: 5V output, very common
- **7812**: 12V output
- **7809**: 9V output
- **7803.3**: 3.3V output
- Require ~2V headroom (dropout voltage)
- TO-220 package typically handles 1A with heatsink

#### 79xx Series (Negative Voltage)
- Negative voltage equivalents
- Less common but useful for split supplies

#### LM317 (Adjustable)
- Variable output: 1.25V to 37V
- Set with resistor divider
- Very popular for custom voltages

#### Low-Dropout (LDO) Regulators
- **LM1117**: 3.3V/5V, 800mA, low dropout (~1V)
- **AMS1117**: Similar to LM1117, very common
- **LD1117**: Alternative, good availability
- Better efficiency than 78xx series

### Switching Regulators (DC-DC Converters)

#### Buck Converters (Step-Down)
- **LM2596**: Adjustable, 3A output, very popular
- **MP1584**: Tiny module, 3A, high efficiency
- **XL4015**: 5A capable, wider input range
- More efficient than linear regulators
- Can handle higher currents

#### Boost Converters (Step-Up)
- **MT3608**: 2A, up to 28V output
- **XL6009**: Higher power version
- Useful for battery projects (3.7V → 5V/12V)

#### Buck-Boost Converters
- Can step up or down
- Output can be higher or lower than input
- More complex but very flexible

### Power Management Modules

#### USB Power Modules
- **TP4056**: Lithium battery charger, very common
- **Protection circuits**: Overcharge, over-discharge, overcurrent
- **Boost modules with battery management**: Complete power solution

#### Battery Charging
- **TP4056**: 1A LiPo/Li-ion charger
- **MCP73831**: Small SMD charger IC
- Always use protection circuits with lithium batteries!

---

## Communication Modules

### Wireless

#### WiFi
- **ESP8266/ESP32**: Built-in WiFi (covered above)
- **ESP-01**: Minimal WiFi module for adding to other projects

#### Bluetooth
- **HC-05**: Classic Bluetooth, UART interface ($5-8)
- **HC-06**: Bluetooth slave mode only ($4-6)
- **HM-10**: Bluetooth Low Energy (BLE) ($5-10)
- **ESP32**: Built-in Bluetooth and BLE

#### RF (Radio Frequency)
- **nRF24L01**: 2.4GHz transceiver, very cheap ($1-3)
  - Can create mesh networks
  - Low power
  - 100m+ range with antenna
- **HC-12**: 433MHz long-range module ($3-5)
  - UART interface
  - Up to 1km range
- **LoRa (SX1278)**: Long range, low power ($5-15)
  - Multi-kilometer range
  - Great for IoT applications

#### Infrared
- **IR LEDs and receivers**: For remote control projects ($0.50-2)
- **VS1838B**: Common IR receiver

### Wired Communication

#### UART/Serial
- **USB-to-Serial adapters**: CP2102, CH340G, FT232RL ($2-8)
- **RS485 modules**: For industrial/long-distance communication ($2-5)
- **MAX3232**: TTL to RS232 level shifter ($1-3)

#### I2C & SPI
- Built into most microcontrollers
- **Level shifters**: For 3.3V ↔ 5V communication ($1-3)
- **I2C multiplexers (TCA9548A)**: Connect multiple devices with same address ($3-6)

---

## Storage and Organization

### Where to Find Components

#### Location
- Electronics area in the workshop
- Components organized by type
- [Specific location/cabinet to be added]

#### Organization System
- **Labeled drawers/bins**: By component type
- **Resistor book**: Organized by value
- **Component cards**: Index cards showing what's available
- **Inventory list**: [Digital inventory to be added]

### Borrowing Policy

- **Members can use** components for projects
- Please **ask before taking large quantities**
- **Return unused components** in good condition
- **Replenish if you use the last** of something
- **Donations welcome!** Help keep stock levels up

### Component Storage Tips

- Keep in anti-static bags (especially ICs)
- Label everything clearly
- Store in cool, dry place
- Keep datasheets handy
- Organize by function, then value

---

## Getting Started

### For Complete Beginners

#### Recommended First Projects
1. **Blink an LED**: The "Hello World" of electronics
2. **Button input**: Read a switch, control an LED
3. **Analog reading**: Use a potentiometer, read values
4. **Temperature sensor**: DHT11/DHT22 with display
5. **Servo control**: Move a servo motor

#### Starter Kits
Consider getting:
- Arduino Uno starter kit
- Breadboard and jumper wires
- Basic component assortment
- Multimeter
- USB power supply

### Electronics Basics to Learn

#### Essential Concepts
- **Ohm's Law**: V = I × R (Voltage = Current × Resistance)
- **Power**: P = V × I (Watts = Volts × Amps)
- **Series vs Parallel**: How components connect
- **Polarity**: Important for LEDs, capacitors, diodes
- **Current limiting**: Why LEDs need resistors

#### Soldering
- See [Soldering Tools](../TOOLS/soldering-tools.md)
- Practice on scrap before your project
- Use proper ventilation
- Good solder joints are shiny and smooth

### Safety

#### General Safety
- **Don't exceed voltage ratings** of components
- **Check polarity** before powering up
- **Use current limiting** with LEDs
- **Disconnect power** before modifying circuits
- **Lithium batteries**: Use protection circuits!
- **Hot components**: Voltage regulators get hot
- **Static sensitivity**: Handle ICs carefully

#### Power Safety
- Start with low voltages (3.3V, 5V)
- Use fuses for higher current projects
- Don't connect batteries backward
- LiPo batteries can be dangerous if mishandled

---

## Resources

### Online Learning

#### Tutorials & Documentation
- **Arduino Official**: <https://www.arduino.cc/en/Tutorial/HomePage>
- **SparkFun Tutorials**: <https://learn.sparkfun.com/>
- **Adafruit Learning**: <https://learn.adafruit.com/>
- **RandomNerdTutorials**: Great ESP8266/ESP32 guides
- **Paul McWhorter**: Excellent Arduino video tutorials on YouTube

#### Datasheets
- **Alldatasheet**: <https://www.alldatasheet.com/>
- **Datasheet Archive**: <https://www.datasheetarchive.com/>
- Always read the datasheet for unfamiliar components!

#### Community
- **Arduino Forums**: <https://forum.arduino.cc/>
- **Reddit**: r/arduino, r/esp8266, r/AskElectronics
- **Stack Overflow**: Electronics section
- **EEVblog Forums**: Professional discussions

### Component References

#### Pinouts
- **Pinout.xyz**: Visual pinout diagrams for Raspberry Pi
- **Random Nerd Tutorials**: ESP8266/ESP32 pinouts

#### Calculators
- **LED resistor calculator**: Calculate current-limiting resistors
- **Voltage divider calculator**: Design voltage dividers
- **555 timer calculator**: Calculate timing components

### Shopping

#### Online Retailers
- **AliExpress/Banggood**: Cheapest, slow shipping (2-6 weeks)
- **Amazon**: Fast shipping, moderate prices
- **Adafruit**: Quality, documentation, support US maker community
- **SparkFun**: Similar to Adafruit
- **Digi-Key/Mouser**: Professional components, fast shipping
- **eBay**: Good for surplus and deals

#### Local Sources
- [Add local electronics stores if any]
- Hardware stores for basics (wire, switches)
- Salvage from old electronics!

### Tools & Equipment

Essential tools (see also [Soldering Tools](../TOOLS/soldering-tools.md) and [Multimeters](../TOOLS/multimeters.md)):
- Soldering iron and solder
- Multimeter
- Breadboards
- Jumper wires
- Wire strippers
- Helping hands / PCB holder
- Diagonal cutters
- Needle-nose pliers

### Workshop Resources

#### In the Space
- [Soldering stations](../TOOLS/soldering-tools.md)
- [Multimeters](../TOOLS/multimeters.md)
- Oscilloscope: [Location to be added]
- Power supplies: [Location to be added]
- Function generator: [Location to be added]

#### Getting Help
- Ask experienced members
- Check documentation first
- Post questions in member chat/forum
- Attend electronics workshops/classes
- [Electronics working group meeting time/place to be added]

---

## Tips and Best Practices

### Design Tips
- **Start simple**: Get basic version working first
- **Test incrementally**: Don't build everything at once
- **Use breadboard first**: Before soldering
- **Keep wires short**: Reduces noise and problems
- **Label everything**: Future you will thank you
- **Document your work**: Take photos, save code, write notes

### Troubleshooting
1. **Check power supply**: Is everything getting power?
2. **Check connections**: Breadboard connections can be loose
3. **Measure voltages**: Use multimeter to verify
4. **Check polarity**: LEDs, capacitors, ICs
5. **Simplify**: Remove components until it works
6. **Read error messages**: They usually point to the problem
7. **Search online**: Someone has probably had your exact problem

### Component Selection
- **Buy extras**: Components are cheap, your time isn't
- **Get variety packs**: Resistor/capacitor/LED kits
- **Quality matters**: Cheap sensors can be unreliable
- **Check reviews**: Especially for modules
- **Verify voltage levels**: 3.3V vs 5V compatibility

### Code Best Practices
- **Comment your code**: Explain what and why
- **Use meaningful names**: Not just "a", "b", "c"
- **Test modules separately**: Before integrating
- **Version control**: Use Git for your projects
- **Save working versions**: Before major changes
- **Use libraries**: Don't reinvent the wheel

---

## Project Ideas by Skill Level

### Beginner
- LED blinker with button control
- Temperature/humidity monitor with display
- Light-activated nightlight
- Distance measuring tool (ultrasonic)
- Simple alarm system (PIR sensor + buzzer)

### Intermediate
- Weather station (multiple sensors + display)
- WiFi-controlled LED strip (ESP8266 + WS2812B)
- Line-following robot
- MQTT home automation node
- Data logger (sensors + SD card)

### Advanced
- ESP32 camera security system
- Multi-room sensor network
- Gesture-controlled interface
- GPS tracker with mapping
- Voice-controlled home automation
- Custom PCB projects

---

## Contributing to Inventory

Help keep our electronics inventory well-stocked!

### Donations Welcome
- Surplus components from your projects
- Old electronics for salvage
- Test equipment
- Tools
- Documentation and books

### Wishlist
- [Components needed to be added]
- [Tools needed to be added]

### Organizing Events
- Component sorting parties
- Salvage workshops
- Project showcases
- Skill-sharing sessions

---

## Questions?

**Electronics coordinator**: [Contact to be added]  
**Workshop Discord/Slack**: [Channel to be added]  
**Email**: [Contact to be added]

**Remember**: Everyone started as a beginner. Don't be afraid to ask questions, experiment, and learn from mistakes. The electronics community is generally very helpful and welcoming!

Happy making! ⚡🔧
