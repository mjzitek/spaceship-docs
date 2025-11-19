# Docking System Error Codes (E-DOCK Series)

**Document ID:** ERR-DOCK-400
**Revision:** 3.5
**Last Updated:** 2847.11.01
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides a complete reference of error codes for docking systems, airlock interfaces, and port connection mechanisms. Error codes are displayed on docking control panels and logged in navigation diagnostics.

## Error Code Format

**E-DOCK-XXX** or **E-NAV-4XX** (legacy)
- **E**: Error code indicator
- **DOCK** or **NAV-4XX**: Docking system
- **XXX**: Specific error number

**Note:** Some older ships use E-NAV-4XX format for docking errors. Both formats documented here.

## Severity Levels

- **CRITICAL** (Red): Cannot dock, safety hazard, possible collision risk
- **WARNING** (Orange): Docking difficult or unreliable, investigate before attempting
- **ADVISORY** (Yellow): Reduced functionality, manual workaround available
- **INFO** (Blue): Informational only, no action required

---

## Alignment and Positioning Errors (E-DOCK-100 / E-NAV-400 series)

### E-DOCK-101 / E-NAV-401: Alignment Out of Tolerance
**Severity:** WARNING
**Cause:** Ship position or rotation not aligned with docking port axis
**Symptoms:**
- Auto-dock refuses to engage
- Alignment indicators showing red
- Ship unable to connect despite proximity

**Resolution:**
1. Check alignment displays (X, Y, Z position and roll angle)
2. Use maneuvering thrusters to correct position
3. Acceptable alignment:
   - Position: Within ±0.5 meters on X and Y axis
   - Rotation: Within ±5 degrees
   - Angle: Ship axis within ±2 degrees of port axis
4. Re-attempt docking after alignment correction
5. If auto-align available, engage to automatically correct

**Related:** KB-301 (Docking Alignment Issues), DOCK-SYS-001 (Docking Procedures)

---

### E-DOCK-102 / E-NAV-402: Approach Velocity Too High
**Severity:** WARNING
**Cause:** Ship approaching docking port too fast
**Symptoms:**
- Auto-dock aborts approach
- "REDUCE VELOCITY" warning
- Ship may bounce off port if contact attempted

**Resolution:**
1. Reduce approach velocity:
   - >10m: <0.5 m/s
   - >5m: <0.3 m/s
   - >2m: <0.1 m/s
   - Final 1m: Drift (no thrust)
2. Use retro thrusters to slow approach
3. Be patient - slower is safer
4. Re-engage auto-dock after velocity reduced

**Related:** KB-301 (Docking Issues), NAV-OPS-005 (Docking Procedures)

---

### E-DOCK-103: Relative Rotation Detected
**Severity:** WARNING
**Cause:** Ship rotating relative to docking port during approach
**Symptoms:**
- Auto-dock aborts
- "ROTATION DETECTED" warning
- Ship and port rotation rates don't match

**Resolution:**
1. If docking with rotating station:
   - Must match station rotation rate
   - Use rotational thrusters to sync rotation
   - Maintain rotation match during approach
2. If ship rotating when port is stationary:
   - Use RCS thrusters to stop rotation
   - Stabilize ship completely before approach
3. Disable auto-stabilization (may cause unwanted rotation corrections)

**Related:** NAV-OPS-005 (Docking with Rotating Stations)

---

### E-DOCK-105: Obstacle Detected in Approach Path
**Severity:** CRITICAL
**Cause:** Proximity sensors detect object between ship and port
**Symptoms:**
- Auto-dock aborts immediately
- "OBSTACLE DETECTED" alert
- Collision avoidance system engaged

**Resolution:**
1. Stop approach immediately
2. Identify obstacle:
   - Debris floating in path
   - Another ship in vicinity
   - Station structure or equipment
   - Sensor false positive (ice, reflections)
3. Clear obstacle if possible (maneuvering)
4. Verify sensors functioning correctly
5. Retry approach with clear path

**Related:** SENS-SYS-002 (Proximity Sensors)

---

## Docking Beacon and Communication Errors (E-DOCK-200 series)

