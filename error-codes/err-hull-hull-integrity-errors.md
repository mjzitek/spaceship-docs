# Hull Integrity System Error Codes (E-HULL Series)

**Document ID:** ERR-HULL-100
**Revision:** 4.2
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides complete error code reference for Hull Integrity Systems including stress sensors, breach detection, emergency bulkheads, and auto-seal systems.

## Error Code Format

**E-HULL-XXX**
- **E**: Error code indicator
- **HULL**: Hull integrity system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Hull breach, immediate danger, life-threatening
- **WARNING** (Orange): Structural risk, investigate immediately
- **ADVISORY** (Yellow): Maintenance required, monitor situation
- **INFO** (Blue): Informational, no immediate danger

---

## Breach Detection Errors (E-HULL-100 series)

### E-HULL-101: Hull Breach Detected
**Severity:** CRITICAL
**Cause:** Pressure loss indicating hole in hull

**Symptoms:**
- Rapid pressure drop
- Breach alarm sounding
- Integrity display shows breach location
- May hear rushing air

**Immediate Actions:**
1. **Don pressure suits immediately**
2. Sound general alarm
3. Locate breach (check integrity display)
4. Evacuate affected compartment
5. Seal bulkheads
6. Deploy emergency seal if safe to approach

**Resolution:**
- Apply emergency sealant or patches
- May need to evacuate and seal compartment
- Permanent repair required at port

**Related:** EMERG-007, HULL-SYS-001

---

### E-HULL-105: Multiple Breach Points Detected
**Severity:** CRITICAL
**Cause:** Two or more breaches simultaneously

**What This Means:**
- Severe damage event (combat, major collision)
- Multiple compartments may be affected
- Ship survival questionable

**Immediate Actions:**
1. All crew don pressure suits
2. Seal multiple bulkheads
3. Triage: Save what can be saved
4. May need to abandon ship if too many breaches
5. Send distress signal

**Resolution:**
- Seal what breaches possible
- Accept loss of severely damaged sections
- Emergency docking/rescue may be required

**Related:** EMERG-007

---

### E-HULL-110: Pressure Loss - Source Unknown
**Severity:** WARNING
**Cause:** Cabin pressure dropping but no specific breach detected

**Possible Causes:**
- Very small leak sensors cannot localize
- Seal failure (door, hatch, window)
- Multiple micro-leaks
- Sensor array malfunction

**Resolution:**
- Use smoke test to locate leak
- Check all seals and hatches
- Inspect recent maintenance work
- May need systematic compartment isolation

**Related:** HULL-SYS-001

---

### E-HULL-115: Decompression Rate Critical
**Severity:** CRITICAL
**Cause:** Pressure dropping faster than emergency systems can compensate

**Symptoms:**
- Pressure gauge rapidly declining
- Large breach or multiple breaches
- Explosive decompression risk

**Immediate Actions:**
1. Emergency evacuation of affected areas
2. All crew don suits immediately
3. Seal multiple bulkheads (isolate large area)
4. Do NOT attempt to seal breach - too dangerous
5. Accept loss of compartment

**Related:** EMERG-007

---

## Structural Integrity Errors (E-HULL-200 series)

### E-HULL-201: Hull Stress Elevated
**Severity:** ADVISORY
**Cause:** Stress sensors showing above-normal readings

**Symptoms:**
- Single or multiple sensors reading 60-75% of max stress
- Yellow indicators on hull display
- May be normal during high-G maneuvers

**Resolution:**
- Check if readings return to normal after maneuver ends
- Inspect high-stress areas for damage
- May be normal for current operations
- If persistent: Schedule inspection within 24 hours

**Related:** HULL-SYS-001

---

### E-HULL-205: Hull Stress Critical
**Severity:** CRITICAL
**Cause:** Stress sensors at or exceeding safe limits

**Symptoms:**
- Sensors showing >85% of maximum rated stress
- Red indicators on hull display
- May hear creaking or popping sounds
- Imminent structural failure risk

