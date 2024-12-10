# Congestion Control in TCP

## Overview
Congestion control in TCP is designed to prevent network congestion by adjusting the rate at which data is sent. It uses several algorithms to ensure efficient and fair data transmission.

---

## Key Algorithms

### 1. **Slow Start**
- The congestion window (`cwnd`) starts small (e.g., 1 MSS) and grows exponentially until a threshold (`ssthresh`) is reached.
- After reaching the threshold, it switches to the Congestion Avoidance phase.

### 2. **Congestion Avoidance**
- `cwnd` increases linearly instead of exponentially.
- The growth formula: `cwnd += 1 MSS per RTT`.

### 3. **Fast Retransmit and Fast Recovery**
- **Fast Retransmit**: If three duplicate ACKs are received, the sender assumes a packet loss and retransmits the lost packet.
- **Fast Recovery**: Instead of reducing `cwnd` to 1 MSS, it reduces it to half the current size and resumes linear growth.

---

## AIMD (Additive Increase, Multiplicative Decrease)
- **Additive Increase**: After every successful RTT, `cwnd` increases by 1 MSS.
- **Multiplicative Decrease**: On packet loss, `cwnd` is reduced to half.

---

## Practical Example
- Initial `cwnd = 1 MSS`.
- After 4 RTTs with no loss:
  - `cwnd = 1, 2, 4, 8 MSS` during slow start.
  - Switch to linear growth in Congestion Avoidance.

---

## References
- RFC 5681: TCP Congestion Control
- [Wireshark TCP Analysis](https://www.wireshark.org/docs/)
