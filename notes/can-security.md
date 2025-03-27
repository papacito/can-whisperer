# CAN Bus security

## TL;DR – CAN is like a party
- Everyone’s shouting, nobody’s checking IDs, and if you get in the room, you can yell too.

## What CAN does:
- Broadcasts messages with an ID
- Any node on the bus can read or send messages
- There’s no “handshake,” no password, no cryptographic signature

## What CAN does not do:
- Doesn’t authenticate senders
- Doesn’t verify message contents
- Doesn’t encrypt data
- Doesn’t check if a sender is legit


## If you have physical access to the OBD2 port or another CAN tap:
- You can see everything being broadcast (like RPM, throttle, gear position)
- You can replay messages
- You can even inject fake commands (e.g., flash dashboard lights, spoof gear position, or worse)


## Real-World Examples
- Hacking the Jeep Cherokee (2015): Researchers remotely controlled steering/brakes via CAN after gaining access through the infotainment system.
- RollJam: Exploited unencrypted key fob CAN traffic to replay/unlock cars.
- Replay attacks: Record a “window down” message → replay it later.


## Modern Defenses (kind of…)

Newer cars try to patch it:
- Gateways that firewall off certain ECUs
- Encrypted ECUs (rare, usually high-end only)
- Timeout-based message rejection
- Some intrusion detection systems on high-end vehicles

But none of that is part of the CAN protocol itself — it’s all layers on top of it.

