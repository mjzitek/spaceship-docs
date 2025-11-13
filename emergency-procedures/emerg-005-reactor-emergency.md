# Emergency Procedure: Reactor Critical Failures

**Document ID:** EMERG-005
**Revision:** 4.3
**Last Updated:** 2847.09.14
**Severity:** LIFE-CRITICAL

## Purpose

This document provides emergency procedures for Q-Core reactor critical failures including overheating, containment breach, coolant loss, and radiation emergencies.

**TIME CRITICAL**: Many reactor emergencies require immediate action. Seconds count. Know these procedures.

## Emergency Classification

### Level 1: CRITICAL IMMEDIATE (Red)
- Containment breach imminent or occurring
- Core temperature >3,000°C
- Radiation levels dangerous (>2.0 mSv/h external)
- Complete coolant loss
- Multiple critical system failures

**Response**: SCRAM immediately, evacuate reactor compartment

### Level 2: SERIOUS URGENT (Orange)
- Core temperature 2,800-3,000°C and rising
- Coolant pressure <60 PSI
- Single critical system failure (coolant, containment, etc.)
- Plasma instability severe

**Response**: Emergency shutdown procedures, prepare for possible evacuation

### Level 3: WARNING (Yellow)
- Core temperature >2,800°C but stable
- Coolant pressure low but not critical
- Minor plasma instability
- Single coil failure

**Response**: Controlled shutdown, investigate and repair before restart

## Emergency Actions Summary

| Situation | Immediate Action | Time |
|-----------|------------------|------|
| Core >3,000°C | SCRAM, evacuate | <30 sec |
| Coolant loss detected | SCRAM, locate leak | <1 min |
| Containment breach | SCRAM, evacuate, seal compartment | <1 min |
| Radiation >2.0 mSv/h | Evacuate, don protection | <2 min |
| Plasma instability severe | Reduce power 50%, monitor | <30 sec |

---

## SCRAM Procedure (Emergency Shutdown)

**When to Use:** Imminent danger, catastrophic failure, no other option

**Duration:** 30-90 seconds to shutdown

### Step 1: Initiate SCRAM (0-3 seconds)

1. **Locate SCRAM button**
   - Large red button on reactor control panel
   - Labeled "EMERGENCY SCRAM"
   - May have protective cover (flip up first)

2. **Press and hold for 3 seconds**
   - Until confirmation tone sounds
   - Display shows "EMERGENCY SHUTDOWN INITIATED"

3. **System will automatically:**
   - Cease fuel injection immediately (0 seconds)
   - Dump magnetic containment field (3 seconds)
   - Activate emergency coolant flood (5 seconds)
   - Vent residual plasma to emergency exhaust (10-30 seconds)
   - Engage reactor lockdown

### Step 2: Monitor SCRAM Progress (10-90 seconds)

**Watch for:**
- Core temperature begins dropping (should decrease 500°C in first 30 seconds)
- Plasma density drops to zero (within 15 seconds)
- Coolant temperature rises briefly then stabilizes (normal during SCRAM)
- Radiation levels should remain stable or decrease

**Warning Signs During SCRAM:**
- Core temperature continuing to rise (coolant flood may have failed)
- Radiation levels increasing (possible containment damage)
- Loud sounds, vibrations, or visible damage
- Coolant not flooding (check emergency coolant tank valve)

### Step 3: Evacuate Reactor Compartment (Immediately)

1. **Sound general alarm**
   - Alert all crew to emergency
   - Announce: "REACTOR SCRAM - EVACUATE REACTOR COMPARTMENT"

2. **All personnel exit reactor area**
   - Use nearest exit
   - Close bulkhead doors behind you
   - Don't stop to collect belongings

3. **Seal reactor compartment**
   - Close all hatches leading to reactor
   - Engage emergency seals if available
   - Post warning signs on sealed hatches

### Step 4: Radiation Check (2-5 minutes post-SCRAM)

1. **Don radiation protection gear**
   - Lead-lined suit if available
   - At minimum: dosimeter to measure exposure

2. **Measure radiation at sealed hatches**
   - Use portable radiation detector
   - Check multiple points around reactor compartment
   - Safe level: <0.5 mSv/h
   - Elevated: 0.5-1.0 mSv/h (monitor closely)
   - Dangerous: >1.0 mSv/h (do not enter)

3. **If radiation levels safe:**
   - May cautiously enter to assess damage
   - Limit exposure time (15 minutes maximum)
   - Continue monitoring radiation

4. **If radiation levels dangerous:**
   - Do not enter
   - Seal compartment completely
   - Vent compartment atmosphere to space if possible (radiation may contaminate air)
   - Contact emergency support

### Step 5: Post-SCRAM Assessment (30+ minutes)

**DO NOT attempt restart until:**
- [ ] Complete inspection by qualified technician
- [ ] Cause of emergency identified and resolved
- [ ] All damaged components repaired or replaced
- [ ] Full system diagnostic passed
- [ ] Radiation levels confirmed safe
- [ ] SCRAM lockout manually reset (requires technician authorization)