### E-DOCK-201: Docking Beacon Not Detected
**Severity:** WARNING
**Cause:** Cannot receive docking beacon signal from port
**Symptoms:**
- Auto-dock unavailable ("NO BEACON" message)
- Docking guidance data not received
- Must use manual docking

**Resolution:**
1. Verify docking clearance granted by station
2. Confirm approaching correct/assigned port
3. Check communications system operational
4. Distance may be too far (beacon range typically 100m)
5. Station beacon may be offline (contact station)
6. Use manual docking as alternative

**Related:** KB-301 (Docking Issues), COMM-SYS-001 (Communications)

---

### E-DOCK-205: Beacon Signal Conflict
**Severity:** WARNING
**Cause:** Receiving multiple docking beacon signals (ambiguous)
**Symptoms:**
- Auto-dock confused or selecting wrong port
- Multiple beacons detected
- Docking guidance data inconsistent

**Resolution:**
1. Verify which port assigned to your ship
2. Move closer to assigned port (stronger signal)
3. Manually select correct beacon in docking menu
4. Contact station for clarification
5. Station may need to disable unused beacons

**Related:** DOCK-SYS-001 (Beacon Systems)

---

## Mechanical System Errors (E-DOCK-300 series)

### E-DOCK-301: Docking Clamp Failure
**Severity:** CRITICAL
**Cause:** Docking clamps unable to engage or hold ship
**Symptoms:**
- Ship makes contact but doesn't lock
- Clamps extending but not gripping
- "CLAMP FAILURE" warning
- Ship bouncing off or drifting away from port

**Resolution:**
1. Attempt manual clamp engagement:
   - Navigate to: Docking > Manual Controls
   - Activate "ENGAGE CLAMPS" manually
2. Check docking system power (circuit breakers)
3. Cycle docking system (power off/on)
4. Inspect clamps visually (external cameras):
   - Mechanical damage?
   - Ice or debris blocking clamps?
   - Clamps stuck in retracted position?
5. May require EVA to clear obstruction or repair
6. If clamps failed, cannot dock safely - request tugboat assistance

**Related:** DOCK-SYS-003 (Mechanism Maintenance), KB-301 (Docking Issues)

---

### E-DOCK-305: Airlock Seal Failure
**Severity:** CRITICAL
**Cause:** Docking tunnel seal not making contact or leaking
**Symptoms:**
- Ship docked (clamps holding) but tunnel won't pressurize
- "SEAL FAILURE" or "LEAK DETECTED" warning
- Pressure in docking tunnel dropping
- Cannot open hatches

**Resolution:**
1. Verify both hatches closed before pressurizing tunnel
2. Check seal alignment (may need to disconnect and re-dock)
3. Increase seal pressure if manual control available
4. Inspect seal ring condition (external camera):
   - Seal damaged or torn?
   - Debris preventing contact?
   - Seal retracted when should be extended?
5. If seal cannot be achieved:
   - Cannot transfer crew through tunnel
   - Alternative: EVA transfer if necessary
   - Alternative: Station may have flexible coupling
6. Seal may need replacement at port maintenance

**Related:** DOCK-SYS-002 (Airlock Systems), KB-301 (Docking Issues)

---

### E-DOCK-310: Docking Port Incompatibility
**Severity:** WARNING
**Cause:** Ship docking interface doesn't match port standard
**Symptoms:**
- Mechanical fit issues
- "INCOMPATIBLE PORT" warning
- Clamps or seal not matching port configuration

**Resolution:**
1. Verify docking standards:
   - Ship: Check docking system type (UDC, CommDock-3, MilSpec-D, HeavyDock)
   - Port: Confirm port standard (contact station)
2. If incompatible:
   - Request different port (station may have multiple types)
   - Use adapter collar if available
   - Request tugboat to specialized port
3. Document incompatibility for future reference

**Related:** DOCK-SYS-001 (Docking Standards)

---

### E-DOCK-315: Magnetic Capture Failure
**Severity:** WARNING
**Cause:** Magnetic capture system not engaging (if equipped)
**Symptoms:**
- Ship not being pulled into final docking position
- "MAG CAPTURE OFFLINE" warning
- Must rely on manual final approach

