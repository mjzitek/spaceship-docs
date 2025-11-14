# Sensor Array System Error Codes

**Document ID:** ERR-SENS-001
**Revision:** 1.9
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Error Code Format

Sensor error codes follow the format: **E-SENS-XXX**

- **E**: Error prefix
- **SENS**: Sensor system
- **XXX**: Specific error number (100-999)

## Error Severity Levels

- **INFO** (100-199): Informational, no action required
- **WARNING** (200-399): Non-critical issue, monitor and address when convenient
- **ERROR** (400-599): Significant problem, affects functionality, repair soon
- **CRITICAL** (600-799): Major failure, system compromised, immediate attention required
- **EMERGENCY** (800-999): Life-threatening or mission-critical failure, emergency response required

---

## Informational (100-199)

### E-SENS-100: Scan Cycle Complete
**Severity**: INFO
**Description**: Full 360° sensor sweep completed
**Impact**: None, normal operation
**Action**: None required

### E-SENS-101: New Contact Detected
**Severity**: INFO
**Description**: Sensor array detected new object
**Impact**: Contact added to tracking database
**Action**: Review contact for identification and classification

### E-SENS-102: Contact Lost
**Severity**: INFO
**Description**: Previously tracked object no longer detected
**Cause**: Object moved out of range, passed behind obstacle, sensors degraded
**Impact**: None if expected
**Action**: Verify object left sensor range normally

### E-SENS-103: Sensor Calibration Optimal
**Severity**: INFO
**Description**: Sensor calibration within optimal parameters
**Impact**: None
**Action**: Informational only

---

## Warnings (200-399)

### E-SENS-200: Radar Gain Reduced
**Severity**: WARNING
**Description**: Radar sensitivity lower than optimal
**Cause**: Component degradation, power reduction, interference
**Impact**: Reduced detection range (typically 10-30%)
**Action**:
1. Check power supply to radar array
2. Verify radar amplifier functioning
3. Run radar diagnostic
4. Increase gain if within safe limits
5. Schedule maintenance if persists

### E-SENS-201: Optical System Alignment Drift
**Severity**: WARNING
**Description**: Telescope array alignment off by >0.1°
**Cause**: Vibration, thermal expansion, mechanical wear
**Impact**: Reduced imaging accuracy, targeting errors
**Action**:
1. Run optical alignment calibration
2. Check mounting hardware secure
3. Verify no physical damage to telescope mount
4. Re-align optical array

### E-SENS-202: Graviton Detector Sensitivity Low
**Severity**: WARNING
**Description**: Graviton sensor not operating at full sensitivity
**Cause**: Sensor drift, calibration error, interference from nearby mass
**Impact**: Reduced mass detection range, may miss distant objects
**Action**:
1. Move away from large masses (planets, stations) if possible
2. Recalibrate graviton detector
3. Check for power fluctuations
4. Verify sensor cooling system operational

### E-SENS-210: Excessive False Contacts
**Severity**: WARNING
**Description**: Sensor reporting many contacts that don't exist
**Cause**: Sensitivity too high, interference, sensor malfunction
**Impact**: Cluttered display, difficult to identify real contacts
**Action**:
1. Reduce sensor sensitivity/gain
2. Apply contact filtering (size, speed thresholds)
3. Check for interference sources (nearby equipment)
4. Update sensor filtering algorithms
5. Recalibrate sensors

### E-SENS-215: Lidar Range Reduced
**Severity**: WARNING
**Description**: Lidar effective range lower than rated
**Cause**: Laser power low, receiver sensitivity degraded, dust/debris
**Impact**: Cannot measure precise distances at full range
**Action**:
1. Clean lidar optical windows
2. Check laser power output
3. Verify receiver alignment
4. Increase power if within safe limits

### E-SENS-220: Thermal Imaging Noise High
**Severity**: WARNING
**Description**: Thermal sensors showing excessive noise/static
**Cause**: Sensor temperature too high, interference, sensor degradation
**Impact**: Difficult to detect heat signatures clearly
**Action**:
1. Cool thermal sensor (may need better cooling system)
2. Recalibrate thermal baseline
3. Filter out noise in software
4. Check for interference sources

### E-SENS-225: Radiation Background Elevated
**Severity**: WARNING
**Description**: Background radiation higher than normal
**Cause**: Stellar environment (near star, nebula), radiation leak on vessel
**Impact**: Radiation sensors less sensitive to specific sources
**Action**:
1. Normal if near radiation sources (stars, etc.)
2. If in open space, check for radiation leak on vessel
3. Increase sensor threshold to filter background
4. Wear radiation badges if elevated on vessel

