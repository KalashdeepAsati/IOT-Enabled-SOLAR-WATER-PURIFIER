<br />
<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3105/3105807.png" alt="Logo" width="80" height="80">

  <h3 align="center">IoT-Enabled Solar-Powered Water Purification System</h3>

  <p align="center">
    Verifiable clean water, powered by the sun. Built for decentralized rural communities.
    <br />
    <br />
    <a href="#about-the-project"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="#system-architecture">View Architecture</a>
    ·
    <a href="#getting-started">Installation</a>
    ·
    <a href="#performance-data">Performance Data</a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Embedded_C-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="Embedded C" />
    <img src="https://img.shields.io/badge/Arduino_Nano-00979D?style=for-the-badge&logo=Arduino&logoColor=white" alt="Arduino Nano" />
    <img src="https://img.shields.io/badge/ESP8266-000000?style=for-the-badge&logo=espressif&logoColor=white" alt="ESP8266" />
    <img src="https://img.shields.io/badge/ThingSpeak_API-blue?style=for-the-badge" alt="ThingSpeak" />
    <img src="https://img.shields.io/badge/I2C_|_UART_|_TCP/IP-lightgrey?style=for-the-badge" alt="Protocols" />
    <img src="https://img.shields.io/badge/Solar_|_Li--Po_Powered-FFB900?style=for-the-badge" alt="Power" />
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#key-features--technical-specs">Key Features & Technical Specs</a></li>
    <li><a href="#tech-stack--hardware">Tech Stack & Hardware</a></li>
    <li><a href="#system-architecture">System Architecture</a></li>
    <li><a href="#performance-data">Performance Data</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
  </ol>
</details>

## 📖 About The Project

[cite_start]Access to clean and safe drinking water remains a significant global challenge, with the "silent crisis" of water contamination disproportionately affecting rural populations[cite: 54, 56, 57]. [cite_start]In rural Madhya Pradesh, nearly 36.7% of drinking water samples were found not potable, often harboring dangerous levels of invisible dissolved minerals and microbiological pathogens[cite: 86, 92]. [cite_start]Because communities heavily rely on visual judgment—assuming clear water is safe—they remain unaware of these hidden threats[cite: 63, 64]. 

[cite_start]This project delivers an autonomous, decentralized water purification unit designed to shift the paradigm from reactive assumptions to proactive health management[cite: 88]. [cite_start]By combining advanced sequential filtration with an Internet of Things (IoT) monitoring framework, the system provides an unambiguous digital readout of water quality, ensuring "verifiable safety" in regions without access to laboratory testing[cite: 62, 93, 94]. 

## ✨ Key Features & Technical Specs

* [cite_start]**☀️ 100% Off-Grid Energy Harvesting:** The system is powered by a 12V 25W polycrystalline solar panel operating with a solar-priority model[cite: 202]. [cite_start]In regions like Sehore, it generates approximately 110 Wh daily, ensuring sustained power for the 15W operational load[cite: 200, 204]. [cite_start]Energy is buffered by a high-density 12V 7AH Lithium Polymer (Li-Po) battery, which offers an 85% depth-of-discharge and maintains an energy buffer sufficient for three days of autonomous operation[cite: 201, 293].
* [cite_start]**💧 Sequential Filtration & Total Dynamic Head (TDH):** A 24V DC booster pump generates a calculated TDH of 4.0 meters (accounting for 2.5m vertical lift and 1.5m frictional losses) to drive water through the filters[cite: 195, 197]. [cite_start]The sequence deliberately routes water through a Granular Activated Carbon filter first (for odor/chemical adsorption), followed by a 5-micron PP sediment filter to protect the downstream UV-C quartz sleeve from particulate fouling[cite: 187, 416, 417].
* [cite_start]**🦠 11W UV-C Germicidal Sterilization:** An 11W UV-C module destroys the genetic core (DNA/RNA) of microbial cells, providing 100% pathogen inactivation[cite: 157]. [cite_start]Firmware logic dynamically controls pump flow to guarantee adequate UV exposure time[cite: 393]. 
* [cite_start]**🔋 Nutritional Restoration:** The system features a specialized Mineral Remineralization Cartridge that bridges the "demineralization gap" by reintroducing essential calcium and magnesium ions into the purified water[cite: 160, 161].
* [cite_start]**📡 Real-Time IoT Telemetry & Alert Logic:** An Arduino Nano continuously polls a Gravity TDS probe and an optical IR turbidity sensor[cite: 189]. [cite_start]Utilizing median filtering algorithms and temperature compensation to strip signal noise, the system displays data locally on a 16x2 I2C LCD[cite: 370, 371]. [cite_start]An ESP8266 simultaneously pushes HTTP-GET requests to a private ThingSpeak cloud dashboard for remote municipal monitoring[cite: 390, 391].
* [cite_start]**🌡️ Thermal Insulation Housing:** The entire system is enclosed in a custom 2x1x1 feet red plywood cabinet[cite: 183]. [cite_start]Plywood was explicitly selected over standard plastics for its superior thermal insulation, which keeps the internal ambient temperature below 45°C, protecting the Li-Po battery and logic components from thermal runaway[cite: 164, 410, 412].

