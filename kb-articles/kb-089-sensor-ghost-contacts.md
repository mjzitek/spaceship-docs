# KB-089: Sensor Ghost Contacts - False Readings and Phantom Objects

**Article ID:** KB-089
**Category:** Sensors & Navigation
**Severity:** Medium
**Last Updated:** 2847.09.14
**Author:** ORSM Technical Support

## Problem Description

Sensor array reporting contacts (objects) that don't actually exist, commonly called "ghost contacts" or "phantom readings." These false positives can clutter displays, waste crew time investigating non-existent objects, and in rare cases cause dangerous course changes to avoid imaginary hazards.

## Symptoms

- Contacts appear on sensor display but cannot be visually confirmed
- Objects detected briefly then disappear without logical explanation
- Contacts with inconsistent or impossible properties (wrong size, speed, behavior)
- Multiple weak contacts scattered randomly
- Contacts that don't respond to hailing or show on other ships' sensors
- Sensor shows objects in known-empty space
- "Flickering" contacts (appear/disappear repeatedly)

## Affected Systems

- **Primary**: Sensor Array System (SAS)
- **Secondary**: Navigation Computer, Tactical Display
- **Related**: Communications (wasted time hailing ghosts)

## Common Causes

### 1. Sensor Sensitivity Too High

**Description**: Gain/sensitivity set too high for current environment

**Why it happens**:
- Manually increased sensitivity to detect distant objects
- Auto-gain malfunctioned and increased sensitivity
- Leftover settings from searching for weak signals
- Wrong sensitivity profile for environment type

**How to identify**:
- Many weak contacts scattered across display
- Contacts very small or distant
- Issue worsens when sensitivity increased
- Ghost contacts disappear when sensitivity reduced

**Fix**:
```
1. Access sensor control panel
2. Review current gain settings (radar, optical, etc.)
3. Reduce sensitivity by 20-30%
4. Observe if ghost contacts reduce
5. Find optimal sensitivity (detects real objects, minimal ghosts)
6. Save as new baseline setting
```

**Prevention**: Use sensitivity appropriate for environment. Don't leave high-sensitivity mode enabled after completing search.

### 2. Background Interference

**Description**: External radiation or electromagnetic interference creating false signals

**Sources of interference**:
- Solar flares or stellar radiation
- Nearby high-power transmitters (stations, other ships)
- Nebulae or plasma clouds
- Electromagnetic storms
- Pulsar radiation
- Cosmic ray bursts

**How to identify**:
- Ghost contacts increase near interference source (star, nebula, etc.)
- Multiple sensor types affected simultaneously
- Radiation sensors show elevated background
- Issue resolves when moving away from source

**Fix**:
```
1. Identify interference source (stellar, artificial, environmental)
2. If natural source (star, nebula):
   - Reduce sensor gain
   - Apply noise filtering
   - Increase detection threshold
   - Move away from source if possible
3. If artificial (station, ship):
   - Change sensor frequency band
   - Request interfering party reduce power
   - Increase distance
4. Update sensor filters for environment type
```

**Prevention**: Expect ghosts near stars, nebulae, and high-traffic areas. Adjust sensor settings preemptively.

### 3. Sensor Calibration Drift

**Description**: Sensor calibration has drifted from baseline, misinterpreting noise as contacts

**Why it happens**:
- Time since last calibration (sensors drift over months)
- Temperature extremes affecting sensor performance
- Component aging
- Vibration or shock damage

**How to identify**:
- Ghost contacts persistent across all environments
- Calibration test shows drift from baseline
- Other sensor accuracy issues (ranging errors, misidentification)
- Gradual increase in ghosts over weeks/months

**Fix**:
```
1. Run sensor diagnostic in Sensors > Diagnostics
2. Compare current calibration to baseline values
3. If drift >5%, recalibration needed
4. Run full sensor calibration procedure:
   - Scan known reference objects (stars, planets, beacons)
   - Allow system to auto-adjust
   - Or manual calibration per SENS-SYS-002
5. Verify ghost contacts reduced after calibration
```

**Prevention**: Calibrate sensors monthly. Log calibration dates. Replace aging components before serious drift.

### 4. Internal Reflections and Echoes

**Description**: Radar/lidar signals reflecting off ship's own structure or cargo

**Why it happens**:
- Incorrectly positioned cargo (reflects radar)
- Extended antennas or booms creating reflections
- Metallic cargo or equipment
- Ice or debris on hull reflecting signals
- Sensor poorly positioned (seeing own ship structure)

**How to identify**:
- Ghost contacts at consistent positions relative to ship
- Contacts move with ship (maintain same bearing/distance)
- Only affects active sensors (radar, lidar), not passive (optical)
- Contact position matches ship structure or cargo location

