## Wireless Notes

#### Introduction
- Wireless started out as a way of sending audio programs through the air we called it ______ (Radio)
- Then it was used to transmit pictures we called it _ (Television)
- Wireless will struggle to offer us the same robustness as a wired network can They do offer:
  - Mobility
  - Installation speed and simplicity
  - Felxibility - they can allow access to places
  - Cost
  - Security (recently)
  - Convienence
  - Scalability

#### You can create two types of wireless networks
1. Ad hoc mode wireless network
  - Wireless devices are connected directly to other wireless devices
  - Peer-to-peer 
  - No need for an access point
  - Dont need to purchase access point
  - Example: users sharing data or playing a LAN game together
2. Infrasturcture mode wireless network
  - Wireless clients are connected to a central wireless access point
  - Wireless client sends data to the access point which then sends data on to the wired network
  - Can control who can connect to wireless network
  
#### Devices
##### Access point
- Connects wireless devices together and allows them to communicate with each other
- A device that creates a wireless local area network, or WLAN, usually in an office or large building.
- An access point connects to a wired router, switch, or hub via an Ethernet cable, and projects a Wi-Fi signal to a designated area.
  - EX: For example, if you want to enable Wi-Fi access in your company's reception area but don’t have a router within range, you can install an access point near the front desk and run an Ethernet cable through the ceiling back to the server room.
- Have at least 1 antenna and a port to connect them to a wired network
- There are the standalone AP’s and also ones that include a built-in router which you can use to connect both wired and wireless clients to the internet
  - These can also be called a wireless router
  
##### Difference Between a Router and An Access Point

- Wireless routers can function as access points, but not all access points can work as routers. While routers manage local area networks, communicate with outside network systems, acquire, distribute, and dispatch data in multiple directions, establish a point of connectivity, and ensure security, access points typically only provide access to the router’s established network.
- An access point, on the other hand, is a sub-device within the local area network that provides another location for devices to connect from and enables more devices to be on the network.
- The router acts as a hub that sets up a local area network and manages all of the devices and communication in it. An access point, on the other hand, is a sub-device within the local area network that provides another location for devices to connect from and enables more devices to be on the network.

##### NIC
- Every host that wants to connect to a wireless network needs a NIC
- You might use an external nic to increase your signal in an area of poor reception
- What layer of the OSi model (1 & 2)

##### Wireless Antenna
- Act as both transmitters and receivers
- There are two types:
  - Omni directional (point-to-multipoint) 
    - OMNI- Your car can be parked in any direction and still get same signal reception
     - Most AP’s use Omni’s because often clients and other AP’s could be located in any direction
  - Directional or yagi (point-to-point)
    - Yagi- Television antenna that you had to dial
    - Yagi’s provide greater range focus all their power in a single direction whereas Omni antennas must disperse the same amount of power in all directions at the same time
    - Very precise when aligning
  
#### Standards
IEEE (Institute of Electrical and Electronics Engineers) created and regulates the wireless standards. The FCC released 3 unlicensed bands for public use: 900MHz, 2.4GHz and 5GHz
- 802.11a
    - First wireless satndard that runs the 5-GHz frequency
    
 - 802.11b
    - has a transfer rate of 11Mbps while using a frequency of 2.4GHz
    - Not compatible with 802.11a networks because they run on different frequencies
   
- 802.11g
    - Increases transfer rate and was designed to be compatible with 802.11b.
    - The transfer rate of 802.11g devices is 54 Mbps in the 2.4-GHz frequency
    
- 802.11n
    - finalized in 2009
    - The goal is to increase the transfer rate beyond the current standards like 802.11g
    - Rumored to support transfer rates up to 600 Mpbs but most networking components transfer at 150 Mbps
    - Uses channel bonding which uses multiple antennas and can transmit data over two channels to achieve more throughput.
    - Backwards compatible with 802.11a, 802.11b, 802.11g, and can run at both 2.4-GHz or 5-GHz frequencies
 
 - 802.11ac
    - Approved in 2014 and is considered a high-throughput wireless standard that runs at the 5-GHz frequency range.
    - Potentially 1 Gbps
    - Multiple transmitters send seperate signals and multiple recievers to recieve separate signals at the same time.
    
