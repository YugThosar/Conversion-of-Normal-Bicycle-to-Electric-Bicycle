# Electric Bicycle Conversion Project

A step-by-step documentation for converting a standard mechanical bicycle into an electric bicycle (e-bike) using a dual-drive system and custom controller integration.

---

## 🚴 Project Overview
This project details the mechanical and electrical conversion of a conventional bicycle into a 24V electric hybrid. By retaining the standard chain drive on the right side and installing a customized hub/sprocket on the left, the bicycle achieves an independent dual-side drive system capable of both motorized power and manual pedaling.

---

## 📊 Technical Specifications

### Power & Drive System
*   **Motor:** 24V, 350W Brushed/Brushless DC Motor (Side-mount configuration)
*   **Hub Assembly:** Two-sided rear wheel hub (Right side: standard pedal chain freewheel | Left side: motor drive sprocket/freewheel)

### Energy Storage
*   **Battery Pack:** 24V, 12Ah Lithium-ion (or Lead-Acid configuration)
*   **Calculated Capacity:** 288 Wh (Watt-hours)

### Controls & Safety
*   **User Interface:** Twist/Thumb Throttle with built-in battery level indicator
*   **Brain Unit:** Microcontroller / Electronic Speed Controller (ESC)
*   **Braking Mechanism:** Electric Cut-off Brake Levers (instantly cuts power to the motor upon engagement)
*   **Auxiliary:** High-efficiency LED Headlight integrated with the main battery circuit

---

## 🔌 System Architecture & Wiring Diagram

The diagram below outlines the core electrical routing between the battery, microcontroller, inputs, and outputs.
+--------------------------------+|      24V 12Ah Battery Pack     |+---------------+----------------+|v[Fuse / Switch]|v+------------------+     +--------+--------+     +-------------------+|  Twist Throttle  |---->|                 |<----+  Electric Brakes  ||  (Input Command) |     | Microcontroller |     |  (Safety Cut-off) |+------------------+     |   / Motor ESC   |     +-------------------++--------+--------+|+------------------+------------------+|                                     |v                                     v+---------+---------+                 +---------+---------+|  24V 350W DC Motor|                 |   LED Headlight   |+-------------------+                 +-------------------+

## 🛠️ Step-by-Step Assembly Guide

### Step 1: Mechanical Modifications & Hub Installation
1.  **Wheel Disassembly:** Remove the rear wheel assembly from the bicycle frame.
2.  **Two-Sided Hub Mounting:** Replace the standard single-threaded rear hub with the two-sided hub. Ensure the threads match your standard pedal freewheel on the right.
3.  **Left-Side Drive Adaptation:** Thread the motor drive sprocket/freewheel onto the left side of the new hub.
4.  **Motor Mount Fabrication:** Securely bolt the motor mounting bracket to the left side of the rear bicycle frame (chainstay/seatstay area), aligning the motor gear perfectly with the left-side hub sprocket.
5.  **Chain Tensioning:** Mount the secondary drive chain between the motor and the left hub sprocket. Ensure optimal tension to prevent chain drops under torque load.

### Step 2: Component Mounting
1.  **Battery Enclosure:** Secure the 24V battery pack inside the frame triangle or on a heavy-duty rear rack to maintain a low center of gravity.
2.  **Controller Placement:** Place the microcontroller/ESC inside a weatherproof enclosure near the battery.
3.  **Handlebar Controls:** Remove old grips and mount the **Throttle**, **Electric Brake Levers**, and **Headlight Switch** onto the handlebars.

### Step 3: Electrical Wiring
1.  **Power Loop:** Connect the battery positive and negative terminals to the controller power inputs. *Crucial: Install an inline fuse (20A–25A) on the positive wire.*
2.  **Motor Connection:** Wire the controller’s thick motor output leads directly to the 350W motor terminals.
3.  **Control Peripherals:** Plug the 3-wire throttle interface and the 2-wire brake cutoff switches into their designated controller pins.
4.  **Lighting System:** Wire the headlight through a step-down switch module directly to the main power line or the auxiliary light output ports on the controller.

---

## ⚠️ Safety Precautions & Validation Checklist

Before testing the e-bike on open roads, complete the following safety validation sequence:

- [ ] **E-Brake Test:** Elevate the drive wheel, engage the throttle, and press the brakes. The motor must shut off immediately.
- [ ] **Thermal Inspection:** Run the motor continuously for 5 minutes and check for excessive heat generation in the wires, battery, or microcontroller.
- [ ] **Structural Check:** Double-check that all frame-mounted motor brackets are torqued down and do not flex under load.
- [ ] **Insulation Check:** Verify that all solder points and terminal junctions are fully wrapped in heat-shrink tubing to prevent short circuits.
