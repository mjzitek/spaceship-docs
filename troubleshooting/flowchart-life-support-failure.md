# Troubleshooting Flowchart: Life Support System Failure

**System:** Atmospheric Processing Unit (APU) and Water Recycling
**Document Type:** Decision Tree / Flowchart
**Last Updated:** 2847.09.14

## How to Use This Flowchart

1. Start at "BEGIN" and answer each question
2. Follow the arrows based on your answers
3. Each endpoint provides a SOLUTION reference
4. Solutions lettered A-N at bottom of document
5. If solution doesn't resolve, return to flowchart and try alternate path

---

## Main Flowchart

```
BEGIN: Life Support Issue
        │
        ├─────────────────────────────┬─────────────────────────────┐
        │                             │                             │
    O₂ Issue?                     Water Issue?              Temperature Issue?
        │                             │                             │
        YES                          YES                           YES
        │                             │                             │
        ↓                             ↓                             └→ See KB-018 (Temp Control)
                                                                       SOLUTION N
┌───────────────────┐         ┌───────────────────┐
│  O₂ Problem Path  │         │  Water Problem    │
└───────────────────┘         │      Path         │
                              └───────────────────┘

═══════════════════════════════════════════════════════════════════
OXYGEN PROBLEM PATH
═══════════════════════════════════════════════════════════════════

O₂ Level?
   │
   ├─ <16%: CRITICAL EMERGENCY → Deploy Emergency O₂ → SOLUTION A1
   ├─ 16-18%: URGENT → Continue troubleshooting quickly
   └─ >18%: Degraded but safe → Continue troubleshooting systematically

APU Panel Status?
   │
   ├─ Panel Dark (no lights) → Check Power
   │    │
   │    ├─ No power to APU → Circuit breaker tripped?
   │    │    │
   │    │    ├─ YES → Reset breaker → SOLUTION A
   │    │    └─ NO → Check reactor output
   │    │         │
   │    │         ├─ Reactor <40% → Reactor issue → See KB-015
   │    │         └─ Reactor OK → Wiring fault → SOLUTION B
   │    │
   │    └─ Power present but panel dark → Panel failure → SOLUTION C
   │
   ├─ Panel ON, showing errors → What error code?
   │    │
   │    ├─ E-LIFE-101 to E-LIFE-110 → APU component failure
   │    │    │
   │    │    ├─ E-LIFE-101 (Electrolysis unit) → SOLUTION D
   │    │    ├─ E-LIFE-102 (CO₂ scrubber) → SOLUTION E
   │    │    ├─ E-LIFE-105 (Water supply) → Cross-ref Water Path
   │    │    └─ Other codes → See ERR-LIFE-100 reference
   │    │
   │    └─ E-LIFE-201 to E-LIFE-215 → Environmental (see Temp path)
   │
   └─ Panel ON, no errors, but O₂ still low
        │
        ├─ Check O₂ sensor accuracy → Test with portable O₂ meter
        │    │
        │    ├─ Sensor reading low but actual O₂ normal → SOLUTION F
        │    └─ Sensor accurate, O₂ actually low → Continue
        │
        ├─ Check for O₂ leaks → Hull breach? See ERR-HULL sensors
        │    │
        │    ├─ Breach detected → EMERG-007 (Hull Breach) → SOLUTION G
        │    └─ No breach → Continue
        │
        └─ APU running but insufficient O₂ production
             │
             ├─ How many crew vs APU rated capacity?
             │    │
             │    ├─ Crew > capacity → Overloaded → SOLUTION H
             │    └─ Within capacity → APU degraded performance
             │
             ├─ Check water supply to electrolysis unit
             │    │
             │    ├─ Water tank empty/low → Fill tank → SOLUTION I
             │    └─ Water supply adequate → Continue
             │
             ├─ Check electrolysis current/voltage
             │    │
             │    ├─ Abnormal readings → Electrolysis unit degraded → SOLUTION D
             │    └─ Normal readings → Continue
             │
             └─ Check HEPA filters and air circulation
                  │
                  ├─ Filters clogged → Replace filters → SOLUTION J
                  └─ Filters OK → APU throughput issue → SOLUTION K

═══════════════════════════════════════════════════════════════════
WATER PROBLEM PATH
═══════════════════════════════════════════════════════════════════

Water Issue Type?
   │
   ├─ No water output → WRMS not producing water
   │    │
   │    ├─ WRMS panel status?
   │    │    │
   │    │    ├─ Panel dark → Check power
   │    │    │    │
   │    │    │    ├─ Breaker tripped → Reset → SOLUTION A
   │    │    │    └─ Breaker OK → Wiring or panel fault → SOLUTION B/C
   │    │    │
   │    │    └─ Panel ON, showing error?
   │    │         │
   │    │         ├─ E-LIFE-301 (RO membrane) → SOLUTION L1
   │    │         ├─ E-LIFE-302 (UV sterilizer) → SOLUTION L2
   │    │         ├─ E-LIFE-305 (Low input) → SOLUTION L3
   │    │         └─ Other → See ERR-LIFE-100
   │    │
   │    └─ Check source water supply
   │         │
   │         ├─ Gray water tank empty → No water to recycle → SOLUTION L3
   │         └─ Gray water present → Pump or filter issue → SOLUTION L4
   │
   ├─ Water output low (reduced flow) → Partially working
   │    │
   │    ├─ Check filters in WRMS
   │    │    │
   │    │    ├─ Sediment filter clogged → Replace → SOLUTION L5
   │    │    ├─ RO membrane fouled → Clean or replace → SOLUTION L1
   │    │    └─ Filters OK → Pump degraded → SOLUTION L4
   │    │
   │    └─ Check for leaks in system
   │         │
   │         ├─ Leak detected → Repair leak → SOLUTION L6
   │         └─ No leak → Continue above
   │
   └─ Water quality issue (contaminated, bad taste/smell)
        │
        ├─ What's wrong with water?
        │    │
        │    ├─ Cloudy or particles → Sediment filter → SOLUTION L5
        │    ├─ Bad smell → Biological contamination → SOLUTION M
        │    ├─ Metallic taste → Dissolved metals → SOLUTION L7
        │    └─ Other → Test water quality → SOLUTION L8
        │
        └─ Check UV sterilizer status
             │
             ├─ UV lamp failed → Replace → SOLUTION L2
             └─ UV OK → Continue above

═══════════════════════════════════════════════════════════════════
MULTIPLE SYSTEMS AFFECTED PATH
═══════════════════════════════════════════════════════════════════

If O₂ AND Water AND Temperature all affected:
   │
   └─ Likely ship-wide issue, not life support specific
        │
        ├─ Check reactor power output
        │    │
        │    ├─ Low power → See KB-015 (Reactor Low Output)
        │    └─ Power OK → Continue
        │
        ├─ Check main computer status
        │    │
        │    ├─ Computer fault → May be false readings → Reboot
        │    └─ Computer OK → Continue
        │
        └─ Multiple real failures → See EMERG-009 (Multiple System Failure)
```