**Fix**:
```
1. Visual inspection of hull and cargo
   - Look for reflective surfaces
   - Check for extended antennas or equipment
   - Inspect for ice buildup or debris
2. Adjust radar/lidar beam pattern
   - Narrow beam to avoid ship structure
   - Mask certain angles where echoes occur
3. Reposition cargo if causing reflections
4. Clean hull of ice/debris (may require EVA)
5. Update sensor exclusion zones (ignore certain bearings)
```

**Prevention**: Proper cargo positioning, regular hull cleaning, sensor exclusion zones for known ship structures.

### 5. Computer Processing Errors

**Description**: Sensor computer misprocessing data, creating false contacts

**Why it happens**:
- Software bugs or glitches
- Memory corruption
- CPU overload (too many real contacts + processing overhead)
- Outdated contact library (misidentifying objects)
- Database errors

**How to identify**:
- Contacts with impossible properties (FTL speed, bizarre trajectories)
- Sensor raw data shows no object but processed display does
- Error logs show processing faults
- Issue resolves after computer restart
- Ghosts appear during high processing load

**Fix**:
```
1. Check sensor computer error logs
   - Look for processing errors, memory faults
2. Restart sensor computer
   - May clear glitches and memory issues
3. Reduce processing load
   - Filter low-priority contacts
   - Decrease scan rate temporarily
4. Update sensor software
   - Latest version may fix bugs
5. Run memory diagnostic
   - Identify and isolate faulty RAM if needed
```

**Prevention**: Keep software updated, restart sensor computer monthly, don't overload with excessive contacts.

### 6. Debris Fields and Particle Clouds

**Description**: Small debris, dust, or particles detected as contacts

**Why it happens**:
- Traveling through asteroid belt debris
- Micro-meteoroid clouds
- Vented gases from other ships
- Ice crystals
- Space junk

**How to identify**:
- Many small, slow-moving contacts
- Contacts consistent with environment (asteroid belt, high traffic area)
- Optically visible as small particles or dust
- Real objects, but too small to be relevant

**Fix**:
```
1. Adjust contact size filter
   - Ignore objects below certain size threshold
   - Filter menu: Set minimum object size to 1m, 5m, or 10m
2. Filter by velocity
   - Ignore very slow objects (likely debris)
3. Apply environmental filter
   - Debris field mode
   - Clutter reduction
4. Focus sensors on specific area
   - Narrow scan to area of interest, ignore debris zones
```

**Note**: These aren't technically "ghosts" (objects are real), but functionally treated as false contacts for navigation.

**Prevention**: Expect debris in belts, near stations, combat zones. Enable debris filters preemptively.

### 7. Rare Causes

**Spatial Anomalies**:
- Quantum fluctuations
- Spacetime distortions near black holes/neutron stars
- Exotic matter presence
- Subspace tears or rifts

**How to identify**: Sensor anomalies, graviton detector readings, navigation oddities

**Fix**: Avoid anomaly area, report to authorities for charting

**Hardware Malfunction**:
- Sensor element failing intermittently
- Loose connection causing intermittent false signals
- Water or corrosion in sensor housing

**How to identify**: Ghosts from specific sensor only, physical inspection reveals damage

**Fix**: Repair or replace faulty sensor element

## Diagnostic Procedure

### Step 1: Characterize the Ghosts

Answer these questions:

1. **How many ghost contacts?**
   - Few (1-5): Likely specific cause (reflection, malfunction)
   - Many (>10): Likely sensitivity, interference, or debris

2. **Where do they appear?**
   - Specific bearing/range: Likely reflection or environmental
   - Random positions: Likely interference or calibration
   - Same position relative to ship: Likely internal reflection

3. **When do they appear?**
   - Constantly: Calibration, hardware fault
   - Near certain locations: Environmental (stars, nebulae, stations)
   - During high activity: Computer overload

4. **What sensor types report them?**
   - Radar only: Active sensor issue (reflection, calibration)
   - All sensors: Interference or computer processing issue
   - One specific sensor: Hardware fault in that sensor

### Step 2: Quick Tests

**Test 1: Sensitivity Test**
- Reduce sensor gain by 30%
- Do ghosts disappear? → Sensitivity too high
- Do ghosts persist? → Not a sensitivity issue

**Test 2: Visual Confirmation**
- Point optical telescope at ghost contact
- Can you see it visually? → Real object (maybe too small to worry about)
- Nothing visible? → Likely ghost contact