**Resolution:**
1. Check magnetic capture system power
2. Verify magnets activated (should auto-activate <3 meters)
3. Manual activation: Docking > Mag Capture > Engage
4. Magnetic capture is convenience feature, not required:
   - Can still dock manually without mag capture
   - Just requires more precise final approach
5. May need recalibration or repair

**Related:** DOCK-SYS-003 (Mechanism Diagnostics)

---

## Sensor and Control Errors (E-DOCK-400 series)

### E-DOCK-401: Proximity Sensor Failure
**Severity:** WARNING
**Cause:** Sensors that measure distance to port failed or inaccurate
**Symptoms:**
- Auto-dock unavailable
- Distance readings incorrect or missing
- "SENSOR FAULT" warning

**Resolution:**
1. Run sensor diagnostic test
2. Recalibrate proximity sensors
3. Check for sensor physical damage (ice, debris, impact)
4. Can still dock manually using visual reference
5. Repair or replace failed sensors when possible

**Related:** SENS-SYS-002 (Proximity Sensors), KB-531 (Sensor Malfunction)

---

### E-DOCK-405: Auto-Dock System Failure
**Severity:** ADVISORY
**Cause:** Automatic docking computer or software malfunction
**Symptoms:**
- Auto-dock feature unavailable
- "AUTO-DOCK OFFLINE" message
- Must use manual docking

**Resolution:**
1. Restart auto-dock computer:
   - Navigate to: Docking > Auto-Dock > System Reset
   - Wait 30 seconds, retry
2. Check auto-dock system power
3. Update auto-dock software if outdated
4. Use manual docking as workaround:
   - Manual docking is reliable alternative
   - Many pilots prefer manual control
5. Repair auto-dock at next port if desired

**Related:** KB-301 (Docking Issues - Auto-Dock), DOCK-SYS-001 (Manual Docking)

---

### E-DOCK-410: Gyroscope Calibration Error
**Severity:** WARNING
**Cause:** Gyroscope or orientation sensors need recalibration
**Symptoms:**
- Alignment indicators inaccurate
- Auto-dock makes incorrect adjustments
- Ship "thinks" it's aligned when it's not

**Resolution:**
1. Recalibrate gyroscope:
   - Navigate to: Navigation > Sensors > Gyro Calibration
   - Follow calibration procedure (ship must be stationary)
2. Recalibrate while not docking, then retry
3. If calibration fails, gyroscope may be damaged
4. Use visual docking references instead of relying on sensors

**Related:** NAV-SYS-002 (Sensor Calibration)

---

## Power and Electrical Errors (E-DOCK-500 series)

### E-DOCK-501: Docking System Power Failure
**Severity:** CRITICAL
**Cause:** No power to docking system
**Symptoms:**
- All docking functions offline
- Control panel dark
- Clamps, seals, sensors not operational

**Resolution:**
1. Check docking system circuit breaker (may be tripped)
2. Reset breaker and retry
3. Check main power supply to ship
4. Verify power connections to docking system
5. Cannot safely dock without power:
   - Request tugboat assistance
   - Or restore power before docking

**Related:** ERR-PWR-100 (Power System Errors)

---

### E-DOCK-505: Insufficient Power for Docking Operations
**Severity:** WARNING
**Cause:** Power available but insufficient for all docking systems
**Symptoms:**
- Some docking functions unavailable
- "LOW POWER" warning during docking operations
- Intermittent system operation

**Resolution:**
1. Reduce power consumption elsewhere on ship
2. Shut down non-essential systems during docking
3. Ensure reactor/power system providing adequate output
4. Docking typically requires 5-15 kW (varies by ship size)
5. If on battery power, ensure sufficient charge

**Related:** PWR-SYS-001 (Power Management)

---

## Safety and Abort Conditions (E-DOCK-600 series)

### E-DOCK-601: Collision Risk - Docking Aborted
**Severity:** CRITICAL
**Cause:** Auto-dock detected collision risk and aborted
**Symptoms:**
- Sudden abort during approach
- "COLLISION RISK" alert
- Ship emergency stop engaged

