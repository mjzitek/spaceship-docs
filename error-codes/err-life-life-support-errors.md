# Life Support System Error Codes (E-LIFE Series)

**Document ID:** ERR-LIFE-100
**Revision:** 4.1
**Last Updated:** 2847.10.22
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides a complete reference of error codes for atmospheric processing, life support, and environmental control systems. Error codes are displayed on life support control panels and logged in system diagnostics.

## Error Code Format

**E-LIFE-XXX**
- **E**: Error code indicator
- **LIFE**: Life support system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Immediate action required, life safety risk, crew in danger
- **WARNING** (Orange): Investigate promptly, may escalate to critical
- **ADVISORY** (Yellow): Monitor situation, schedule maintenance
- **INFO** (Blue): Informational only, no action required

---

## System Failures (E-LIFE-100 series)

### E-LIFE-100: Atmospheric System Offline
**Severity:** CRITICAL
**Cause:** Complete failure of atmospheric processing system
**Symptoms:**
- No oxygen generation
- No CO₂ scrubbing
- Atmospheric composition degrading
- Life support control panel dark or unresponsive

**Resolution:**
1. Switch to backup atmospheric system immediately
2. All crew don emergency oxygen masks
3. Check main power to life support (circuit breakers)
4. Attempt system restart via emergency controls
5. If restart fails, prepare for emergency rescue (limited oxygen reserves)

**Related:** EMERG-015 (Life Support Failures), LIFE-SYS-001 (System Overview)

---

### E-LIFE-101: Power Supply Failure
**Severity:** CRITICAL
**Cause:** Loss of power to life support systems
**Symptoms:**
- Life support systems shutting down
- Atmospheric processing stopped
- Fans and pumps ceasing operation

**Resolution:**
1. Check life support circuit breakers (main panel)
2. Verify reactor providing power to ship
3. Check backup battery status for life support
4. If main power lost, activate emergency backup power
5. Reduce power consumption (shut down non-essential systems)

**Related:** ERR-PWR-100 (Power System Errors)

---

## Oxygen System Errors (E-LIFE-110 series)

### E-LIFE-110: Oxygen Level Low
**Severity:** WARNING (becomes CRITICAL if O₂ <16%)
**Cause:** Oxygen generation insufficient or oxygen being consumed/lost faster than generated
**Symptoms:**
- Oxygen percentage dropping below 19%
- Crew experiencing shortness of breath
- Warning tone and alarm

**Resolution:**
1. Increase oxygen generation rate to maximum
2. Check water supply to electrolysis system
3. Release emergency oxygen from reserve tanks
4. Reduce crew activity (lowers oxygen consumption)
5. Check for hull breaches (oxygen escaping)
6. Seal unused compartments (concentrate atmosphere)

**Related:** KB-027 (Low Oxygen Alert), EMERG-015 (Life Support Failures)

---

### E-LIFE-120: Oxygen Generation System Failure
**Severity:** CRITICAL
**Cause:** Electrolysis system or oxygen generators not functioning
**Symptoms:**
- Oxygen level dropping continuously
- Oxygen generation rate shows 0%
- No oxygen being produced despite demand

**Resolution:**
1. All crew don emergency oxygen masks immediately
2. Attempt to restart oxygen generation system
3. Check water supply (electrolysis requires water)
4. Check power to oxygen generation system
5. Switch to emergency oxygen tanks
6. Calculate oxygen reserve duration vs. rescue/port arrival time
7. Send distress signal if reserves insufficient

**Related:** EMERG-015 (Life Support Failures), LIFE-SYS-001 (Atmospheric Processing)

---

### E-LIFE-121: Electrolysis Cell Failure
**Severity:** CRITICAL
**Cause:** Electrolysis cell damaged, fouled, or worn out
**Symptoms:**
- Oxygen generation reduced or stopped
- Cell voltage abnormal
- Cell efficiency below 50%

