# happy-toaster-3d-printer
<p align="center">
  <img src="images/Printerirl.jpg" width="400"> <br/>
  <img src="images/bitbap-clean.jpg" width="200">
</p>
</p>
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
- 3 × GT2 idler pulleys (without teeth)  

---

### Boards & Electronics
- 5 × Cloudray NEMA17 stepper motors (0.42 N·m torque, 1.7 A, 2-phase, 40 mm)  
- 1 × HT-100K NTC thermistor (100K Ω)  
- 1 × 30A heated bed MOSFET expansion module (with cables, compatible with Anet A8/A6/A2/RAMPS 1.4)  
- 1 × MZMW LRS350/LRS400 switching power supply (400 W, 12 V)  
- 1 × MK3/MK2 heated bed (220×220×3.0 mm, 12 V)  
- 1 × Arduino Mega 2560 R3  
- 1 × RAMPS 1.4 controller board  
- 5 × A4988 stepper driver modules
- 1 x M8 Inductive Proximity Sensor Z Probe
- 2 x Switch Endstop
- 1x LCD Display for Ramps Board

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

---


Step 1 — Frame Setup
<p align="center"> <img src="images/Base1shapetopview.png" width="400"><br> <em>Base Frame *top view*</em> </p>

3x 2020v 300mm Frame
<br/>2x 2020v 400mm Frame
<br/>8x Frame connectors

- Begin with the base 2020 extrusions and corner connectors.
- Ensure perfect 90° alignment using a square or angle bracket.


<p align="center"> <img src="images/Base2frontview.png" width="400"><br> <em>Base Frame *FRONT VIEW*</em> </p

3x 2040V Frame 400mm (1x for X frame, 2x for vertical Z frame)
<br/>1x 2020v Frame 300mm
<br/>2x Frame Connectors
<br/>2x Internal Frame Connectors
<br/>4x Wheels

- Start getting the 2040 extrusions and work you way up to make the frame the X axis frame will hold onto, along with the bowden extruder and later on hang up the 3d printer screen.
- Use the slightly larger 2040v (400mm) to place 4 wheels that will bite onto the vertical 2040v frame
- after loading the x axis frame with wheels onto the vertical frame, connect a top piece so that the x axis frame is set inside.

                                                                                                
<p align="center"> <img src="images/Z axis frames w belt.png" width="400"><br> <em>Base Frame w/ X Axis mechanism *BACK VIEW*</em> </p>
1x NEMA17 stepper motors
<br/>2x GT2 20-tooth idler pulleys
<br/>2x GT2 idler pulleys no teeth
<br/>10 m GT2 open timing belt, 6 mm width  
<br/>4x wheels
<br/>2x Zip ties
<br/>some drop in tee nuts and screws for the following frames:
<br/>NEMA17 stepper motor mounting bracket
<br/>Open-source idler pulley plate bracket
<br/>Funssor HE3D/Tarantula I3 aluminum X-axis carriage plate (MGN12H upgrade, 3 mm thick)  
<br/><br/>