**Resolution:**
1. Do not override - safety system protecting ship
2. Back away to safe distance (10+ meters)
3. Identify collision risk:
   - Approach too fast?
   - Alignment off?
   - Obstacle detected?
   - Rotation mismatch?
4. Correct issue and retry carefully
5. If repeated aborts, switch to manual docking (extra care)

**Related:** DOCK-SYS-001 (Safety Systems)

---

### E-DOCK-605: Emergency Disconnect Activated
**Severity:** WARNING
**Cause:** Emergency undocking procedure engaged (intentional or accidental)
**Symptoms:**
- Docking clamps released
- Ship separating from port
- "EMERGENCY DISCONNECT" message

**Resolution:**
1. If intentional: Normal response to emergency disconnect command
2. If accidental:
   - May be button pressed accidentally
   - May be electrical fault triggering disconnect
   - Re-dock if needed
3. Emergency disconnect used when:
   - Station emergency requiring immediate departure
   - Ship emergency requiring separation
   - Docking system malfunction with ship stuck
4. Inspect docking system after emergency disconnect (stressful event)

**Related:** EMERG-025 (Emergency Procedures), DOCK-SYS-001 (Emergency Disconnect)

---

## Informational Messages (E-DOCK-900 series)

### E-DOCK-900: Docking System Self-Test in Progress
**Severity:** INFO
**Cause:** System running diagnostic self-test (not an error)
**Symptoms:**
- Docking temporarily unavailable
- "SELF-TEST" indicator active

**Resolution:**
- Normal operational message
- Wait for self-test to complete (typically 1-2 minutes)
- Docking will be available after test completes

---

### E-DOCK-901: Docking Clearance Awaiting
**Severity:** INFO
**Cause:** Waiting for station to grant docking clearance (not an error)
**Symptoms:**
- Auto-dock won't engage
- "AWAITING CLEARANCE" message

**Resolution:**
- Normal - must receive clearance before docking
- Contact station if clearance delayed
- Do not attempt to dock without clearance

**Related:** COMM-SYS-002 (Station Communications)

---

### E-DOCK-999: Docking System Maintenance Required
**Severity:** ADVISORY
**Cause:** Scheduled maintenance interval reached
**Symptoms:**
- Persistent advisory message
- System operating normally but maintenance recommended

**Resolution:**
- Schedule docking system maintenance at next port
- Includes: Seal inspection, clamp lubrication, sensor calibration
- Recommended interval: Every 6 months or 100 docking cycles
- Safe to continue operation but don't defer maintenance indefinitely

**Related:** DOCK-SYS-003 (Maintenance Procedures)

---

## Error Code Quick Reference

**Cannot Dock (CRITICAL):**
- E-DOCK-301: Docking clamp failure
- E-DOCK-305: Airlock seal failure
- E-DOCK-501: Power failure
- E-DOCK-601: Collision risk

**Difficult Docking (WARNING):**
- E-DOCK-101: Alignment out of tolerance
- E-DOCK-102: Velocity too high
- E-DOCK-201: No docking beacon
- E-DOCK-310: Port incompatibility
- E-DOCK-401: Proximity sensor failure

**Reduced Functionality (ADVISORY):**
- E-DOCK-405: Auto-dock offline (use manual)
- E-DOCK-999: Maintenance due

---

## Related Documents

- DOCK-SYS-001: Docking Systems Overview and Procedures
- DOCK-SYS-002: Airlock and Seal Systems
- DOCK-SYS-003: Docking Mechanism Maintenance
- KB-301: Docking Alignment and Connection Issues
- NAV-OPS-005: Docking Procedures and Best Practices

---

**Support Note**: Most docking errors result from pilot technique rather than equipment failure. "Slow and aligned" solves 90% of docking problems. If customer having persistent docking issues, walk through manual procedure step-by-step - often reveals they're approaching too fast or not checking alignment. Auto-dock is convenient but temperamental - manual docking is more reliable backup skill.
