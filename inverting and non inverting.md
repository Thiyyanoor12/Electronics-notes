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

---

## Why is Input Impedance Different?

### Inverting:
- Signal goes through \( R_{in} \) into the **virtual ground** at inverting input
- Current flows → input impedance = \( R_{in} \)

### Non-Inverting:
- Signal goes into the **non-inverting input (+)** of op-amp
- Op-amp draws **almost zero current** → **very high input impedance** (MΩ to GΩ)

---

## Which is Used More in Industry?

| Configuration      | Common Use                                         |
|-------------------|----------------------------------------------------|
| **Non-Inverting** | Front-end signal conditioning, sensor buffering    |
| **Inverting**     | Filters, summing amps, control systems             |

**Non-Inverting** is more commonly used for general-purpose signal interfaces because of high input impedance and buffering capability.

---

## Is a Non-Inverting Op-Amp a Buffer?
Yes! When gain = 1, it's called:
- **Voltage Follower**
- **Unity Gain Amplifier**
- **Op-Amp Buffer**
- **Impedance Buffer**

Used to **isolate circuits**, prevent loading, and transfer signals cleanly.

---

## Do Buffers and Optocouplers Do the Same Thing?
| Feature           | **Op-Amp Buffer**              | **Optocoupler**                          |
|------------------|--------------------------------|------------------------------------------|
| Isolation Type    | Impedance isolation (no loading) | **Electrical isolation**                  |
| Ground Shared?    | ✅ Yes                         | ❌ No (optical link between circuits)     |
| Use Case          | Signal conditioning            | High-voltage isolation, SMPS, protection |

---

## Real-World Example of Buffer Use

### 🔧 Buffering an LM35 Temperature Sensor
- LM35 has low current capability
- Connect output to op-amp buffer → then to ADC
- Prevents sensor loading & gives stable ADC reading

### Benefits:
| Without Buffer         | With Buffer                 |
|------------------------|-----------------------------|
| Unstable ADC reading   | Accurate voltage reading    |
| Sensor gets loaded     | Sensor protected            |

---

## Summary of Buffer Names

- **Voltage Follower**
- **Unity Gain Amplifier**
- **Non-Inverting Buffer**
- **Impedance Buffer**
- **Op-Amp Buffer**

These all describe a non-inverting op-amp circuit with **gain = 1**.