**Expected SCRAM Consequences:**
- Thermal stress may damage reactor components (injectors, seals, chamber walls)
- Coolant may be contaminated from emergency flood
- Magnetic coils may need recalibration
- Downtime: Minimum several hours, possibly days for full inspection

---

## Core Overheating Emergency

**Trigger:** Core temperature >2,800°C and rising, or >3,000°C at any time

### If Temperature 2,800-3,000°C:

**Step 1: Immediate Reduction (0-30 seconds)**
1. Reduce fuel injection rate to 50% of current
2. Increase coolant flow to maximum (100%)
3. Reduce power demand (shut down non-essential systems)
4. Monitor temperature response

**Step 2: Assess (30-60 seconds)**
- **If temperature stabilizing or dropping:**
  - Continue reduced operation
  - Investigate cause (coolant issue? Over-fueling?)
  - Plan controlled shutdown when safe

- **If temperature continuing to rise:**
  - Prepare for SCRAM
  - Alert crew
  - Continue to Step 3

**Step 3: Critical Decision Point (1-2 minutes)**
- **Temperature >2,900°C:** Strongly consider SCRAM
- **Temperature >3,000°C:** SCRAM immediately, no delay

### If Temperature >3,000°C:

**IMMEDIATE SCRAM - NO DELAY**
1. Press SCRAM button (0-3 seconds)
2. Evacuate reactor compartment (immediate)
3. Follow SCRAM procedure above

**Extreme Temperature Dangers:**
- Plasma chamber wall failure (breach)
- Magnetic coil burnout (containment loss)
- Coolant flash boiling (pressure explosion)
- Radioactive material release

---

## Coolant Loss Emergency

**Trigger:** Coolant pressure dropping, leak detected, or E-PWR-260 error

### Immediate Actions (0-60 seconds)

**Step 1: Initiate Emergency Shutdown**
1. **If coolant pressure <40 PSI:** SCRAM immediately
2. **If coolant pressure 40-80 PSI:** Controlled emergency shutdown:
   - Reduce reactor power to minimum
   - Cease fuel injection
   - Maintain magnetic containment
   - Allow reactor to cool naturally

**Step 2: Locate Leak (Parallel with Step 1)**
1. Check coolant pressure gauge (declining = active leak)
2. Check coolant level indicator (should show dropping)
3. Look for visible signs:
   - Wet spots or puddles (coolant is silver-gray liquid)
   - Steam or vapor (if leak in hot section)
   - Pressure readings at different points in system

4. Common leak locations:
   - Pipe fittings and joints
   - Pump seals
   - Heat exchanger connections
   - Containment vessel coolant jacket
   - Filter housings

### Leak Response (1-5 minutes)

**Small Leak (Pressure dropping slowly, >60 PSI):**
1. Mark leak location
2. Complete emergency shutdown
3. Allow reactor to cool (wait until core <500°C)
4. Repair leak when safe
5. Refill coolant system
6. Pressure test before restart

**Large Leak (Pressure dropping rapidly, <60 PSI):**
1. SCRAM immediately if not already done
2. Attempt emergency isolation:
   - Close valves to isolate leaking section (if possible)
   - Bypass damaged section (if possible)
3. Activate backup coolant if equipped
4. If leak cannot be stopped:
   - Accept coolant loss
   - Ensure reactor fully shut down
   - Monitor core temperature (residual heat will cause temperature rise)
   - Do not allow core temperature to exceed 3,000°C
   - If necessary, vent reactor compartment to space for emergency cooling

### Critical Coolant Loss (Pressure <40 PSI)

**This is Life-Critical Emergency:**
1. SCRAM if not done (immediate)
2. Evacuate reactor compartment
3. Seal compartment
4. Accept reactor may be damaged - crew safety priority
5. Monitor from external displays
6. Contact emergency support

**Dangers:**
- Core temperature will rise even after shutdown (residual heat)
- Without coolant, temperature can reach dangerous levels
- Possible chamber breach, radiation release
- May need to jettison reactor module (if design allows)

---

## Plasma Containment Emergency

**Trigger:** E-PWR-250 (instability), E-PWR-251 (containment failure imminent), or magnetic field critically low

### Severe Plasma Instability

**Symptoms:**
- Plasma density varying rapidly (±1.0 g/cm³ or more)
- Core temperature swinging ±200°C or more
- Power output oscillating
- Severe vibrations from reactor
- Magnetic field strength fluctuating

**Immediate Actions (0-30 seconds):**
1. Reduce fuel injection to 50%
2. Increase magnetic field strength by 0.5 Tesla
3. Reduce power demand on reactor

**Assessment (30-90 seconds):**
- **If instability decreasing:**
  - Continue reduced operation until stable
  - Then proceed to controlled shutdown
  - Investigate cause before restart

- **If instability continuing or worsening:**
  - SCRAM immediately
  - Evacuate reactor compartment
  - Instability can lead to containment breach

### Containment Field Failure Imminent (E-PWR-251)

**This is Maximum Danger:**

**IMMEDIATE ACTIONS (0-10 seconds):**
1. **PRESS SCRAM BUTTON** - Do not hesitate
2. **SOUND EVACUATION ALARM** - Reactor compartment and adjacent areas
3. **DO NOT attempt to stabilize** - Risk too high