- For the hotend x-axis carriage plate start with putting on the four wheels and place onto the x frame accordingly
- Place the nema 17 motor onto its respected plate, screw onto the motor a toothed gear and for one of the screws on the top left use an extra long screw to place a Idle pulley no teeth (refer to left side of diagram where the motor is) then place onto either side of the x axis frame
- on the other side place one toothed pulley and one smooth no teeth, thats so far your base for running a timing belt onto the x axis frame
- Using zip ties, lock the timing belt onto either side of the tarantula hotend x carriage plate and then run the timing belt around the frame make sure it is latched onto the idler pulleys and also make sure it is run through the middle of the 2040V FRAME in the middle (there should be a little space in the middle of the frame where it can go through.

<p align="center"> <img src="images/motors n rods set.png" width="400"><br> <em>Base Frame, Z rod Mechanism *BACK VIEW*</em> </p>

2x NEMA17 Stepper Motors
<br/>2x Z Axis Stepper Mounts (aluminum bracket type)
<br/>2x Threaded T8 Lead Screws, 8mm pitch, 400mm length
<br/>2x Flexible Couplers for T8 rods
<br/>2x Z Rod Bearing Holders (for top frame)
<br/> **I MUST MENTION, i had no way of finding a frame that works with the BRASS NUT for the Z rods, so i cut out a piece of wood and anchored the BRASS NUT TO IT to place on the X frame (the one with wheels)**

- Mount each NEMA17 motor to its aluminum bracket using M3 screws.
- Secure both motor mounts at the base of the vertical 2040V extrusions; make sure they sit flush and parallel.
- Insert each T8 lead screw into its flexible coupler and tighten the grub screws evenly (leave a small gap between shafts to prevent stress).
- Attach the 2020V top frame and fit the Z-rod bearing holders at the top ends of the lead screws for stability.
- Spin both lead screws manually — they should move smoothly and evenly with no binding.
- Once aligned, apply a tiny drop of threadlocker to each coupler’s grub screw to prevent loosening over time.

<p align="center"> <img src="images/frotntfiew hotend n extruder.png" width="400"><br> <em>Base Frame, Bowden Extruder and hotend *FRONT VIEW*</em> </p>

1x NEMA17 Stepper Motors
<br/>1x Nema17 Stepper Motor Holder Bracket Frame
<br/>1x Bowden Extruder (mounted onto the frame)
<br/>1x PTFE Bowden Tube (should come with bowden extruder)
<br/>1x J6 Hotend assembly (heatsink, heatbreak, nozzle) 
<br/>M8 Inductive Proximity Sensor Z Probe<br/>

- Mount the Bowden extruder assembly on the right side of the upper 2040 frame using drop-in T-nuts and screws.
- Attach the NEMA17 stepper motor onto the extruder bracket and secure it firmly so it doesn’t flex during retraction.
- Cut the PTFE tube to the appropriate length, ensuring smooth filament travel with minimal bend radius.
- Connect one end of the tube into the extruder fitting and the other into the hotend’s pneumatic connector.
- Place the hotend assembly onto the X-axis carriage plate and secure it using M3 screws.
- Plug in the cooling fan onto the hotend side, ensuring airflow faces the heatsink (not the nozzle).
- Double-check alignment between the Bowden tube and the hotend so filament feeds straight and smoothly.
- IMPORTANT NOTE: In the diagram it doesnt show but there is a Z Probe **(M8 Inductive Proximity Sensor Z Probe)** that is hooked to a washer and the washer is held in place with the X Carriage by a screw

<p align="center"> <img src="images/frotntfiew hotend n extruder w bed.png" width="400"><br> <em>Base Frame, bed Mechanism *FRONT VIEW*</em> </p>
1x NEMA17 Stepper Motor (for Y-Axis)
<br/>1x NEMA17 Motor Mount Frame
<br/>1x GT2 20-Tooth Pulley Gear (toothed)
<br/>1x GT2 Smooth Idler Pulley (toothless)
<br/>10 m GT2 Timing Belt, 6 mm width
<br/>4x V-slot Wheels (for Bed Carriage)
<br/>1x Aluminum Bed Carriage Frame
<br/>1x 220×220 mm Heated Bed with Screws and Springs
<br/>1x 2020V Aluminum Extrusion 400 mm
<br/> 4x Frame Connectors
<br/>1x Spacer Block / Riser (for electronics clearance under frame)
<br/><br/>

- Start by mounting the NEMA17 stepper motor onto the Y-axis motor bracket, attaching the toothed pulley gear to the motor shaft.
- On the opposite end of the 2020V frame, mount the smooth idler pulley using a drop-in T-nut and screw — ensure it aligns perfectly with the motor pulley to prevent belt skew.
- Attach the bed carriage frame onto the V-slot extrusion with four wheels, ensuring smooth linear motion along the Y-axis.
- Mount the heated bed onto the carriage frame using the provided screws and springs for height leveling.
- Run the GT2 timing belt through the pulley system — one end anchored to the bed carriage, looping around both pulleys, then tied back to the carriage with zip ties.
- Finally, place a spacer block or printed riser under the 2020V Y-axis frame to lift it slightly and make room for electronics wiring underneath.

  <br/><br/>NOW, so far it should looks somewhat like this:
<p align="center">
  <img src="images/frame finished almost.jpg" width="300">
  <img src="images/HOTEND.jpg" width="300">
  <img src="images/bowdenextruder.jpg" width="300">
</p>

---

Part 2: Electronics, boards, & wiring


<p align="center">
  <img src="images/Wiring.png" width="300">
  <img src="images/Screenshot 2023-06-19 102715.png" width="500"> 
</p>


1× Arduino Mega 2560 R3
<br/>1× RAMPS 1.4 Controller Board
<br/>5× A4988 Stepper Driver Modules
<br/>5× NEMA17 Stepper Motors
<br/>1× MZMW LRS350/LRS400 12V 400W Power Supply
<br/>1× MK3/MK2 Heated Bed (220×220×3.0 mm, 12 V)
<br/>1× 30A Heated Bed MOSFET Expansion Module (with cables)
<br/>1× HT-100K NTC Thermistor (100K Ω)
<br/>1× M8 Inductive Proximity Sensor (Z-Probe)
<br/>2× Mechanical Endstop Switches
<br/>1× LCD Display Screen (with EXP1/EXP2 cables)
<br/>Assorted: 12 AWG wire (for power), Dupont jumpers, heat shrink, zip ties, cable sleeves for clean routing

- Begin by mounting the Arduino Mega 2560 beneath the frame, leaving room for access to the USB and power ports. Attach the RAMPS 1.4 board on top of it.
- Insert the five A4988 stepper drivers into their sockets on the RAMPS board, ensuring correct orientation (reference the small “EN” and “DIR” labels).
- Connect each NEMA17 motor to its respective axis output on the RAMPS board:

X-Axis → X Motor

Y-Axis → Y Motor (bed carriage motor)

Z-Axis → both Z motors (connect in parallel)

E0 → Extruder motor

- Wire the endstops to the X-min and Y-min connectors on the RAMPS board, and the inductive Z-probe sensor to the Z-min input (the firmware will later handle the probing logic).
- For the hotend: connect the HT-100K thermistor to T0 and the hotend heater cartridge to D10.
- The heated bed connects through the MOSFET module to offload current:
- RAMPS D8 output → MOSFET signal input
- Power Supply 12V → MOSFET power input → Heated bed
- Attach the LCD Display using the EXP1 and EXP2 ribbon cables; it should power up alongside the RAMPS board.
- Finally, connect the 12V power supply to both the RAMPS and MOSFET modules, using 12 AWG wire for main power lines. Double-check polarity before powering up.

<p align="center"> <img src="images/IMG_7072.jpg" width="400"><br> <em>RAMPS 1.4 Wiring — *Hotend, Bed, Motors & Endstops*</em> </p>

- Dont expect the wiring to be clean the first try. Once everything is connected, use cable sleeves and zip ties to manage your wiring. Keep motor and signal cables away from power lines to reduce interference. Don’t power on yet—firmware setup and calibration come next.

---

Step 3: Flashing firmware to arduino

<br/><br/>Once the wiring is complete and verified, the next step is to flash the custom Marlin firmware onto the Arduino Mega 2560 through the RAMPS 1.4 board.
This firmware defines how the printer moves, heats, homes, and communicates. Below are the major configuration details used for the Happy Toaster 3D Printer.

<h3>⚙️ General Configuration</h3>
<table>
<tr><td><strong>Machine Name</strong></td><td>Happy Toaster</td></tr>
<tr><td><strong>Firmware Author</strong></td><td>Toaster Erection Co.</td></tr>
<tr><td><strong>Mainboard</strong></td><td>RAMPS 1.4 (EFB layout)</td></tr>
<tr><td><strong>Baudrate</strong></td><td>250000</td></tr>
<tr><td><strong>Bootscreen</strong></td><td>Custom + Marlin</td></tr>
</table>

<hr>

<h3>🛠 Stepper &amp; Mechanics</h3>
<table>
<tr><td><strong>Driver Type</strong></td><td>A4988 (on all axes)</td></tr>
<tr><td><strong>Dual Z Motors</strong></td><td>Enabled (<code>Z2_DRIVER_TYPE</code>)</td></tr>
<tr><td><strong>Axis Steps/mm</strong></td><td>X: 83.7 &nbsp;&nbsp; Y: 80.4 &nbsp;&nbsp; Z: 400 &nbsp;&nbsp; E: 95</td></tr>
<tr><td><strong>Max Feedrate (mm/s)</strong></td><td>X/Y: 300 &nbsp;&nbsp; Z: 5 &nbsp;&nbsp; E: 25</td></tr>
<tr><td><strong>Max Acceleration (mm/s²)</strong></td><td>X/Y: 1000 &nbsp;&nbsp; Z: 100 &nbsp;&nbsp; E: 10000</td></tr>
<tr><td><strong>Build Volume</strong></td><td>220 × 220 × 230 mm</td></tr>
</table>

<hr>

<h3>🧊 Temperature &amp; Cooling</h3>
<table>
<tr><td><strong>Hotend Sensor</strong></td><td>EPCOS 100K (type 1)</td></tr>
<tr><td><strong>Bed Sensor</strong></td><td>EPCOS 100K (type 1)</td></tr>
<tr><td><strong>Thermal Protection</strong></td><td>Enabled (hotend &amp; bed)</td></tr>
<tr><td><strong>Auto Temperature Mode</strong></td><td>Enabled (<code>AUTOTEMP</code>)</td></tr>
<tr><td><strong>E0 Auto Fan</strong></td><td>Pin 1, activates at 50 °C</td></tr>
<tr><td><strong>Fan Kickstart</strong></td><td>100 ms</td></tr>
</table>

<hr>

<h3>🏠 Homing &amp; Bed Leveling</h3>
<table>
<tr><td><strong>Z Safe Homing</strong></td><td>Enabled (center of bed)</td></tr>
<tr><td><strong>Auto Bed Leveling</strong></td><td>Bilinear</td></tr>
<tr><td><strong>Software Endstops</strong></td><td>Enabled</td></tr>
<tr><td><strong>Endstop Interrupts</strong></td><td>Enabled</td></tr>
<tr><td><strong>Endstop Logic</strong></td><td>Inverted (active LOW)</td></tr>
</table>

<hr>

<h3>🧪 Additional Features</h3>
<table>
<tr><td><strong>Linear Advance</strong></td><td>Enabled (<code>K = 0.4</code>)</td></tr>
<tr><td><strong>Arc Support</strong></td><td>Enabled (G2/G3)</td></tr>
<tr><td><strong>Custom Boot Screen</strong></td><td>Enabled</td></tr>
<tr><td><strong>EEPROM Storage</strong></td><td>Enabled (saves calibration data)</td></tr>
</table>

<hr>

<h3>🧩 Flashing Instructions</h3>

<ol>
<li>Connect the <strong>Arduino Mega 2560</strong> to your computer via USB.</li>
<li>Open the <code>Marlin.ino</code> file in the Arduino IDE (or use <strong>PlatformIO</strong> in VS Code).</li>
<li>Select the correct board and port:<br>
&nbsp;&nbsp;&nbsp;&nbsp;• Tools → Board → <em>Arduino Mega or Mega 2560</em><br>
&nbsp;&nbsp;&nbsp;&nbsp;• Tools → Port → (your COM port)</li>
<li>Click the <strong>Upload</strong> button to flash the firmware.</li>
<li>Once complete, reboot the printer and verify the boot screen reads:<br>
<p align="center"><code>Happy Toaster – Toaster Erection Co.</code></p></li>
</ol>

<p align="center">
The custom <strong>Marlin Firmware</strong> for the <em>Happy Toaster</em> 3D Printer is located in:<br/><br/>
<code>Marlin-2.1.2/</code>
</p>

<p align="center">
Inside, you'll find the complete configuration used for this build.<br/>
It’s ready to compile and flash using the <strong>Arduino IDE</strong> or <strong>PlatformIO</strong> on the <strong>Arduino Mega 2560 + RAMPS 1.4</strong> board.
</p>

<p align="center"><em>After successful flashing, your machine should display the custom boot screen and all configured settings can be verified from the LCD under <strong>Control → Motion</strong>.</em></p>

## 🏁 Final Steps: Testing, Calibration & First Print

Before you start printing, follow these essential checks to ensure your **Happy Toaster** runs safely and accurately.

### 1. Power-On & Initial Checks
1. Verify all wiring connections: stepper motors, endstops, thermistors, heaters, and display.  
2. Ensure the MOSFET module is wired correctly to the heated bed and power supply.  
3. Connect the Arduino Mega 2560 to your computer via USB and power the printer.  
4. Confirm the LCD display powers on and shows the custom **Happy Toaster** boot screen.  

> ⚠️ **Safety tip:** Never touch moving parts, hotend, or heated bed while powered. Always wear safety glasses.

---

### 2. Homing & Axis Movement
1. From the LCD menu, select **Control → Motion → Auto Home**.  
2. Observe each axis moving smoothly and stopping at the endstops.  
3. Move each axis manually using the LCD controls to ensure no binding occurs.  
4. Adjust belts or wheel tension if any axis feels rough or misaligned.

---

### 3. Z-Probe & Bed Leveling
1. Check that the **M8 inductive Z-probe** is mounted securely and triggers when the bed approaches.  
2. Perform **Auto Bed Leveling (Bilinear)** from the LCD menu:
   - The probe will measure points across the bed.  
   - The firmware uses these measurements to compensate during printing.  
3. Adjust the Z-offset so the nozzle just touches a piece of paper on the bed.  

> Tip: Recheck after a few test prints — small tweaks improve first-layer adhesion dramatically.

---

### 4. Heating Test
1. Preheat the **hotend** (e.g., 200 °C) and **bed** (e.g., 60 °C) using the LCD menu.  
2. Ensure thermistors read temperatures correctly and heating is stable.  
3. Check for unusual smells, sparks, or noises — stop immediately if anything seems wrong.

---

### 5. First Test Print
1. Load filament into the Bowden extruder.  
2. Use a small calibration object, like a **20 mm cube** or **benchy**, to verify movement, extrusion, and leveling.  
3. Observe the print for:
   - Correct first layer adhesion  
   - Smooth extrusion  
   - Accurate dimensions (adjust steps/mm if needed)  

> Tip: Start at slow speed (~30 mm/s) for the first print to reduce chances of failure.

---

### 6. Maintenance & Adjustments
- Tighten screws, belts, and couplers after a few prints.  
- Keep the V-slot wheels and rods clean for smooth motion.  
- Store extra T-nuts, screws, and zip ties — they’re always handy for mods.  

With these final checks, your **Happy Toaster** is ready for full-scale printing! 🎉

## Project Final
<p align="center"> <img src="images/Screenshot 2025-11-01 153037.png" width="1000"><br>  </p>