---

## Solutions Reference

### SOLUTION A: No Power - Reset Circuit Breaker

**Steps:**
1. Locate electrical panel (usually engineering section)
2. Find LIFE SUPPORT or APU/WRMS breaker
3. If tripped (middle position or OFF):
   - Switch to OFF
   - Wait 10 seconds
   - Switch to ON
4. APU/WRMS should power up within 30 seconds
5. Check that O₂ production resumes (takes 2-3 minutes to see level change)

**If breaker immediately trips again:**
- Short circuit present
- DO NOT repeatedly reset
- See SOLUTION B

**Reference:** KB-027, Section: Power Supply Issues

---

### SOLUTION A1: CRITICAL - Deploy Emergency O₂

**URGENT - O₂ <16% is CRITICAL**

**Immediate Actions:**
1. **Open emergency O₂ bottles** (stored in wall compartments):
   - Red-handled valve, turn counterclockwise
   - One bottle per crew member minimum
   - Buys 6-8 hours per bottle
2. **Reduce crew activity:**
   - Sit or lie down
   - No running or physical exertion
   - Conserve oxygen
3. **Seal off unused compartments:**
   - Close doors to unoccupied areas
   - Reduces volume to oxygenate
4. **Call for help:**
   - Emergency frequency 121.5 MHz
   - State: "Mayday, life support failure, O₂ critical"
   - Give position and crew size

**Then continue troubleshooting APU while emergency O₂ sustains crew.**

**Time Critical:** Crew has limited time at <16% O₂:
- 16%: Cognitive impairment, must fix within hours
- 14%: Severe impairment, risk of unconsciousness
- <12%: Unconsciousness imminent

**Reference:** KB-027, EMERG-004

---

