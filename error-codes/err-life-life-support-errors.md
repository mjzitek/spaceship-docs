# Life Support System Error Codes (E-LIFE Series)

**Document ID:** ERR-LIFE-100
**Revision:** 4.4
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides complete error code reference for Life Support Systems including Atmospheric Processing Unit (APU) and Water Recycling and Management System (WRMS). Error codes displayed on life support control panels and logged in system diagnostics.

## Error Code Format

**E-LIFE-XXX**
- **E**: Error code indicator
- **LIFE**: Life support system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Life-threatening, immediate action required
- **WARNING** (Orange): Serious issue, investigate urgently
- **ADVISORY** (Yellow): Non-critical, schedule maintenance
- **INFO** (Blue): Informational, no action required

---

## Atmospheric System Errors (E-LIFE-100 series)

### E-LIFE-101: Oxygen Generation Below Required Rate
**Severity:** CRITICAL
**Cause:** Electrolysis unit not producing sufficient O₂ for crew

**Symptoms:**
- O₂ level slowly declining (may still be in normal range initially)
- Generation rate display shows <0.84 kg per person per day
- Electrolysis unit status yellow or red

**Immediate Actions:**
1. Activate emergency oxygen tanks
2. Reduce crew activity (minimize O₂ consumption)
3. Check water supply to electrolysis unit
4. Verify electrolysis unit power supply
5. Increase electrolysis power to maximum

