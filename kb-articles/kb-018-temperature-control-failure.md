# KB-018: Environmental Temperature Control Failure

**Category:** Life Support Systems - Environmental Control
**Difficulty:** Beginner to Intermediate
**Est. Time to Resolve:** 15-90 minutes
**Last Updated:** 2847.09.14

## Issue Description

Ship interior temperature outside comfortable range (too hot or too cold). Climate control system unable to maintain set temperature. Affects crew comfort, equipment operation, and potentially crew safety in extreme cases.

## Symptoms

- Temperature reading outside normal range (18-24°C)
- HVAC system running but not effective
- Some areas hot while others cold (uneven distribution)
- Error codes E-LIFE-201 through E-LIFE-215
- Crew complaining of discomfort

## Temperature Ranges and Safety

**Comfortable Operating Range:** 18-24°C (64-75°F)

**Uncomfortable but Safe:**
- Cold: 10-17°C (crew can wear extra layers, operations continue)
- Hot: 25-30°C (crew sweating, uncomfortable but not dangerous)

**Degraded Operations:**
- Cold: 5-9°C (manual dexterity impaired, crew fatigue)
- Hot: 31-35°C (heat exhaustion possible, cognitive impairment)

**Dangerous Extremes:**
- Cold: <5°C (hypothermia risk in 2-6 hours)
- Hot: >35°C (heat stroke risk in 1-4 hours)

**Time to Danger** (if unable to repair):
- From 24°C comfortable to dangerous extremes:
  - In space (cooling): 4-12 hours depending on ship size and insulation
  - Near star (heating): 2-8 hours depending on distance and exposure

## Quick Diagnostic Questions

Ask the customer:

1. **"Is the temperature too hot or too cold?"**
   - Hot: Likely cooling system failure
   - Cold: Likely heating system failure or heat loss
   - Both (different areas): Distribution problem

2. **"What temperature is the display showing?"**
   - Actual measurement helps determine severity
   - Is it changing (getting worse) or stable?

3. **"Is this affecting the whole ship or specific areas?"**
   - Whole ship: Main HVAC system failure
   - Specific areas: Duct blockage, local sensor, or zone valve issue
   - One compartment: Insulation breach or local equipment malfunction

4. **"Are you near a star or in deep space?"**
   - Near star: Ship absorbing solar heat, cooling system may be overwhelmed
   - Deep space: Ship radiating heat, heating system working harder

5. **"What's your reactor power output?"**
   - HVAC requires 5-15 kW depending on ship size
   - If reactor <40% output, may not have power for full climate control

## Common Solutions

### Solution A: Thermostat Setting or Sensor Error (30% of cases)

**Cause**: Temperature sensor reading incorrectly or thermostat set wrong.

**Symptoms Specific to This Cause:**
- Temperature feels different than display shows
- HVAC system running constantly or not at all
- Recent changes to settings
- Thermostat display showing unusual readings

**Resolution Steps:**

1. **Check Thermostat Setting**
   - Located on bridge or in main corridor
   - Current set point: Should be 20-22°C typically
   - If set to extreme value (10°C or 30°C): Someone adjusted it accidentally
   - Reset to 21°C and wait 15 minutes

2. **Verify Actual Temperature**
   - Use handheld thermometer or crew experience
   - Does it match thermostat display?
   - If display says 21°C but feels like 15°C: Sensor error
   - If display matches feeling: Sensor working, system not responding

3. **Test Temperature Sensor**
   - Access: Environmental Panel > Diagnostics > Sensor Test
   - System checks primary and backup temperature sensors
   - Should read ambient temperature accurately (±1°C)
   - If sensor reading way off: Sensor failed

4. **Replace Failed Sensor**
   - Location: Usually in main corridor or bridge, wall-mounted
   - Part #: TEMP-SENS-A (standard resistance temperature detector)
   - Replacement:
     - Power OFF HVAC system
     - Remove sensor cover (2 screws)
     - Disconnect wiring (note wire positions: red, black, green)
     - Remove old sensor
     - Install new sensor
     - Reconnect wiring (match colors)
     - Replace cover
     - Power ON HVAC
     - System auto-calibrates new sensor (2-3 minutes)

5. **Recalibrate Sensor** (if sensor reading slightly off)
   - Access: Environmental Panel > Settings > Sensor Calibration
   - Use accurate reference thermometer
   - Adjust sensor reading to match reference
   - Save calibration

**Expected Result:** HVAC system responds to correct temperature reading, brings ship to comfortable temperature in 20-45 minutes.

