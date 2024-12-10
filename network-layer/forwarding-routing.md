# Forwarding and Routing in the Network Layer

## Forwarding
Forwarding refers to the process of moving packets from an input port to the appropriate output port within a router.

### Key Mechanisms
1. **Longest Prefix Matching**
   - Used to match the destination IP address with the routing table.
   - Example:
     ```
     Prefix        Next Hop
     192.168.1.0/24   Router A
     192.168.0.0/16   Router B
     Default          Router C
     ```

2. **Switching Fabrics**
   - **Memory-Based**: Oldest, relies on CPU for packet transfer.
   - **Bus-Based**: Packets travel over a shared bus.
   - **Interconnection Network**: High-speed, used in modern routers.

---

## Routing
Routing involves determining the path that a packet takes from the source to the destination.

### Types of Routing
1. **Static Routing**: Manually configured routes.
2. **Dynamic Routing**: Routes determined by algorithms (e.g., OSPF, BGP).

---

## Practical Example
- A router uses OSPF to calculate the shortest path to destination networks.
- For example:
