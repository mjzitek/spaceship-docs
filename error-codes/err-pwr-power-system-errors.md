# Power System Error Codes (E-PWR Series)

**Document ID:** ERR-PWR-100
**Revision:** 5.2
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides a complete reference of error codes for Q-Core Reactor and power distribution systems. Error codes are displayed on reactor control panels and logged in system diagnostics.

## Error Code Format

**E-PWR-XXX**
- **E**: Error code indicator
- **PWR**: Power system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Immediate action required, safety risk, reactor shutdown recommended
- **WARNING** (Orange): Investigate promptly, may escalate to critical
- **ADVISORY** (Yellow): Monitor situation, schedule maintenance
- **INFO** (Blue): Informational only, no action required

---

## Startup and Initialization Errors (E-PWR-100 series)

### E-PWR-101: Fuel System Initialization Failed
**Severity:** WARNING
**Cause:** Insufficient fuel pressure or fuel delivery system malfunction
**Symptoms:**
- Startup sequence aborts before ignition
- Fuel pressure gauge shows <100 PSI
- Plasma injectors not firing

**Resolution:**
1. Check fuel canister pressure (should be 150-200 PSI)
2. Replace fuel canister if depleted
3. Inspect fuel lines for blockages or leaks
4. Test fuel valve operation (should be fully open)