**If Unresolved:** Sensor may not be the issue, check HVAC system itself.

---

### Solution B: Cooling System Failure (Too Hot - 25% of cases)

**Cause**: Heat exchanger or coolant loop malfunction, unable to reject heat to space.

**Symptoms Specific to This Cause:**
- Ship temperature steadily rising
- Worse when near star or after high power operations
- Coolant pump running but not effective
- Heat exchanger radiators deployed but insufficient

**Resolution Steps:**

1. **Check Heat Exchanger Status**
   - Access: Environmental Panel > Cooling > Heat Exchanger
   - Radiator panels should be deployed (extended to space)
   - If retracted: Deploy now (takes 30 seconds)
   - Some ships have retractable radiators for protection during docking

2. **Verify Coolant Pump Operation**
   - Pump should be audible (low hum)
   - Check pump status: Running? Flow rate normal?
   - Normal flow: 15-40 L/min depending on ship size
   - If pump not running: Check power supply and circuit breaker

3. **Check Coolant Level**
   - View coolant reservoir (usually in engineering)
   - Sight glass should show 75-100% full
   - If low (<50%): Top off with approved coolant (Part #: COOL-HX-A)
   - If very low: Check for leaks

4. **Inspect Heat Exchanger for Blockage**
   - Radiator tubes can become clogged with ice (from tiny leaks) or debris
   - Access: Diagnostics > Cooling > Flow Test
   - System measures coolant flow through each radiator section
   - Low flow indicates blockage

5. **Clear Blockage or Purge System**
   - If ice blockage:
     - Retract radiators into warm environment (inside hull space)
     - Wait 20-30 minutes for ice to melt
     - Extend radiators again
     - Check for coolant leaks (may need to refill)
   - If debris blockage:
     - May require EVA to clear radiator fins
     - Or flush coolant system with cleaning solution at port

6. **Increase Cooling Capacity** (temporary)
   - If system working but insufficient:
     - Reduce power consumption (less heat generated):
       - Dim lights to 50%
       - Shut down non-essential equipment
       - Reduce crew activity
     - Orient ship to minimize solar exposure (broadside to star, not facing)
     - If ship has reflective thermal shields, deploy them

**Expected Result:** Heat exchanger rejecting heat effectively, ship temperature stabilizes then decreases. May take 1-2 hours to cool large ship from 30°C to 21°C.

**If Unresolved:** Heat exchanger may have major damage (micrometeorite holes, pump failure). May need to run ship at elevated temperature until port repairs possible.

---

### Solution C: Heating System Failure (Too Cold - 20% of cases)

**Cause**: Heating elements or waste heat recovery not functioning.

**Symptoms Specific to This Cause:**
- Ship temperature steadily dropping
- Worse in deep space (far from stars)
- Heating elements not warm to touch
- Reactor heat not being utilized

**Resolution Steps:**

1. **Check Heating Element Status**
   - Access: Environmental Panel > Heating > Element Status
   - Should show elements active and consuming power (2-8 kW)
   - If OFF: Check power supply, circuit breakers

2. **Verify Waste Heat Recovery**
   - Ships normally use waste heat from reactor and other systems
   - Heat exchangers transfer reactor coolant heat to cabin air
   - Access: Environmental Panel > Heating > Heat Recovery
   - Should show heat being extracted from reactor coolant loop
   - If not: Valve may be closed or pump not running

3. **Open Heat Recovery Valves**
   - Locate heat recovery valve (usually in engineering, near reactor)
   - Should be in OPEN position (handle parallel to pipe)
   - If closed (handle perpendicular): Open it
   - Heat should start flowing to cabin within 5 minutes

4. **Test Heating Elements**
   - If waste heat insufficient, electric heating elements supplement
   - Access: Diagnostics > Heating > Element Test
   - Each element tested individually
   - Failed element shows no current draw or infinite resistance
   - Replace failed elements

5. **Replace Heating Element**
   - Location: Usually in air ducts or under deck plates
   - Part #: HEAT-ELEM-1500W (1.5 kW elements typical)
   - Replacement:
     - Power OFF heating system
     - Access element (may require removing duct cover)
     - Disconnect electrical
     - Remove mounting hardware
     - Install new element
     - Reconnect electrical
     - Test before closing duct

6. **Reduce Heat Loss** (temporary measure)
   - If heating system working but insufficient:
     - Seal off unused compartments (close doors, shut off ventilation)
     - Wear insulated clothing
     - Use emergency thermal blankets
     - Gather crew in smallest comfortable space (body heat helps)
     - Orient ship to maximize solar exposure (if near star)

**Expected Result:** Heating system brings ship temperature up 2-4°C per hour. May take several hours to reach comfortable temperature.

**If Unresolved:** May need to operate at reduced temperature (15-18°C) until professional repair.

---

### Solution D: Air Circulation Fan Failure (15% of cases)

**Cause**: Fans not circulating air properly, creating hot and cold spots.

**Symptoms Specific to This Cause:**
- Some areas comfortable, others too hot or cold
- Still air (no breeze from vents)
- Inconsistent temperature readings in different compartments
- Can hear difference in fan noise (quieter or absent)

**Resolution Steps:**

1. **Check Fan Status**
   - Access: Environmental Panel > Ventilation > Fan Status
   - Shows each of 4-12 circulation fans (depending on ship size)
   - Should all show "Running" and normal RPM (1,200-2,400 RPM typical)

2. **Identify Failed Fans**
   - Not running: 0 RPM, no power
   - Degraded: Low RPM, noisy, high current draw

3. **Reset or Restart Fan**
   - Try soft restart:
     - Access: Environmental Panel > Ventilation > Fan Control
     - Select problem fan
     - Stop, wait 10 seconds, Start
   - If fan restarts: May have been temporary jam

4. **Check for Duct Blockage**
   - Fan running but no airflow: Duct may be blocked
   - Common causes:
     - Cargo improperly stowed blocking vent
     - Filter extremely dirty
     - Duct collapse (damaged ship)
   - Inspect vents: Is air flowing? Hold paper near vent, should flutter

5. **Replace Air Filter**
   - Blocked filter restricts airflow dramatically
   - Location: At main return air vent(s), usually in corridor
   - Remove filter access panel (2-4 screws)
   - Slide out old filter (Part #: FILT-AIR-HEPA)
   - Note: May be very dirty/dusty
   - Install new filter (arrow on filter points in direction of airflow)
   - Replace access panel
   - Airflow should improve immediately

6. **Replace Failed Fan**
   - If fan motor burned out or damaged:
   - Location: In ductwork or mechanical space
   - Part #: FAN-CIRC-120W (typical 120-watt fans)
   - Replacement:
     - Power OFF ventilation system
     - Access fan (may require duct work)
     - Disconnect electrical
     - Unbolt fan from duct (4 bolts typically)
     - Remove old fan
     - Install new fan (check rotation direction)
     - Bolt in place, reconnect electrical
     - Power ON, verify operation

**Expected Result:** With all fans running, air circulates evenly. Hot/cold spots resolve within 20-40 minutes as air mixes.

**Time Required:** Filter replacement 10 minutes, fan replacement 1-2 hours

---

### Solution E: Insulation Damage or Hull Breach (10% of cases)

**Cause**: Heat escaping through damaged insulation or small hull breach.

**Symptoms Specific to This Cause:**
- Localized cold spot (if breach/damage in specific area)
- HVAC system running constantly but can't keep up
- May have visible damage to wall panels
- Recent collision, combat, or micrometeorite impact
- Frost forming on interior wall (extreme case)

**Resolution Steps:**

1. **Locate Cold Spot**
   - Use handheld thermometer or thermal camera
   - Scan walls, deck, ceiling in affected area
   - Cold spot indicates heat loss location

2. **Visual Inspection**
   - Check wall panels for cracks, holes, damage
   - Look for signs of impact
   - Feel for air movement (small leak)

3. **Hull Breach Check**
   - Access: Bridge > Hull Integrity > Breach Detection
   - Sensors should show any pressure loss
   - Small leak may not trigger alarm but still loses heat
   - If breach detected: Follow EMERG-007 (Hull Breach)

4. **Temporary Insulation Repair**
   - If insulation damaged but no hull breach:
   - Use emergency thermal blankets to cover cold area
   - Tape or fasten in place
   - Reduces heat loss by 50-70% (temporary)
   - Plan permanent repair at port

5. **Seal Small Leak**
   - If tiny hull breach (<5mm):
   - Use emergency sealant (Part #: SEAL-EMER-A)
   - Clean area around leak
   - Apply sealant generously
   - Allow to cure (sets in 5 minutes, full cure 30 minutes)
   - Monitor for re-leak

6. **Isolate Damaged Compartment**
   - If leak cannot be sealed or damage extensive:
   - Close doors to affected compartment
   - Shut off ventilation to that area
   - Reduces heat loss from rest of ship
   - Live/work in undamaged areas until repair

**Expected Result:** Heat loss reduced or eliminated, HVAC able to maintain temperature. Full repair requires yard service.

**If Unresolved:** May need to operate at slightly reduced temperature (17-19°C) until professional hull repair.

---

### Solution F: Insufficient Power to HVAC (5% of cases)

**Cause**: Reactor output low or power being prioritized to other systems.

**Symptoms Specific to This Cause:**
- HVAC system cycling on and off
- Works briefly then stops
- Multiple ship systems degraded
- Reactor output indicator showing <60%

**Resolution Steps:**

1. **Check Reactor Output**
   - View Q-Core control panel
   - Current output should be 60-85% for normal operations
   - If <60%: Reactor issue

2. **Calculate Power Budget**
   - HVAC requires: 5-15 kW (depending on ship size)
   - Life support (APU): 8-15 kW
   - Lights, computer: 3-8 kW
   - Propulsion (if active): 10-50 kW
   - **Total demand** may exceed reactor output

3. **Prioritize Power**
   - If reactor cannot provide full power:
   - Keep: Life support (O₂ generation), critical lights, computer
   - Reduce: HVAC to minimum, dim lights, stop propulsion if safe
   - Shut down: Galley, entertainment, cargo bay systems

4. **Restore Reactor Output**
   - Address reactor issue (see KB-015: Low Reactor Power)
   - Common fixes:
     - Check reactor fuel supply
     - Verify magnetic containment field
     - Check coolant flow
   - Once reactor restored, HVAC returns to normal

**Expected Result:** With adequate power, HVAC functions normally. Temperature stabilizes.

**Temporary Workaround:** Crew can tolerate slightly uncomfortable temperatures (16-26°C) while reactor issue resolved. Not dangerous, just uncomfortable.

---

## Emergency Temperature Extremes

**If temperature drops below 10°C and cannot be restored:**

1. **Prevent Hypothermia**
   - Wear all available clothing in layers
   - Use emergency thermal blankets
   - Stay active (movement generates heat)
   - Gather crew in smallest comfortable space
   - Hot beverages if galley functional

2. **Time to Danger**
   - At 10°C: Can survive days
   - At 5°C: Hypothermia risk in 2-6 hours
   - At 0°C: Hypothermia likely in 1-2 hours
   - Below 0°C: Critical emergency

**If temperature rises above 30°C and cannot be restored:**

1. **Prevent Heat Illness**
   - Remove excess clothing
   - Drink water frequently (minimum 4L/person/day)
   - Reduce physical activity
   - Wet towels on neck and wrists (evaporative cooling)
   - If possible, stay in coolest compartment

2. **Time to Danger**
   - At 30°C: Can work for days (uncomfortable)
   - At 32°C: Reduce activity, heat exhaustion possible
   - At 35°C: Heat stroke risk in 1-4 hours
   - Above 37°C: Critical emergency, crew cannot maintain body temperature

**In either extreme**: Prioritize repairs to HVAC or proceed to nearest port immediately.

## Escalation Criteria

Escalate to emergency support if:

- Temperature dropping below 10°C or rising above 32°C with no fix in sight
- Multiple repair attempts unsuccessful
- Equipment or parts not available
- Crew showing signs of hypothermia or heat illness
- Hull damage suspected (needs professional assessment)

## Prevention Tips

- **Monthly filter changes**: Single most important maintenance
- **Annual HVAC inspection**: Pumps, fans, heat exchanger
- **Monitor coolant levels**: Top off as needed
- **Keep spare sensors and heating elements**: Common failure points
- **Check insulation**: Especially after docking or maneuvering (bumps/scrapes)
- **Avoid extreme temperatures**: Park in shade if near hot star, face star if in distant cold orbit

## Related Articles

- KB-027: Low Oxygen Alert (APU system includes HVAC)
- KB-015: Low Reactor Power Output
- EMERG-007: Hull Breach (if temperature loss from breach)
- KB-087: HVAC Preventive Maintenance

## Related Manuals

- LIFE-ENV-001: Environmental Control System Overview
- LIFE-ENV-002: HVAC Maintenance Procedures
- ERR-LIFE-200: Environmental Control Error Codes

---

**Support Note**: Most temperature control calls are simple: sensor error, dirty filter, or radiators not deployed. Ask about these three first before diving into complex diagnostics. Can resolve 60% of calls in under 15 minutes this way.