## 🛠️ Tech Stack & Hardware

**Languages, Firmware & Libraries**
* **Embedded C**
* **Arduino-IDE**
* **Libraries:** `GravityTDS.h`, `LiquidCrystal.h`, `LiquidCrystal_I2C`, `SoftwareSerial.h`

**Microcontrollers & Core Electronics**
* **Arduino-Nano**
* **ESP8266**
* **PCF8574-I2C-Expander**
* **Optoisolated-Relays**
* **Buck-Converters**

**Cloud Services, APIs & Protocols**
* **ThinkSpeak**
* **ThingSpeak-Write-API**
* **Protocols:** **TCP/IP**, **HTTP-GET**, **I2C**, **UART**

**Sensors & User Interface**
* **Gravity-TDS-Probe**
* **16×2-I2C-LCD-Display**
* **5V-Buzzer**

**Energy & Power Systems**
* **12V-25W-Polycrystalline-Solar-Panel**
* **12V-7AH-Li-Po-Battery**
* **Solar-Charge-Controller**

**Purification & Hydraulics**
* **24V-DC-Booster-Pump**
* **Granular-Activated-Carbon-Filter**
* **5-Micron-PP-Sediment-Filter**
* **Mineral-Remineralization-Cartridge**
* **11W-UV-C-Sterilizer**

## 🧠 System Architecture

[cite_start]The architecture is divided into three synchronized layers: Energy, Purification, and Monitoring[cite: 185]. 

<p align="center">
  <img src="assets/System Architecture of Smart Water Purification System with IoT-Based Monitoring and Control.png" alt="System Architecture Diagram" width="800">
</p>

## 📊 Performance Data

[cite_start]Field testing in the Sehore district validated the system's operational efficacy against World Health Organization (WHO) Guidelines[cite: 282, 421]. 

* [cite_start]**Chemical Purification:** Raw groundwater exhibiting hazardous concentrations of 550 ppm was successfully reduced to a highly potable 120 ppm, representing a 78.1% reduction in dissolved solids[cite: 313, 315, 431, 432].
* [cite_start]**Physical Clarity:** Turbidity testing confirmed a 97.44% reduction[cite: 50]. [cite_start]Post-treatment levels stabilized below 2.5 NTU, completely preventing "shadowing" effects during the final UV-C sterilization stage[cite: 321, 328, 425].
* [cite_start]**Energy Stability:** Field telemetry confirmed the Li-Po battery voltage remained stable between 12.5V and 13.13V under operational loads, with the solar panel tracking peak inputs of 12.71V during standard sun hours[cite: 283, 294, 300]. [cite_start]The charging logic securely maintains the state of charge within the safe 11.1V to 12.9V operating threshold[cite: 291].

### Water Quality Dashboards
<p align="center">
  <img src="assets/Total Dissolved Solids (TDS) reduction curve showing the transition from contaminated (550 ppm) to potable (120 ppm) water.jpg" alt="TDS Chart" width="48%">
  &nbsp;
  <img src="assets/Water turbidity (NTU) measurement trend post-treatment on the ThingSpeak dashboard..jpg" alt="Turbidity Chart" width="48%">
</p>

### Energy Harvesting & System Status Dashboards
<p align="center">
  <img src="assets/12V 25W Solar Panel output voltage trend during the energy.jpg" alt="Solar Voltage" width="32%">
  <img src="assets/Real-time monitoring of 12V Lithium Polymer (Li-Po) battery voltage via the ThingSpeak IoT platform..jpg" alt="Battery Voltage" width="32%">
  <img src="assets/Visual system status indicator for active battery charging on the user dashboard..jpg" alt="Charging Status" width="32%">
</p>

## 🚀 Getting Started

To replicate this project, follow these hardware and software setup steps.

### Hardware Assembly
> **Warning:** Follow the hydraulic plumbing sequence exactly (`Pump -> Carbon -> Sediment -> Mineral -> UV-C`) to protect the fragile quartz sleeve from particulate fouling. Ensure the optoisolated relays are properly wired between the 24V pump and the 5V logic circuit to prevent back-EMF from causing microcontroller brown-outs.

### Installation
1. Clone the repository.
   ```sh
   git clone [https://github.com/yourusername/solar-iot-purifier.git](https://github.com/yourusername/solar-iot-purifier.git)
2. Open the primary firmware file in the Arduino IDE.

3. Install the required libraries via the Library Manager (GravityTDS, LiquidCrystal_I2C).

4. Enter your private ThingSpeak API Key in the source code:
   C++
   String apiKey = "YOUR_API_KEY_HERE";
   Compile and flash the code to the Arduino Nano (ATmega328P).

5. Configure your ThingSpeak dashboard to receive 4 telemetry fields: Battery Voltage, Solar Voltage, TDS, and Turbidity.

<div align="center">
<i>"Transforming passive utilities into active, data-driven resources for smart villages."</i>
</div>
