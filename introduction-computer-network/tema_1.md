# 1.1 Intro

##  Basic Concepts

* **Network (Rete)**
  A distributed system that interconnects multiple devices, allowing communication between them.

* **Communication**
  Transfer of information.

* **Information**
  Technically, it is the message itself that is being transmitted.
  > The **amount** of information is measured by the **entropy** of the text $\rightarrow$ **number of bits**.

---

##  Communication Model

> 🖼️ **[PLACEHOLDER: Source System Diagram]**
> *Source System (Source $\to$ Transmitter) $\to$ Transmission System $\to$ Destination System (Receiver $\to$ Destination)*

---

## ⏱ Transmission & Propagation Mechanics

> 🖼️ **[PLACEHOLDER: Space-Time Diagram]**
> *Diagram illustrating transmission delay ($T_x$) vs propagation delay ($R_p$) between point A and B over distance $d$.*

### Key Formulas & Definitions

**1. Transmission Time ($T_x$)**
$$T_x = \frac{L}{V_t}$$
> **Units:** $\frac{[\text{bits}]}{[\text{bits/s}]} = [\text{seconds}]$

**2. Transmission Speed ($V_t$)**
Speed at which information is transmitted over a link.
* **Unit:** bits per second (**bps**)

**3. Propagation Speed ($V_p$)**
Speed at which a signal travels through the transmission medium.
* **Unit:** meters per second (**m/s**)
* **Approximation (Speed of light in medium):**
  $$V_p \approx 2 \cdot 10^8 \text{ m/s}$$

**4. Propagation Delay ($R_p$)**
$$R_p = \frac{d}{V_p}$$
> *Where $d$ is the distance between transmitter and receiver.*

### Total Delay ($T$)
The total time is the sum of transmission time and propagation delay:
$$T = T_x + R_p$$

# 1.2-2 Network Evolution

##  1950's - 60's: The Origins

### Key Definitions
* **WAN (Wide Area Network)**
  Type of network that covers a large geographical area. It is typically operated by service providers.

* **Switching (Circuit Switching)**
  A switching mechanism that establishes a **dedicated path** through the network's nodes for the duration of the communication.

---

##  1970's: Standardization & Packets

**Standard ITU** --> *International Telecommunication Union*

### Packet Switching
Mechanism in which data is sent in sequences, divided into small units of data called **packets**.

> 🖼️ **[PLACEHOLDER: Insert Image - Page 2]**
> *Diagram showing data stream divided into packets.*

**Mechanism:**
Each packet is passed from **node to node**.

$$V_t = \frac{L}{T_{tx}}$$

### X.25 Protocol
It is a packet switching mechanism that verifies the correctness of each packet **at every hop**.
* **Process:** If necessary, the packet is forwarded from one node to the next *only* until it arrives correctly (error correction at every step).

**Characteristics:**
* 📈 **Complexity:** Increases project complexity.
* 💰 **Cost:** Higher monetary cost due to resource usage.
* ⚠️ **Limit:** **64 kbps MAX**

> 🖼️ **[PLACEHOLDER: Insert Image - Page 3]**
> *Diagram illustrating X.25 hop-by-hop verification.*

**Example: Flow Control**
This network uses a mechanism of flow regulation known as a **buffer**.

---

##  1980's
*(Section to be continued...)*