**Immediate Actions:**
1. **Reduce all stress immediately**
   - Cut engines to zero
   - Cancel all maneuvers
   - Maintain steady course and speed
2. Alert crew to potential structural failure
3. Prepare for emergency (don suits, evacuation readiness)
4. Inspect stressed area if safe to do so

**Resolution:**
- Do NOT resume high stress operations
- Proceed to port at minimum safe speed
- Emergency structural reinforcement may be needed
- Professional inspection required

**Related:** HULL-SYS-001

---

### E-HULL-210: Stress Fracture Detected
**Severity:** WARNING
**Cause:** Micro-cracks in hull detected by sensors

**Symptoms:**
- Stress sensors showing localized anomaly
- May have cre aking sounds during acceleration
- Fracture will worsen over time if not repaired

**Resolution:**
- Reduce operations in affected area
- Apply structural reinforcement bracing
- Limit acceleration and maneuvers
- Repair at port (may require hull plating replacement)
- Do NOT defer - fractures can catastrophically fail

**Related:** HULL-SYS-001

---

### E-HULL-215: Structural Failure Imminent
**Severity:** CRITICAL
**Cause:** Hull about to fail catastrophically

**Symptoms:**
- Multiple critical stress readings
- Propagating cracks detected
- Visible hull deformation
- Loud sounds from hull

**Immediate Actions:**
1. **Emergency evacuation of affected section**
2. All crew don pressure suits
3. Seal multiple bulkheads (anticipate breach)
4. Reduce ALL stress to zero
5. Send distress signal
6. Prepare to abandon ship if failure occurs

**Related:** EMERG-007, HULL-SYS-001

---

## Bulkhead and Seal Errors (E-HULL-300 series)

### E-HULL-301: Bulkhead Seal Failure
**Severity:** CRITICAL (if breach present)
**Cause:** Emergency bulkhead not sealing properly

**Symptoms:**
- Bulkhead closed but still leaking air
- Pressure equalizing across bulkhead
- Seal indicators showing red

**Immediate Actions:**
1. Evacuate both sides of failed bulkhead
2. Seal next bulkhead in line
3. Accept loss of additional compartment
4. May need manual seal reinforcement