### E-SENS-230: Tracking Capacity at 80%
**Severity**: WARNING
**Description**: Sensor computer tracking near maximum object count
**Cause**: High traffic area, debris field, combat zone
**Impact**: May lose ability to track additional objects
**Action**:
1. Filter low-priority tracks (small, distant, low threat)
2. Increase update rate to clear stale tracks
3. Upgrade sensor computer if frequently occurs
4. Focus tracking on priority contacts only

---

## Errors (400-599)

### E-SENS-400: Radar Array Offline
**Severity**: ERROR
**Description**: Primary radar system not functioning
**Cause**: Hardware failure, power loss, antenna damage
**Impact**: No active radar detection (passive sensors only)
**Action**:
1. Check power to radar array
2. Verify antenna elements intact
3. Check for blown fuses or circuit breakers
4. Restart radar system
5. Switch to backup radar if equipped
6. Requires repair for full functionality

### E-SENS-401: Radar Transmitter Failure
**Severity**: ERROR
**Description**: Radar not transmitting pulses
**Cause**: Transmitter hardware failure, power supply fault
**Impact**: Radar cannot actively scan (passive reception only)
**Action**:
1. Check transmitter power supply
2. Verify antenna connection
3. Test transmitter output with diagnostic tool
4. Replace transmitter module if failed

### E-SENS-410: Optical Telescope System Fault
**Severity**: ERROR
**Description**: Telescope array not producing images
**Cause**: Lens/mirror damage, motor failure, sensor array failure
**Impact**: No visual imaging capability
**Action**:
1. Visual inspection of optical components (may require EVA)
2. Check motorized positioning system
3. Verify camera/sensor array functioning
4. Clean optics (dust, ice, debris)
5. Replace damaged components

### E-SENS-411: Optical Focus Motor Jammed
**Severity**: ERROR
**Description**: Telescope focus mechanism not responding
**Cause**: Mechanical jam, motor failure, ice buildup
**Impact**: Cannot focus telescope, blurry images
**Action**:
1. Attempt manual focus (if accessible)
2. Check for debris or ice on mechanism
3. Test motor power and control signals
4. Warm mechanism if ice present
5. May require disassembly and repair

### E-SENS-420: Graviton Detector Offline
**Severity**: ERROR
**Description**: Gravitational sensor not operational
**Cause**: Hardware failure, cooling system failure, power fault
**Impact**: Cannot detect mass shadows, no gravity-based sensing
**Action**:
1. Check power to graviton detector
2. Verify cooling system operational (runs very cold)
3. Restart graviton detector system
4. Check for error codes on detector unit
5. Requires specialist repair if hardware fault

**WARNING**: Without graviton detector, cannot reliably detect mass shadows for FTL jumps!

### E-SENS-430: Radiation Sensors Malfunctioning
**Severity**: ERROR
**Description**: Radiation detection system not working correctly
**Cause**: Sensor contamination, calibration error, hardware failure
**Impact**: Cannot detect radiation hazards or reactor signatures
**Action**:
1. Check for sensor contamination (radioactive exposure)
2. Recalibrate radiation sensors
3. Test with known radiation source
4. Replace contaminated sensors
5. Critical for hazmat detection and reactor monitoring

### E-SENS-440: Lidar System Inoperative
**Severity**: ERROR
**Description**: Lidar ranging system not functioning
**Cause**: Laser failure, receiver damage, alignment lost
**Impact**: No precision distance measurement, docking difficult
**Action**:
1. Check laser power and status
2. Verify receiver alignment
3. Test laser with diagnostic tool
4. Use alternate ranging methods (radar, visual estimation)
5. Repair before attempting precision docking

### E-SENS-450: Mass Spectrometer Fault
**Severity**: ERROR
**Description**: Atmospheric analysis system not working
**Cause**: Sample collector clogged, analyzer failure, contamination
**Impact**: Cannot analyze atmospheric composition or chemical samples
**Action**:
1. Check sample collector (may be clogged with debris)
2. Run diagnostic on analyzer unit
3. Clean or replace sample filters
4. Recalibrate spectrometer
5. Purge contaminated samples

### E-SENS-460: Sensor Computer Processing Overload
**Severity**: ERROR
**Description**: Sensor computer cannot process data quickly enough
**Cause**: Too many contacts, complex environment, computer degradation
**Impact**: Delayed sensor updates, slow tracking, system lag
**Action**:
1. Reduce tracked contact count (filter low priority)
2. Decrease scan rate temporarily
3. Restart sensor computer
4. Close unnecessary analysis programs
5. May need computer upgrade for high-traffic environments

