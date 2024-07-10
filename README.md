# Mawaquit: 

## Introduction

The prayer control panel is an important tool in mosques to inform worshipers about prayer times. It plays a key role in organizing the spiritual life of Muslims by effectively communicating prayer times and other important information. Therefore, it is crucial for the panel to be accurate and reliable. However, a recurring problem is the imprecision of the displayed time, which can vary from 2 to 3 minutes compared to the actual time. This discrepancy can cause disruptions for worshipers who rely on the panel's display to organize their time. As an engineer specializing in embedded systems and digital services, we have undertaken to solve this problem by creating a real-time prayer control panel.

The choice of hardware components for an embedded system is crucial to ensure system performance, reliability, and stability. Particularly for a project like the prayer control panel, display accuracy and communication reliability are key factors in ensuring that worshipers receive information accurately and timely.

The prayer control panel project requires solving several challenges such as:
- Choosing appropriate hardware components to ensure display accuracy and communication reliability.
- It is also important to collect accurate data and filter it correctly to avoid errors in the display.
- Finally, precise configuration of the digits to be displayed on the LED screens must be taken into account to ensure that worshipers receive accurate and timely information.

## ESP32 Overview

The ESP32 is a low-power, cost-effective microcontroller manufactured by the Chinese company Espressif Systems. It is designed to be used in a wide variety of applications such as the Internet of Things (IoT), embedded systems, industrial control applications, sensors, wireless communication devices, etc.

## MAX7219 Overview

The MAX7219 has several advantages:
- It allows control of multiple LEDs in series with a single integrated circuit.
- It supports multiple display modes, including digits, letters, and custom symbols.
- It allows control of LED display brightness and selection of the number of columns to be displayed.
- It is easy to program with a simple serial interface.
- It can be used with different types of LED displays, such as seven-segment displays and LED matrices.
- It offers low power consumption thanks to its standby mode.

## Transmission Format of MAX7219

The MAX7219 utilizes a 16-bit transmission format from D0 to D15 represented in the table below:

- The first eight bits from D0 to D7 represent data (data). D0 being the least significant bit (LSB) and D7 the most significant bit (MSB).
- The next four bits from D8 to D11 are used for addresses (register).
- The remaining four bits from D12 to D15, however, remain unused.

## Data Retrieval and Filtering

After connecting the ESP32 to the WIFI network, access to the HABOUS prayer times website allows us to retrieve the necessary data. This data retrieval is facilitated by a data filter function implemented in our code.

## MAX7219 Connection and Control

Next, we cascade the 3 MAX7219 in series to control the display of the 6 prayers, translating into 24 7SEG digits. Each MAX7210 controls 8 digits since it operates with 16 bits.

<p>
  <img src="https://github.com/Nouhaila-Akhziz/MAWAQIT/assets/114859285/d36c85eb-d1ec-4215-81e4-d69bb363d26c, alt="Capture d'écran 2024-07-10 133036",width="20"></p>



## Prayer Display Sequence

The prayer times are displayed sequentially, starting with AL FAJR and CHOROK, followed by ADOHR and AL ASR, and finally AL MAGHRIB and AL ICHAA.

## Protocol Used

The SPI (Serial Peripheral Interface) is a data communication protocol used to connect external devices to a microcontroller. We used it between the microcontroller and the MAX7219 to control the LED displays effectively.


##Rapport

[MAWAQUIT.pdf](https://github.com/aminal22/Mawaquit/files/14984303/MAWAQUIT.pdf)
