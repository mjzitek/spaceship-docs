# Navigation System Error Codes (E-NAV Series)

**Document ID:** ERR-NAV-500
**Revision:** 4.7
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides complete reference for error codes related to navigation systems including sublight engines (Model-3 Impellers) and FTL drive (Horizon-Class). Error codes displayed on navigation console and helm displays.

## Error Code Format

**E-NAV-XXX**
- **E**: Error code indicator
- **NAV**: Navigation system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Immediate action required, safety risk, abort operations
- **WARNING** (Orange): Investigate promptly, may prevent navigation
- **ADVISORY** (Yellow): Monitor situation, schedule maintenance
- **INFO** (Blue): Informational only, no action required

---

## Sublight Engine Errors (E-NAV-100 series)

### E-NAV-101: Engine Startup Failure
**Severity:** WARNING
**Cause:** Sublight impeller unable to complete startup sequence
**Symptoms:**
- Engine remains cold when startup initiated
- Plasma chamber won't reach operating temperature
- Thrust output zero despite throttle command

**Resolution:**
1. Check power supply from Q-Core reactor
2. Verify coolant system operational
3. Test fuel pressure (deuterium should be 120-150 PSI)
4. Check plasma chamber pre-heater operation
5. Inspect acceleration coil power (should reach 10 A in standby)

**Related:** NAV-SUB-001 (Sublight Engine Overview), NAV-SUB-003 (Troubleshooting)

---

### E-NAV-102: Thrust Output Below Expected
**Severity:** WARNING
**Cause:** Engine running but producing insufficient thrust
**Symptoms:**
- Thrust indicator showing <70% of commanded level
- Acceleration lower than expected
- Engine parameters appear normal otherwise

**Resolution:**
1. Clean or replace fuel injectors (clogged injectors common)
2. Check plasma chamber for carbon buildup
3. Test acceleration coil current (should be 80-180 A depending on thrust)
4. Inspect thrust nozzle for blockage or damage
5. Verify fuel quality (contaminated deuterium reduces efficiency)

**Related:** NAV-SUB-002 (Maintenance), KB-015 (Low Thrust Output)

---

### E-NAV-110: Engine Overheating
**Severity:** CRITICAL
**Cause:** Plasma chamber temperature exceeding safe limits
**Symptoms:**
- Temperature >1,800°C
- Automatic thrust reduction engaged
- Thermal alarms sounding

**Resolution:**
1. **IMMEDIATE**: Reduce thrust to 50% or less
2. Increase coolant flow to maximum
3. Check for coolant leaks or pump failure
4. Verify coolant level adequate (≥85%)
5. If temperature >1,900°C, shut down engine immediately
6. Investigate cause before resuming high-thrust operations

**Related:** NAV-SUB-003 (Troubleshooting), EMERG-010 (Engine Emergencies)

---

### E-NAV-115: Coolant System Malfunction
**Severity:** CRITICAL
**Cause:** Engine coolant pressure low or pump failure
**Symptoms:**
- Coolant pressure <60 PSI during operation
- Engine temperature rising rapidly
- Coolant pump status showing fault

**Resolution:**
1. **IMMEDIATE**: Reduce engine thrust to minimum
2. Check coolant reservoir level
3. Inspect for visible coolant leaks
4. Verify coolant pump operating (should hear pump motor)
5. Switch to backup cooling if available
6. If coolant system cannot be restored, shut down engine

**Related:** NAV-SUB-003 (Troubleshooting)

---

### E-NAV-120: Acceleration Coil Failure
**Severity:** CRITICAL (if multiple coils)
**Cause:** One or more electromagnetic acceleration coils not functioning
**Symptoms:**
- Thrust significantly reduced
- Uneven exhaust pattern
- Vibration from engine

