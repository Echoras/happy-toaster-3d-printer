# happy-toaster-3d-printer
A personal 3D printer build designed from scratch, featuring custom marlin firmware and hardware tweaks. 

Where I live, 3D printers are imported and usually cost far more than most people can justify.  
To make 3D printing accessible (and satisfy my curiosity), I decided to design and build my own printer from scratch — for a fraction of the usual price.  

**Note:** The diagrams and setup steps below show the original 220×220 mm build area.  
In my later revision, I upgraded the printer to a larger bed (300×300 mm) and updated the firmware accordingly
— this involved only two lines of code changing the bed size constants. Both versions are compatible with this design.

---

### Acknowledgments
Thanks to the open-source 3D printing community — especially Marlin devs and countless makers who share their designs online. This project wouldn’t exist without that shared knowledge.

---

## Materials

### Frames
- 3 × 2020V-4.2 aluminum extrusion, 400 mm  
- 3 × 2040V aluminum extrusion, 400 mm  
- 4 × 2020V-4.2 aluminum extrusion, 300 mm  
- 20 × 2020 Aluminum Profile Connector Set  
  - *Make sure they include drop-in T-nuts. Buy extra; they’re useful for later mods.*  
- 2 × Threaded T8 lead screw, 8 mm pitch, 400 mm length  
- 1 × Alloy black hotbed Y carriage plate (for Ender 3 / CR-10)  
- 4 × Anti-vibration feet (for i3 MK3 printer kits)  
- 1 × Funssor HE3D/Tarantula I3 aluminum X-axis carriage plate (MGN12H upgrade, 3 mm thick)  
- 2 × Z-rod bearing holder (for aluminum profile frame)  

---

### Mechanical Components
- 2 × Z-axis stepper motor mount (NEMA17)  
- 2 × NEMA17 stepper motor mounting brackets (42-series)  
- 1 × Open-source idler pulley plate  
- 1 × NEMA17 stepper motor fixed mount (for X-axis)  
- 1 × V6 J-head Bowden hotend + extruder kit  
- 20 × 2020-series L-type internal corner brackets (with screws)  
- 12 × POM V-slot linear pulleys (clear polycarbonate)  
- 2 × Flexible couplers for T8 threaded rod (8 mm)  
- 1 × All-metal Bowden extruder feeder kit (with PTFE tube)  
- 10 m GT2 open timing belt, 6 mm width  
- 5 × GT2 20-tooth idler pulleys (with teeth)  
- 3 × GT2 20-tooth idler pulleys (without teeth)  

---

### Boards & Electronics
- 4 × Cloudray NEMA17 stepper motors (0.42 N·m torque, 1.7 A, 2-phase, 40 mm)  
- 1 × HT-100K NTC thermistor (100K Ω)  
- 1 × 30A heated bed MOSFET expansion module (with cables, compatible with Anet A8/A6/A2/RAMPS 1.4)  
- 1 × MZMW LRS350/LRS400 switching power supply (400 W, 12 V)  
- 1 × MK3/MK2 heated bed (220×220×3.0 mm, 12 V)  
- 1 × Arduino Mega 2560 R3  
- 1 × RAMPS 1.4 controller board  
- 5 × A4988 stepper driver modules  

---

### Notes
If you’re sourcing parts locally or from multiple suppliers, double-check connector compatibility (especially for the stepper motors and MOSFET module). Keep a few extra T-nuts and corner brackets for future modifications — they’re always useful. I needn't mention that but you must have tools ready at hand at all times like screwdrivers, power tools, screws, nuts, the general stuff.


## Build Process

The **Happy Toaster** is built in **three main stages**, followed by firmware setup.  
Each stage can be completed independently and tested before moving on.

### 1. Frame Assembly
The foundation of the printer — aluminum extrusion frame and motion rails.  
This step covers:
- Cutting and assembling the frame to the 220×220 mm spec (later expanded to 300×300 mm).  
- Installing linear bearings and ensuring square alignment.  
- Mounting the bed platform and Z-axis supports.

> **Tip:** Even small misalignments here can cause major print issues later, so take your time squaring the frame.

---

### 2. Mechanical Systems
This stage adds motion and structure:
- Mounting the X, Y, and Z carriages  
- Installing lead screws, belts, and pulleys  
- Assembling the hotend and extruder  
- Checking smooth travel and calibration manually  

> **Note:** At this point, the printer should move freely by hand without binding.

---

### 3. Electronics and Wiring
This is where the printer becomes alive.  
Steps include:
- Installing stepper motors and limit switches  
- Wiring the mainboard, display, and power supply  
- Cable management and grounding safety checks  

> **Optional Add-ons:** LED lighting, cooling fans, or cable sleeves can be added here.

---

### 4. Custom Firmware (Marlin)
Once the hardware is ready, flash the custom **Marlin CFW** provided in this repository.  
The configuration includes:
- Bed dimensions (adjustable for 220×220 or 300×300)  
- Motor direction and steps/mm tuning  
- Endstop and thermistor setup  



