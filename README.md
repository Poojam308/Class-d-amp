# 🔊 Class-D Audio Pre-Amplifier

A specialized hardware design for a high-efficiency Class-D audio pre-amplifier. This project leverages the precision of KiCad 8.0 to implement a switching amplifier topology, focusing on low-noise signal processing and high-frequency pulse-width modulation (PWM).

## **✨ Features**

* **⚡ Class-D Topology:** Utilizes high-frequency switching for superior efficiency compared to traditional linear amplifiers.
* **🎯 Precision Timing:** Employs a CMOS-based LMC555 timer for stable PWM signal generation.
* **📉 Low-Noise Pre-amplification:** Integrated TL072 JFET-input operational amplifiers for high-fidelity audio signal conditioning.
* **🛡️ Robust Power Stage:** Features IRF540N HEXFET Power MOSFETs for reliable switching and power delivery.
* **📏 Compact 2-Layer PCB:** Optimized layout with a small footprint (187.55 mm x 103.05 mm) suitable for various enclosures.

## **🛠️ Design Requirements**

1. **💻 [KiCad 8.0+**](https://www.kicad.org/) (For viewing/modifying schematic and PCB files)
2. **📄 Gerber Viewer** (To inspect manufacturing files)
3. **🔌 12V-24V DC Power Supply** (Recommended for operation)

## **🏗️ Manufacturing Instructions**

### **🖨️ 1. PCB Fabrication**

The `Gerbers/` directory (or the root `.gbr` files) contains everything needed for professional fabrication:

1. **📤 Upload to Fabricator:** Submit the `.gbr` (Gerber) and `.drl` (Drill) files to your preferred PCB manufacturer (e.g., JLCPCB, PCBWay).
2. **⚙️ Stackup Settings:**
* **Layers:** 2
* **Material:** FR4
* **Thickness:** 1.6 mm
* **Copper Weight:** 1oz (standard)


3. **🔍 Solder Mask/Silkscreen:** Standard Green/White (or your preference).

### **🧪 2. Assembly (BOM Highlights)**

* **IC1/IC2:** TL072 (Dual Op-Amp)
* **IC3:** LM311 (Voltage Comparator)
* **IC4:** LMC555 (Timer)
* **Q1-Q4:** BC547/BC557 (Bipolar Junction Transistors)
* **M1:** IRF540N (Power MOSFET)

## **🧠 How It Works**

* **🎙️ Input Stage (`pre audio amplifier.kicad_sch`):** The audio signal enters through the TL072 stages, where it is buffered and amplified to a level suitable for modulation.
* **〰️ PWM Generation:** The LMC555 timer and LM311 comparator work in tandem to convert the analog audio signal into a high-frequency pulse-width modulated (PWM) square wave.
* **🔌 Output Stage:** The modulated signal drives the IRF540N MOSFET, which switches the power supply to the output. This high-frequency signal is then filtered (via external low-pass filter) to reconstruct the amplified audio waveform.
* **📐 PCB Layout:** The `pre audio amplifier.kicad_pcb` uses 0.2mm trace widths and clearances to ensure signal integrity while maintaining a high-density component arrangement.

---