**Resolution:**
1. Run coil diagnostic test (identifies which coils failed)
2. Single coil failure: Can operate at reduced thrust (~85% capacity)
3. Multiple coil failures: Engine should be shut down
4. Check coil power supply
5. Replace failed coils (Part #: ACC-COIL-M3 series)

**Related:** NAV-SUB-002 (Maintenance)

---

### E-NAV-125: Thrust Vectoring Malfunction
**Severity:** WARNING
**Cause:** Thrust nozzle unable to gimbal properly for directional control
**Symptoms:**
- Poor maneuverability
- Nozzle stuck in fixed position
- Grinding or scraping sounds when vectoring attempted

**Resolution:**
1. Check hydraulic pressure for nozzle actuators (180-220 PSI)
2. Inspect nozzle gimbal mechanism for mechanical binding
3. Test actuator motor operation
4. Lubricate gimbal joints if dry
5. Can operate in fixed-nozzle mode (reduced maneuverability)

**Related:** NAV-SUB-002 (Maintenance)

---

### E-NAV-130: Inertial Dampener Fault
**Severity:** CRITICAL
**Cause:** Inertial dampening system not compensating for acceleration
**Symptoms:**
- Crew feeling full acceleration forces (uncomfortable or dangerous)
- Dampener status showing red
- Cannot perform high-G maneuvers safely

**Resolution:**
1. **IMMEDIATE**: Limit acceleration to ≤1 G until repaired
2. Check dampener field generator power supply
3. Test dampener field uniformity
4. Verify dampener calibrated for ship mass
5. Replace dampener field coils if failed
6. **DO NOT** perform high-G maneuvers with failed dampeners (crew injury risk)

**Related:** NAV-SUB-001 (Sublight Systems), EMERG-010 (Engine Emergencies)

---

### E-NAV-135: Fuel Flow Irregular
**Severity:** WARNING
**Cause:** Deuterium fuel delivery inconsistent
**Symptoms:**
- Thrust output fluctuating
- Engine vibration
- Plasma chamber temperature varying

**Resolution:**
1. Check fuel pressure (should be stable at 120-150 PSI)
2. Inspect fuel pump operation
3. Check for air in fuel lines (purge if present)
4. Replace fuel filters if clogged
5. Verify fuel valve fully open and not sticking

**Related:** NAV-SUB-003 (Troubleshooting)

---

### E-NAV-140: Maneuvering Thruster Failure
**Severity:** WARNING
**Cause:** One or more RCS thrusters not responding
**Symptoms:**
- Poor attitude control
- Drift during docking approach
- Specific axis of rotation affected

**Resolution:**
1. Identify which thrusters failed (RCS diagnostic panel)
2. Check nitrogen pressure (should be 2,500-3,000 PSI)
3. Test thruster valve operation
4. Inspect thruster nozzles for blockage
5. Can compensate with remaining thrusters (reduced precision)

**Related:** NAV-SUB-001 (Sublight Systems)

---

## FTL Drive Errors (E-NAV-500 series)

### E-NAV-501: Insufficient Power for FTL Charge
**Severity:** WARNING
**Cause:** Q-Core reactor not providing minimum 80% capacity for FTL jump
**Symptoms:**
- Charge sequence won't initiate
- Message "REACTOR OUTPUT INSUFFICIENT"
- Power meter showing red

**Resolution:**
1. Check Q-Core reactor status and output level
2. Increase reactor throttle to at least 80% capacity
3. Shut down non-essential systems to free power
4. Verify FTL power requirements for drive model:
   - Horizon-1: 20-25 MW
   - Horizon-2: 70-80 MW
   - Horizon-3: 160-180 MW
5. Address any reactor issues preventing adequate output

**Related:** KB-012 (FTL Jump Fails), PWR-SYS-001 (Reactor Overview)

---

### E-NAV-502: Mass Shadow Detected
**Severity:** CRITICAL
**Cause:** Attempting FTL activation within gravity well of stellar object
**Symptoms:**
- Jump execution blocked by safety system
- Red zones on navigation display
- Message "UNSAFE PROXIMITY TO MASS"

**Resolution:**
1. **CANNOT OVERRIDE**: This is safety-critical lockout
2. Identify source of interference:
   - Star: Minimum 2 AU distance required
   - Planet: Minimum 100,000 km required
   - Station/asteroid: Minimum 1,000 km required
3. Use sublight engines to move to clear zone
4. Navigation computer "Clear Zone Calculator" shows nearest safe point
5. Wait until navigation shows "CLEAR FOR JUMP" status

**Related:** KB-012 (FTL Jump Fails), NAV-FTL-002 (Jump Procedures)

---

### E-NAV-503: FTL Cooldown Timer Active
**Severity:** INFO
**Cause:** Attempting jump before minimum cooldown interval expired
**Symptoms:**
- Countdown timer displayed on FTL panel
- Charge sequence won't initiate
- Time remaining shown (hours:minutes:seconds)

**Resolution:**
1. **CANNOT OVERRIDE**: Mandatory cooldown prevents QFM thermal damage
2. Wait for timer to reach 00:00:00
3. Cooldown periods:
   - Horizon-1: 8 hours
   - Horizon-2: 6 hours
   - Horizon-3: 4 hours
4. Use waiting time for ship maintenance, crew rest, route planning
5. Monitor QFM temperature (should decline to <600°C during cooldown)

**Related:** KB-012 (FTL Jump Fails), NAV-FTL-001 (FTL Overview)

---

### E-NAV-504: Navigation Lock Failed
**Severity:** WARNING
**Cause:** Computer unable to calculate stable tunnel vector to destination
**Symptoms:**
- Navigation lock indicator showing red
- Charge holds at 90-95%
- Message "UNABLE TO CALCULATE TUNNEL VECTOR"

**Resolution:**
1. Verify destination coordinates correct (check for typos)
2. Confirm destination within FTL drive range:
   - Horizon-1: 20 light-years max
   - Horizon-2: 50 light-years max
   - Horizon-3: 100 light-years max
3. Check for spatial interference:
   - Quantum turbulence near black holes
   - Dense nebulae
   - Gravitational anomalies
4. Update star charts (outdated data causes calculation errors)
5. Try alternate destination to test navigation computer

**Related:** KB-012 (FTL Jump Fails), NAV-FTL-004 (FTL Troubleshooting)

---

### E-NAV-505: Tachyon Emitter Failure
**Severity:** CRITICAL
**Cause:** One or more of 16 tachyon emitters not operational
**Symptoms:**
- Emitter status panel showing red for failed unit(s)
- Charge sequence aborted
- Message "EMITTER ARRAY INCOMPLETE"

**Resolution:**
1. **ALL 16 EMITTERS REQUIRED**: Cannot jump with failed emitter
2. Identify failed emitter number (1-16) and location
3. Attempt emitter reset:
   - Select emitter on control panel
   - Press "RESET" button
   - Wait 30 seconds for reinitialization
4. If reset fails:
   - Check emitter power supply (420 VDC required)
   - Inspect physical emitter (if accessible)
   - Replace failed emitter (Part #: TAC-EM-H series)
5. Must use sublight propulsion until repaired

**Related:** KB-012 (FTL Jump Fails), NAV-FTL-003 (FTL Maintenance)

---

### E-NAV-510: QFM Overheating
**Severity:** CRITICAL
**Cause:** Quantum Field Manipulator core temperature exceeding safe limits
**Symptoms:**
- QFM temperature >1,600°C during charge
- Charge sequence automatically aborted
- Thermal alarms from FTL drive bay

**Resolution:**
1. **IMMEDIATE**: Abort charge sequence if not auto-aborted
2. Allow QFM to cool completely before retry
3. Check QFM cooling system operation
4. Verify cooldown period fully elapsed before last jump
5. Inspect QFM heat exchanger for blockages
6. If recurring: QFM may be degraded, requires service

**Related:** NAV-FTL-004 (FTL Troubleshooting)

---

### E-NAV-515: Tunnel Stability Below Minimum
**Severity:** CRITICAL
**Cause:** During FTL transit, quantum tunnel stability dropped below 85%
**Symptoms:**
- Stability indicator showing <90%
- Yellow or red stability warning
- Vibrations or visual distortions increasing

**Resolution:**
**If Before Jump:**
1. Abort charge sequence
2. Run FTL diagnostic
3. Check tachyon field uniformity
4. Verify QFM operating temperature correct
5. Recalibrate tachyon emitters

**If During Transit:**
1. Increase tachyon field intensity by 25-50 TU
2. Verify Q-Core maintaining steady power
3. Monitor stability trend
4. If stability continues dropping or reaches <85%:
   - Initiate emergency drop-out (press FTL ABORT)
5. See EMERG-006 for mid-transit emergency procedures

**Related:** NAV-FTL-002 (Jump Procedures), EMERG-006 (FTL Emergencies)

---

### E-NAV-520: Graviton Compensator Overload
**Severity:** CRITICAL
**Cause:** Compensators unable to handle gravitational shear
**Symptoms:**
- Compensator load >90%
- May indicate unexpected gravitational interference
- Structural stress on vessel

**Resolution:**
**During Charge:**
1. Abort charge sequence
2. Re-scan for mass shadows
3. May be uncharted gravitational source nearby
4. Recalculate jump from different location

**During Transit:**
1. Monitor compensator load closely
2. If reaches 95%: Strongly consider emergency abort
3. May be passing near undetected massive object
4. Load should decrease as distance from source increases
5. If sustained overload: Execute emergency drop-out

**Related:** EMERG-006 (FTL Emergencies)

---

### E-NAV-525: Tachyon Field Asymmetry
**Severity:** WARNING
**Cause:** Tachyon field not uniform around vessel
**Symptoms:**
- Field symmetry <95%
- Charge time extended
- May cause increased spatial drift during jump

**Resolution:**
1. Check all 16 emitter outputs (should be balanced)
2. Identify weak or strong emitters
3. Run emitter calibration sequence
4. Replace degraded emitters
5. Can complete jump with symmetry >92% (expect higher drift)

**Related:** NAV-FTL-003 (FTL Maintenance)

---

### E-NAV-530: FTL Drive Integrity Fault
**Severity:** CRITICAL
**Cause:** Structural or component damage to FTL drive detected
**Symptoms:**
- Self-diagnostic reports component failures
- May be result of previous emergency abort
- Multiple system warnings

**Resolution:**
1. **DO NOT ATTEMPT FTL JUMP**
2. Run complete FTL diagnostic
3. Identify failed or damaged components
4. Contact ORSM FTL specialist for guidance
5. May require yard service for repair
6. Use sublight propulsion to reach repair facility

**Related:** Contact ORSM Emergency Support

---

### E-NAV-535: Navigation Database Corrupted
**Severity:** WARNING
**Cause:** Star chart data corrupted or missing
**Symptoms:**
- Navigation computer unable to identify stellar objects
- Destination coordinates produce errors
- Position uncertainty after FTL exit

**Resolution:**
1. Backup current navigation database (if possible)
2. Download fresh star charts from ORSM navigation network
3. Restore navigation database to factory defaults
4. Update with latest chart data
5. Recalibrate navigation sensors
6. Verify position using visual star identification

**Related:** NAV-FTL-002 (Jump Procedures)

---

### E-NAV-540: Excessive Spatial Drift
**Severity:** ADVISORY
**Cause:** Exit point differs from predicted by >0.05% of jump distance
**Symptoms:**
- Emerged at unexpected location
- Navigation error higher than normal
- Post-jump position check shows significant deviation

**Resolution:**
1. Normal drift: ±0.01% of jump distance
2. Drift 0.01-0.05%: Indicates navigation calibration needed
3. Drift >0.05%: Significant issue, investigate immediately
4. Possible causes:
   - QFM degradation
   - Navigation computer miscalculation
   - Gravitational interference during transit
   - Tachyon emitter imbalance
5. Run complete FTL diagnostic
6. Recalibrate navigation before next jump

**Related:** NAV-FTL-003 (FTL Maintenance)

---

## Combined Navigation Errors (E-NAV-600 series)

### E-NAV-601: Navigation Computer Offline
**Severity:** CRITICAL
**Cause:** Primary navigation computer failure
**Symptoms:**
- Navigation displays dark or unresponsive
- Unable to calculate courses
- FTL jumps impossible
- Sublight autopilot unavailable

**Resolution:**
1. Check navigation computer power supply
2. Attempt computer reboot (breaker cycle)
3. Switch to backup navigation computer (if equipped)
4. Run computer diagnostic
5. Replace navigation computer if hardware failure
6. Manual piloting possible for sublight (FTL requires nav computer)

**Related:** Contact ORSM Technical Support

---

### E-NAV-605: Sensor Array Malfunction
**Severity:** WARNING
**Cause:** External sensors providing invalid or no data
**Symptoms:**
- No object detection
- Mass shadow warnings absent (dangerous!)
- Unable to verify position
- Collision avoidance offline

**Resolution:**
1. **CAUTION**: Operate at reduced speed without sensors
2. Check sensor array power supply
3. Inspect sensor housings for damage or debris
4. Test individual sensors
5. Recalibrate sensor array
6. Clean sensor lenses/apertures
7. Replace failed sensor modules

**Related:** Navigation safety protocols

---

### E-NAV-610: Autopilot Disengaged Unexpectedly
**Severity:** WARNING
**Cause:** Autopilot encountered situation it cannot handle
**Symptoms:**
- Autopilot turns off mid-flight
- Manual control required immediately
- May indicate obstacle, sensor issue, or system malfunction

**Resolution:**
1. Take manual control immediately
2. Check for obstacles or hazards
3. Verify sensor array functioning
4. Review autopilot disengagement log
5. Common causes:
   - Unexpected object in path
   - Sensor failure
   - Destination parameters invalid
   - Course calculation error
6. Resolve underlying issue before re-engaging autopilot

**Related:** Navigation operations manual

---

## Error Code Quick Reference

**By Severity - Critical:**
- E-NAV-110 (Engine Overheating)
- E-NAV-115 (Coolant Failure)
- E-NAV-130 (Inertial Dampener)
- E-NAV-502 (Mass Shadow)
- E-NAV-505 (Tachyon Emitter)
- E-NAV-510 (QFM Overheating)
- E-NAV-515 (Tunnel Instability)
- E-NAV-520 (Graviton Overload)
- E-NAV-530 (FTL Integrity Fault)
- E-NAV-601 (Nav Computer Offline)

**By System:**
- **Sublight Engines:** 101-140
- **FTL Drive:** 501-540
- **Navigation Computer:** 601-610

**Most Common Errors:**
1. E-NAV-503 (Cooldown Timer) - 35% of FTL error calls
2. E-NAV-502 (Mass Shadow) - 25% of FTL error calls
3. E-NAV-102 (Low Thrust) - 20% of sublight error calls
4. E-NAV-504 (Nav Lock Failed) - 15% of FTL error calls

## Related Documents

- NAV-SUB-001: Sublight Engine Overview
- NAV-SUB-003: Sublight Engine Troubleshooting
- NAV-FTL-001: FTL Drive Overview
- NAV-FTL-002: FTL Jump Procedures
- NAV-FTL-004: FTL Troubleshooting
- EMERG-006: FTL Emergency Procedures
- EMERG-010: Engine Emergency Procedures

---

**Document maintained by ORSM Technical Publications. For assistance, contact Outer Rim Support Line 24/7.**