**Resolution:**
- Check water tank not empty
- Verify purified water quality (conductivity <10 μS/cm)
- Inspect electrodes (if <70% efficiency, may need replacement)
- Check power to electrolysis unit (requires adequate Q-Core output)
- Replace degraded electrodes (Part #: ELC-OXY-PLT)

**Related:** LIFE-ATM-001, EMERG-008, KB-027

---

### E-LIFE-102: Oxygen Level Critical Low
**Severity:** CRITICAL
**Cause:** O₂ concentration below safe breathing level

**Symptoms:**
- O₂ reading <18%
- Crew symptoms: headache, rapid breathing, confusion
- Automatic alarm sounding

**Immediate Actions:**
1. **EMERGENCY O₂** button pressed (releases emergency tanks)
2. All crew don emergency respirators if available
3. Reduce crew physical activity immediately
4. Seal unused compartments
5. Identify cause of O₂ depletion

**Possible Causes:**
- Electrolysis unit failure (see E-LIFE-101)
- Hull breach venting atmosphere (see EMERG-007)
- Fire consuming oxygen
- Crew count exceeds APU capacity
- Air circulation failure preventing O₂ distribution

**Resolution:**
- Fix underlying cause (equipment failure, breach, etc.)
- Run electrolysis at maximum until O₂ restored
- Evacuate vessel if cannot restore life support

**Related:** EMERG-008, KB-027, LIFE-ATM-001

---

### E-LIFE-103: CO₂ Level High
**Severity:** WARNING
**Cause:** Carbon dioxide accumulation exceeds safe levels

**Symptoms:**
- CO₂ reading >0.5%
- Crew symptoms: headache, dizziness, rapid breathing
- May progress to E-LIFE-104 if not addressed

**Immediate Actions:**
1. Check CO₂ scrubbers
   - Verify airflow through scrubbers
   - Check saturation indicators
   - Replace if saturated (cartridges showing red)
2. Increase air circulation (run fans at maximum)
3. Reduce crew activity (minimize CO₂ production)

**Resolution:**
- Replace saturated CO₂ scrubber cartridges (Part #: SCR-CO2-series)
- Regenerate scrubbers if regenerable type (heat 200°C for 4 hours)
- Verify adequate air circulation through scrubber beds
- If multiple crew, consider isolating to separate compartments

**Related:** LIFE-ATM-001

---

### E-LIFE-104: CO₂ Level Critical
**Severity:** CRITICAL
**Cause:** CO₂ concentration dangerously high

**Symptoms:**
- CO₂ reading >1.0%
- Crew symptoms: severe headache, confusion, drowsiness, unconsciousness
- Life-threatening condition

**Immediate Actions:**
1. Don emergency respirators (if available)
2. Replace CO₂ scrubbers immediately
3. Maximize air circulation
4. If scrubbers cannot be replaced quickly: Vent affected compartment to space and seal
   - **CAUTION**: Only if crew can evacuate and O₂ can be replaced
5. Emergency medical attention for affected crew

**Resolution:**
- Fresh scrubber cartridges installed
- Verify scrubber system airflow restored
- Monitor CO₂ levels until back to <0.04%
- Do not allow crew back until safe levels confirmed

**Related:** EMERG-008, LIFE-ATM-001

---

### E-LIFE-110: HEPA Filter Airflow Restricted
**Severity:** ADVISORY
**Cause:** Air filters clogged, reducing circulation

**Symptoms:**
- Filter status indicator showing yellow or red
- Reduced airflow at vents
- Pressure differential across filters >150 Pa
- O₂ distribution may be uneven

**Resolution:**
- Replace HEPA filters (Part #: FLT-HEPA-APU)
- Clean pre-filters (washable, can reuse 3-4 times)
- Verify fan operation after filter replacement
- Check airflow restored to green range

**Related:** LIFE-ATM-001, KB-027

---

### E-LIFE-115: Circulation Fan Failure
**Severity:** WARNING
**Cause:** One or more air circulation fans not operating

**Symptoms:**
- Fan tachometer shows zero RPM
- No airflow at specific vents
- Uneven atmosphere (O₂ high in some areas, low in others)
- May hear alarm from fan motor

**Immediate Actions:**
1. Identify failed fan (check tachometer readings for each)
2. Activate backup fan (if equipped)
3. Manually mix atmosphere (open doors, create cross-ventilation)

**Resolution:**
- Check fan power supply
- Reset fan motor if thermal cutoff tripped
- Replace failed fan motor (Part #: FAN-APU-series)
- Lubricate fan bearings if grinding sound
- APU requires minimum 75% of fans operational

**Related:** LIFE-ATM-003

---

### E-LIFE-120: Cabin Pressure Low
**Severity:** WARNING (may escalate to CRITICAL)
**Cause:** Atmosphere leaking from vessel

**Symptoms:**
- Pressure gauge showing <95 kPa and declining
- Ears popping
- Hissing sound if leak audible
- May indicate hull breach

**Immediate Actions:**
1. Check rate of pressure loss
   - Slow (hours): Small leak, can investigate
   - Fast (minutes): Hull breach, seal compartments
2. Locate leak:
   - Check hull breach sensors
   - Listen for hissing
   - Use smoke test
3. Seal breach if possible
4. If cannot seal: Evacuate affected compartment and seal bulkhead

**Resolution:**
- Apply emergency hull patch or sealant
- Permanent repair required before resuming normal operations
- Verify pressure stabilizes after repair

**Related:** EMERG-007, HULL-SYS-001

---

### E-LIFE-125: Cabin Pressure High
**Severity:** ADVISORY
**Cause:** Over-pressurization of cabin

**Symptoms:**
- Pressure gauge >110 kPa
- Doors difficult to open
- Stress on hull seals

**Immediate Actions:**
1. Reduce O₂ generation rate
2. Vent excess pressure (controlled release valve)
3. Check pressure regulator function

**Resolution:**
- Calibrate pressure regulator
- Verify O₂ generation not over-producing
- Check for thermal expansion (temperature increase can raise pressure)
- Ensure pressure relief valves functioning

**Related:** LIFE-ATM-001

---

### E-LIFE-130: Temperature Out of Range
**Severity:** ADVISORY (WARNING if extreme)
**Cause:** Cabin temperature too high or too low

**Symptoms:**
- Temperature <10°C or >30°C
- Crew discomfort
- May affect equipment operation

**Resolution:**
- Adjust climate control settings
- Check heating/cooling system operation
- Verify air circulation adequate
- Inspect temperature sensors for accuracy
- If system cannot maintain temp: Check heat exchanger, coolant system

**Related:** LIFE-ATM-001

---

### E-LIFE-135: Humidity Out of Range
**Severity:** ADVISORY
**Cause:** Cabin humidity too high or too low

**Symptoms:**
- Humidity <20% (too dry) or >75% (too wet)
- Crew discomfort, respiratory irritation
- Condensation on surfaces if too wet

**Resolution:**
- Check humidity controller operation
- Verify condensation collector draining
- If too wet: Increase dehumidification, check for water leaks
- If too dry: Reduce dehumidification, may need to add moisture
- Optimal range: 40-60%

**Related:** LIFE-ATM-001

---

## Water System Errors (E-LIFE-200 series)

### E-LIFE-201: Potable Water Tank Low
**Severity:** WARNING
**Cause:** Clean water supply running low

**Symptoms:**
- Potable tank level <30%
- May hear low-water alarm
- Water conservation recommended

**Immediate Actions:**
1. Check wastewater tank level
   - If high: Processing not keeping up
   - If low: Water loss from system
2. Implement water rationing
3. Initiate manual water processing cycle

**Resolution:**
- Run water processing system to convert wastewater to potable
- Check for leaks in potable water system
- If leak found: Repair and refill
- Resupply water at next port if needed

**Related:** LIFE-WAT-001

---

### E-LIFE-202: Wastewater Tank Full
**Severity:** WARNING
**Cause:** Wastewater tank approaching capacity

**Symptoms:**
- Wastewater tank level >80%
- Processing cycle not running or not keeping up
- May indicate processing system failure

**Immediate Actions:**
1. Initiate water processing cycle immediately
2. Reduce water usage until processing catches up
3. Check why processing not keeping pace

**Resolution:**
- Run processing cycle to clear wastewater
- Check for processing system failures
- Verify pumps and filters operational
- If system cannot process: Emergency dump may be required (check regulations)

**Related:** LIFE-WAT-001

---

### E-LIFE-210: Water Quality Below Standard
**Severity:** WARNING
**Cause:** Processed water purity not meeting safe drinking standards

**Symptoms:**
- TDS (Total Dissolved Solids) >300 ppm
- Bacterial contamination detected (CFU >0)
- pH outside 6.5-8.5 range
- Water may have off taste/odor

**Immediate Actions:**
1. **Do not consume water** until issue resolved
2. Switch to emergency water ration
3. Post "DO NOT DRINK" warnings at taps

**Resolution:**
- Check RO membrane performance (should reject >95% of solids)
- Verify UV sterilizer operating (kills bacteria)
- Test UV lamp output (should be >70% rated)
- Replace RO membrane if degraded (Part #: MEM-RO-series)
- Replace UV lamp if low output (Part #: UV-LAMP-254)
- Shock treat system with chlorine if bacterial contamination

**Related:** LIFE-WAT-001

---

### E-LIFE-215: Water Processing Cycle Failure
**Severity:** WARNING
**Cause:** Water recycling system unable to complete processing

**Symptoms:**
- Processing cycle starts but doesn't finish
- Error partway through cycle
- Wastewater not being converted to potable

**Possible Causes:**
- Pump failure (cannot move water through system)
- Filter blockage (RO membrane clogged)
- Power insufficient
- Control system error

**Resolution:**
- Run diagnostic: WRMS > Diagnostics > System Test
- Check pump operation (should hear running)
- Measure pressure across RO membrane (high = clogged)
- Clean or replace RO membrane
- Verify power supply to WRMS
- Reset control system if software error

**Related:** LIFE-WAT-003

---

### E-LIFE-220: RO Membrane Failure
**Severity:** WARNING
**Cause:** Reverse osmosis membrane not filtering properly

**Symptoms:**
- High TDS in output water
- Rejection rate <90%
- Water quality failure (E-LIFE-210)

**Immediate Actions:**
1. Do not consume water from system
2. Use emergency water supply

**Resolution:**
- Clean RO membrane with approved cleaning solution
- If cleaning doesn't restore performance: Replace membrane
- Membrane lifespan: Typically 24 months
- After replacement, flush system before consumption

**Related:** LIFE-WAT-001, KB-056

---

### E-LIFE-225: UV Sterilizer Ineffective
**Severity:** WARNING
**Cause:** UV lamp not producing adequate sterilization

**Symptoms:**
- Bacterial contamination detected
- UV intensity meter shows <70% output
- Lamp may be old or dirty

**Immediate Actions:**
1. Do not consume water
2. Switch to emergency supply

**Resolution:**
- Clean UV lamp quartz sleeve (mineral deposits reduce transmission)
- Check UV lamp output with intensity meter
- Replace lamp if >8,000 hours use or output <70%
- UV lamps degrade over time even if still glowing

**Related:** LIFE-WAT-001

---

### E-LIFE-230: Biological Reactor Contamination
**Severity:** ADVISORY
**Cause:** Bacterial culture in wastewater treatment not healthy

**Symptoms:**
- Reactor smells foul (indicates culture die-off)
- Low treatment efficiency
- May lead to water quality failures

**Resolution:**
- Drain 50% of reactor volume
- Add fresh bacteria culture supplement (Part #: BIO-CULT-WRM)
- Check oxygenation (air bubbler must provide continuous aeration)
- Verify reactor temperature 30-35°C (optimal for bacteria)
- Allow 24 hours for culture to reestablish

**Related:** LIFE-WAT-001

---

## Combined System Errors (E-LIFE-300 series)

### E-LIFE-301: Life Support Computer Offline
**Severity:** CRITICAL
**Cause:** Computer managing life support systems has failed

**Symptoms:**
- Life support panel unresponsive
- Systems not auto-regulating
- May need manual control

**Immediate Actions:**
1. Switch to manual control mode (if available)
2. Monitor systems manually (O₂, CO₂, pressure, water)
3. Attempt computer reboot

**Resolution:**
- Reboot life support computer (breaker off 30 sec, then on)
- Run diagnostic if reboots successfully
- Update firmware if software fault
- Replace control computer if hardware failure (Part #: CTRL-LIFE-A)

**Related:** Contact ORSM Support

---

### E-LIFE-305: Multiple System Failures
**Severity:** CRITICAL
**Cause:** Two or more life support subsystems failed simultaneously

**Symptoms:**
- Multiple error codes active
- Life support compromised on multiple fronts
- May indicate power failure or catastrophic damage

**Immediate Actions:**
1. Don emergency pressure suits
2. Identify common cause:
   - Power failure affecting all systems?
   - Combat/collision damage?
   - Computer failure cascading to subsystems?
3. Prepare for emergency evacuation if cannot restore

**Resolution:**
- Fix root cause (power, damage, computer)
- Repair individual systems as power/capability allows
- May need rescue if cannot restore life support
- Send distress signal

**Related:** EMERG-008, All life support manuals

---

### E-LIFE-310: Emergency Life Support Activated
**Severity:** INFO (but indicates previous failure)
**Cause:** Automatic switchover to emergency backup systems

**What This Means:**
- Emergency O₂ tanks now providing breathable air
- Normal O₂ generation failed
- Time limited (emergency supply 6-48 hours depending on vessel)

**Immediate Actions:**
1. Identify why normal system failed
2. Repair primary system before emergency supply exhausted
3. Ration emergency air if repair will take time

**Resolution:**
- Fix primary electrolysis unit or other failed system
- Switch back to normal operations
- **Refill emergency tanks at next port** (critical!)

**Related:** EMERG-008

---

## Environmental Alert Errors (E-LIFE-400 series)

### E-LIFE-401: Toxic Gas Detected
**Severity:** CRITICAL
**Cause:** Sensors detected poisonous gases in atmosphere

**Possible Toxins:**
- Carbon monoxide (CO) - from incomplete combustion, fires
- Ammonia (NH₃) - from coolant leaks
- Methane (CH₄) - from waste decomposition, fuel leaks

**Immediate Actions:**
1. **Don respirators or pressure suits**
2. Identify toxin source
3. Increase air filtration and circulation
4. Isolate contaminated compartment if possible
5. Vent to space if safe to do so (can replenish O₂ from electrolysis)

**Resolution:**
- Fix source of contamination (seal leak, extinguish fire, etc.)
- Filter contaminated air
- May need to completely purge atmosphere and refill
- Medical attention for exposed crew

**Related:** EMERG-008, LIFE-ATM-001

---

### E-LIFE-405: Particulate Count High
**Severity:** ADVISORY
**Cause:** Excessive dust/particles in air

**Symptoms:**
- Particle counter >500/m³
- Crew respiratory irritation
- May affect sensitive equipment

**Resolution:**
- Replace HEPA filters (clogged filters allow particles through)
- Clean air intake areas
- Identify particle source (damaged equipment? Cargo dust?)
- Increase air filtration until resolved

**Related:** LIFE-ATM-001

---

## Sensor and Diagnostic Errors (E-LIFE-500 series)

### E-LIFE-501: Oxygen Sensor Malfunction
**Severity:** WARNING
**Cause:** O₂ sensor providing invalid readings

**Symptoms:**
- O₂ reading obviously wrong (0%, 100%, fluctuating wildly)
- Sensor disagrees with redundant sensors
- May cause false alarms

**Resolution:**
- Compare to redundant O₂ sensors (multiple sensors installed)
- Calibrate sensor using calibration gas (20.9% O₂)
- If calibration fails: Replace sensor (Part #: SNR-O2-LIFE)
- Do not rely on failed sensor for crew safety decisions

**Related:** LIFE-ATM-001

---

### E-LIFE-505: Multiple Sensor Failures
**Severity:** CRITICAL
**Cause:** Several atmosphere sensors failed simultaneously

**Symptoms:**
- Cannot trust atmospheric readings
- Flying blind on life support status

**Immediate Actions:**
1. Assume worst case (low O₂, high CO₂)
2. Activate emergency O₂
3. Maximize air processing
4. Get to safe port ASAP

**Resolution:**
- Replace all failed sensors
- Calibrate thoroughly before resuming operations
- May indicate electrical fault affecting multiple sensors

**Related:** LIFE-ATM-001

---

## Error Code Quick Reference Table

| Code | System | Severity | Quick Description |
|------|--------|----------|-------------------|
| E-LIFE-101 | APU | CRITICAL | O₂ generation low |
| E-LIFE-102 | APU | CRITICAL | O₂ level critical low |
| E-LIFE-103 | APU | WARNING | CO₂ high |
| E-LIFE-104 | APU | CRITICAL | CO₂ critical |
| E-LIFE-110 | APU | ADVISORY | HEPA filters clogged |
| E-LIFE-115 | APU | WARNING | Fan failure |
| E-LIFE-120 | APU | WARNING | Pressure low |
| E-LIFE-125 | APU | ADVISORY | Pressure high |
| E-LIFE-130 | APU | ADVISORY | Temperature out of range |
| E-LIFE-135 | APU | ADVISORY | Humidity out of range |
| E-LIFE-201 | WRMS | WARNING | Potable water low |
| E-LIFE-202 | WRMS | WARNING | Wastewater full |
| E-LIFE-210 | WRMS | WARNING | Water quality failure |
| E-LIFE-215 | WRMS | WARNING | Processing cycle fail |
| E-LIFE-220 | WRMS | WARNING | RO membrane failure |
| E-LIFE-225 | WRMS | WARNING | UV sterilizer fail |
| E-LIFE-230 | WRMS | ADVISORY | Bio reactor issue |
| E-LIFE-301 | Both | CRITICAL | Computer offline |
| E-LIFE-305 | Both | CRITICAL | Multiple failures |
| E-LIFE-310 | APU | INFO | Emergency O₂ active |
| E-LIFE-401 | APU | CRITICAL | Toxic gas detected |
| E-LIFE-405 | APU | ADVISORY | High particulates |
| E-LIFE-501 | Sensors | WARNING | O₂ sensor fault |
| E-LIFE-505 | Sensors | CRITICAL | Multiple sensor faults |

## Related Documents

- LIFE-ATM-001: Atmospheric Processing Unit
- LIFE-WAT-001: Water Recycling System
- LIFE-ATM-003: APU Troubleshooting
- LIFE-WAT-003: WRMS Troubleshooting
- EMERG-007: Decompression Emergency
- EMERG-008: Low Oxygen Emergency
- KB-027: Low Oxygen Alert
- KB-038: High CO₂ Emergency

---

**Document maintained by ORSM Technical Publications. Life support errors are life-safety critical - respond immediately to WARNING and CRITICAL level codes.**
