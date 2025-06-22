## Inverting vs. Non-Inverting Amplifier using Op-Amps

| Feature                    | Inverting Amplifier                           | Non-Inverting Amplifier                          |
|----------------------------|-----------------------------------------------|--------------------------------------------------|
| **Input Connection**       | Connected to **inverting (−)** terminal via resistor | Connected to **non-inverting (+)** terminal         |
| **Reference Point**        | **Non-inverting (+)** terminal is grounded     | **Inverting (−)** terminal connected to feedback and resistor divider |
| **Phase Relationship**     | **180° phase shift** (inverted output)         | **0° phase shift** (same polarity as input)      |
| **Gain Formula**           | \( A_v = -\frac{R_f}{R_{in}} \)              | \( A_v = 1 + \frac{R_f}{R_{in}} \)             |
| **Input Impedance**        | Low (equal to \( R_{in} \))                   | **Very high** (ideally infinite)                 |
| **Output Polarity**        | Inverted (opposite sign)                      | Non-inverted (same sign)                         |
| **Voltage Follower**       | Not possible                                 | Yes, if \( R_f = 0 \), gain = 1                |
| **Use Cases**              | Signal inversion, summing amplifier, integrator | Buffering, voltage gain stages, impedance matching |

### Example:

- **Inverting**:
  - Input: +5V → Output: −5V (if gain = −1)
- **Non-Inverting**:
  - Input: +5V → Output: +5V (if gain = 1)

### Key Takeaway:

- **Use Inverting** when you want **signal inversion** and precise gain control.
- **Use Non-Inverting** when you need **same polarity**, **high input impedance**, or **buffering**.
