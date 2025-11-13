# KB-067: Proximity Sensors / Collision Avoidance Malfunction

**Category:** Navigation Systems - Sensors and Detection
**Difficulty:** Intermediate
**Est. Time to Resolve:** 20-75 minutes
**Last Updated:** 2847.09.14

## Issue Description

Proximity sensors failing to detect nearby objects (other ships, stations, asteroids, debris). Collision avoidance system not alerting to hazards or giving false alarms. May show error codes E-NAV-301 through E-NAV-320.

## Importance of Proximity Sensors

**Critical for:**
- Collision avoidance during normal flight
- Docking maneuvers (station approach)
- Navigation through asteroid fields or debris zones
- Detection of other vessels in busy space
- Automatic emergency evasion (if equipped)

**Without functioning sensors:**
- Must rely on visual observation (limited range, pilot fatigue)
- Docking extremely difficult (cannot judge distance accurately)
- High risk of collision with unseen objects
- Insurance may be void if collision occurs with known sensor failure

## Symptoms

**Sensors Not Detecting Objects:**
- No proximity alerts when approaching station/ship
- Sensor display shows empty space but objects visible
- Cannot get accurate range to target
- Docking computer shows "NO SIGNAL" or "SENSOR ERROR"

**False Alarms:**
- Constant collision warnings with nothing nearby
- Phantom objects on display
- Alerts trigger randomly
- Unable to silence alarms

**Intermittent Operation:**
- Sensors work sometimes, fail other times
- Detection range reduced (only seeing very close objects)
- Some sensors working, others failed (blind spots)

## Sensor Types and Coverage

**Typical ship has 8-16 proximity sensors covering all directions:**

- Forward: 2-4 sensors (primary navigation, docking)
- Aft: 2 sensors (rear approach, backing maneuvers)
- Port/Starboard: 2 sensors each side (lateral awareness)
- Dorsal/Ventral: 2 sensors top/bottom (complete sphere coverage)

**Sensor Technologies:**
- **RADAR**: Radio wave reflection, 0.1-50 km range, works through dust/debris
- **LIDAR**: Laser reflection, 0.01-20 km range, very accurate, can be blocked by particles
- **IR (Infrared)**: Thermal detection, 0.5-10 km range, detects heat signatures
- **Gravitic**: Mass detection, 0.1-5 km range, cannot be fooled, very expensive (military ships)

Most civilian ships use combination of RADAR and LIDAR for redundancy.

## Quick Diagnostic Questions

Ask the customer:

1. **"Are all sensors showing failure or just some?"**
   - All sensors: System-wide issue (power, computer, calibration)
   - Some sensors: Individual sensor failure
   - One direction (e.g., all forward): Wiring or damage to that section

2. **"Is the problem 'not detecting objects' or 'false alarms'?"**
   - Not detecting: Sensor failure, obstruction, or power issue
   - False alarms: Sensor miscalibration, interference, or contamination

3. **"When did this start? Any recent events?"**
   - After docking: Physical damage to sensors
   - After maintenance: Misconfiguration or wiring error
   - Gradual degradation: Sensor contamination or aging
   - Sudden: Component failure or impact damage

4. **"Can you see the sensors from outside the ship?"**
   - Visible damage: Physical sensor damage (broken lens, bent housing)
   - Covered in debris/ice: Contamination blocking sensor
   - Looks normal: Internal failure or software issue

5. **"What environment are you in?"**
   - Asteroid field: High dust may degrade LIDAR
   - Near station: Electromagnetic interference possible
   - Deep space: Should be clear, sensors should work perfectly
   - Atmosphere: Sensors not designed for atmospheric use, may malfunction

## Common Solutions

### Solution A: Sensor Contamination (35% of cases)

**Cause**: Sensor lenses/emitters covered by ice, dust, or debris.

**Symptoms Specific to This Cause:**
- Gradual degradation of detection range
- All or most sensors affected equally
- Recent travel through dusty region or comet tail
- Condensation/frost visible on sensor housing

**Resolution Steps:**

1. **Visual Inspection**
   - If docked: Direct visual inspection of sensors
   - If in flight: Use external cameras to view sensors
   - Look for:
     - Dust/dirt on lens
     - Ice formation (from water vapor condensation)
     - Burn marks (from thruster exhaust)
     - Physical damage