### E-SENS-470: Sensor Display Failure
**Severity**: ERROR
**Description**: Sensor display screens not showing data
**Cause**: Display hardware failure, computer connection lost, software crash
**Impact**: Cannot view sensor data (data still collected)
**Action**:
1. Restart display terminals
2. Check connection to sensor computer
3. Switch to backup display
4. Access sensor data via portable terminal
5. Repair display hardware

---

## Critical (600-799)

### E-SENS-600: Multiple Sensor Systems Offline
**Severity**: CRITICAL
**Description**: 3 or more primary sensor types simultaneously failed
**Cause**: Power system failure, computer crash, catastrophic damage, electromagnetic pulse
**Impact**: Severely limited situational awareness, navigation hazard
**Action**:
1. Check main power distribution to sensor bay
2. Verify sensor computer operational
3. Restart all sensor systems
4. Check for physical damage (hull breach, fire, impact)
5. Assess which sensors still functional
6. Reduce speed and maneuver cautiously
7. Request assistance if in hazardous area

### E-SENS-610: Total Sensor Blackout
**Severity**: CRITICAL
**Description**: All sensor systems completely non-functional
**Cause**: Complete power loss to sensors, computer failure, EMP damage, catastrophic damage
**Impact**: Vessel is "blind," cannot detect objects or hazards
**Action**:
1. Check power to sensor systems (circuit breakers, fuses)
2. Restart sensor computer
3. Check for catastrophic damage
4. Attempt to restore any single sensor type
5. Use manual methods:
   - Visual observation through windows
   - Portable sensors if available
   - Radio contact with other vessels for guidance
6. DO NOT maneuver at high speed (collision risk)
7. DO NOT attempt FTL jump (cannot detect mass shadows)
8. Send distress signal
9. Request escort to safe port

### E-SENS-620: Sensor Blind Spot Critical
**Severity**: CRITICAL
**Description**: Large area around vessel has no sensor coverage
**Cause**: Multiple sensor array elements damaged, misaligned, or failed
**Impact**: Cannot detect objects in blind area, collision/threat risk
**Action**:
1. Identify blind area precisely
2. Maneuver to compensate (point functioning sensors toward threats)
3. Request other vessels to watch blind spot
4. Repair damaged sensor arrays urgently
5. Extreme caution in traffic or combat

### E-SENS-630: Contact Collision Imminent
**Severity**: CRITICAL
**Description**: Detected object on collision course, impact in <60 seconds
**Cause**: Object detected late, high relative velocity, course error
**Impact**: Collision imminent
**Action**:
1. IMMEDIATE evasive maneuvers
2. Sound collision alarm
3. Attempt communication with object if vessel
4. Brace for impact if unavoidable
5. After avoidance, assess why collision not detected sooner

### E-SENS-640: Mass Shadow Detected in FTL Path
**Severity**: CRITICAL
**Description**: Large mass (planet, star) detected in planned FTL jump vector
**Cause**: Navigation error, inaccurate charts, object moved into path
**Impact**: FTL jump would result in catastrophic collision
**Action**:
1. ABORT FTL JUMP IMMEDIATELY (if not yet initiated)
2. Recalculate jump vector avoiding mass shadow
3. Verify navigation charts accurate
4. Check graviton detector functioning properly
5. Never ignore this warning (collision at FTL speeds = total destruction)

---

## Emergency (800-999)

### E-SENS-800: Sensors Failed During Critical Operation
**Severity**: EMERGENCY
**Description**: Sensor failure during docking, combat, FTL approach, or other critical maneuver
**Cause**: Unfortunate timing, damage, system overload
**Impact**: Cannot complete critical operation safely
**Action**:
**During Docking**:
1. Abort docking approach immediately
2. Increase distance from station/vessel
3. Request visual guidance from station
4. Switch to manual visual navigation
5. Do not attempt blind docking

**During FTL Preparation**:
1. ABORT FTL sequence
2. Do not jump without sensors (mass shadow detection critical)
3. Repair sensors before FTL attempt

**During Combat**:
1. Attempt evasive maneuvers (even without sensors)
2. Use any partial sensor data available
3. Request assistance from allied vessels
4. Withdraw from combat if possible

**During Hazardous Navigation**:
1. Reduce speed immediately
2. Use any remaining sensors
3. Request guidance from nearby vessels
4. Navigate to open space away from hazards

### E-SENS-810: Unknown Object at Close Range
**Severity**: EMERGENCY
**Description**: Large unidentified object detected very close to vessel
**Cause**: Object approached undetected, sensor failure, stealthy object
**Impact**: Potential collision or threat
**Action**:
1. Sound alarm
2. Identify object immediately (visual, communication)
3. Assess threat level
4. Prepare evasive maneuvers
5. Ready defensive systems if threat possible
6. Investigate why not detected earlier

