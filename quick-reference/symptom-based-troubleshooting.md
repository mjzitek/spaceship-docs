# SYMPTOM-BASED TROUBLESHOOTING GUIDE
**When Customers Can't Identify the Problem System**

## PURPOSE
Use this guide when customers report vague symptoms and can't identify which system is malfunctioning. This guide translates customer descriptions into specific systems and troubleshooting paths.

**Customer says: "Something's wrong but I don't know what" → This guide helps you identify the system**

---

## 🎯 HOW TO USE THIS GUIDE

1. **Listen for key words** in customer description
2. **Find matching symptom category** below
3. **Ask clarifying questions** from that section
4. **Route to appropriate documentation** once system identified

---

## 🔥 SENSORY SYMPTOMS

### "I SMELL SOMETHING"

#### Burning Smell
**URGENT - Potential fire hazard**

**Ask:**
- Where is the smell strongest?
- Is there visible smoke?
- Is it a chemical, electrical, or plastic burning smell?

**Likely Systems:**
- 🔴 **Electrical fire** → [EMERG-002: Fire](../emergency-procedures/emerg-002-fire.md)
- 🔴 **Reactor overheating** → [EMERG-005: Reactor](../emergency-procedures/emerg-005-reactor-emergency.md)
- 🟠 **Overloaded circuit** → [Power System](../manuals/power/power-distribution-networks.md)
- 🟠 **Overheating equipment** → Check which system in affected area

