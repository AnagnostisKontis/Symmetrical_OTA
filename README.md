
# 1.8V Non Inverting CMOS Symmetrical OTA

A complete transistor-level CMOS Symmetrical OTA design. The circuit receives a weak 1kHz sine with 1mV Amplitude, amplifies it with 54dB open loop gain (500mV Amplitude) or 22.7dB negative feedback gain (1kΩ/100kΩ resistor Pair). A NMOS Current Mirror provides the circuit with 16μΑ. 3 additional Current Mirrors are used (2 PMOS 1 NMOS), to convert the circuit to a signle-output amplifier and to bias the output NMOS Transistor. The circuit achieves consumption < 100μJ. The circuit is also tested and evaluated under different temperatures. 

All simulations and validations were performed in **LTspice**.

## Key Specifications

| Parameter | Value / Description |
| :--- | :--- |
| **Technology** | Generic NMOS Vth= 0.5V Kp=200u Lambda=0.02 (W/L) = (4u/1u), Generic NMOS Vth= 0.5V Kp=200u Lambda=0.02 (W/L) = (2u/1u), Generic PMOS Vth=-0.5V Kp=100u Lambda=0.02 (W/L) = (4u/1u)|
| **Supply Voltage (VDD)** | 1.8V |
| **Virtual Ground / DC Bias** | 0V |
| **Input Signal Amplitude** | 1mV |
| **Carrier Frequency** | 1kHz |
| **Current** | 16μΑ |
| **Reference Resistor** | 68kΩ |
| **Negative Feedback Pair Resistors** | 1kΩ/100kΩ |
| **Load Capacitor** | 1pF |
| **Bandwidth** | 0 - 2 MHz (Negative Feedback) 0 - 55.7 kHz (open loop)|
| **Midband Gain** | 54dB (open loop), 22.7 (negative feedback)|

## Transistor W/L Reference Table
| Name |Type | W/L |
| :--- | :--- | :--- |
|**Min1**| NMOS | 2u/1u |
|**Min2**| NMOS | 2u/1u |
|**Mnref**| NMOS | 4u/1u |
|**Mntail**| NMOS | 4u/1u |
|**Mpin1**| PMOS | 4u/1u |
|**Mpin2**| PMOS | 4u/1u |
|**Mpout1**| PMOS | 4u/1u |
|**Mpout2**| PMOS | 4u/1u |
|**Mnmirror1**| NMOS | 2u/1u |
|**Mnmirror2**| NMOS | 2u/1u |



## Schematics & Simulation Results

### Schematic

![System Schematic](images/Symmetrical_OTA.png)

### Transient Analysis
The system was evaluated with the use of a weak 1mV input signal to verify the circuit's gain.

### Open Loop 
![Waveforms](images/Symmetrical_OTA_tran_open_loop.png)

- **Green Trace:** Amplified Output Signal

### Negative Feedback (at different temperatures)
![Waveforms](images/Symmetrical_OTA_tran_feedback_temperature.png)

- **Green Trace:** Amplified Output Signal at -40C
- **Blue Trace:** Amplified Output Signal at 25C
- **Red Trace:** Amplified Output Signal at 85C
- **Light Blue Trace:** Amplified Output Signal at 125C

### AC Analysis

### Open Loop (at different temperatures)
![Waveforms](images/Symmetrical_OTA_open_loop_AC_Analysis_temperature.png)

- **Green Trace:** Gain at -40C
- **Blue Trace:** Gain at 25C
- **Red Trace:** Gain at 85C
- **Light Blue Trace:** Gain at 125C
  
### Negative Feedback (at different temperatures)
![Waveforms](images/Symmetrical_OTA_feedback_AC_Analysis_Temperature.png)

- **Green Trace:** Gain at -40C
- **Blue Trace:** Gain at 25C
- **Red Trace:** Gain at 85C
- **Light Blue Trace:** Gain at 125C

### Open Loop Gain As a function of temperature
![Waveforms](images/Symmetrical_OTA_gain_temperature_open_loop.png)

### Negative Feedback Gain As a function of temperature
![Waveforms](images/Symmetrical_OTA_gain_temperature_feedback.png)

### Consumption
![Waveforms](images/Symmetrical_OTA_consumption.png)


---