**Related:** PWR-SYS-002 (Startup Procedures), KB-001 (Reactor Won't Start)

---

### E-PWR-102: Magnetic Containment System Failure
**Severity:** CRITICAL
**Cause:** Magnetic coils not generating adequate field strength
**Symptoms:**
- Startup aborts during field initialization
- Field strength below 4.0 Tesla
- One or more coils showing red status

**Resolution:**
1. Check coil power supply (380-420 VDC required)
2. Test individual coils for failures
3. Reset breaker if tripped
4. Replace failed coils (Part #: MAG-COIL-Q series)
5. Recalibrate magnetic containment system

**Related:** PWR-SYS-004 (Troubleshooting), EMERG-005 (Reactor Emergencies)

---

### E-PWR-103: Coolant System Not Ready
**Severity:** WARNING
**Cause:** Coolant level low or pumps not operating
**Symptoms:**
- Startup sequence prevents ignition
- Coolant level indicator showing <85%
- Coolant pumps not running

**Resolution:**
1. Check coolant reservoir level (must be ≥85%)
2. Top off with Grade-A sodium-potassium coolant
3. Verify coolant pumps powered and running
4. Check for coolant leaks
5. Purge air from coolant system if recently serviced

**Related:** PWR-SYS-003 (Maintenance), KB-042 (Coolant System Issues)

---

### E-PWR-104: Reactor Control System Boot Failure
**Severity:** WARNING
**Cause:** Control computer failed self-test during startup
**Symptoms:**
- Control panel dark or showing garbled display
- No response to button presses
- Reactor unable to initiate startup sequence

**Resolution:**
1. Power cycle control system (breaker off 30 seconds, then on)
2. Check control board power supply (24 VDC required)
3. Run diagnostic test from maintenance menu
4. Update control firmware if outdated
5. Replace control board if failed (Part #: CTL-QCR-series)

**Related:** Contact ORSM Support for control system issues

---

### E-PWR-105: Pre-Startup Safety Check Failed
**Severity:** WARNING
**Cause:** One or more safety interlocks preventing startup
**Symptoms:**
- Startup sequence blocked
- Safety interlock indicator showing red
- May indicate open access panels, failed sensors, or previous SCRAM event

**Resolution:**
1. Check all access panels closed and latched
2. Verify no maintenance locks or safety tags installed
3. Review recent maintenance (may have been tagged out)
4. Check radiation shielding integrity
5. Clear SCRAM lockout if present (requires qualified technician)

**Related:** PWR-SYS-002 (Startup Procedures)

---

## Power Generation Errors (E-PWR-200 series)

### E-PWR-201: Insufficient Power Output
**Severity:** ADVISORY
**Cause:** Reactor running but producing less than expected power
**Symptoms:**
- Power output below 50% despite adequate throttle
- Ship systems starved for power
- Core temperature normal but power low

**Resolution:**
1. Clean or replace fuel injectors
2. Check plasma density (should be 3.5-4.2 g/cm³)
3. Recalibrate magnetic containment
4. Test thermoelectric converters (should show ≥85% efficiency)
5. Check for excessive coolant flow (stealing heat)

**Related:** PWR-SYS-004 (Troubleshooting), KB-015 (Low Power Output)

---

### E-PWR-220: Core Temperature Critical High
**Severity:** CRITICAL
**Cause:** Core temperature exceeding 3,000°C
**Symptoms:**
- Temperature alarms sounding
- Display showing red temperature warning
- Automatic throttle reduction may engage

**Resolution:**
1. **IMMEDIATE**: Reduce fuel injection rate by 50%
2. Increase coolant flow to maximum
3. Reduce power demand (shut down non-essential systems)
4. If temperature continues rising, initiate emergency SCRAM
5. Investigate cause:
   - Coolant system failure?
   - Plasma containment degraded?
   - Over-fueling?

**Related:** PWR-SYS-004 (Troubleshooting), EMERG-005 (Reactor Emergencies)

---

### E-PWR-221: Core Temperature Elevated
**Severity:** WARNING
**Cause:** Core temperature above 2,800°C but below critical
**Symptoms:**
- Temperature higher than normal for power output level
- May indicate cooling system degradation

**Resolution:**
1. Check coolant system operation
2. Verify coolant flow rate appropriate for power level
3. Inspect for coolant leaks
4. Check heat exchanger function
5. Reduce reactor load if temperature continues rising

**Related:** PWR-SYS-004 (Troubleshooting)

---

### E-PWR-225: Core Temperature Critical Low
**Severity:** WARNING
**Cause:** Core temperature below 1,200°C during operation
**Symptoms:**
- Fusion reaction weak or unstable
- Power output very low
- May indicate fuel delivery problem

**Resolution:**
1. Increase fuel injection rate
2. Check fuel pressure and delivery
3. Verify plasma injectors firing correctly
4. Increase magnetic field strength slightly
5. Check for coolant over-circulation

**Related:** PWR-SYS-004 (Troubleshooting)

---

## Plasma Containment Errors (E-PWR-250 series)

### E-PWR-250: Plasma Instability Detected
**Severity:** CRITICAL
**Cause:** Plasma density or temperature fluctuating beyond safe limits
**Symptoms:**
- Rapid plasma density variations
- Power output oscillating
- Vibrations from reactor compartment
- Temperature swings ±200°C or more

**Resolution:**
1. **IMMEDIATE**: Reduce reactor to minimum stable output
2. Decrease fuel injection by 50%
3. Increase magnetic field by 0.5 Tesla
4. Check for magnetic coil failures
5. Verify fuel injection consistency
6. If instability continues, initiate shutdown

**Related:** PWR-SYS-004 (Troubleshooting), EMERG-005 (Reactor Emergencies)

---

### E-PWR-251: Containment Field Failure Imminent
**Severity:** CRITICAL
**Cause:** Magnetic containment field strength critically low or irregular
**Symptoms:**
- Field strength below 5.0 Tesla during operation
- Field uniformity <92%
- Multiple magnetic coils showing faults

**Resolution:**
1. **IMMEDIATE**: Press emergency SCRAM button
2. Do not attempt to stabilize - risk of containment breach too high
3. Evacuate reactor compartment
4. Monitor radiation levels
5. Contact ORSM emergency support immediately

**Related:** EMERG-005 (Reactor Emergencies)

---

### E-PWR-255: Magnetic Field Asymmetry
**Severity:** WARNING
**Cause:** Magnetic containment field not uniform around plasma
**Symptoms:**
- Field uniformity reading <95%
- Plasma touching chamber walls in spots (creates hot spots)
- Reduced efficiency

**Resolution:**
1. Run magnetic field calibration procedure
2. Test all 12 containment coils individually
3. Replace any failed or degraded coils
4. Recalibrate field after coil replacement
5. May need to reduce power output until repairs completed

**Related:** PWR-SYS-003 (Maintenance)

---

## Coolant System Errors (E-PWR-260 series)

### E-PWR-260: Coolant Loss Detected
**Severity:** CRITICAL
**Cause:** Coolant pressure dropping, indicating leak
**Symptoms:**
- Coolant pressure gauge showing declining PSI
- Coolant level indicator dropping
- Visible coolant leaks or puddles
- Rising core temperature despite adequate flow setting

**Resolution:**
1. **IMMEDIATE**: Initiate emergency shutdown
2. Locate coolant leak (follow wet spots, check pressure gauges)
3. Attempt temporary repair if accessible
4. Refill coolant system
5. Do not restart reactor until leak sealed and system pressure-tested

**Related:** PWR-SYS-003 (Maintenance), EMERG-005 (Reactor Emergencies)

---

### E-PWR-261: Coolant Pump Failure
**Severity:** CRITICAL
**Cause:** Primary coolant pump stopped or operating at reduced capacity
**Symptoms:**
- Coolant flow indicator showing zero or low flow
- Pump status light red
- Rapid core temperature rise
- No pump motor sound

**Resolution:**
1. **IMMEDIATE**: Switch to backup coolant pump (if equipped)
2. If no backup or backup also failed, initiate emergency SCRAM
3. Check pump power supply
4. Check for pump mechanical seizure (shaft stuck)
5. Replace pump if failed (Part #: PMP-COL-Q series)

**Related:** EMERG-005 (Reactor Emergencies)

---

### E-PWR-265: Coolant Contaminated
**Severity:** WARNING
**Cause:** Coolant quality degraded, pH out of range, or contamination detected
**Symptoms:**
- Coolant appears brown or black (should be silver-gray)
- pH reading outside 7.5-8.5 range
- Cooling efficiency reduced
- Possible sludge buildup

**Resolution:**
1. Schedule coolant flush and replacement
2. Inspect coolant system for corrosion source
3. Replace coolant filters
4. Can continue operation short-term but plan replacement soon
5. Use fresh Grade-A sodium-potassium coolant

**Related:** PWR-SYS-003 (Maintenance)

---

## Fuel System Errors (E-PWR-180 series)

### E-PWR-180: Fuel Injector Performance Degraded
**Severity:** ADVISORY
**Cause:** One or more fuel injectors clogged or failing
**Symptoms:**
- Uneven plasma density
- Reduced power output
- Some injectors not firing or firing irregularly

**Resolution:**
1. Run individual injector diagnostic test
2. Clean clogged injectors (use 3mm titanium rods)
3. Replace failed injectors (Part #: INJ-ASM-Q3/5/7)
4. Replace injector O-rings during service
5. Check fuel quality (contaminated fuel clogs injectors)

**Related:** PWR-SYS-003 (Maintenance), PWR-SYS-004 (Troubleshooting)

---

### E-PWR-185: Fuel Pressure Low
**Severity:** WARNING
**Cause:** Fuel canister depleted or pressure regulator malfunction
**Symptoms:**
- Fuel pressure gauge <120 PSI during operation
- Plasma density lower than expected
- Power output reduced

**Resolution:**
1. Check fuel canister pressure (should be 150-200 PSI)
2. Replace canister if below 100 PSI
3. Test fuel pressure regulator
4. Check for fuel line leaks
5. Verify fuel valve fully open

**Related:** KB-001 (Reactor Won't Start)

---

### E-PWR-189: Fuel Quality Out of Specification
**Severity:** WARNING
**Cause:** Fuel contaminated or incorrect fuel type installed
**Symptoms:**
- Irregular plasma formation
- Excessive buildup on injectors
- Unusual combustion characteristics

**Resolution:**
1. Check fuel canister label (should be D-T pellets, 3mm diameter)
2. Do not mix fuel types
3. Replace fuel with certified ORSM fuel canisters
4. Clean fuel system if contaminated fuel was used
5. May need to clean or replace injectors

**Related:** Fuel specifications in PWR-SYS-001

---

## Radiation and Safety Errors (E-PWR-270 series)

### E-PWR-270: Radiation Level Critical
**Severity:** CRITICAL
**Cause:** Radiation exceeding safe levels outside reactor shielding
**Symptoms:**
- Radiation detector showing >2.0 mSv/h at 1 meter from reactor
- Radiation alarms sounding
- May indicate shielding damage or breach

**Resolution:**
1. **IMMEDIATE**: Evacuate reactor compartment and adjacent areas
2. Initiate reactor shutdown
3. Don radiation protection gear before approaching reactor
4. Inspect shielding for cracks, gaps, or displaced panels
5. Repair shielding before restarting reactor
6. Contact ORSM for radiation safety assessment

**Related:** EMERG-005 (Reactor Emergencies)

---

### E-PWR-275: Emergency Shutdown System Test Failed
**Severity:** WARNING
**Cause:** SCRAM system self-test detected malfunction
**Symptoms:**
- Monthly diagnostic reports SCRAM system not responding
- Emergency shutdown button may not function

**Resolution:**
1. **DO NOT operate reactor until SCRAM system repaired**
2. Test SCRAM button circuit
3. Check emergency fuel cutoff valve operation
4. Verify magnetic field dump mechanism functional
5. Contact qualified technician for SCRAM system service

**Related:** Safety systems in PWR-SYS-001

---

## Control System Errors (E-PWR-300 series)

### E-PWR-301: Control Computer Memory Error
**Severity:** WARNING
**Cause:** RAM or storage fault in reactor control computer
**Symptoms:**
- Erratic parameter readings
- Control system crashes or freezes
- Data logging failures

**Resolution:**
1. Run memory diagnostic test
2. Power cycle control computer
3. Check for firmware corruption (reinstall if needed)
4. Replace control board if memory hardware failed

**Related:** Contact ORSM technical support

---

### E-PWR-305: Sensor Communication Failure
**Severity:** WARNING
**Cause:** Control computer unable to read one or more sensors
**Symptoms:**
- Parameter readings show "---" or freeze
- Sensor status shows red or disconnected
- System operating on estimates

**Resolution:**
1. Check sensor wiring and connections
2. Test sensor output voltage (varies by sensor type)
3. Replace failed sensors
4. Verify control board sensor input ports functional
5. Recalibrate sensors after replacement

**Related:** PWR-SYS-003 (Maintenance)

---

### E-PWR-350: Parameter Drift Detected
**Severity:** ADVISORY
**Cause:** Sensors showing gradual drift from calibration
**Symptoms:**
- Sensors reading consistently high or low compared to redundant sensors
- Trend analysis shows drift over time

**Resolution:**
1. Run sensor calibration procedure
2. Compare sensor readings to reference standards
3. Adjust sensor calibration if within allowable range
4. Replace sensor if drift excessive or calibration ineffective
5. Monthly sensor check prevents drift from becoming critical

**Related:** PWR-SYS-003 (Maintenance)

---

## Maintenance and Service Errors (E-PWR-400 series)

### E-PWR-400: Routine Maintenance Due
**Severity:** INFO
**Cause:** Scheduled maintenance interval reached
**Symptoms:**
- Yellow wrench icon on display
- Message "MAINTENANCE DUE" on startup

**Resolution:**
1. Review maintenance schedule (PWR-SYS-003)
2. Perform due maintenance items
3. Log maintenance completion in ship's records
4. Clear maintenance reminder in system settings

**Related:** PWR-SYS-003 (Maintenance Schedule)

---

### E-PWR-405: Component Lifespan Warning
**Severity:** ADVISORY
**Cause:** Consumable component approaching end of rated lifespan
**Symptoms:**
- Warning message specifying component (e.g., "Injector O-rings: 90% lifespan")
- Component may still be functional but should be replaced proactively

**Resolution:**
1. Order replacement component
2. Schedule replacement during next maintenance window
3. Don't wait for complete failure (preventive replacement avoids downtime)

**Common Components with Lifespan Warnings:**
- Injector O-rings: Every 3 months
- HEPA filters: Every 6 months
- UV lamp: Every 12 months
- Coolant: Annual replacement

**Related:** Parts list in PWR-SYS-003

---

### E-PWR-410: Firmware Update Available
**Severity:** INFO
**Cause:** New reactor control firmware released by ORSM
**Symptoms:**
- Info message on startup
- May include bug fixes or performance improvements

**Resolution:**
1. Download firmware from ORSM service portal
2. Follow firmware update procedure (see service bulletin)
3. Perform update during scheduled maintenance
4. Verify system functionality after update

**Related:** ORSM Service Portal: support.outerrimstarship.com

---

## Troubleshooting Multiple Error Codes

If multiple error codes present simultaneously:

**Priority Order:**
1. **E-PWR-250 series** (Plasma containment) - Highest priority
2. **E-PWR-260 series** (Coolant system) - Second priority
3. **E-PWR-220/221** (Temperature critical) - Third priority
4. **E-PWR-100 series** (Startup issues) - Fourth priority
5. **E-PWR-400 series** (Maintenance reminders) - Lowest priority

**Cascade Errors:**
Some errors cause others:
- Coolant failure (E-PWR-260) → Temperature critical (E-PWR-220)
- Fuel pressure low (E-PWR-185) → Insufficient power (E-PWR-201)
- Sensor failure (E-PWR-305) → May trigger false alarms

**Strategy:**
1. Address root cause first
2. Secondary errors may clear automatically
3. If in doubt, shut down reactor and diagnose systematically

## Error Code Lookup Quick Reference

**By Severity:**
- **Critical (Immediate Action):** 102, 220, 250, 251, 260, 261, 270
- **Warning (Investigate Promptly):** 101, 103, 221, 225, 255, 265, 275, 301, 305
- **Advisory (Schedule Maintenance):** 201, 180, 189, 350, 405
- **Info (Awareness Only):** 400, 410

**By System:**
- **Startup:** 101-105
- **Power Generation:** 201-225
- **Plasma Containment:** 250-255
- **Coolant:** 260-265
- **Fuel:** 180-189
- **Safety:** 270-275
- **Control:** 301-350
- **Maintenance:** 400-410

## Related Documents

- PWR-SYS-001: Q-Core Reactor Overview
- PWR-SYS-002: Startup and Shutdown Procedures
- PWR-SYS-003: Maintenance Guide
- PWR-SYS-004: Troubleshooting Manual
- EMERG-005: Reactor Emergency Procedures

---

**Document maintained by ORSM Technical Publications. Report errors or omissions to techpubs@outerrimstarship.com**