**Immediate Actions:**
1. Locate source (don't open panels if extremely hot)
2. Check for smoke or visible fire
3. If fire confirmed → Emergency fire protocol
4. If no fire but persistent smell → Shut down suspected system

---

#### Chemical/Sweet Smell
**URGENT - Potential coolant leak**

**Ask:**
- Any wetness or puddles visible?
- Is the smell strongest near engineering?
- Any temperature warnings?

**Likely Systems:**
- 🔴 **Coolant leak** → [Coolant System](../manuals/power/coolant-system-maintenance.md)
- 🟠 **Hydraulic fluid leak** → Check airlocks, cargo doors, landing gear
- 🟡 **Cleaning chemicals** → Verify maintenance wasn't recently performed

**Immediate Actions:**
1. Check radiation levels (coolant may be radioactive)
2. Check coolant reservoir levels
3. Look for puddles or wet spots
4. Reduce reactor output if coolant suspected

---

#### Sewage/Rotten Smell
**Standard - Waste system issue**

**Ask:**
- Strongest near head facilities?
- When did it start?
- Any recent waste system warnings?

**Likely Systems:**
- 🟡 **Waste management** → [Life Support: Water](../manuals/life-support/water-processing.md)
- 🟡 **Water processing contamination** → [Life Support: Water](../manuals/life-support/water-processing.md)
- 🟡 **Blocked drain or vent**

**Immediate Actions:**
1. Check waste tank levels (may be full)
2. Check water purification system
3. Verify waste processing is operating
4. Check for plumbing blockages

---

### "I HEAR SOMETHING"

#### Alarm/Beeping Sound
**Varies - Identify the alarm**

**Ask:**
- Continuous tone or intermittent beeps?
- Can you see any warning lights or messages?
- Where is the sound coming from?

**Likely Systems:**
- Check main console for active alarms
- Each system has distinct alarm tone:
  - **Fast beeping** = Urgent warning
  - **Slow beeping** = Caution/advisory
  - **Continuous tone** = Emergency
  - **Warbling** = Fire alarm

**Immediate Actions:**
1. Check main warning panel
2. Identify which system is alarming
3. Read error message or warning
4. Route to appropriate system guide

---

#### Grinding/Scraping Sound

**Ask:**
- Constant or only during movement?
- Where is it coming from?
- When did it start?

**Likely Systems:**
- 🟠 **Cargo door/bay** → [Cargo Operations](../manuals/cargo/cargo-bay-operations.md)
- 🟠 **Airlock mechanism** → [Hull Integrity](../manuals/hull-integrity/hull-integrity-overview.md)
- 🟡 **HVAC fans** → [Environmental Controls](../manuals/environmental/environmental-control-system.md)
- 🟡 **Gyroscopes** → [Navigation](../manuals/navigation/navigation-overview.md)

**Immediate Actions:**
1. Stop operation of suspected system
2. Visual inspection if accessible
3. Check for obstruction or binding
4. Don't force operation if grinding continues

---

#### Hissing Sound
**URGENT - Potential pressure leak**

**Ask:**
- Constant or intermittent?
- Getting louder?
- Can you locate the source?

**Likely Systems:**
- 🔴 **Hull breach/air leak** → [EMERG-001: Hull Breach](../emergency-procedures/emerg-001-hull-breach.md)
- 🔴 **Coolant leak** → [Coolant System](../manuals/power/coolant-system-maintenance.md)
- 🟠 **Hydraulic leak** → Check doors, actuators
- 🟡 **Pneumatic system** → Normal operation sound

**Immediate Actions:**
1. Check atmospheric pressure (dropping = leak)
2. Check coolant pressure
3. Listen with stethoscope or by ear to locate
4. If pressure dropping → Emergency hull breach protocol

---

#### Rattling/Vibration

**Ask:**
- Continuous or intermittent?
- Worse during acceleration/maneuvering?
- Specific location?

**Likely Systems:**
- 🟡 **Loose cargo** → [KB-045: Cargo Shifted](../kb-articles/kb-045-cargo-shifted-during-transit.md)
- 🟡 **Engine mount issue** → [Propulsion](../manuals/propulsion/propulsion-overview.md)
- 🟡 **Structural stress** → [Hull Inspection](../manuals/hull-integrity/hull-inspection-procedures.md)
- 🟢 **Normal operation** in some conditions

**Immediate Actions:**
1. Reduce acceleration
2. Check cargo restraints
3. Visual inspection of affected area
4. Check structural stress indicators

---

### "I SEE SOMETHING"

#### Smoke
**EMERGENCY - Immediate response required**

**Ask:**
- How much smoke? (Wisp vs. billowing)
- Color of smoke? (White, black, gray)
- Source location?

**Likely Systems:**
- 🔴 **Fire** → [EMERG-002: Fire](../emergency-procedures/emerg-002-fire.md)
- 🔴 **Electrical short** → [Power System](../manuals/power/power-distribution-networks.md)

**Immediate Actions:**
1. **EMERGENCY PROTOCOL**
2. Identify fire location
3. Deploy fire suppression
4. Evacuate affected area if necessary

---

#### Sparks

**URGENT**

**Ask:**
- From specific equipment or panel?
- Continuous or brief flash?
- Any smell of burning?

**Likely Systems:**
- 🔴 **Electrical short** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🔴 **Overloaded circuit** → [Power Distribution](../manuals/power/power-distribution-networks.md)

**Immediate Actions:**
1. Shut off power to affected circuit
2. Do not touch anything until power confirmed off
3. Inspect for damage
4. Do not restore power until issue resolved

---

#### Fluid Leaking

**Ask:**
- What color is the fluid?
- How fast is it leaking?
- Where is it coming from?

**By Fluid Color:**
- **Clear/Blue** = Coolant (potentially radioactive)
- **Clear** = Water
- **Yellow/Amber** = Hydraulic fluid
- **Red** = Certain coolants or hydraulic fluids
- **Dark Brown/Black** = Waste or oil

**Likely Systems:**
- 🔴 **Coolant** (if blue/sweet smell) → [Coolant System](../manuals/power/coolant-system-maintenance.md)
- 🟠 **Hydraulic** → Check actuators, doors, landing gear
- 🟡 **Water** → [Water Processing](../manuals/life-support/water-processing.md)
- 🟡 **Waste** → Waste system maintenance

**Immediate Actions:**
1. Check radiation if coolant suspected
2. Contain leak if possible
3. Check reservoir/tank levels
4. Determine leak rate (drops vs. stream)

---

## 🌡️ ENVIRONMENTAL SYMPTOMS

### "IT'S TOO HOT/COLD"

**Ask:**
- Temperature reading?
- Whole ship or specific area?
- How long has it been this way?
- Getting worse or stable?

**Likely Systems:**
- 🟡 **Environmental controls** → [Environmental System](../manuals/environmental/environmental-control-system.md)
- 🟠 **Reactor overheating** (if hot) → [Reactor Troubleshooting](../manuals/power/power-system-troubleshooting.md)
- 🟡 **HVAC failure** → [Environmental System](../manuals/environmental/environmental-control-system.md)

**Diagnostic Questions:**
- Check thermostat setting
- Check HVAC system status
- Check for blocked vents
- If reactor area hot → Check coolant system

**Route to:** [Top 20 #8: Temperature Extremes](./top-20-common-issues.md#8-environmental-controls---temperature-extremes)

---

### "I CAN'T BREATHE WELL" or "AIR FEELS WRONG"

**URGENT - Potential life support issue**

**Ask:**
- How many crew affected?
- Any symptoms? (Headache, dizziness, nausea)
- Any alarms or warnings?
- O2 and CO2 levels?

**Likely Systems:**
- 🔴 **O2 depletion** → [EMERG-003: Life Support](../emergency-procedures/emerg-003-life-support.md)
- 🔴 **CO2 buildup** → [EMERG-003: Life Support](../emergency-procedures/emerg-003-life-support.md)
- 🔴 **Toxic atmosphere** → [EMERG-003: Life Support](../emergency-procedures/emerg-003-life-support.md)
- 🟠 **Sensor malfunction** → [KB-027: Low O2](../kb-articles/kb-027-low-oxygen-alert.md)

**Immediate Actions:**
1. Check O2 levels (should be 19.5-23%)
2. Check CO2 levels (should be < 0.5%)
3. Verify atmospheric processing is operating
4. If levels abnormal → Emergency life support protocol
5. If levels normal → May be sensor issue or other cause

**Route to:** [KB-027: Low Oxygen Alert](../kb-articles/kb-027-low-oxygen-alert.md)

---

### "IT'S HUMID/DAMP" or "EVERYTHING'S DRY"

**Ask:**
- Humidity reading if available?
- Any condensation visible?
- Any leaks?

**Likely Systems:**
- 🟡 **Environmental controls** → [Environmental System](../manuals/environmental/environmental-control-system.md)
- 🟡 **Water leak** (if humid) → [Water Processing](../manuals/life-support/water-processing.md)
- 🟡 **HVAC dehumidifier** → [Environmental System](../manuals/environmental/environmental-control-system.md)

**Immediate Actions:**
1. Check humidity sensors
2. Check for water leaks
3. Check dehumidifier operation
4. Verify HVAC settings

---

## ⚡ PERFORMANCE SYMPTOMS

### "EVERYTHING IS SLOW"

**Ask:**
- Computer systems slow or ship movement slow?
- Gradual slowdown or sudden?
- Any power warnings?

**If Computer Systems Slow:**
- 🟡 **Computer overload** → Check CPU/memory usage
- 🟡 **Software issue** → Restart control computers
- 🟠 **Power issue affecting computers** → [Power System](../manuals/power/power-distribution-networks.md)

**If Ship Movement Slow:**
- 🟡 **Engine power reduced** → [Propulsion](../manuals/propulsion/propulsion-overview.md)
- 🟡 **Fuel low** → Check fuel levels
- 🟡 **Power insufficient** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🟡 **Thruster malfunction** → [Propulsion](../manuals/propulsion/propulsion-overview.md)

---

### "THINGS KEEP SHUTTING OFF/RESTARTING"

**URGENT if critical systems affected**

**Ask:**
- Which systems restarting?
- How often?
- Any pattern (same time, during specific operations)?
- Any power warnings?

**Likely Systems:**
- 🔴 **Power distribution issue** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🟠 **Power fluctuations** → [Top 20 #6](./top-20-common-issues.md#6-power-fluctuationsbbrownouts)
- 🟠 **Overheating components** → Check cooling systems
- 🟠 **Software bugs** → Check for updates

**Route to:** [Top 20 #20: Intermittent System Resets](./top-20-common-issues.md#20-intermittent-system-resets)

---

### "IT'S NOT RESPONDING" or "CONTROLS DON'T WORK"

**Ask:**
- Which specific controls?
- Completely unresponsive or delayed?
- Any error messages?
- When did it start?

**Likely Systems:**
- 🟠 **Control computer** → Restart affected system
- 🟠 **Power to controls** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🟡 **Interface issue** → Check display and input devices
- 🟡 **Software crash** → Reboot control system

**Immediate Actions:**
1. Try backup controls if available
2. Check power to control panel
3. Restart control computer
4. Switch to manual mode if available

---

## 🚢 MOTION/HANDLING SYMPTOMS

### "SHIP IS DRIFTING" or "CAN'T MAINTAIN COURSE"

**Ask:**
- How much drift? (meters, kilometers)
- Constant direction or random?
- RCS thrusters responding?
- Autopilot engaged?

**Likely Systems:**
- 🟡 **Navigation drift** → [Top 20 #12](./top-20-common-issues.md#12-navigation-driftposition-errors)
- 🟡 **Thruster imbalance** → [Propulsion](../manuals/propulsion/propulsion-overview.md)
- 🟡 **Gyroscope calibration** → [Navigation](../manuals/navigation/navigation-overview.md)
- 🟡 **External forces** → Check for gravity sources, solar wind

**Route to:** [Top 20 #12: Navigation Drift](./top-20-common-issues.md#12-navigation-driftposition-errors)

---

### "SHIP IS SHAKING/VIBRATING ABNORMALLY"

**URGENT if severe or increasing**

**Ask:**
- Constant or intermittent?
- During specific operations (acceleration, turning)?
- Severity (minor annoyance vs. violent shaking)?

**Likely Systems:**
- 🔴 **Critical structural failure** (if severe) → [Hull Integrity](../manuals/hull-integrity/hull-integrity-overview.md)
- 🟠 **Engine problem** → [Propulsion](../manuals/propulsion/propulsion-overview.md)
- 🟠 **Loose cargo** → [KB-045: Cargo Shifted](../kb-articles/kb-045-cargo-shifted-during-transit.md)
- 🟡 **Thruster misfire** → [Propulsion](../manuals/propulsion/propulsion-overview.md)

**Immediate Actions:**
1. Reduce speed/acceleration
2. Check cargo restraints
3. Check engine indicators
4. Check structural stress indicators
5. If severe → Emergency shutdown and inspection

---

### "CAN'T ACCELERATE/DECELERATE PROPERLY"

**Ask:**
- Engines responding at all?
- Partial power or no power?
- Fuel levels?
- Any error codes?

**Likely Systems:**
- 🟠 **Engine malfunction** → [Propulsion](../manuals/propulsion/propulsion-overview.md)
- 🟠 **Fuel system** → Check fuel levels and flow
- 🟠 **Power to engines** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🟡 **Thruster problem** → [Propulsion](../manuals/propulsion/propulsion-overview.md)

---

## 💻 DISPLAY/INTERFACE SYMPTOMS

### "SCREEN SHOWS WEIRD THINGS" or "DISPLAY WRONG"

**Ask:**
- Which display/screen?
- What's wrong? (Flickering, wrong info, frozen, blank)
- All screens or just one?

**Likely Systems:**
- 🟡 **Display hardware** → Replace/restart display
- 🟡 **Computer glitch** → Restart control computer
- 🟠 **Sensor data corrupt** → Check sensor systems
- 🟡 **Power fluctuation** → [Power Distribution](../manuals/power/power-distribution-networks.md)

**Immediate Actions:**
1. Restart affected display
2. Check power to display
3. Switch to backup display if available
4. Verify data source (sensors, computers) is working

---

### "CAN'T SEE ANYTHING" or "SCREEN IS BLANK"

**Ask:**
- All screens or specific screen?
- Completely black or just no data?
- Any sounds/indicators showing system is on?

**Likely Systems:**
- 🟠 **Power to displays** → [Power Distribution](../manuals/power/power-distribution-networks.md)
- 🟡 **Display failure** → Hardware replacement
- 🟠 **Control computer crashed** → Restart computer
- 🟡 **Brightness turned down** → Check brightness setting

---

### "GETTING ERRORS BUT DON'T KNOW WHAT THEY MEAN"

**Ask:**
- What's the exact error code or message?
- When does it appear?
- Can you take a picture/write it down?

**Route to Error Code References:**
- **PWR-xxx** → [Error Codes: Power](../error-codes/error-codes-power.md)
- **NAV-xxx** → [Error Codes: Navigation](../error-codes/error-codes-navigation.md)
- **COM-xxx** → [Error Codes: Communications](../error-codes/error-codes-communications.md)
- **SEN-xxx** → [Error Codes: Sensors](../error-codes/error-codes-sensors.md)

---

## 🔌 CONNECTIVITY SYMPTOMS

### "CAN'T CONNECT TO..." (Other Ships, Stations, Networks)

**Ask:**
- Connect to what? (Comms, network, docking, etc.)
- Any error messages?
- When did it last work?
- Are you in range?

**Likely Systems:**
- 🟡 **Communications** → [Comms Protocols](../manuals/communications/communications-protocols.md)
- 🟡 **Encryption** → [Top 20 #18](./top-20-common-issues.md#18-encryption-key-exchange-failure)
- 🟡 **Network** → Check network settings
- 🟡 **Range** → Verify you're within range

**Route to:** [Top 20 #4: Communications Interference](./top-20-common-issues.md#4-communications-interferferencestatic)

---

### "LOST SIGNAL/SIGNAL WEAK"

**Ask:**
- What kind of signal? (Comms, GPS/nav beacon, sensor)
- Completely lost or weak/intermittent?
- When/where did you lose it?

**Likely Systems:**
- 🟡 **Communications** → [Signal Processing](../manuals/communications/signal-processing.md)
- 🟡 **Navigation beacons** → [Navigation](../manuals/navigation/navigation-overview.md)
- 🟡 **Antenna orientation** → Check antenna tracking
- 🟡 **Interference** → [Comms Error Codes](../error-codes/error-codes-communications.md)

---

## 🎚️ MULTI-SYSTEM SYMPTOMS

### "MULTIPLE THINGS FAILING AT ONCE"

**URGENT - Possible cascade failure**

**Ask:**
- Which systems are affected?
- Did they fail simultaneously or one after another?
- Any power warnings?
- Any recent events (combat, collision, maintenance)?

**Likely Causes:**
- 🔴 **Power failure** → [Power System](../manuals/power/power-distribution-networks.md)
- 🔴 **Control computer failure** → Restart main computer
- 🔴 **Hull damage** → [Hull Integrity](../manuals/hull-integrity/hull-integrity-overview.md)
- 🟠 **Cascade failure** → [System Interaction Matrix](./system-interaction-matrix.md)

**Immediate Actions:**
1. Check reactor status and power generation
2. Check life support (priority system)
3. Check for hull damage
4. Identify root cause system (others may be secondary failures)

**Route to:** [System Interaction Matrix](./system-interaction-matrix.md) to understand dependencies

---

### "SOMETHING'S WRONG BUT CAN'T PINPOINT IT"

**Ask specific questions:**
- Any alarms or warnings (even if acknowledged)?
- Any unusual readings on any displays?
- Performance normal or degraded?
- When did you first notice something was off?
- Has anything changed recently?

**Diagnostic Approach:**
1. Methodically check each major system
2. Review system logs for errors
3. Check sensor data for anomalies
4. Compare current readings to baseline
5. Look for trends (deteriorating vs. stable)

**Common Hidden Issues:**
- Slow pressure leak (hard to detect)
- Gradual coolant loss
- Sensor drift making readings unreliable
- Intermittent electrical problem
- Software bug causing subtle issues

---

## 🔧 ACTION-BASED SYMPTOMS

### "I TRIED TO [ACTION] AND IT DIDN'T WORK"

**Common Actions and Quick Routes:**

#### "Start the reactor"
→ [KB-001: Reactor Won't Start](../kb-articles/kb-001-reactor-wont-start.md)

#### "Jump to FTL"
→ [KB-012: FTL Jump Fails](../kb-articles/kb-012-ftl-jump-fails.md)

#### "Open/close cargo door"
→ [Top 20 #16: Cargo Door](./top-20-common-issues.md#16-cargo-bay-door-wont-openclose)

#### "Open/close airlock"
→ [Top 20 #13: Airlock Malfunction](./top-20-common-issues.md#13-airlock-malfunction)

#### "Activate shields"
→ [Top 20 #10: Shields Not Activating](./top-20-common-issues.md#10-shields-not-activating)

#### "Lock onto target"
→ [Top 20 #15: Targeting System Errors](./top-20-common-issues.md#15-targeting-system-errors)

#### "Send a message"
→ [Top 20 #4: Communications Interference](./top-20-common-issues.md#4-communications-interferferencestatic)

---

## 📊 DECISION FLOWCHART

```
Customer calls with vague symptom
           ↓
    [First Responder Checklist]
           ↓
    Safety concerns? → YES → [Emergency Protocol]
           ↓ NO
    Can identify system? → YES → [System-specific docs]
           ↓ NO
    [Use this Symptom Guide]
           ↓
    Match symptom category
           ↓
    Ask clarifying questions
           ↓
    Identify likely system(s)
           ↓
    Route to appropriate documentation
           ↓
    Begin troubleshooting
```

---

## 💡 TIPS FOR USING THIS GUIDE

### Listen for These Keywords:
- **Sensory**: smell, hear, see, feel, taste
- **Environmental**: hot, cold, stuffy, humid, dry
- **Performance**: slow, fast, erratic, unstable
- **Motion**: shaking, drifting, vibrating
- **Connectivity**: can't connect, lost signal, no response
- **Display**: error, warning, alarm, message

### Ask Open-Ended Follow-Ups:
- "Tell me more about that..."
- "What else are you noticing?"
- "Walk me through what happens when you..."
- "What was the ship doing when this started?"

### Don't Assume:
- Customer may not know technical terms
- "Not working" could mean many things
- What they think is the problem may not be
- Verify everything they tell you when possible

### Build a Mental Model:
- Picture the ship and its systems
- Think about how systems interact
- Consider what could cause the described symptom
- Eliminate possibilities with targeted questions

---

## 🔗 QUICK LINKS

- [First Responder Checklist](./first-responder-checklist.md) - Start here for every call
- [Help Desk Index](./HELP-DESK-INDEX.md) - Central navigation once system identified
- [Top 20 Common Issues](./top-20-common-issues.md) - Quick solutions for frequent problems
- [System Interaction Matrix](./system-interaction-matrix.md) - Multi-system failures
- [All KB Articles](../kb-articles/) - Detailed troubleshooting procedures
- [All Error Codes](../error-codes/) - If customer has error code

---

**Document Version:** 1.0 | **Last Updated:** Stardate 2438.11
**Use Case:** For vague customer descriptions where system is not immediately obvious