**Evacuation (10-60 seconds):**
1. All personnel exit reactor area immediately
2. Seal all hatches to reactor compartment
3. Don radiation protection gear
4. Monitor radiation levels from safe distance

**If Containment Breach Occurs:**

**Symptoms:**
- Radiation alarms throughout ship
- Possible visible glow from reactor (blue Cherenkov radiation)
- Loud sounds (magnetic field collapse, pressure release)
- Possible structural damage to reactor compartment

**Critical Actions:**
1. Evacuate all areas showing elevated radiation
2. Seal multiple bulkheads between crew and reactor
3. Don radiation suits for any crew in affected areas
4. May need to vent reactor compartment atmosphere to space
5. Assess radiation exposure to crew (medical priority)
6. Send distress signal - reactor breach is emergency requiring rescue
7. Prepare to abandon ship if radiation cannot be contained

**Containment Breach is Worst-Case Scenario:**
- Reactor may be total loss
- Ship may be contaminated beyond safe occupancy
- Crew may receive dangerous radiation doses
- Prevention through proper maintenance and quick response to warnings is critical

---

## Radiation Emergency

**Trigger:** Radiation levels >1.0 mSv/h outside reactor shielding, or E-PWR-270 error

### Radiation Level Response

**1.0-2.0 mSv/h (Elevated):**
1. Limit time in area (15 minutes maximum)
2. Don radiation protection
3. Investigate source (shielding damage? Reactor malfunction?)
4. Plan reactor shutdown
5. Repair shielding before restart

**>2.0 mSv/h (Dangerous):**
1. **EVACUATE immediately**
2. Seal affected areas
3. SCRAM reactor
4. Do not re-enter without protection
5. Identify radiation source
6. May indicate serious reactor damage

**>5.0 mSv/h (Life-Threatening):**
1. **EMERGENCY EVACUATION**
2. Sound ship-wide alarm
3. Seal reactor section completely
4. All crew to radiation-shielded areas
5. Send distress signal
6. Prepare for possible ship abandonment

### Radiation Exposure

**Immediate Symptoms (high dose):**
- Nausea, vomiting
- Headache, dizziness
- Skin reddening (radiation burn)
- Weakness, fatigue

**If Crew Exposed:**
1. Move to shielded area immediately
2. Remove contaminated clothing (seal in bags)
3. Decontamination shower if available
4. Monitor dosimeters - record exposure levels
5. Medical attention (supportive care, anti-radiation meds if available)
6. Contact medical emergency support

**Safe Exposure Limits:**
- **Occupational**: <20 mSv per year
- **Emergency**: <100 mSv for lifesaving actions
- **Dangerous**: >1,000 mSv (acute radiation sickness possible)
- **Lethal**: >5,000 mSv (death likely without treatment)

---

## Recovery After Emergency

### Do Not Restart Reactor Until:

1. **Complete Inspection**
   - Qualified technician examines all systems
   - Cause of emergency identified
   - All damage assessed

2. **Repairs Completed**
   - Replace damaged components
   - Repair leaks
   - Restore shielding integrity

3. **Testing Passed**
   - Pressure tests (coolant system)
   - Radiation survey (confirm safe levels)
   - Full diagnostic (all systems green)

4. **Authorization Obtained**
   - Technician signs off on restart
   - SCRAM lockout manually reset
   - Captain/owner approval

### Documentation Required

1. **Incident Report**
   - Date, time, nature of emergency
   - Actions taken
   - Cause identified
   - Damage sustained

2. **Inspection Report**
   - All systems checked
   - Components replaced
   - Tests performed

3. **Restart Authorization**
   - Technician certification
   - Command approval
   - Logged in ship's permanent record

**Regulatory**: Serious reactor emergencies must be reported to authorities at next port. May require official inspection.

---

## Emergency Contacts

### ORSM Emergency Hotline
- **Critical failures, SCRAM events**
- **Radiation emergencies**
- **Life-threatening situations**
- **Available 24/7**

### What to Report:
- Ship identification and location
- Nature of emergency
- Current status (reactor shutdown? Radiation levels?)
- Crew status (injuries? Exposure?)
- Assistance needed

### Emergency Supplies to Have Aboard:

- [ ] Radiation detection equipment (dosimeters, survey meters)
- [ ] Radiation protection gear (lead suits or vests)
- [ ] Emergency coolant supply (enough to refill system)
- [ ] Reactor repair parts (coils, seals, injectors)
- [ ] Emergency power backup (for life support if reactor offline)
- [ ] Medical supplies (anti-radiation medication, burn treatment)

---

## Related Documents

- PWR-SYS-001: Q-Core Reactor Overview
- PWR-SYS-002: Startup and Shutdown Procedures
- PWR-SYS-004: Troubleshooting Manual
- ERR-PWR-100: Power System Error Codes
- EMERG-001: General Emergency Procedures

---

**DRILL THESE PROCEDURES**: Crew should practice emergency procedures regularly. In real emergency, quick response saves lives and ship.

**WHEN IN DOUBT, SCRAM**: Better to shut down unnecessarily than risk catastrophic failure.