**Resolution:**
- Inspect gaskets (may be damaged or worn)
- Check seal mechanism for obstruction
- Replace gaskets if possible (Part #: GSK-BH-series)
- May need professional repair

**Related:** HULL-SYS-001, EMERG-007

---

### E-HULL-305: Bulkhead Will Not Close
**Severity:** CRITICAL (during emergency)
**Cause:** Bulkhead door stuck open

**Possible Causes:**
- Mechanical jam (object in doorway)
- Hydraulic failure
- Control system failure
- Structural deformation preventing closure

**Immediate Actions:**
1. Check for obstruction (remove if present)
2. Try manual closure mechanism
3. If cannot close: Evacuate to next bulkhead
4. Seal next bulkhead in sequence

**Resolution:**
- Clear obstruction
- Check hydraulic pressure
- Lubricate door mechanism
- Check control system power
- May need hydraulic pump replacement

**Related:** HULL-SYS-001

---

### E-HULL-310: Bulkhead Auto-Close Malfunction
**Severity:** WARNING
**Cause:** Automatic closure system not responding

**What This Means:**
- Bulkhead will not close automatically on breach
- Manual closure still available
- Safety system degraded

**Resolution:**
- Test bulkhead manually (verify can still close)
- Check auto-close sensors
- Check control system connection
- Repair auto-close system promptly
- Required for safety compliance

**Related:** HULL-SYS-001

---

### E-HULL-315: Multiple Bulkhead Failures
**Severity:** CRITICAL
**Cause:** Several bulkheads not functioning

**What This Means:**
- May indicate ship-wide system failure
- Could be power, computer, or hydraulic system
- Compartment isolation compromised

**Resolution:**
- Check bulkhead control system power
- Check hydraulic system pressure (if hydraulic bulkheads)
- May be control computer failure
- Manual closure still possible (use manual handles)

**Related:** HULL-SYS-001

---

## Auto-Seal System Errors (E-HULL-400 series)

### E-HULL-401: Auto-Seal System Failure
**Severity:** WARNING
**Cause:** Emergency sealant dispensers not functioning

**Symptoms:**
- Dispenser status showing "FAULT"
- May not deploy when breach occurs
- Manual sealant still available

**Resolution:**
- Check dispenser power supply
- Verify sealant canisters installed and pressurized
- Check dispenser nozzles not clogged
- Replace sealant canisters if expired (Part #: SEAL-AUTO-CAN)
- Test dispenser in test mode

**Related:** HULL-SYS-001

---

### E-HULL-405: Auto-Seal Deployment Failed
**Severity:** CRITICAL (if breach present)
**Cause:** Sealant did not deploy despite breach detected

**Possible Causes:**
- Dispenser empty or canisters expired
- Nozzle clogged
- Deployment system mechanical failure
- Breach too large for auto-seal

**Immediate Actions:**
1. Use manual sealant immediately (canisters from emergency lockers)
2. Apply hull patches if breach small enough
3. May need to evacuate and seal bulkhead if cannot seal breach

**Resolution:**
- Refill/replace auto-seal canisters
- Clear clogged nozzles
- Repair deployment mechanism

**Related:** HULL-SYS-001, EMERG-007

---

### E-HULL-410: Auto-Seal Supply Low
**Severity:** ADVISORY
**Cause:** Sealant canisters below 50% capacity

**What This Means:**
- Still functional but reduced capacity
- May not be sufficient for large breach
- Needs refill soon

**Resolution:**
- Replace or refill sealant canisters
- Stock minimum 6 canisters per dispenser location
- Check expiration dates (sealant expires after 24 months)

**Related:** HULL-SYS-001

---

## Sensor and Monitoring Errors (E-HULL-500 series)

### E-HULL-501: Stress Sensor Malfunction
**Severity:** ADVISORY
**Cause:** One or more hull stress sensors failed

**Symptoms:**
- Sensor reading obviously wrong (0%, 100%, or erratic)
- Sensor disagrees with adjacent sensors
- Hull display shows sensor fault

**Resolution:**
- Note which sensor failed (hull display shows location)
- Can operate with some sensors failed (redundancy)
- Replace failed sensor when convenient (Part #: SNR-STR-HULL)
- If multiple sensors failed: May indicate wiring or computer issue

**Related:** HULL-SYS-001

---

### E-HULL-505: Breach Detector Malfunction
**Severity:** WARNING
**Cause:** Pressure sensors used for breach detection failed

**Symptoms:**
- Pressure reading incorrect or erratic
- May cause false alarms or miss real breaches
- Multiple sensors disagreeing

**Resolution:**
- Compare to manual pressure gauges
- Calibrate sensors
- Replace failed sensors (Part #: SNR-PRES-HULL)
- Minimum 2 sensors per compartment required for breach detection

**Related:** HULL-SYS-001

---

### E-HULL-510: Hull Temperature Sensor Fault
**Severity:** ADVISORY
**Cause:** Temperature sensor giving invalid readings

**What This Means:**
- May indicate hull damage (hot or cold spots)
- Or sensor failure
- Cannot distinguish without inspection

**Resolution:**
- Inspect area around failed sensor
- Check for actual temperature anomaly (thermal camera if available)
- Replace sensor if faulty
- Investigate if real temperature issue

**Related:** HULL-SYS-001

---

### E-HULL-515: Integrity Monitor Computer Offline
**Severity:** CRITICAL
**Cause:** Computer processing sensor data has failed

**Symptoms:**
- Hull integrity display dark or unresponsive
- No automatic breach detection
- No automatic bulkhead closure
- Sensors still working but not monitored

**Immediate Actions:**
1. Manual monitoring required
2. Crew must watch pressure gauges manually
3. Manual bulkhead operation if breach
4. Reduce risky operations until repaired

**Resolution:**
- Reboot integrity monitor computer
- Check power supply
- Replace computer if failed (Part #: CTRL-HULL-A)
- System restore from backup if software corruption

**Related:** HULL-SYS-001

---

## Radiation Shielding Errors (E-HULL-600 series)

### E-HULL-601: Radiation Level Elevated
**Severity:** WARNING
**Cause:** Radiation detector showing higher than normal readings

**Possible Causes:**
- Hull shielding damaged
- Reactor shielding breach
- External radiation source (nearby pulsar, etc.)

**Resolution:**
- Check radiation detectors (multiple locations)
- Identify radiation source
- If shielding damaged: Repair at port
- If reactor issue: See EMERG-005
- If external source: Move away from source

**Related:** PWR-SYS-001, HULL-SYS-001

---

### E-HULL-605: Shielding Integrity Compromised
**Severity:** WARNING
**Cause:** Hull breach or damage affecting radiation shielding

**What This Means:**
- Lead-polymer shielding layers damaged
- Crew exposed to higher cosmic radiation
- Not immediately life-threatening but increases cancer risk
- Long-term exposure dangerous

**Resolution:**
- Identify damaged section
- Evacuate crew from high-radiation areas
- Apply shielding patches if possible (Part #: SHD-RAD-25)
- Permanent repair at port required

**Related:** HULL-SYS-001

---

### E-HULL-610: Radiation Detector Malfunction
**Severity:** ADVISORY
**Cause:** Radiation sensor failed

**Resolution:**
- Use portable radiation detectors
- Replace failed sensor (Part #: SNR-RAD-HULL)
- Multiple sensors for redundancy
- Can operate with some sensors failed

**Related:** HULL-SYS-001

---

## External Hull Errors (E-HULL-700 series)

### E-HULL-701: Hull Corrosion Detected
**Severity:** ADVISORY
**Cause:** Hull plating showing corrosion/degradation

**Symptoms:**
- Visual inspection shows discoloration, pitting
- Ultrasonic thickness measurement shows thinning
- Older vessels or those in corrosive environments

**Resolution:**
- Identify corroded areas
- Sandblast and apply anti-corrosion coating
- Replace plating if severely degraded
- Determine corrosion cause (eliminate if possible)

**Related:** HULL-SYS-001

---

### E-HULL-705: Hull Thickness Below Minimum
**Severity:** WARNING
**Cause:** Hull plating worn/corroded below safe thickness

**What This Means:**
- Hull strength compromised
- Breach risk elevated
- Pressure rating reduced

**Resolution:**
- Replace affected hull plating sections
- Requires yard service
- Do NOT defer - thin hull can fail

**Related:** HULL-SYS-001

---

### E-HULL-710: Micrometeorite Damage Detected
**Severity:** ADVISORY (INFO if sealed)
**Cause:** Small impacts creating pits or tiny breaches

**Symptoms:**
- Small holes (1-5mm) in hull
- Slow pressure leak
- Very common in space travel

**Resolution:**
- Locate impacts (may be multiple)
- Apply adhesive patches
- Log locations for inspection at port
- Part of normal wear and tear

**Related:** HULL-SYS-001

---

### E-HULL-715: Hull Deformation Detected
**Severity:** WARNING
**Cause:** Hull structure bent or warped

**Possible Causes:**
- Collision damage
- Excessive stress
- Explosion or impact
- Structural failure

**Resolution:**
- Inspect affected area
- May need structural reinforcement
- Professional assessment required
- May require hull plating replacement and frame repair

**Related:** HULL-SYS-001

---

## Emergency Equipment Errors (E-HULL-800 series)

### E-HULL-801: Pressure Suit Missing or Expired
**Severity:** WARNING
**Cause:** Emergency suit not in expected location or past service date

**What This Means:**
- During decompression, crew may not have suits
- Potentially life-threatening
- Regulatory violation

**Resolution:**
- Locate missing suits (may be in wrong locker)
- Replace expired suits (service life: 5 years)
- Verify suit count (minimum: 1 per crew + 25% spare)
- Conduct monthly suit inventory

**Related:** HULL-SYS-001, EMERG-007

---

### E-HULL-805: Pressure Suit O₂ Depleted
**Severity:** ADVISORY
**Cause:** Emergency suit oxygen tank empty or low

**Resolution:**
- Recharge O₂ tanks (requires compression equipment or port service)
- Replace O₂ cartridges if expired
- Check all suits monthly
- Suits with low O₂ useless in emergency

**Related:** HULL-SYS-001

---

### E-HULL-810: Emergency Patch Kit Incomplete
**Severity:** ADVISORY
**Cause:** Patch kit missing items or depleted

**What This Means:**
- May not be able to seal breach if one occurs
- Check kit inventory

**Resolution:**
- Replenish patch kit (Part #: PATCH-EMERG-KIT)
- Should contain: 10 patches (various sizes), epoxy, clamps, tools
- Replace used items immediately
- Minimum 2 kits per vessel section

**Related:** HULL-SYS-001

---

## Error Code Quick Reference

| Code | System | Severity | Description |
|------|--------|----------|-------------|
| E-HULL-101 | Breach | CRITICAL | Hull breach detected |
| E-HULL-105 | Breach | CRITICAL | Multiple breaches |
| E-HULL-110 | Pressure | WARNING | Leak source unknown |
| E-HULL-115 | Decompression | CRITICAL | Critical decompression rate |
| E-HULL-201 | Stress | ADVISORY | Stress elevated |
| E-HULL-205 | Stress | CRITICAL | Stress critical |
| E-HULL-210 | Fracture | WARNING | Stress fracture detected |
| E-HULL-215 | Structure | CRITICAL | Failure imminent |
| E-HULL-301 | Bulkhead | CRITICAL | Seal failure |
| E-HULL-305 | Bulkhead | CRITICAL | Won't close |
| E-HULL-310 | Bulkhead | WARNING | Auto-close fault |
| E-HULL-315 | Bulkhead | CRITICAL | Multiple failures |
| E-HULL-401 | Auto-Seal | WARNING | System failure |
| E-HULL-405 | Auto-Seal | CRITICAL | Deployment failed |
| E-HULL-410 | Auto-Seal | ADVISORY | Supply low |
| E-HULL-501 | Sensor | ADVISORY | Stress sensor fault |
| E-HULL-505 | Sensor | WARNING | Breach detector fault |
| E-HULL-510 | Sensor | ADVISORY | Temperature sensor fault |
| E-HULL-515 | Computer | CRITICAL | Monitor offline |
| E-HULL-601 | Radiation | WARNING | Radiation elevated |
| E-HULL-605 | Shielding | WARNING | Shielding compromised |
| E-HULL-610 | Sensor | ADVISORY | Rad detector fault |
| E-HULL-701 | Hull | ADVISORY | Corrosion detected |
| E-HULL-705 | Hull | WARNING | Thickness below min |
| E-HULL-710 | Hull | ADVISORY | Micrometeorite damage |
| E-HULL-715 | Hull | WARNING | Deformation |
| E-HULL-801 | Equipment | WARNING | Suit missing/expired |
| E-HULL-805 | Equipment | ADVISORY | Suit O₂ depleted |
| E-HULL-810 | Equipment | ADVISORY | Patch kit incomplete |

## Related Documents

- HULL-SYS-001: Hull Integrity Systems Overview
- HULL-SYS-002: Hull Inspection Procedures
- HULL-SYS-004: Hull Repair Manual
- EMERG-007: Decompression Emergency Procedures
- PWR-SYS-001: Q-Core Reactor (radiation shielding)

---

**Document maintained by ORSM Technical Publications. Hull integrity is life-critical - respond to all WARNING and CRITICAL level codes immediately.**
