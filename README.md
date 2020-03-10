# Send
Transfer files between devices in IIITB network via Send

## How does this work?

**TL;DR** A server in the data center selects two random ports and sets up port forwarding through them via  IP Tables. Your devices communicate via these ports.

Direct device-to-device communication is blocked inside IIITB Intranet.
To overcome this, we use a server in the data center to act as a relay.
The server selects two random ports and sets up portforwarding across them via IP Tables.
IP Tables use Netfilter underneath, which is in kernel space and should make the data transfer fast.

I'm still deciding if I should add encryption.
