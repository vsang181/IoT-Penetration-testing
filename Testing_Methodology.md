# Testing Methodology

## IoTA - Internet of Things Attack Methodology

The IoTA methodology was first introduced by Larry Pesce of InGuardians in a SANS Webcast. The goal of IoTA is to formalize the process of testing the security of every component of an IoT solution.

To do this, IoTA breaks IoT into five environments:

1. Hardware (including firmware, radio, Wi-Fi, and Bluetooth/BLE)
2. Web App
3. Mobile App (iOS and Android)
4. Network/Traditional pen test/Cloud (Internal/B2B and internet-facing)
5. API

For each of these, IoTA outlines how to test them to ensure full coverage of the potential attack surface of IoT devices.

### Web Services and APIs

When analyzing the security of IoT devices for potential attack vectors, the network is a good place to start. Most IoT devices are designed to collect data and perform minimal data processing before sending information on to a server for more in-depth analysis or command and control.

Additionally, most IoT devices allow users to monitor and manage their devices over the internet. This may be accomplished via web portals or through mobile apps. 

Between the IoT device, the server, and the user, several different communications channels and types of communications exist. All of these network traffic and internet-facing services creates the potential for vulnerabilities and attack vectors.

### Wi-Fi and Network

When analyzing IoT devices at the network level, there are a lot of things to look for. IoTA recommends taking the following steps:

1. Determine which devices are connected to local networks. This helps with identification of potential IoT devices.
2. Perform discovery on the network to learn about network architecture, common communication patterns, etc.
3. Look for Wi-Fi Routers and Authentication Portals. Vulnerabilities in these can be used to steal credentials, or they may be vulnerable to credential stuffing attacks.
4. Scan for device services and ports. An understanding of the services running on different devices provides clues to their purpose and may help with identifying an exploitable vulnerability.
5. If possible, perform remote exploitation. If any vulnerabilities are discovered, take advantage of them,
6. Perform active attacks on network traffic. Exploit opportunities to perform Man-in-the-Middle (MitM) attacks, intercept, and forge MQTT traffic, etc.

###  Hardware and Firmware

Analysis of a device’s hardware and firmware can help to reveal vulnerabilities. Two case studies mentioned earlier highlight classic examples of this:

- **Foscam Baby Monitor**: An attacker can easily download the memory of the device, which stores the user credentials.
- **Onity Locks**: Onity locks stored the master key on the lock and provided an interface that allowed this key to be read out and then used to unlock the door

IoT devices are typically cyber-physical systems, meaning that exploitation of digital vulnerabilities can cause real-world impacts. Also, the physical components used to build these devices can sometimes undermine their digital security.

### RF, BLE, Bluetooth, SDR, Zigbee, and Zwave

When discussing network communications for IoT devices, it is important not to focus too much on just Wi-Fi. While Wi-Fi is a commonly used wireless network protocol, it is not the only one out there.

IoT devices are commonly resource constrained, and, in many cases, the intent is for them to only be wirelessly controllable by devices nearby. Both of these factors mean that the use of more lightweight protocols like Zigbee or Bluetooth Low Energy (BLE) may be a better fit than Wi-Fi for some applications. When analyzing the security of IoT devices, be sure to check for and analyze traffic on non-Wi-Fi protocols.

## IoT Security Testing Considerations

When performing a penetration test for IoT devices, there are a few different approaches that can be taken. These include:

|Full Knowledge|Limited Knowledge|Zero Knowledge|
|---|---|---|
|In a full knowledge penetration test, the tester is given full access to the system, including documentation, credentials, etc. This provides in-depth visibility, but all this data can be overwhelming and may cause testers to focus on how a system is designed to work rather than how it actually does.|In a limited knowledge penetration test, the tester is provided with some access and information about the system. This often simulates an insider threat, where some knowledge of the environment is assumed but not at the same level as the designer or security team would have.|In a zero-knowledge assessment, the tester is provided with no information or access to the target environment. While these tests can be more difficult and time-consuming to perform, they more accurately simulate a real-world attack, meaning that they can uncover the attack vectors most likely to be exploited.|