#### Note:
1. 802.11a was an early implementation of wireless networking and is not compatible with the Wi-Fi Networks.
2. b,g, and n are all compatible and make up the Wi-Fi standard. All run on 2.4-GHz frequency
3. An examples is a previous wireless network at home had an access point that was an 802.11g device, but one of the old laptops had an 802.11b wireless network card. It would still be able to communicate on the network because the two standards are compatible but it will use the slowest speed of 11 Mbps.
  
   ![Chart of standards](https://github.com/alyssaknight/Wireless/blob/master/wireless/chart.PNG)
   
 ### Channels
- 2.4GHz is a frequency range. Each frequency in the range is known as a channel.
- 802.11b/g/n Wi-Fi radios can transmit in the 2.4 GHz band with a total of fourteen available channels. In the US only eleven of those channels are legally available and only 13 are available in Europe.
- It is likely to get interference from the channels if all of your devices are on the same channel. To fix this you can experiment by changing the channels used by your devices

### Authentication and Encryption
#### WEP
- Wired Equivalent Privacy designed to give wireless the level of security equivalent to that of wired network
- Desigend to add security to wireless networking by requiring anyone wishing to connect to the wireless network to input a wireless key
- WEP is now a deprecated protocol and should not be used, however it still is.
- Uses RC4 encryption protocol as the symettric encryption algorithm using 64-bit or 128-bit encryption
- Note* Talk about symmetric encryption
- Encryption key is based on a 24-bit initialized vector (IV), a value that is randomly generated and sent in the header of the packet.
- It is used with a 40-bit or 104-bit key that is then configured on wireless access point and the wireless client.
- WEP has HUGE flaws in its implementation of encryption and key usage that as a result both 64-bit and 18-bit WEP have been cracked
- There are only 16,777,216 possible IV's so a hacker can capture enough traffic and crack WEP
#### WPA
- Wi-Fi protected access was designed to improve upon security in WEP
- Uses a 128-bit key and TKIP (Temperal Key Intergity Protocol) which is a protocol used to change the encryption keys for eevery packet that is sent.
- Uses EAP protocol (Extensive Authentication Protocol)
- EAP
  - A very secure authentication protocol that supports a number of authentication methods such as kerberos, token cards, certificates and smart cards
  - LEAP
  - PEAP
  - EAP-TLS
  - EAP-TTLS
- WPA operates in the follwoing modes: (pg. 409)
  - WPA Personal
  - WPA Enterprise
  - Open
#### WPA2
- Improves on the security of WPA 
- Uses the counter mode with cipher block chaining message authentication protocol (CCMP or CCM) for data privacy, integrity and authentication
- Uses AES (Advanced Encryption Standard) for encryption of wireless traffic instead of TKIP
- Uses RADIUS

#### SSID
- The Service Set Identifier is the name that you give wireless networks and in order for anyone to connect they need to know the SSID
- Routers are configured to advertise their SSID by default so even if you change the SSID to something hard to guess, the router will advertise the name
- You should configure your router to not broadcast the SSID

#### Wireless Security
- The original 802.11 comittee never thought that wireless devices would ever outnumber wired devices 
- To secure your wireless router consider changing the settings such as the admin password, the SSID, MAC filtering, etc.
- War driving is driving around with a laptop a wireless nic and a high-gain antenna trying to locate open AP's
- In a secured wireless connection, internet data is sent in the form of encrypted packets. These packets are encrypted with network security keys. If you somehow manage to get hold of the key for a particular wireless network you virtually have access to the wireless internet connection.
- Open access mode - security features are turned off
- SSID's
  - open shared-key authentication, static WEP (wired Equivalent Privacy) and optional MAC authentication
  - An SSID prevents access by any client device that does not have the SSID
  - However by default an access point broadcasts its SSID
  - Even if the SSID broadcast is off, a bad person could monitor the network and discover a client connecting to an access point
  - Why? Because that information is regulated by the original 802.11 speciffications and must be transmitted in clear text
- Shared Key Authentication
  - The access point sends the client device a challenge-text packet that the client must then encrypt with the correct WEP key and return to access point
  - All an intruder has to do is detect both the clear text challenge and the same challenge encrypted with a WEP key and decipher the WEP Key
    - This is not really used anymore in todays WLAN's
- MAC Addresses
  - MAC addresses can be manually configured in the AP of the hosts and denied access in the filter table
  - All mac layer information is sent in the clear so anyone equipped with a wireless sniffer can just read the packets sent to the access point and then spoof their MAC Address
- WPA and WPA 2 Pre-Shared Key
  - Another form of security that is added on
  - Wi-Fi protected Access is a standard developed by the Wi-Fi alliance
  - The PSK verifies users via a password or identifying code (passphrase) on both the client machine and access point
  - A client can only gain access if its password matches the access points password