### SOLUTION B: Wiring Fault Between Breaker and APU/WRMS

**Symptoms:**
- Breaker ON but no power reaching system
- No tripping when reset

**Steps:**
1. Verify voltage at breaker output: Should be 380-420 VDC
2. If voltage present at breaker but not at APU/WRMS:
   - Broken wire between breaker and unit
   - Disconnected connector
3. Trace wiring from breaker to unit (may be in conduits or cable trays)
4. Check for:
   - Loose connectors (reseat)
   - Damaged wire (splice or replace)
   - Corrosion on terminals (clean and reconnect)

**Requires:** Electrical knowledge, multimeter

**If uncomfortable with electrical work:** Call for help, use emergency O₂/water while awaiting assistance

---

### SOLUTION C: APU/WRMS Control Panel Failure

**Symptoms:**
- Power reaching panel but display dark or unresponsive
- System may be running but cannot monitor or control

**Steps:**
1. Try hard reboot:
   - Power OFF (breaker or panel switch)
   - Wait 60 seconds
   - Power ON
   - Panel should boot (30-90 seconds)
2. If panel still dark: Panel hardware failure
3. **Workaround:**
   - APU/WRMS may still function even with dead panel
   - Check O₂ levels with portable meter
   - Check water output directly from tap
   - If system still producing O₂/water, panel failure is annoyance not emergency