2. **Clean Sensors** (if contaminated)
   - **If docked and accessible**:
     - Soft cloth and approved cleaner (Part #: CLN-OPT-A)
     - Gently wipe sensor lens/emitter
     - Do not use abrasives (will scratch)
     - Do not touch with bare hands (oils contaminate)
   - **If in flight (EVA required)**:
     - Full EVA suit and safety line
     - Clean each sensor carefully
     - Check mounting integrity while outside
   - **If in flight (no EVA possible)**:
     - Some ships have automated wiper system: Access > Sensors > Clean
     - Or wait until docking for manual cleaning

3. **De-Ice Sensors** (if frozen)
   - Sensor heating elements (if equipped):
     - Access: Navigation Panel > Sensors > Heater ON
     - Applies low heat to sensor housing (takes 10-15 minutes)
   - Or wait in warm environment (docked in heated bay)
   - Ice will sublimate in vacuum once heated

4. **Test Sensors After Cleaning**
   - Access: Navigation Panel > Sensors > Diagnostic Test
   - Should show clear returns on test targets
   - Detection range should be back to normal (see specifications)

**Expected Result:** Clean sensors detect objects at full rated range. Problem resolved.

**Prevention:** Monthly sensor inspection and cleaning, especially after traveling through dusty regions.

---

### Solution B: Individual Sensor Failure (25% of cases)

**Cause**: One or more specific sensors damaged or failed.

**Symptoms Specific to This Cause:**
- Sensors fail one at a time over weeks/months
- Blind spot in detection (e.g., port side)
- Some sensors show green (working), others red (failed) on diagnostics
- Recent impact or docking incident

**Resolution Steps:**

1. **Run Sensor Diagnostic**
   - Access: Navigation Panel > Sensors > System Diagnostic
   - Tests each sensor individually
   - Shows status:
     - Green: Sensor operational, normal returns
     - Yellow: Sensor degraded (weak returns, range reduced)
     - Red: Sensor failed (no returns or no response)

2. **Identify Failed Sensors**
   - Note which sensors are red or yellow
   - Note their locations (forward-port, aft-starboard, etc.)
   - Pattern may indicate cause:
     - One sensor: Random failure or specific impact
     - Multiple in same area: Damage to that hull section or wiring
     - Multiple random: Age-related failures (sensors near end of life)

3. **Check Sensor Wiring**
   - Failed sensor may have disconnected or damaged wire
   - Access sensor wiring from interior (through access panel)
   - Verify connector firmly seated
   - Check for damaged wire (crushed, cut, corroded)
   - Repair or replace wiring if damaged

4. **Replace Failed Sensor**
   - Part #: SENS-PROX-RAD (RADAR) or SENS-PROX-LID (LIDAR)
   - **May require EVA or yard service** (sensor mounted on exterior hull)
   - Replacement procedure:
     - Power OFF sensor system
     - Access sensor from exterior (EVA) or interior (if design allows)
     - Disconnect electrical connector
     - Unbolt sensor from hull (typically 4 bolts)
     - Remove old sensor and gasket
     - Install new gasket (Part #: GSK-SENS)
     - Install new sensor
     - Torque bolts to 8 Nm
     - Reconnect electrical
     - Power ON sensor system
     - Run calibration (automatic, 3-5 minutes)

5. **Temporary Workaround** (if replacement not immediately possible)
   - Ship can operate with some sensors failed
   - Be aware of blind spots
   - Extra vigilance when maneuvering in direction of failed sensor
   - Use visual observation to compensate
   - Reduced speed in congested areas
   - Proceed to port for sensor replacement

**Expected Result:** With working sensors, full coverage restored. Blind spots eliminated.

**Time Required:** Sensor replacement 2-4 hours (includes EVA or yard work)

---

### Solution C: Sensor Computer / Processing Unit Failure (15% of cases)

**Cause**: Computer that processes sensor data has crashed or malfunctioned.

**Symptoms Specific to This Cause:**
- All sensors show failed even though likely not all damaged
- Sensor display frozen or blank
- Recent software update or computer glitch
- Error codes E-NAV-350 (computer fault)

**Resolution Steps:**

1. **Check Sensor Computer Status**
   - Access: Navigation Panel > Sensors > System Status
   - Look for:
     - "Computer Error"
     - "Processor Fault"
     - "Memory Error"
     - System frozen (display not updating)

2. **Reboot Sensor Computer**
   - **Soft Reboot** (try first):
     - Access: Navigation Panel > Sensors > Restart System
     - System shuts down and restarts (2-3 minutes)
     - All settings preserved
   - **Hard Reboot** (if soft fails):
     - Power OFF sensor system (circuit breaker or panel switch)
     - Wait 30 seconds
     - Power ON
     - System boots from scratch (5-7 minutes)
     - May lose custom settings

3. **After Reboot, Run Diagnostics**
   - Access: Navigation Panel > Sensors > System Diagnostic
   - Should show all sensors initializing then testing
   - Sensors should come online one by one
   - If all sensors now working: Problem was computer, not sensors

4. **If Reboot Doesn't Help**
   - Run comprehensive diagnostic:
   - Access: Navigation Panel > Sensors > Extended Diagnostics
   - Tests: Processor, memory, I/O connections, sensors
   - Review results:
     - Processor or memory failure: Computer hardware issue
     - I/O failures: Wiring between computer and sensors
     - Sensor failures: Actual sensor damage

5. **Firmware Reload** (if software corruption suspected)
   - **CAUTION: Erases all settings**
   - Backup settings: System > Backup Configuration
   - Download firmware from ORSM support portal or use ship's backup
   - Access: Navigation Panel > Sensors > Update > Manual Firmware Load
   - Follow on-screen instructions (15-20 minutes)
   - After reload, restore settings from backup
   - Run calibration

**Expected Result:** Computer reboots successfully, processes sensor data normally, sensors detect objects.

**If Unresolved:** Sensor computer may need replacement (Part #: NAV-CPU-PROX). Requires professional service.

---

### Solution D: False Alarms from Interference or Miscalibration (10% of cases)

**Cause**: Sensors miscalibrated or picking up electromagnetic interference.

**Symptoms Specific to This Cause:**
- Constant alarms with no visible objects
- Phantom targets on display
- Worse near stations or other ships (interference)
- Recent installation of new equipment (creates interference)

**Resolution Steps:**

1. **Identify Interference Source**
   - When do false alarms occur?
     - Near stations: Station's radar/communications interfering
     - When comms transmitting: Own communications system interfering
     - When using certain equipment: Identify which equipment
   - If pattern identified, interference likely

2. **Adjust Sensor Filters**
   - Access: Navigation Panel > Sensors > Settings > Interference Filter
   - Increase filter level (rejects more noise, but may reduce sensitivity)
   - Test: Do false alarms decrease?
   - Balance: Want to reject false alarms but still detect real objects

3. **Recalibrate Sensors**
   - Sensors may drift from calibration over time
   - Best done in clear space (deep space, no nearby objects)
   - Access: Navigation Panel > Sensors > Calibration
   - Follow on-screen instructions:
     - Point ship away from any objects
     - System establishes baseline (no returns expected)
     - Then point toward known object (station, buoy)
     - System establishes detection threshold
   - Calibration takes 10-20 minutes

4. **Check Sensor Sensitivity Settings**
   - Access: Navigation Panel > Sensors > Settings > Sensitivity
   - Too high: False alarms (detecting cosmic dust as threats)
   - Too low: Not detecting objects until very close
   - Recommended: Medium to Medium-High
   - Adjust based on environment:
     - Clear space: Can use higher sensitivity
     - Dusty region: Reduce sensitivity to avoid false alarms

5. **Shield Interference Source**
   - If specific equipment causing interference:
   - Check equipment installation (proper shielding, grounding)
   - May need to add shielding or filter to that equipment
   - Consult equipment manual or ORSM support

**Expected Result:** False alarms reduced or eliminated. Sensors detect real objects reliably.

**Maintenance:** Recalibrate sensors quarterly or after major repairs.

---

### Solution E: Power Supply Issue (8% of cases)

**Cause**: Sensors not receiving adequate electrical power.

**Symptoms Specific to This Cause:**
- All sensors failed simultaneously
- Recent power fluctuation or reactor issue
- Other ship systems also degraded
- Sensor display dark or flickering

**Resolution Steps:**

1. **Check Sensor Panel Power**
   - Is display lit? Responsive?
   - If completely dark: No power reaching panel

2. **Check Circuit Breakers**
   - Locate electrical panel
   - Find sensor system breaker (labeled "SENSORS" or "PROXIMITY")
   - Check if tripped (switch in middle position or OFF)

3. **Reset Tripped Breaker**
   - Switch breaker to OFF
   - Wait 10 seconds
   - Switch to ON
   - Check if sensor panel powers up

4. **If Breaker Immediately Trips Again**
   - Indicates short circuit in sensor system
   - Do NOT repeatedly reset (fire hazard)
   - Isolate fault:
     - Turn OFF sensor panel switch
     - Reset breaker
     - If holds: Fault in panel/computer
     - If trips: Fault in wiring between breaker and panel
   - Escalate to electrician or repair facility

5. **Check Reactor Output**
   - Verify reactor producing adequate power
   - Sensors require 0.5-2 kW depending on number and type
   - If reactor output low, sensors may be shed to preserve critical systems
   - Refer to KB-015 (Low Reactor Power) if reactor issue

**Expected Result:** With power restored, sensors initialize and begin detecting objects.

**If Unresolved:** Wiring fault or panel failure, requires professional repair.

---

### Solution F: Damage from Collision or Combat (7% of cases)

**Cause**: Physical damage to sensors or sensor housing from impact.

**Symptoms Specific to This Cause:**
- Sensor failure immediately after collision, docking incident, or combat
- Visible damage to hull in area of failed sensors
- Multiple sensors in same area failed
- Possible hull breach or stress warnings

**Resolution Steps:**

1. **Assess Damage**
   - Visual inspection (external cameras or EVA)
   - How many sensors damaged?
   - Hull damage present?
   - Wiring damaged?

2. **Prioritize Safety**
   - If hull breached: Address breach first (EMERG-007)
   - Sensors are secondary to hull integrity

3. **Document Damage**
   - Photos of damaged sensors
   - Note which sensors affected
   - Needed for insurance claim and repair estimate

4. **Temporary Operation**
   - Ship can operate with damaged sensors
   - Be aware of blind spots
   - Extra caution in congested space
   - Reduce speed when maneuvering

5. **Professional Repair Required**
   - Collision damage typically requires yard service
   - May need hull repair, sensor replacement, wiring repair
   - Cannot be fully repaired by crew in most cases

6. **Insurance Claim**
   - File claim for repair costs
   - Provide documentation
   - May cover sensor replacement and hull repair

**Expected Result:** Temporary operation until professional repair. Plan yard visit.

**Cost:** Sensor replacement 2,000-5,000 credits each, plus labor

---

## Emergency Workarounds

**If sensors cannot be repaired and must continue flight:**

### Visual Navigation Only
- Post lookout on bridge
- Use binoculars or bridge windows
- Slow speed (allows more reaction time)
- Avoid congested areas (high collision risk)

### Manual Range-Finding
- If approaching station/ship:
- Use communications to request distance information
- Station traffic control can provide range and bearing
- Other ship can report distance

### Docking Without Sensors
- Request visual guidance from station
- Station operator talks you in: "50 meters, closing at 2 m/s, decrease thrust..."
- Very slow approach (0.5-1 m/s final approach)
- Experienced pilot only

### Collision Avoidance
- Maintain safe distance from all objects (minimum 5 km)
- Frequent course checks
- Listen to traffic control warnings
- Use radar/lidar on communications panel if available (shorter range but better than nothing)

**Note**: Many insurance policies require functional sensors. Operating without may void coverage if collision occurs.

## Escalation Criteria

Escalate to emergency support if:

- All sensors failed and cannot be restored
- Sensors needed urgently (congested space, docking, asteroid field)
- Physical damage suspected requiring professional assessment
- Customer uncomfortable with manual navigation

## Prevention Tips

- **Monthly sensor cleaning**: Especially after dusty regions
- **Quarterly calibration**: Maintains accuracy
- **Careful docking**: Sensor damage often occurs during docking (bumps, scrapes)
- **Protect sensors**: Avoid thruster exhaust directed at sensors
- **Keep spares**: Stock common sensor types (RADAR, LIDAR)
- **Regular diagnostics**: Catch degrading sensors before they fail

## Sensor Specifications (Typical)

**RADAR Sensors:**
- Range: 0.1-50 km (depending on target size)
- Accuracy: ±50 meters
- Update rate: 1 Hz
- Works in dust, debris fields

**LIDAR Sensors:**
- Range: 0.01-20 km
- Accuracy: ±1 meter (very precise)
- Update rate: 10 Hz
- Can be blocked by particles

**Combined System:**
- RADAR for long-range detection
- LIDAR for close-range precision (docking)
- Redundancy if one type fails

## Related Articles

- KB-089: Docking Procedure Without Sensors
- KB-102: Asteroid Field Navigation
- KB-134: Collision Damage Assessment
- EMERG-007: Hull Breach and Decompression

## Related Manuals

- NAV-SENS-001: Proximity Sensor System Overview
- NAV-SENS-002: Sensor Maintenance and Calibration
- ERR-NAV-300: Proximity Sensor Error Codes

---

**Support Note**: Start with sensor cleaning - fixes 35% of cases in 15 minutes. Then run diagnostics to identify failed sensors. Only escalate to complex troubleshooting if cleaning and diagnostics don't reveal obvious issue. Many calls are just dirty sensors from dust/ice.
