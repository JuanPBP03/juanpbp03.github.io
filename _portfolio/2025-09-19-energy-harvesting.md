---
title: Energy Harvesting IOT Development Board
date: 2025-09-19
tags:
  - firmware
  - embedded systems
  - electronics
  - CAD
  - hardware design
  - IoT
  - nRF52
  - BLE
  - PCB design
  - USB-C
  - energy harvesting
  - wireless protocols
  - Zigbee
  - Thread
  - low power design
header:
  image: /assets/images/portfolio/pcbnrf/PCB2.PNG
  teaser: /assets/images/portfolio/pcbnrf/PCB.PNG
published: true
excerpt: "A custom prototyping board for low energy/energy harvesting, wireless/IOT devices based on the nRF52820 microcontroller and BQ25505 IC."
---

# Introduction

This project is a custom prototyping board designed for low-energy, energy-harvesting wireless IoT applications. At its core, it combines the Nordic nRF52820 microcontroller with the Texas Instruments BQ25505 energy harvesting IC, creating a platform that can stay operational even in energy-limited environments. 

# Features

This design features ultra low-power energy harvesting and battery charging thanks to the BQ25505. Using the screw-terminal, the user can connect a low impedence energy harvesting device such as a photovoltaic (PV) cell, thermoelectric generator, or piezoelectric energy source. In its current state, the hardware is configured to most optimally support PV cells, however in future versions it may be possible to change the configuration using jumpers to optimize it for a different application. It is also possible to power the device and charge the battery using the USB-C port.

The 64MHz nRF52820 offers a variety of communication interfaces and peripherals for programming your application, and even includes 2.4GHz wireless communication using the on-board PCB antenna for  data rates up to 2Mbps. Features include:

- Bluetooth mesh/BLE
- Full-speed(12Mbps) USB 2.0
- Zigbee
- Thread
- 2x I2C master/slave
- 2x SPI master/slave
- UART
- 128-bit AES Encryption Co-processor
- Quadrature Decoding

Along with many other interesting features which can be seen in detail [here](https://docs.nordicsemi.com/bundle/ps_nrf52820/page/keyfeatures_html5.html). For external I/O the board exposes the 15 remaining digital pins of the nRF52820, 4 of which can be configured for analog input.

# Hardware Design
{% include figure popup=true image_path="/assets/images/portfolio/pcbnrf/nRF52820 Energy harvesting boar.png" caption="System Block Diagram" %}

The design goal for this device was to operate indefinitely in energy limited environments, even using only ambient energy like indoor lighting to get the power it needs. 

This being the case, I aimed to strike a balance between cost-effectiveness, features, and efficiency when selecting components for this project.   

I initially considered using an ESP32-C3 given their availability, extensive support, and ease of use. However, with transmissions drawing up to 335mA, it became clear that it wasnt up for the challenge. After a bit of research I remembered a recent [video I had seen](https://youtu.be/TGbtzlWb-Kc?si=AeI3lu0n20ohvCK3) about Nordic microcontrollers and their incredible energy efficiency. [Another video](https://youtu.be/vrcPGeYinVQ?t=708) showcasing someone achieving barely 600 MICRO amps of (average) current draw even with intermittent RF activity made the decision a no-brainer.

{% include figure popup=true image_path="/assets/images/portfolio/pcbnrf/SCH_Schematic 1_1-Main Board_2025-09-19.png" alt="electrical schematic" caption="Board Schematic" %}

I chose nRF52 over the newer nRF54 due to their availability and slight price advantage. Among the nRF52 series, the nRF52820 offers a great featureset including the USB interface, improved power management, and more memory than lower tiers, at a lower price than the higher tiers.

I followed the same philosophy to choose the BQ25505 and BQ24073. Each one is a highly efficient tool for the job 

For the form factor, the pin headers are spaced to fit across a standard breadboard, similar to a Raspberry Pi Pico. This makes it easy to prototype circuits and quickly test external sensors or modules.

This is my **first PCB design**, and I threw myself into the deep end with RF. The design isn’t perfect, but every iteration has been a valuable learning step.

<figure class="online_3d_viewer"
    style="width: $max-width; height: 400px;"
    model="{{ '/assets/models/nrf.glb' | relative_url }}"
    backgroundcolor="37, 42, 52"
    environmentmap="{{ '/assets/js/o3dv/envmaps/citadella/posx.jpg' | relative_url }},
                    {{ '/assets/js/o3dv/envmaps/citadella/negx.jpg' | relative_url }},
                    {{ '/assets/js/o3dv/envmaps/citadella/posy.jpg' | relative_url }},
                    {{ '/assets/js/o3dv/envmaps/citadella/negx.jpg' | relative_url }},
                    {{ '/assets/js/o3dv/envmaps/citadella/posz.jpg' | relative_url }},
                    {{ '/assets/js/o3dv/envmaps/citadella/negx.jpg' | relative_url }}">
   
</figure>

**I'm 3D!**
{: .text-center}
{: .notice--primary }

# Firmware

By default, the board must be programmed over the Serial Wire Debug (SWD) interface. For convenience, my first goal for firmware development is to implement a custom bootloader that will allow me to flash programs over USB.

# Future Plans

Some of the improvements I’d like to explore:

- **Selectable configuration** for non-PV sources (thermoelectric, piezoelectric)
- **Optimizing RF** performance for maximum efficiency
- **Field-testing** with real-world IoT use cases (e.g., indoor environmental sensing)

# Closing Thoughts

This project represents both a challenge and a milestone for me. Taking on RF and energy harvesting on my first PCB has been ambitious, but rewarding. While the design has plenty of room for improvement, it already demonstrates the viability of **energy-harvesting IoT hardware** built from affordable, widely available components. Most importantly, it reflects the intersection of two of my core interests: **embedded systems and sustainable energy**, areas I’m excited to keep pushing further.



<script src="{{ '/assets/js/o3dv/o3dv.min.js' | relative_url }}"></script>

<script>
  
OV.Init3DViewerElements (); // init all viewers on the page

</script>