4. Replace panel at next port (Part #: CTL-APU-A or CTL-WRMS-A)

**Temporary operation without panel:** Possible but blind (no monitoring or adjustment)

---

### SOLUTION D: Electrolysis Unit Failure (O₂ Production)

**Error Code:** E-LIFE-101

**Symptoms:**
- APU panel shows electrolysis unit fault
- No O₂ production or very low
- May see abnormal current/voltage readings

**Steps:**
1. Check electrolysis unit status:
   - Access: APU Panel > Diagnostics > Electrolysis Test
   - Should draw 2-6 kW and produce O₂ proportionally
2. If unit failed test:
   - Check water supply to unit (needs water to make O₂)
   - Check electrode condition (may be scaled or corroded)
3. **Clean electrodes** (if accessible):
   - Power OFF APU
   - Access electrolysis chamber
   - Remove electrodes (typically 6-12 plates)
   - Clean with vinegar or citric acid solution (removes scale)
   - Rinse thoroughly, reinstall
   - Power ON, test
4. **If still failed:**
   - Replace electrolysis unit (Part #: ELEC-O2-A)
   - Requires 2-4 hours to replace
   - Use emergency O₂ during repair

**Reference:** APU Maintenance Manual, Section 3

---

### SOLUTION E: CO₂ Scrubber Failure

**Error Code:** E-LIFE-102

**Symptoms:**
- O₂ level OK but crew feeling lightheaded or short of breath
- CO₂ level elevated (>0.5%)
- CO₂ scrubber not regenerating

**Steps:**
1. Check scrubber status:
   - Access: APU Panel > Diagnostics > Scrubber Test
   - Shows scrubber temperature, pressure, regeneration status
2. **If scrubber not heating (cannot regenerate):**
   - Check heating element (Part #: HEAT-SCRUB-500W)
   - May have failed
   - Replace heating element
3. **If scrubber saturated (full of CO₂, not regenerating):**
   - Force regeneration cycle:
   - Access: APU Panel > Scrubber > Force Regeneration
   - Takes 30-45 minutes
   - During regen, scrubber offline (use backup if equipped)
4. **Replace scrubber chemical bed** (if old or contaminated):
   - Part #: CHEM-LiOH-25KG (lithium hydroxide)
   - Remove old chemical (dispose properly - caustic)
   - Install fresh chemical bed
   - Reset scrubber controller

**Temporary workaround:**
- Open airlock vent briefly to space (vents CO₂)
- Risk: Loses some O₂ also, use sparingly
- Only in severe CO₂ buildup emergency

**Reference:** APU Maintenance Manual, Section 4

---

### SOLUTION F: O₂ Sensor Failure (False Low Reading)

**Symptoms:**
- Sensor shows low O₂ but crew feels fine
- Portable meter shows O₂ normal (20-21%)
- APU producing O₂ normally

**Steps:**
1. Confirm with portable O₂ meter:
   - If reads 20-21%: APU working, sensor wrong
   - If reads <18%: APU not working, sensor correct
2. **Recalibrate O₂ sensor:**
   - Access: APU Panel > Sensors > O₂ Calibration
   - Follow on-screen instructions
   - Usually requires known O₂ concentration (room air ~20.9%)
3. **Replace O₂ sensor** (if calibration doesn't help):
   - Location: In main ventilation duct or APU unit
   - Part #: SENS-O2-A
   - Unplug old sensor
   - Install new sensor (usually threaded fitting)
   - System auto-calibrates (3-5 minutes)

**Not an emergency** if actual O₂ normal, but fix soon (need accurate monitoring)

---

### SOLUTION G: O₂ Loss Due to Hull Breach

**Symptoms:**
- O₂ dropping despite APU working
- Pressure dropping
- Hull breach sensors triggered

**Immediate Actions:**
1. **Seal breach:** Follow EMERG-007 (Hull Breach procedure)
   - Close bulkheads to isolate breach
   - Deploy emergency sealant foam
   - Verify pressure stabilizes
2. **After breach sealed:**
   - APU will replenish O₂ (takes 20-60 minutes depending on APU size)
   - Monitor O₂ level climbing back to 20-21%
   - Use emergency O₂ if needed while APU catches up

**Reference:** EMERG-007 (Hull Breach), KB-027

---

### SOLUTION H: APU Overloaded (Too Many Crew)

**Symptoms:**
- APU running normally but O₂ slowly dropping
- Crew count exceeds APU rated capacity

**Capacity:**
- APU-Compact: 2-4 crew
- APU-Standard: 4-8 crew
- APU-Industrial: 8-16 crew

**If over capacity:**
1. **Reduce O₂ consumption:**
   - Minimize physical activity
   - Seal unused compartments (smaller volume)
   - Lower temperature (crew consumes less O₂ when cool)
2. **Supplement with emergency O₂:**
   - Use bottles to make up deficit
   - Not permanent solution (bottles finite)
3. **Permanent solution:**
   - Reduce crew (drop personnel at next port)
   - Upgrade to larger APU
   - Install second APU (if space available)

**Not an emergency** if short-term (few days), use emergency O₂ to supplement

---

### SOLUTION I: Water Tank Empty - No Water to Make O₂

**Symptoms:**
- Electrolysis unit shows "Low Water" error
- O₂ production stopped or very low
- Water tank gauge showing empty

**Steps:**
1. **Fill water tank:**
   - If docked: Refill from station water supply
   - If in flight: Transfer water from other tanks (if available)
   - Emergency: Can use water from any source (coolant loops - must purify first)
2. **Check for leaks:**
   - If tank repeatedly goes empty, may have leak
   - Inspect tank and connections
   - Repair leak (SOLUTION L6)
3. **Once tank filled:**
   - APU should resume O₂ production within 5 minutes
   - O₂ level should start climbing

**Water requirements for O₂:**
- 1 liter water produces ~620 liters O₂ (at STP)
- 4-person crew needs ~2 kg O₂/day = ~3.2 liters water/day for O₂ production

---

### SOLUTION J: Clogged HEPA Filters

**Symptoms:**
- APU producing O₂ but not circulating well
- Air feels "stuffy"
- Some areas high O₂, others low O₂ (poor mixing)
- Reduced airflow from vents

**Steps:**
1. **Check filter status:**
   - Access: APU Panel > Filters > Status
   - Shows filter pressure drop (should be <2 kPa)
   - If >5 kPa: Filters clogged
2. **Replace HEPA filters:**
   - Location: Return air vents or in APU unit
   - Remove access panel (2-4 screws)
   - Slide out old filter (Part #: FILT-HEPA-A)
   - Install new filter (note airflow direction arrow)
   - Replace panel
3. **Airflow should improve immediately**
4. **Schedule:** Replace filters monthly or when pressure drop >5 kPa

**Not an emergency** but fix soon (poor air circulation causes discomfort and inefficiency)

---

### SOLUTION K: APU Throughput Degraded

**Symptoms:**
- APU running but O₂ production below rated capacity
- No obvious faults
- Unit may be old or poorly maintained

**Steps:**
1. **Run full APU diagnostic:**
   - Access: APU Panel > Diagnostics > Complete System Test
   - Takes 15-20 minutes
   - Identifies weak components
2. **Common degraded components:**
   - Electrolysis electrodes scaled (clean or replace)
   - Compressor worn (less airflow)
   - Heat exchanger fouled (inefficient)
   - Seals leaking (pressure loss)
3. **Perform comprehensive maintenance:**
   - Follow APU Maintenance Manual annual procedures
   - Clean all components
   - Replace worn parts
   - Recalibrate system
4. **If maintenance doesn't restore capacity:**
   - APU may be at end of life (typical 10-15 years)
   - Replace APU unit at next port

**Temporary:** Reduce crew activity, supplement with emergency O₂ as needed

---

### SOLUTION L1: RO Membrane Failure (Water System)

**Error Code:** E-LIFE-301

**Symptoms:**
- Water production stopped or very low
- WRMS shows high pressure or membrane fault

**Steps:**
1. **Check RO membrane status:**
   - Access: WRMS Panel > Diagnostics > Membrane Test
   - Shows membrane pressure, flow, rejection rate
2. **If membrane fouled (clogged):**
   - Run cleaning cycle:
   - Access: WRMS Panel > Maintenance > Membrane Cleaning
   - Uses citric acid to dissolve scale (takes 2 hours)
3. **If cleaning doesn't help:**
   - Replace RO membrane (Part #: MEM-RO-A)
   - Location: Inside WRMS unit, cartridge-style
   - Turn off water supply, release pressure
   - Unscrew old membrane cartridge
   - Install new membrane
   - Prime system, run test
4. **RO membrane lifespan:** 6-18 months depending on water quality

---

### SOLUTION L2: UV Sterilizer Failure

**Error Code:** E-LIFE-302

**Symptoms:**
- Water produced but not sterile (bacteria, bad smell)
- UV lamp not working

**Steps:**
1. **Check UV lamp status:**
   - Access: WRMS Panel > Diagnostics > UV Lamp Test
   - Shows lamp hours and intensity
2. **If lamp failed or weak:**
   - Replace UV lamp (Part #: LAMP-UV-254)
   - Power OFF WRMS
   - Access UV chamber (may require draining)
   - Remove old lamp (quartz tube)
   - Install new lamp (do not touch quartz with bare hands)
   - Power ON, verify lamp illuminated
3. **UV lamp lifespan:** 8,000-10,000 hours (about 12-18 months continuous use)
4. **After replacement:**
   - Run disinfection cycle (SOLUTION M)

---

### SOLUTION L3: Gray Water Tank Empty

**Symptoms:**
- WRMS shows "Low Input" error
- Cannot recycle water (no source water)

**Steps:**
1. **Fill gray water tank:**
   - From crew water usage (sinks, showers, etc.)
   - If tank empty and no water being generated:
     - Use potable water as input (inefficient but works)
     - Or get water from station when docked
2. **Check why gray water not being collected:**
   - Crew not using water (unlikely)
   - Drain lines clogged (water not reaching tank)
   - Leak (water escaping before reaching tank)
3. **In emergency:**
   - Can add any water to gray tank (even coolant - WRMS purifies)
   - Just need volume for system to recycle

---

### SOLUTION L4: Water Pump Failure

**Symptoms:**
- Water in gray tank but WRMS not processing
- Pump not running (no sound) or weak flow

**Steps:**
1. **Check pump status:**
   - Access: WRMS Panel > Diagnostics > Pump Test
   - Should show 15-40 L/min flow and normal pressure
2. **If pump not running:**
   - Check power (breaker, wiring)
   - Check pump motor (may be seized or burned out)
3. **Replace pump** (Part #: PUMP-H2O-A):
   - Power OFF WRMS
   - Close isolation valves on pump inlet/outlet
   - Disconnect electrical
   - Unbolt pump (4 bolts typically)
   - Install new pump with new gaskets
   - Reconnect, test
4. **Pump lifespan:** 5-10 years depending on usage

---

### SOLUTION L5: Sediment Filter Clogged

**Symptoms:**
- Water flow reduced
- WRMS shows high pressure upstream of filter

**Steps:**
1. **Replace sediment filter:**
   - Location: First stage of WRMS, before RO membrane
   - Part #: FILT-SED-5MIC
   - Turn off water flow
   - Unscrew filter housing
   - Remove old filter (may be very dirty)
   - Install new filter
   - Reassemble, restore water flow
2. **Schedule:** Replace monthly or when flow drops significantly

---

### SOLUTION L6: Water System Leak

**Symptoms:**
- Water loss (tanks going empty)
- Visible drips or wet areas
- Water production insufficient

**Steps:**
1. **Locate leak:**
   - Follow water lines, look for drips
   - Check connections, fittings, tank seams
2. **Repair leak:**
   - Tighten loose fittings
   - Replace damaged O-rings or gaskets
   - Patch or replace leaking pipe
   - Seal tank leak with approved sealant
3. **Verify repair:** Run system, check for continued leaking

---

### SOLUTION L7: Metallic Taste in Water

**Symptoms:**
- Water safe but tastes bad (metallic, mineral taste)
- Dissolved metals from piping or tank

**Steps:**
1. **Test water quality:**
   - Use water test kit (Part #: TEST-H2O-A)
   - Check for copper, iron, zinc, lead
2. **If metals present:**
   - Run additional purification cycle
   - Install additional carbon filter (reduces metal taste)
   - Check for corrosion in water lines (replace corroded pipes)

**Not an emergency** but fix for crew morale (bad water discourages drinking)

---

### SOLUTION L8: Water Quality Test and Analysis

**If water problem not obvious, test comprehensively:**

**Test Kit (Part #: TEST-H2O-A) checks:**
- pH (should be 6.5-8.5)
- Bacteria count (should be 0 CFU/mL)
- Dissolved solids (should be <500 ppm)
- Metals (should be negligible)
- Chlorine (if disinfection used, 0.2-2 ppm acceptable)

**Based on test results:**
- High bacteria → UV sterilizer issue (SOLUTION L2) or need disinfection (SOLUTION M)
- High dissolved solids → RO membrane not working (SOLUTION L1)
- Metals → Corrosion issue (SOLUTION L7)
- pH out of range → Check WRMS calibration

---

### SOLUTION M: Water Contamination - Biological

**Symptoms:**
- Water smells bad (musty, rotten egg smell)
- Slimy biofilm in tanks or lines
- Crew illness (diarrhea, nausea)

**Steps:**
1. **DO NOT DRINK** contaminated water
   - Switch to emergency water rations
   - Use water only for non-drinking purposes until decontaminated
2. **Shock chlorination treatment:**
   - Add chlorine tablets to water system (Part #: CHLOR-DISINF)
   - Typical: 50-100 ppm chlorine (50-100 tablets for 300-liter system)
   - Circulate chlorinated water through entire system (4 hours minimum)
   - Drain system completely
   - Refill with fresh water
   - Run through several cycles until chlorine smell gone
3. **Clean tanks and lines:**
   - Physically scrub tanks if accessible
   - Flush lines with chlorinated water
4. **Replace UV lamp** if not already done (SOLUTION L2)
5. **Test water** before drinking (SOLUTION L8)

**Prevention:** Monthly UV lamp check, periodic disinfection

**Reference:** See TRAIN-LIFE-002 (Water Contamination Scenario)

---

### SOLUTION N: Temperature Issues

**If temperature too hot or too cold:**

**Reference:** See KB-018 (Temperature Control Failure) for complete decision tree

**Quick Solutions:**
- Too cold: Check heating elements, heat recovery valves, insulation
- Too hot: Check heat exchanger deployed, coolant pumps, reduce power consumption

**Not immediately life-threatening** but address within hours for crew comfort and safety

---

## Emergency Priority

**If multiple life support issues, address in this order:**

1. **O₂ <16%:** CRITICAL - Deploy emergency O₂, restore APU immediately
2. **Hull breach:** CRITICAL - Seal breach, stabilize pressure
3. **O₂ 16-18%:** URGENT - Troubleshoot APU, use emergency O₂
4. **Water contaminated/unsafe:** URGENT - Switch to emergency rations, decontaminate
5. **No water production:** Moderate - Use stored water, repair WRMS
6. **Temperature extremes:** Moderate - Crew can tolerate for hours with precautions
7. **O₂ >18% but degraded:** Non-critical - Repair systematically

## Related Documents

- KB-027: Low Oxygen Alert (detailed O₂ troubleshooting)
- KB-018: Temperature Control Failure
- EMERG-004: Life Support Emergencies
- EMERG-007: Hull Breach
- TRAIN-LIFE-002: Water Contamination Scenario
- APU Maintenance Manual: Atmospheric Processing Unit
- WRMS Maintenance Manual: Water Recycling System
- ERR-LIFE-100: Life Support Error Codes

---

**Support Note:** This flowchart covers 90% of life support calls. Start here, follow systematically. If issue not covered, escalate to Level 2 support with details of what you've ruled out.