### E-SENS-820: Radiation Levels Critical
**Severity**: EMERGENCY
**Description**: Radiation sensors detecting dangerous levels
**Cause**: Reactor leak, nearby radiation source, damaged shielding, stellar event
**Impact**: Crew radiation exposure, potential radiation sickness
**Action**:
1. Identify radiation source immediately
2. If internal (reactor leak):
   - See EMERG-005 reactor emergency procedures
   - Evacuate affected areas
3. If external:
   - Move away from radiation source
   - Increase shielding (use cargo, water tanks as barriers)
4. Crew to protected areas
5. Monitor crew exposure levels
6. Medical check for all exposed personnel

### E-SENS-830: Tracking System Overwhelmed
**Severity**: EMERGENCY
**Description**: Sensor system cannot track all contacts, losing critical information
**Cause**: Extreme high-traffic environment, combat with many missiles, dense debris field
**Impact**: May lose track of threats or hazards
**Action**:
1. Prioritize tracking by threat level
2. Filter out low-priority contacts
3. Manually track highest threats
4. Request assistance from other vessels
5. Withdraw from area if possible
6. Activate defensive systems (if combat)

### E-SENS-900: Sensor Failure Before FTL Jump
**Severity**: EMERGENCY
**Description**: Sensors failed after FTL jump initiated but before tunnel entry
**Cause**: System failure, damage during charge sequence
**Impact**: Cannot detect mass shadows during FTL, catastrophic collision risk
**Action**:
1. EMERGENCY FTL ABORT
2. Press FTL ABORT button immediately
3. Accept spatial displacement (better than collision)
4. Do not attempt to continue jump
5. Repair sensors fully before any FTL attempt
6. Verify graviton detector especially (mass shadow detection critical)

**See EMERG-006 for FTL emergency procedures**

### E-SENS-910: Hostile Weapon Lock Detected
**Severity**: EMERGENCY
**Description**: Sensors detect active targeting lock from hostile vessel
**Cause**: Hostile action, combat situation, pirate attack
**Impact**: Weapons may be fired at your vessel imminently
**Action**:
1. Sound combat alarm
2. Evasive maneuvers
3. Activate defensive systems if equipped
4. Attempt communication with hostile
5. Prepare for impact
6. Send distress signal
7. Protect critical systems and crew

---

## Troubleshooting Quick Reference

| Symptom | Likely Error Codes | First Check |
|---------|-------------------|-------------|
| No radar detection | E-SENS-400, E-SENS-401 | Power, antenna, transmitter |
| Can't see visually | E-SENS-410, E-SENS-411 | Optics clean, focus system, power |
| No gravity sensing | E-SENS-420, E-SENS-600 | Power, cooling system, calibration |
| Radiation sensors dead | E-SENS-430 | Calibration, contamination, power |
| Can't range accurately | E-SENS-440 | Lidar power, alignment, optical cleanliness |
| Display shows nothing | E-SENS-470 | Display power, connection to computer |
| Many false contacts | E-SENS-210 | Reduce sensitivity, filter settings |
| All sensors dead | E-SENS-610 | Main power, sensor computer, damage |
| Tracking limit reached | E-SENS-230, E-SENS-830 | Filter contacts, prioritize tracking |

## Sensor System Failure Impact Matrix

| Failed Sensor | Navigation Impact | Docking Impact | FTL Impact | Combat Impact |
|---------------|-------------------|----------------|------------|---------------|
| Radar | Moderate | Moderate | Low | High |
| Optical | Low | High | Low | Moderate |
| Graviton | Low | Low | CRITICAL | Low |
| Radiation | Low | Low | Moderate | Moderate |
| Lidar | Low | CRITICAL | Low | Low |

**CRITICAL Impact**: Operation extremely dangerous or impossible without this sensor

## Related Documents

- SENS-SYS-001: Sensor Array System Overview
- SENS-SYS-002: Sensor Calibration Procedures
- SENS-SYS-003: Tactical Sensor Operations
- NAV-SYS-002: Sensor-Based Navigation
- EMERG-013: Sensor Failure Emergency Procedures

## Support Contact

For sensor system errors:
- **Outer Rim Support Line**: 24/7 assistance
- **Sensor Specialist Hotline**: Complex sensor issues
- **Navigation Emergency**: Sensor failure during critical operations

---

**SAFETY REMINDER**: Never attempt FTL jump without functional graviton detector (mass shadow detection). Sensor failures during critical operations require immediate abort. Maintain sensor redundancy where possible.
