# 📡 TCP/IP

TCP/IP (**T**ransmission **C**ontrol **P**rotocol/**I**nternet **P**rotocol): The fundamental suite of internet protocols that define the internet's architecture and operation.
TCP/IP facilitates the reliable transmission of data packets across diverse networks.

## History

The TCP/IP protocol suite was developed in the 1970s by a team of researchers at the United States Department of Defense.
It was designed to connect multiple networks to form a single, global network, which would later become the internet.

## Structure

TCP/IP is a layered protocol, with each layer responsible for a specific aspect of data transmission.

### TCP (Transmission Control Protocol)

- **Connection-Oriented**: Establishes a connection between the sender and the receiver before data transmission.
- **Reliable**: Ensures that data is delivered in the correct order and without errors.
- **Flow Control**: Manages the rate of data transmission to prevent congestion and packet loss.
- **Error Detection and Correction**: Detects and retransmits lost or corrupted data packets.

### IP (Internet Protocol)

- **Connectionless**: Does not establish a connection before data transmission.
- **Best-Effort Delivery**: Does not guarantee that data packets will be delivered, but it does its best to deliver them.
- **Routing**: Determines the best path for data packets to travel from the sender to the receiver.
- **Addressing**: Assigns unique IP addresses to devices on the network.
- **Fragmentation and Reassembly**: Splits large data packets into smaller ones for transmission and reassembles them at the destination.
