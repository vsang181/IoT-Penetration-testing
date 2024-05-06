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