All of these testing methodologies have their pros and cons. The “right” choice depends on the situation and the objectives of the assessment.

Penetration testing is not all about the test itself. When planning for IoT security testing, it is also important to consider the administrative components of the exercise.

**Scoping**

When planning out an assessment, accurate scoping is essential. During an engagement, it is only possible to do so much within a given period of time.

The scope of the assessment should be tailored to the environment under test. Each system will require a certain level of effort to assess, and this varies from one system to another. The depth, breadth, and duration of an assessment should be balanced to ensure that the penetration testing team can provide a full assessment of the environment at the desired level within the time available.

**Reporting**

Reporting is the most important part of any penetration testing exercise. The client is paying to learn about the vulnerabilities in their systems, not for you to have fun discovering and exploiting them. 

When generating reports, it is important to provide information for different target audiences at varying levels of detail. Reports should include everything from a high-level, non-technical executive summary to a play-by-play breakdown of the assessment for technical staff. A good report provides an organization with everything that it needs to fix its vulnerabilities from finding the funding to the actual remediation.

## Some Tools and Utilities

Like any other type of penetration testing, effective IoT security testing requires access to the right tools. IoT security testing tools can be broken up into three main categories:

- **Network/Web**: The IoTA methodology includes network-level analysis in multiple categories. Network/web testing tools include both passive reconnaissance tools (like Wireshark) and ones used to actively interact with the target environment (Burp and Postman).
  