**Test 3: Multiple Sensor Confirmation**
- Check if multiple sensor types detect same contact
- All sensors detect it? → More likely real
- Only one sensor type? → Likely ghost or malfunction

**Test 4: Contact Behavior**
- Track contact over time
- Logical motion? → Likely real
- Impossible motion (teleporting, FTL, erratic)? → Ghost or processing error

**Test 5: Restart Test**
- Restart sensor computer
- Ghosts disappear? → Software/processing glitch
- Ghosts return immediately? → Hardware or environmental issue

### Step 3: Apply Fixes

Based on test results, apply appropriate fix from Common Causes section above.

## Sensor Filtering Best Practices

### Configure Filters for Environment

**Open Space** (between systems):
- Medium sensitivity
- Minimum object size: 5 meters
- Detection range: Maximum
- Debris filter: Off

**Asteroid Belt / Debris Field**:
- Medium-low sensitivity
- Minimum object size: 10-50 meters (ignore small debris)
- Debris filter: On (clutter reduction)
- Focus on navigation hazards only

**Near Star / High Interference**:
- Low sensitivity (reduce interference)
- Noise filtering: Maximum
- Higher detection threshold
- Accept reduced range for accuracy

**High Traffic Area** (near stations):
- Medium sensitivity
- Maximum tracking contacts (many real ships)
- Filter very small objects (debris)
- Prioritize transponder-equipped vessels

**Nebula / Plasma Cloud**:
- Low sensitivity
- High noise filtering
- Accept significantly reduced range
- Rely more on passive sensors

### Filter Menu Settings

Most sensor systems have adjustable filters:

**Minimum Object Size**:
- 0.5m: Detect everything (many ghosts)
- 5m: Good general purpose
- 50m: Debris fields (navigation hazards only)

**Minimum Velocity**:
- Filter stationary or very slow objects
- Useful in debris fields
- WARNING: Won't detect stationary vessels!

**Maximum Range Filter**:
- Ignore very distant contacts
- Reduces ghosts from weak distant signals

**Signal Strength Threshold**:
- Require minimum signal strength for contact
- Higher threshold = fewer ghosts, but may miss real weak contacts

**Contact Persistence**:
- Require contact detected multiple scans before displaying
- Eliminates brief glitches
- May delay detection of new real contacts

## When Ghost Contacts Are Dangerous

### Combat Situations

**Problem**: Ghost contacts mistaken for hostile vessels

**Risk**: Waste ammunition, reveal position, tactical confusion

**Solution**:
- Visually confirm all targets before engaging
- Use multiple sensor types
- Request IFF (identification friend/foe) before firing

### Collision Avoidance

**Problem**: Maneuvering to avoid non-existent object

**Risk**: Wasted fuel, course deviation, collision with real object while avoiding ghost

**Solution**:
- Visual confirmation before evasive maneuvers
- Track object over time (real objects have consistent motion)
- Use multiple sensors

### FTL Jump Planning

**Problem**: Aborting jump due to ghost contact in path

**Risk**: Delayed transit, wasted jump preparation

**Solution**:
- Graviton detector is most reliable (few false positives)
- Visually confirm large objects
- Use updated star charts (known objects in area)

## Crew Training

All crew should know:
- Ghost contacts are common, not always a problem
- Confirm with multiple sensors before acting on contacts
- Report persistent ghosts (may indicate malfunction)
- Don't adjust sensitivity without noting original settings
- Visual confirmation is gold standard

## Related Error Codes

- **E-SENS-210**: Excessive False Contacts
- **E-SENS-200**: Radar Gain Reduced
- **E-SENS-201**: Subspace Carrier Drift
- **E-SENS-460**: Sensor Computer Processing Overload

## Related Documents

- **SENS-SYS-001**: Sensor Array System Overview
- **SENS-SYS-002**: Sensor Calibration Procedures
- **ERR-SENS-001**: Sensor System Error Codes

## Technical Support

**If ghosts persist after troubleshooting**:
- **ORSM Support Line**: Sensor specialists can remote-diagnose
- **Sensor Hotline**: Complex sensor issues
- **Software Support**: Processing or filter issues

---

## Real-World Example

*"We were showing 15-20 ghost contacts near the Oort Cloud. Crew was nervous—couldn't confirm visually, but sensors insisted they were there. Turned out sensitivity was cranked up from when we searched for a lost probe. Reduced gain by 40%, ghosts disappeared immediately. Lesson learned: check your sensor settings first!"*

— Navigator Patel, Deep Space Survey Vessel *Horizon*

---

**Final Tip**: Some ghost contacts are better than missing real ones. Don't reduce sensitivity so much that you can't detect actual hazards. Find the balance for your environment.