**Resolution:**
1. Switch to backup electrolysis cell if equipped
2. Attempt cell cleaning procedure (automated if available)
3. Check cell voltage and current (should be 1.8-2.2V per cell)
4. Replace electrolysis cell if failed (Part #: ELEC-CELL-LSS)
5. Use emergency oxygen reserves while repairing

**Related:** LIFE-SYS-002 (Maintenance Procedures)

---

### E-LIFE-122: Water Supply Depleted
**Severity:** WARNING
**Cause:** Insufficient water for oxygen generation via electrolysis
**Symptoms:**
- Water tank level <10%
- Oxygen generation reduced due to lack of water
- Warning indicators on water system

**Resolution:**
1. Refill water tanks from potable water or reserves
2. Check water recycling system (should be producing water)
3. Reduce water consumption (crew rationing)
4. In emergency: Can use any water (coolant water, gray water) for oxygen generation
5. Water requirement: ~1 liter per person per day for oxygen generation

**Related:** LIFE-SYS-002 (Water Recycling)

---

## Carbon Dioxide Errors (E-LIFE-130 series)

### E-LIFE-130: Carbon Dioxide Level High
**Severity:** WARNING (becomes CRITICAL if CO₂ >4%)
**Cause:** CO₂ scrubbers insufficient or malfunctioning
**Symptoms:**
- CO₂ level rising above 1%
- Crew experiencing headache, drowsiness
- Air feels "stuffy" or "stale"

**Resolution:**
1. Activate all CO₂ scrubbers at maximum rate
2. Increase ventilation circulation
3. Check scrubber media saturation (may need replacement)
4. Reduce crew activity (lowers CO₂ production)
5. Seal unused compartments
6. If critical: Vent atmosphere and replace (uses oxygen reserves)

**Related:** KB-027 (Poor Air Quality), EMERG-015 (Life Support Failures)

---

### E-LIFE-131: CO₂ Scrubber System Failure
**Severity:** CRITICAL
**Cause:** Scrubber system not removing CO₂ from atmosphere
**Symptoms:**
- CO₂ level rising continuously
- Scrubber efficiency 0% or very low
- Scrubber system offline

**Resolution:**
1. Restart scrubber system
2. Check scrubber power supply
3. Replace scrubber cartridges (may be saturated)
4. Activate backup scrubbers if equipped
5. Emergency: Use lithium hydroxide canisters (chemical CO₂ absorption)
6. Increase ventilation to dilute CO₂
7. May need to vent atmosphere to space periodically

**Related:** EMERG-015 (Life Support Failures), LIFE-SYS-001 (Atmospheric Processing)

---

### E-LIFE-135: Scrubber Media Saturated
**Severity:** WARNING
**Cause:** CO₂ scrubber media has absorbed maximum capacity
**Symptoms:**
- Scrubber efficiency below 50%
- CO₂ level gradually increasing
- Time since last media replacement exceeds rated lifespan

**Resolution:**
1. Replace scrubber media/cartridges with fresh (Part #: SCR-MED-LH or SCR-MED-AMINE)
2. If no spare media available:
   - Reduce CO₂ production (crew rest, low activity)
   - Increase ventilation
   - May be able to regenerate some media types (heat treatment)
3. Scrubber media lifespan: Typically 30-90 days depending on crew size

**Related:** LIFE-SYS-003 (Maintenance Schedule)

---

## Pressure and Ventilation Errors (E-LIFE-140 series)

### E-LIFE-140: Cabin Pressure Low
**Severity:** CRITICAL
**Cause:** Hull breach, leak, or atmospheric dump
**Symptoms:**
- Pressure dropping below 12 PSI (normal is 14.7 PSI)
- Crew experiencing ear popping, breathing difficulty
- Decompression alarm

**Resolution:**
1. All crew don emergency oxygen masks immediately
2. Locate breach/leak (check compartment pressure readings)
3. Seal affected compartment (close hatches)
4. Patch breach if accessible
5. Repressurize from atmospheric reserves
6. Do not allow pressure below 10 PSI (serious hypoxia risk)

**Related:** EMERG-010 (Hull Breach), EMERG-015 (Life Support Failures)

---

### E-LIFE-141: Rapid Decompression Detected
**Severity:** CRITICAL
**Cause:** Large hull breach causing rapid pressure loss
**Symptoms:**
- Pressure dropping >5 PSI/minute
- Loud rushing air sound
- Objects being pulled toward breach

**Resolution:**
1. EMERGENCY - All crew emergency oxygen immediately
2. Sound decompression alarm
3. Seal all compartments (emergency bulkhead closure)
4. Locate and seal breach (see EMERG-010)
5. Do not enter depressurized areas without pressure suit
6. Repressurize only after breach sealed

**Related:** EMERG-010 (Hull Breach), EMERG-025 (Collision Damage)

---

### E-LIFE-145: Ventilation Fan Failure
**Severity:** WARNING
**Cause:** Circulation fans not operating
**Symptoms:**
- Poor air circulation
- Localized hot/cold spots
- Odors or CO₂ concentrating in areas
- Fan motor not running

**Resolution:**
1. Check fan power supply
2. Reset fan controller
3. Check for obstructions in fan blades or ducts
4. Manually restart fans if auto-start failed
5. If primary fan failed, activate backup fans
6. Clean fan filters (clogged filter prevents airflow)

**Related:** LIFE-SYS-004 (Ventilation System)

---

## Temperature Control Errors (E-LIFE-150 series)

### E-LIFE-150: Temperature Out of Range
**Severity:** WARNING (CRITICAL if <5°C or >40°C)
**Cause:** Heating or cooling system insufficient or failed
**Symptoms:**
- Temperature below 15°C or above 30°C in habitable areas
- Heating/cooling unable to maintain setpoint
- Crew discomfort, possible hypothermia or heat stress

**Resolution:**
1. Check thermostat settings (verify set to comfortable range)
2. Verify heating/cooling system powered and operating
3. Check for heat sources (reactor waste heat, equipment)
4. Check for cooling loss (poor insulation, heat radiators failed)
5. Crew should dress appropriately (layers for cold, minimal for heat)
6. Seal unused compartments (reduce area to heat/cool)

**Related:** EMERG-015 (Life Support - Temperature Emergency)

---

### E-LIFE-151: Heating System Failure
**Severity:** CRITICAL (in cold environments)
**Cause:** Heating system offline or insufficient
**Symptoms:**
- Temperature dropping toward freezing
- Heating system not generating heat
- Crew experiencing cold stress, hypothermia risk

**Resolution:**
1. Restart heating system
2. Check power to heating coils/elements
3. Check coolant circulation (if waste heat recovery system)
4. Emergency: Use portable heaters if available
5. Crew gather in single compartment (shared body heat)
6. Increase reactor output (generates waste heat)
7. Don cold weather gear

**Related:** EMERG-015 (Life Support Failures - Cold Emergency)

---

### E-LIFE-152: Cooling System Failure
**Severity:** CRITICAL (in hot environments or near reactors)
**Cause:** Cooling system offline or heat radiators failed
**Symptoms:**
- Temperature rising above 35°C
- Cooling system not functioning
- Crew experiencing heat stress, heat stroke risk

**Resolution:**
1. Restart cooling system
2. Check heat radiators (may be damaged or clogged)
3. Reduce heat generation (lower reactor output, shut down hot equipment)
4. Increase ventilation
5. Crew should hydrate, rest, minimal activity
6. Emergency cooling: Vent air to space and replace (wasteful but effective)

**Related:** EMERG-015 (Life Support Failures - Heat Emergency)

---

## Contamination Errors (E-LIFE-160 series)

### E-LIFE-160: Atmospheric Contamination Detected
**Severity:** WARNING to CRITICAL (depends on contaminant)
**Cause:** Toxic fumes, chemical leak, smoke detected in atmosphere
**Symptoms:**
- Air quality sensors showing contamination
- Unusual odors
- Crew respiratory irritation or symptoms

**Resolution:**
1. All crew don emergency breathing protection
2. Locate contamination source
3. Seal affected area
4. Increase ventilation to maximum
5. Activate atmospheric scrubbers/filters
6. May need to vent atmosphere and replace
7. Identify and remove contaminant source

**Related:** KB-193 (Unusual Smell), EMERG-020 (Fire - Smoke)

---

### E-LIFE-165: Radiation Contamination
**Severity:** CRITICAL
**Cause:** Radioactive material in atmosphere (reactor leak, etc.)
**Symptoms:**
- Radiation detectors showing elevated levels
- Possible reactor compartment breach

**Resolution:**
1. All crew evacuate contaminated areas immediately
2. Seal reactor compartment and affected areas
3. Don radiation protection gear
4. May need to vent contaminated atmosphere to space
5. Crew decontamination procedures
6. Do not re-enter contaminated areas without protection

**Related:** EMERG-005 (Reactor Emergency - Radiation), ERR-PWR-270 (Radiation Errors)

---

## Water System Errors (E-LIFE-170 series)

### E-LIFE-170: Water Recycling System Failure
**Severity:** WARNING
**Cause:** Water recycling/purification system not functioning
**Symptoms:**
- No potable water being produced
- Water quality degraded
- System offline

**Resolution:**
1. Restart water recycling system
2. Check power to system
3. Replace filters if clogged
4. Use emergency water reserves
5. Ration water consumption
6. Calculate water reserves vs. time to port

**Related:** LIFE-SYS-002 (Water Recycling System)

---

### E-LIFE-175: Water Quality Failure
**Severity:** WARNING
**Cause:** Water contamination or purification inadequate
**Symptoms:**
- Water quality sensors showing contamination
- Water appears cloudy or discolored
- Unusual taste or odor

**Resolution:**
1. Do not drink contaminated water
2. Run extra purification cycles
3. Replace water filters
4. Flush system with clean water
5. Use bottled/packaged water reserves
6. Identify contamination source

**Related:** LIFE-SYS-002 (Water System)

---

## System Status and Diagnostics (E-LIFE-900 series)

### E-LIFE-900: Life Support System Test Mode
**Severity:** INFO
**Cause:** System in diagnostic/test mode (not an error)
**Symptoms:**
- Test mode indicator active
- Some functions may be disabled during test

**Resolution:**
- This is informational only
- Exit test mode when diagnostics complete
- Normal operation will resume

---

### E-LIFE-999: Life Support System Reset Required
**Severity:** ADVISORY
**Cause:** System requesting restart after updates or configuration changes
**Symptoms:**
- Persistent advisory message
- System operating but reset recommended

**Resolution:**
1. Plan system restart at convenient time
2. Ensure backup systems ready
3. Perform life support system restart
4. Monitor for proper operation after restart

---

## Error Code Quick Reference

**Immediate Action Required (CRITICAL):**
- E-LIFE-100: Atmospheric system offline
- E-LIFE-120: Oxygen generation failure
- E-LIFE-131: CO₂ scrubber failure
- E-LIFE-140: Low cabin pressure
- E-LIFE-141: Rapid decompression
- E-LIFE-150: Temperature extreme (<5°C or >40°C)
- E-LIFE-165: Radiation contamination

**Investigate Promptly (WARNING):**
- E-LIFE-110: Oxygen level low
- E-LIFE-130: CO₂ level high
- E-LIFE-145: Ventilation failure
- E-LIFE-150: Temperature uncomfortable
- E-LIFE-160: Atmospheric contamination
- E-LIFE-170: Water recycling failure

**Monitor and Schedule (ADVISORY):**
- E-LIFE-135: Scrubber media aging
- E-LIFE-175: Water quality degraded

---

## Related Documents

- LIFE-SYS-001: Atmospheric Processing System Overview
- LIFE-SYS-002: Water Recycling System Manual
- EMERG-015: Life Support System Emergency Procedures
- KB-027: Low Oxygen Alert Troubleshooting

---

**Support Note**: Life support errors are highest priority - crew survival depends on these systems. Even "WARNING" level errors can escalate to life-threatening rapidly. Always assess oxygen reserves and time to safety when troubleshooting life support issues. When in doubt, have crew don emergency oxygen and call for help.
