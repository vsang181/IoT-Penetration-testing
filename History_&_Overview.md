# History and Overview

![image](https://github.com/vsang181/IoT-Penetration-testing/assets/28651683/1e789f98-519d-428f-8aa6-bed77da76bae)

The number of internet-connected devices has grown exponentially over the past few decades. In the early days of the internet, most internet-connected machines were desktop computers. Over time, laptops, mobile phones, and Internet of Things (IoT) devices were connected to the internet as well.

In the modern internet, IoT devices make up a growing percentage of internet-connected devices. Virtual assistants are built into almost everything these days, and most technology has the option to be remotely monitored and controlled over the web or from a smartphone app.

With the rise of 5G, the IoT is only expected to grow larger. 5G enables devices to achieve higher data speeds over mobile networks, and these networks can support more densely packed devices than previous iterations of mobile networks. This makes 5G ideal for providing reliable, high-performance internet connectivity for IoT devices.

## Classes of IoT Applications

|IoT Class|Implementation Examples|
|---|---|
|CONSUMER IoT|Home Lighting, Appliances, Voice Assistants, Wall Outlets, Wearables|
|COMMERCIAL IoT |Healthcare and Transport industries, and Monitoring systems|
|INDUSTRIAL IoT |Digital Control Systems, Smart Agriculture, Statistical Evaluations|
|INFRASTRUCTURE IoT|Smart Cities via Sensors, Management Systems, and interconnectivity|
|MILITARY IoT |Surveillance robots and drones, human wearable biometrics, and combat|

The IoT is not growing simply because consumers want to be able to remotely control their lightbulbs and coffeepots from their smartphones. IoT devices have permeated every part of modern life. Some of the main classes of IoT applications include:

- **Consumer IoT**: Consumer IoT devices are designed to make life easier by making everything more accessible and centrally controllable. In addition to their common use at home, these devices are often deployed in offices as well.

- **Commercial IoT**: IoT devices are ideally suited to performing monitoring and providing frequent updates to a centralized command and control center. This can be invaluable for tracking good in the shipping industry or monitoring patient status for healthcare providers.

- **Industrial IoT**: The use of computers to manage industrial machinery is nothing new, but these devices are increasingly being connected to the internet. This makes it possible to monitor and manage them from a centralized location, increasing efficiency and streamlining operations.

- **Infrastructure IoT**: In recent years, many local governments have been pursuing the concept of smart cities. These cities would use the monitoring and management capabilities of IoT to optimize infrastructure across the entire city.

- **Military IoT**: IoT devices can support an array of different sensors, making them well suited to supporting military operations. Whether autonomous vehicles or biometric enhancements for soldiers, IoT devices can make military operations more effective.

## Shortcomings of IoT - Non-Security

IoT devices are convenient, but they also have their limitations. While many of the most referenced issues with IoT devices are security related, IoT devices also have a number of non-security shortcomings, including:

- **Ease of Use**: Many IoT devices have a number of different features and complex functionality. Often, the process for setting up these devices and unlocking this functionality is complex and poorly documented, making the systems hard to use.

- **Production and Consumer Costs**: The IoT part of many devices is an add-on to the core functionality of the device. This means that smart devices are often much more expensive than the non-smart alternatives.

- **Customer Support**: For most IoT devices, the documentation is sparse and poorly written, and no help desk support is available. Many issues are only solvable by looking on forums for other users that had and solved the same problem.

- **Processing Cycles**: IoT devices are often designed for planned obsolescence with short lifecycles. Instead of maintaining and updating past versions of devices, manufacturers try to sell consumers on upgrades to the latest versions.

- **Interconnectivity and Standards**: IoT devices are made by a variety of different manufacturers, often in competition with one another. This means that these devices often have interconnectivity issues, making it impossible to use devices from a range of vendors in a fully integrated system.

- **Open-Source vs. Closed-Source**: The level of transparency and documentation about IoT device functionality varies greatly. This can make it difficult to write third-party code to interact with IoT devices’ APIs.

## Shortcomings of IoT - Security Related

IoT devices have a number of different security-related shortcomings. Some of the major ones include:

- **Poor Development Practices**: Many IoT developers are not professional computer and software vendors. This means that they often don’t follow secure development best practices, resulting in large numbers of exploitable vulnerabilities in their systems.

- **Difficulty in Upgrading Software/Firmware**: Few IoT device owners remember to check if their coffeepot or lightbulb needs a software update, and the update process is commonly time-consuming and complex. As a result, these devices commonly contain unpatched vulnerabilities.

- **Consumer Awareness**: Many IoT devices are marketed to the average consumer, who is not a security expert. This means that these devices are commonly deployed and used in ways that violate security best practices.

- **Systemic Impact and Scale**: Most IoT devices use similar protocols, code samples, and development practices. This means that an error in shared code or a faulty protocol can impact devices across many different vendors.

- **Complexity in Testing**: Security testing for IoT devices is often non-existent or focuses on simple, high-level attack scenarios. As a result, real-world use cases or attack scenarios go untested, leaving devices potentially vulnerable.

- **Reliance on Other Control Layers**: IoT device vendors commonly assume that their devices will be deployed in an environment with certain security controls in place, such as a firewall. These misguided assumptions mean that these devices are more vulnerable to exploitation.

## Common Security Issues for Each Layer of IoT

IoT devices are multi-layered systems. At each layer, IoT devices can suffer from a few different security issues.

|Layer|Component|Function|Security Issue|
|---|---|---|---|
|Device Sensors|Smart sensors, actuators, RFID tags|Data sensing, data acquisition|Authentication, authorization, access control, and data integrity|
|Network|Wired, wireless networks, big data repositories|Data aggregation, QoS scheduling, transmission|Modification of routing path, or sniffing of information|
|Service Component|Middle-ware technology|Analysis and processing of data|Service authentication and data confidentiality|
|Application|Smart home, smart city, portals, mobile applications|Determines message passing protocols|Weak or vulnerable code, lack of strong access controls or encryption|
|User Interface|User|Export services to the end-users|Awareness and accountability|

- **Device Sensors**: The device sensors are used for monitoring and data acquisition. These include smart sensors, actuators, and RFID tags. With sensors, the main security threats arise around controlling access to the data. An IoT device much authenticate users, determine their level of authorization, and appropriately control access to the data collected and stored by the device.

- **Network**: IoT devices are designed to send data over the network to on-prem or cloud-based servers. These servers will perform data processing and send instructions to the devices.  At the network level, the main security concern is that an unauthorized party gains access to or control over the communications. Rerouting traffic could cause performance issues or allow an attacker to sniff the traffic and extract valuable, unprotected data. 

- **Service Component**: Service components include middleware technologies. Their role is to analyze and process data collected by IoT devices.  When sending data to an external service component, data security is a primary concern. If the service is not properly authenticated or data is not protected, sensitive data could be exposed to an unauthorized party.

- **Application**: At the application layer, the message passing protocols are determined. Examples of this layer include smart homes and cities, portals, and mobile applications. Whenever data is in transit or accessible to a third party, it needs to be properly protected. A failure to properly encrypt data and weak authentication and access controls are common issues at this layer.

- **User Interface**: IoT devices are designed to be accessible to the user. This means that the user may have access to sensitive data or the ability to control the actions of the IoT device. When interacting with users, awareness and accountability are key. This ensures that access to data and control over functionality are limited to what is necessary and activities are appropriately tracked.

## Malicious IoT Use – Real World Examples

IoT devices are commonly used for high-trust applications. However, their numerous security issues mean that they create significant security risks. Some examples of the malicious use of IoT devices include:

|Malicious IoT use|Example|
|---|---|
|Theft and Burglary|Onity – Hotel Card to Break into Rooms|
|Denial of Service Attacks|The Mirai Botnet (aka Dyn Attack)|
|Remote Control of Healthcare Systems|Hackable Cardiac Devices from St. Jude|
|Personal Privacy Breach|TRENDnet and Foscam Webcam Hacks|
|Remote Control of Connected Cars|The Jeep Hack|

- **Theft and Burglary**: Onity manufactures keycard locks like those used in hotels. The encryption key used as the master key for these devices was stored in the lock itself, enabling an attacker to extract and use it to unlock hotel room doors.

- **Denial of Service Attacks**: Mirai was a botnet composed of many compromised IoT devices. One of the most famous Mirai attacks targeted Dyn, a DNS provider. This attack made many major websites unreachable because visitors couldn’t look up the IP addresses of the sites.

- **Remote Control of Healthcare Systems**: IoT devices are increasingly used in healthcare applications. In 2017, pacemakers created by St Jude Medical were reported to have authentication vulnerabilities that allowed an attacker to remotely control the devices.

- **Personal Privacy Breach**: IoT devices commonly collect and process sensitive personal information. Hacks of internet-connected cameras can allow unauthorized users to view live video streams.

- **Remote Control of Connected Cars**: Cars are increasingly connected to the internet for software updates and other remote-control functionality. A 2015 proof of concept demonstrated that an attacker could remotely gain complete control of a Jeep Cherokee.

