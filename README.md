# water-level-indicator
A basic circuit that lights up LEDs to show low, medium, and full water levels using BC547 transistors and metal probes. It helped me understand transistor switching and how water can act as a sensor.
# 💧 Water-Level Indicator (Transistor & LED Version)

A simple water-tank level indicator that lights different LEDs as the water rises.  
The circuit uses stainless-steel probes, BC547 transistors, and current-limiting resistors. No microcontroller required.

## 🧰 Components Used
| Qty | Part                         | Notes                          |
|-----|------------------------------|--------------------------------|
| 3   | BC547 NPN Transistor         | One per level LED              |
| 3   | LED (Red / Yellow / Green)   | Low, Mid, High indicators      |
| 3   | 220 Ω Resistor               | LED current limit              |
| 3   | 100 kΩ Resistor              | Base pull-down for each stage  |
| 3–4 | Stainless-steel probes       | Immersed at different heights  |
| 1   | Power supply 5 V–9 V         | Battery or DC adaptor          |
| —   | Breadboard / strip-board     | Prototyping                    |
| —   | Hook-up wires                | Connections                    |


## ⚙️ Working Principle
1. **Probes** are fixed at LOW, MID, and HIGH positions inside the tank.  
2. Water conducts a tiny current between the common probe (GND) and each level probe.  
3. When a probe touches water, the small current biases the **BC547** base.  
4. The transistor switches **ON**, lighting its corresponding LED.  
5. As water rises, more LEDs turn on, giving a visual indication of the level.

## 📌 Assembly Steps
1. Mount the three BC547 transistors on the breadboard.  
2. Connect each LED in series with a 220 Ω resistor to the transistor collector.  
3. Tie all emitters to the **ground** line (common probe).  
4. Run individual wires from the transistor bases to the separate **level probes**, each with a 100 kΩ pull-down to ground.  
5. Connect Vcc (5 V–9 V) to the positive LED ends.  
6. Immerse probes—LOW at bottom, MID mid-height, HIGH near the top—and test.

## 🌱 What I Learned
- How water can act as a conductive trigger in low-current circuits  
- Using NPN transistors as switches for visual indicators  
- Importance of base pull-down resistors to avoid false triggering  
- Practical probe placement for reliable sensing

## 🚀 Future Improvements
- Add a buzzer for overflow or low-level alarm  
- Replace LEDs with a 7-segment display or LCD  
- Upgrade to a microcontroller (Arduino/Pico) for remote alerts  
