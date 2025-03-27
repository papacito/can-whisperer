# CAN Bus – The Basics

## What is CAN?
- Controller Area Network
- Developed by Bosch in the 1980s
- Used to allow microcontrollers and devices to communicate without a host computer

## Where is it used?
- Automotive (OBD2, engine control, lights, sensors)
- Industrial automation
- Medical devices
- Aviation

## Why is it useful?
- Robust: works well in noisy environments
- Fast: speeds up to 1 Mbps (CAN FD goes even higher)
- Lightweight: messages are small (8 bytes payload in classic CAN)
- Broadcast-based: all nodes see all messages

## Basic Concepts
- Nodes (ECUs)
- Arbitration (message priority)
- Message IDs
- Standard vs Extended frames
- Data length
- No MAC addresses – ID is king

## Limitations
- Limited bandwidth
- No security/authentication
- Message IDs not standardized across manufacturers

## What CAN does:
- Broadcasts messages with an ID
- Any node on the bus can read or send messages
- There’s no “handshake,” no password, no cryptographic signature

## What CAN does not do:
- Doesn’t authenticate senders
- Doesn’t verify message contents
- Doesn’t encrypt data
- Doesn’t check if a sender is legit