> Wireshark - widely used network protocol analyzer. (https://www.wireshark.org/)

> Burp – software to proxy and inspect/edit web traffic (https://portswigger.net/)

> Postman – software to build and interact with APIs (https://www.postman.com/)

- **Hardware**: Firmware and hardware testing is a major part of the IoTA methodology. To effectively test the hardware and firmware on a device, testers need tools that can connect to the devices and interact with them over the protocols that they use.

> Buspirate - Troubleshooting tool supporting multiple interfaces: 1-wire, 2-wire, 3-
wire, UART, I²C, SPI, JTAG interfacing via USB

> Raspberry Pi - small single-board computers developed for multi-functions

> Logic Analyzer – 130+ protocol decoders including SPI, I2C, Modbus, UART, etc.

- **Wireless**: IoT devices get their names from the fact that they connect to the internet, typically over wireless protocols. When assessing wireless protocols, it is important to have tools capable of collecting and analyzing traffic and communicating over more than just Wi-Fi.

> Panda PAU06 – Wi-Fi testing device capable of monitor mode capture

> HackRF One – Unknown wireless protocol testing device for 1MHz to 6GHz Ranges

> CC2531 – Module for transmitting and receiving Zigbee (and others)

## Bus Pirate

> Troubleshooting tool supporting multiple interfaces
> - 1-wire, 2-wire, 3-wire, UART, I²C, SPI, JTAG interfacing
> - 0-5.5-volt tolerant pins

> Accessed over USB
> - Menu driven interface
> - AVRDUDE, flashrom support
> - Python, perl scriptable

> PIC24FJ64 processor and a FT232RL USB-to-Serial chip Community driven and supported
> - Firmware updatable, extensible
> - Many additional features!

> Includes several cabling options, DuPont wires

![41XEvIOhBaL _AC_](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/2ffe3c3e-9244-4ce8-9493-f2dd2bbf9d1d)

[Buy Link](https://www.sparkfun.com/products/12942)

The Bus Pirate is a multipurpose troubleshooting tool with the ability to interact with multiple protocols for sniffing, receiving, and transmitting. It is truly a multifunctional tool and can accept many of our common IoT device operating voltages, up to 5.5 volts.

We access the functionality of the Bus Pirate via USB and a menu driven interface, as well as direct interaction with AVRDUDE and flashrom utilities. It is also scriptable with python and perl. The PIC24FJ64 processor and USB to serial chip combination has huge community support and some developers provide additional features through the open-source nature of the device.

Connectivity to our target device is accomplished through a dedicated connector, in which several “supported” cabling options to reflect documented cable colors. In addition to the supported cables, standard DuPont wires can also be used for connectivity.

## HackRF One

> Two varieties, HackRF One readily available
> - RX and TX, Half Duplex
> - 1 MHz to 6 GHz
> - 20 MHz wide capture
> - SMA antenna connector
> - USB connectivity
> - Huge community support, education and opensource hardware
> - Includes the ANT-500 telescoping antenna

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/96a4b0f3-3ba4-46e4-9067-e10422fdb782)

[Buy Link](https://coolcomponents.co.uk/products/hackrf-one)

Currently, two models are available. All models feature the ability to do half-duplex TX and RX. The HackRF was created and developed by Michael Ossman in full support of the open-source community.

The Hack RF Jawbreaker uses USB, has a 100 MHz–6 GHz frequency range, is priced from Mr. Ossman’s Kickstarter campaign, and has an extremely limited used market. The Jawbreaker was also able to benefit from support from DARPA’s Cyber Fast Track Program, which allowed Mr. Ossman the resources to develop the device.

The Hack RF One provides some updates to the Jawbreaker concept and was released via Kickstarter at $199 for early adopters. It was slated for release in early 2014. Early beta models were available for demonstration at Shmoocon 10 in early 2014 and are now readily available from many online retailers and select brick-and-mortar locations. The HackRF One can safely tune between 1 MHz and 6 GHz.

Mike Ossman has had success with Kickstarter campaigns and designing radio devices, including the Bluetooth Ubertooth One and YARD Stick One. Mr. Ossman’s device following is due in part to his commitment to hackability and the community that uses his designs. There is huge community support and either direct support for HackRF or support for all sorts of applications via shim/additional driver support (often developed by the community). The HackRF One schematics are freely available and have been used to produce derivative works, such as the Rad1o project at the 2015 Chaos Communication Congress.

Included the ANT-500 telescoping antenna, which makes it adjustable in length and tunable to many different frequencies. Note that when adjusting the length of the ANT-500, always adjust form the bottom or base, as the top bends easily. Should the antenna bend and fail, it can render it unusable.

## PANDA USB Adapter

> PANDA PAU06 USB 802.11 b/g/n
> - Unfortunately, no a/ac support
> - Many IoT devices aren’t that robust yet!

> Ralink RT5372 Chipset
> - Supported by the Linux rt2800usb driver

> Excellent receive sensitivity

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/dda7e2e0-49bf-4798-9128-0d1e13cf964e)

[Buy Link](https://www.amazon.co.uk/Panda-300Mbps-Wireless-Adapter-Antenna/dp/B00JDVRCI0)

This USB adapter supports IEEE 802.11 b/g/n (2.4 GHz) with a 300-mW transmitter and a detachable antenna. While this device does not support 5Ghz technologies, many IoT devices are not yet supporting them either!

The PANDA card uses a Ralink RT5372 Chipset, which is supported on Linux with the rt2800usb driver.

The PANDA card has excellent receive sensitivity, which allows us to detect wireless activity even from an extended distance. It also supports wireless monitor mode packet sniffing on Linux and can be used for injecting malformed packets in monitor mode as well.

## TP-Link USB UB400 Bluetooth Adapter

> Class 2 Bluetooth adapter (10 mW) Supported on Windows and Linux Bluetooth 4.x compliant
> - Supports classic, EDR, and Bluetooth Low Energy connections
> - BLE, BTLE, Bluetooth Smart

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/c6e21194-e842-4ded-b6a8-4c5e698afe39)

[Buy Link](https://www.amazon.co.uk/gp/product/B07NDVQMY4/ref=as_li_tl?ie=UTF8&tag=tplinkwifi-21&camp=1634&creative=6738&linkCode=as2&creativeASIN=B07NDVQMY4&linkId=15cdb6e8cbae3f5c56607478976ad57b)

The TP-Link UB400 is a Class 1 Bluetooth adapter, capable of transmitting at 10 mW for an effective range of approximately 10 meters if unobstructed. It is supported on Windows and Linux, but our best tools in this class will be under Linux!

The UB-400 is Bluetooth 4.x compliant, which allows it to interact with the vast majority of deployed Bluetooth devices in use today, including Bluetooth Low Energy (BLE) devices where we will focus in this course.

## Logic Analyzer

> HiLetgo (and other brands)
> - 24Mhz, 8 channel
> - 24M/s capable, 10M/s stable
> - More than enough for most use cases!

> CY7C68013A based
> - 8051 MCU
> - Integrated USB 2.0 interface
> Support under Sigrok PulseView, Saelea Logic
> - 130+ protocol decoders!
> - SPI, I2C, Modbus, UART, and more

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/00a1f918-2b02-4e57-b8f8-a888a875f4f0)

[Buy Link](https://amzn.eu/d/bVqA5sM)

The SIPT kits also includes an affordable logic analyzer from HiLetgo (also under other brands as well), supporting 8 individual channels at 24 Mhz, using the CYT7C68013A chipset with an 8051 MCU.

While this particular logic analyzer supports up to 24M/second sample rate, a more reasonable 10M/Second sample rate is typically more stable. This stable sample rate, is typically more than enough for our desired use cases, such as sniffing SPI, I2C, UART serial and more.

This logic analyzer is supported under PulseView and Saelea Logic software, which can interpret the data that we sniff. Both sets of software feature hundreds of protocol decoders, turning our observed samples into something human readable.

We can also use our Bus Pirate cables with the logic analyzer but will largely rely on our color-coded DuPont wires for connectivity.

## CC2531 (x2)

> Zigbee (and BLE) development kit

> Pre-flashed with Bumblebee firmware
> - No flash over USB
> - Requires cc-tool, ccDebugger hardware

> Killerbee TX, RX and sniff support

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/d39e20f9-ef0d-40f6-9c4f-67b890657bb3)

[Buy Link](https://www.cncgeeker.com/index.php?main_page=product_info&products_id=51)

The CC2532 is a Zigbee development “kit”, that can also support Bluetooth Low Energy and 802.15.4 (with the possibility for Thread support in the future). Texas Instruments supports development in C and flashing with the ccDebugger hardware. With no ability to flash new firmware over USB, this means there is the need for additional hardware investments. The additional cost is lousy for the limited need to reprogram. Fortunately, the ccDebugger hardware is inexpensive and open-source tools for flashing, such as cc-tool are available.

In the SIPT kit, we have already flashed a pair of CC2531 modules with an appropriate version of the Bumblebee firmware. The use of the Bumblebee firmware makes them compatible with the Killerbee suite of tools For Zigbee transmit, receive and even sniffing!

## Raspberry Pi

> Raspberry Pi 4 with useful accessories

> Not all assessments can be performed with virtualized hardware

> Capability for assessment tools using built in GPIO, Wiring Pi libraries

> Emulation of various attack targets

> Customized Raspbian image (PioT) to support tools needed for this class

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/6419dfc3-ffd1-4afa-a93d-ef9b64972136)

[Buy Link](https://shop.pimoroni.com/products/raspberry-pi-5?variant=41044580171859)

In your SIPT Kit, you will receive A Raspberry Pi 4 kit featuring several useful accessories.

Unfortunately, some of the tools that we will explore during this class do not perform well, or at all, under a virtualized operating system, largely due to the introduction of USB timing issues under virtualization. With the inclusion of the PioT platform, this allows for us to develop Bluetooth Low Energy applications, providing you with appropriate attack targets. Additionally, the PioT platform allows for you to have an attack platform and additional options for hardware hacking to use during class, as well as when you return to the office.

The included microSD card has been pre-programmed with a custom Raspbian image, dubbed PioT, to include all of the tools that you will need for the appropriate exercises. The login to the customized Raspbian image can be found in the Workbook.

You won’t need to use PioT right away, but it is recommended to assemble the case, apply heat syncs, and insert the microSD card early on.

.
.
.
.
.
.
_In progress..._

## Let's Connect

I welcome your insights, feedback, and opportunities for collaboration. Together, we can make the digital world safer, one challenge at a time.

- **LinkedIn**: (https://www.linkedin.com/in/aashwadhaama/)

I look forward to connecting with fellow cybersecurity enthusiasts and professionals to share knowledge and work together towards a more secure digital environment.
