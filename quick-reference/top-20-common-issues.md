# TOP 20 COMMON ISSUES - QUICK REFERENCE
**For Help Desk Use | Revision 1.0**

## PURPOSE
This guide covers the 20 most frequent support calls, representing approximately 80% of all customer contacts. Each issue includes symptoms, quick diagnosis, and fast resolution steps.

---

## HOW TO USE THIS GUIDE
1. Match customer symptom to issue number
2. Follow the QUICK FIX first (resolves 60% of cases)
3. If quick fix fails, proceed to FULL DIAGNOSIS
4. Escalate if issue persists after full diagnosis

**Average Resolution Times Listed** | 🟢 < 5 min | 🟡 5-15 min | 🔴 15+ min or escalate

---

## 1. REACTOR WON'T START 🟡
**Frequency:** 15% of all calls | **Avg Resolution:** 8 minutes

### Symptoms
- Startup sequence fails
- "PWR-001: Reactor Startup Failed" error
- Control rods won't insert/withdraw
- Coolant flow warnings

### Quick Fix (Resolves 70% of cases)
```
1. Verify coolant system pressure: 3.5-4.2 MPa
2. Check fuel rod position: All rods should be at 100% withdrawal for startup
3. Reset reactor control computer: Main panel → Diagnostics → Reset
4. Retry startup sequence
```

### Full Diagnosis
- Check coolant temperature: Must be 15-25°C for cold start
- Verify neutron flux sensors are calibrated (< 30 days old)
- Check for control rod mechanical binding
- Review recent maintenance logs for incomplete work

### Escalate If
- Radiation levels abnormal (> 0.5 mSv/hr in control room)
- Multiple failed startups (> 3 attempts)
- Physical damage to reactor components visible

**Reference:** [KB-001](../kb-articles/kb-001-reactor-wont-start.md) | [Error Codes: Power](../error-codes/error-codes-power.md)

---

## 2. FTL JUMP FAILS TO INITIATE 🟡
**Frequency:** 12% of all calls | **Avg Resolution:** 10 minutes

### Symptoms
- "NAV-104: FTL Drive Not Ready" error
- Jump sequence aborts
- Coordinate validation fails
- Drive charging stalls below 100%

### Quick Fix (Resolves 65% of cases)
```
1. Verify destination coordinates are in valid format (3 decimal places max)
2. Check power allocation: FTL needs minimum 35% of reactor output
3. Run pre-jump checklist: Nav Console → FTL → Pre-Jump Check
4. Wait for 100% charge completion (don't interrupt)
```

### Full Diagnosis
- Verify ship is outside gravity well: > 2 AU from stellar body
- Check for local space-time anomalies (sensor scan)
- Ensure all mandatory systems are online (life support, nav, shields)
- Review FTL drive maintenance: Coil calibration current? (< 500 cycles)

### Escalate If
- Drive won't charge above 80%
- Coordinates validate but jump still fails
- Ship is stranded in hostile territory (expedite)

**Reference:** [KB-012](../kb-articles/kb-012-ftl-jump-fails.md) | [FTL Checklist](./qr-ftl-jump-checklist.md)

---

## 3. LOW OXYGEN ALERT 🟢
**Frequency:** 10% of all calls | **Avg Resolution:** 4 minutes

### Symptoms
- "O2 level at 18.5%" or similar warning
- Crew reports difficulty breathing
- Life support panel shows atmospheric warnings

### Quick Fix (Resolves 80% of cases)
```
1. Check sensor calibration date: Life Support → Sensors → Last Cal Date
2. If > 60 days old: Recalibrate sensors (auto procedure, 2 minutes)
3. If < 60 days: Check atmospheric scrubber filters (replace if orange/red)
4. Verify oxygen generation is active and tanks not empty
```

### Full Diagnosis
- Actual O2 measurement: Use portable analyzer if available
- Check for leaks: Pressurization test on affected compartments
- Verify crew count vs. capacity: Overcrowding reduces O2 per person
- Review CO2 scrubber performance: Should remove 98%+ CO2

### Escalate If
- O2 continues dropping despite fixes
- Multiple compartments affected simultaneously
- Hull breach suspected

**Reference:** [KB-027](../kb-articles/kb-027-low-oxygen-alert.md) | [Life Support Manual](../manuals/life-support/atmospheric-processing.md)

---

## 4. COMMUNICATIONS INTERFERENCE/STATIC 🟢
**Frequency:** 8% of all calls | **Avg Resolution:** 5 minutes

### Symptoms
- Garbled transmissions
- "COM-201: Signal Degradation" error
- Can't establish connection
- High noise-to-signal ratio

### Quick Fix (Resolves 75% of cases)
```
1. Change transmission frequency: Comms Panel → Frequency → Auto-Select
2. Increase transmission power: +20% boost usually sufficient
3. Check antenna orientation: Auto-track should be enabled
4. Verify receiver is not out of range: Max range = 15 light-minutes
```

### Full Diagnosis
- Check for local EM interference: Sensors → EM Spectrum Scan
- Verify encryption handshake: Might be protocol mismatch
- Check relay satellite availability and functionality
- Review antenna physical condition: Damage from debris/combat?

### Escalate If
- All frequencies affected equally
- Hardware damage visible to antenna array
- Security protocol issues (encryption failures)

**Reference:** [Error Codes: Communications](../error-codes/error-codes-communications.md) | [Comms Manual](../manuals/communications/communications-protocols.md)

---

## 5. CARGO RESTRAINTS FAILED 🟡
**Frequency:** 7% of all calls | **Avg Resolution:** 12 minutes

### Symptoms
- "Cargo shifted during transit" alert
- Cargo bay sensors show displacement
- Unusual sounds from cargo hold during maneuvers

### Quick Fix (Resolves 60% of cases)
```
1. Immediate: Reduce acceleration to < 0.5G until secured
2. Dispatch crew to cargo bay to assess damage (safety gear required)
3. Re-engage magnetic restraints or deploy backup netting
4. Redistribute load to balance center of gravity
```

### Full Diagnosis
- Check cargo manifest: Was weight limit exceeded?
- Review restraint maintenance logs: Last inspection date?
- Assess damage to cargo and bay structure
- Verify restraint system power supply and sensors

### Escalate If
- Hazmat cargo is involved
- Structural damage to ship from impact
- Restraint system completely non-functional

**Reference:** [KB-045](../kb-articles/kb-045-cargo-shifted-during-transit.md) | [Cargo Manual](../manuals/cargo/cargo-handling-procedures.md)

---

## 6. POWER FLUCTUATIONS/BROWNOUTS 🟡
**Frequency:** 6% of all calls | **Avg Resolution:** 10 minutes

### Symptoms
- Lights dimming/flickering
- Systems randomly restarting
- "PWR-015: Distribution Instability" error
- Non-critical systems shutting down

### Quick Fix (Resolves 55% of cases)
```
1. Check total power draw vs. reactor output: Should be < 95%
2. Disable non-essential systems to reduce load
3. Verify power distribution priority settings: Critical systems first
4. Look for short circuits: Check for burned smell or heat in panels
```

### Full Diagnosis
- Check capacitor banks: Should show steady voltage
- Review recent system additions: New equipment overloading grid?
- Verify reactor output is steady: May indicate reactor issue
- Check distribution node health: Any nodes running hot (> 85°C)?

### Escalate If
- Reactor output is unstable
- Critical systems affected (life support, navigation, shields)
- Physical damage to power distribution system evident

**Reference:** [Error Codes: Power](../error-codes/error-codes-power.md) | [Power Distribution Manual](../manuals/power/power-distribution-networks.md)

---

## 7. SENSOR GHOST CONTACTS 🟢
**Frequency:** 6% of all calls | **Avg Resolution:** 6 minutes

### Symptoms
- Sensors show contacts that aren't there
- "SEN-034: Contact Validation Failed" error
- Multiple phantom readings
- Readings disappear when approached

### Quick Fix (Resolves 70% of cases)
```
1. Recalibrate sensor array: Sensors Panel → Calibrate → Auto-Cal
2. Check for local EM interference or stellar phenomena
3. Adjust sensor sensitivity: Reduce gain by 10-15%
4. Cross-check with visual confirmation if possible
```

### Full Diagnosis
- Review sensor maintenance: Emitters need cleaning? (dust, debris)
- Check for sensor hardware faults: Run diagnostic on each sensor node
- Verify ship isn't generating own interference (reactor, engines)
- Check space environment: Nebulae, asteroid fields cause false positives

### Escalate If
- Sensors show consistent blind spots (potential real threat)
- Calibration fails or can't complete
- Multiple sensor systems failing simultaneously

**Reference:** [KB-089](../kb-articles/kb-089-sensor-ghost-contacts.md) | [Sensor Manual](../manuals/sensors/sensor-calibration.md)

---

## 8. ENVIRONMENTAL CONTROLS - TEMPERATURE EXTREMES 🟢
**Frequency:** 5% of all calls | **Avg Resolution:** 5 minutes

### Symptoms
- Compartments too hot (> 28°C) or too cold (< 18°C)
- "ENV-012: Temperature Out of Range" warning
- Crew comfort complaints
- HVAC system running constantly

### Quick Fix (Resolves 80% of cases)
```
1. Check thermostat setpoint: Should be 20-24°C
2. Verify HVAC filters are clean (replace if > 90 days old)
3. Check for blocked vents: Ensure airflow not obstructed
4. Balance zones: Close vents in comfortable areas to redirect air
```

### Full Diagnosis
- Check coolant loop pressure: Should be stable
- Verify heat exchanger efficiency: May need cleaning
- Look for heat sources: Equipment running hot in affected area?
- Check insulation: Damage to hull insulation from micro-meteorites?

### Escalate If
- Temperature continues rising > 35°C (heat stroke risk)
- Cooling system completely offline
- Temperature drops < 10°C (hypothermia risk)

**Reference:** [Environmental Manual](../manuals/environmental/environmental-control-system.md)

---

## 9. WATER SYSTEM ISSUES 🟡
**Frequency:** 4% of all calls | **Avg Resolution:** 8 minutes

### Symptoms
- Low water pressure
- Water tastes/smells bad
- "Water recycling efficiency < 85%" warning
- Brown/discolored water

### Quick Fix (Resolves 65% of cases)
```
1. Check water filter status: Replace if > 180 days old or indicator red
2. Run purification cycle: Water Panel → Purify → Full Cycle (30 min)
3. Check storage tank levels: May need to ration if low
4. Verify recycling system is active and not bypassed
```

### Full Diagnosis
- Run water quality test: Check for contaminants (test kit in med bay)
- Check for leaks: Inspect pipes in accessible areas
- Verify UV sterilization working: Lamp life < 12 months?
- Review water usage: Is consumption higher than normal?

### Escalate If
- Water quality test shows dangerous contaminants
- Major leak detected (> 10 L/hour loss)
- Water supply critically low (< 48 hours remaining)

**Reference:** [Life Support: Water](../manuals/life-support/water-processing.md)

---

## 10. SHIELDS NOT ACTIVATING 🟡
**Frequency:** 4% of all calls | **Avg Resolution:** 7 minutes

### Symptoms
- Shield button doesn't respond
- "DEF-001: Shield Generator Offline" error
- Shields at 0% after activation attempt
- Generator charging but shields won't deploy

### Quick Fix (Resolves 60% of cases)
```
1. Check power allocation: Shields need 25% reactor output minimum
2. Verify shield emitters not damaged: Visual inspection if possible
3. Reset shield control computer: Defense Panel → Reset Shields
4. Check for interference: Other systems blocking shield harmonic?
```

### Full Diagnosis
- Run shield diagnostic: Defense Panel → Diagnostics → Full Test
- Check shield capacitor charge: Should hold charge when offline
- Verify emitter alignment: Misalignment prevents field formation
- Review combat log: Recent damage to shield generators?

### Escalate If
- In combat situation (expedite response)
- Physical damage to shield generators visible
- Power routing to shields but no activation

**Reference:** [Defensive Systems Manual](../manuals/defensive/shield-systems.md)

---

## 11. COOLANT SYSTEM WARNINGS 🔴
**Frequency:** 4% of all calls | **Avg Resolution:** Escalate immediately

### Symptoms
- "PWR-023: Coolant Pressure Low" error
- "PWR-024: Coolant Temperature High" error
- Reactor temperature rising
- Visible coolant leaks

### Quick Fix (SAFETY CRITICAL)
```
1. IMMEDIATELY reduce reactor output to 50% or less
2. Check coolant reservoir levels: Add coolant if low (< 70%)
3. Look for visible leaks: Report size and location
4. Monitor reactor temperature: Should stabilize below 500°C
```

### Full Diagnosis
- Check coolant pumps: Both should be running
- Verify heat exchanger: May be clogged or fouled
- Check for radiation: Coolant leaks can be radioactive
- Review pressure readings: Sudden drop indicates breach

### Escalate If
- Coolant leak exceeds 5 L/minute
- Reactor temperature continues rising despite throttle
- Radiation levels elevated in engineering spaces
- **ALL COOLANT ISSUES SHOULD BE ESCALATED TO POWER SPECIALIST**

**Reference:** [Coolant Maintenance](../manuals/power/coolant-system-maintenance.md) | [EMERG-005](../emergency-procedures/emerg-005-reactor-emergency.md)

---

## 12. NAVIGATION DRIFT/POSITION ERRORS 🟢
**Frequency:** 3% of all calls | **Avg Resolution:** 6 minutes

### Symptoms
- Ship position doesn't match calculated position
- "NAV-029: Position Drift Detected" warning
- Autopilot corrections increasing in frequency
- Course deviations during transit

### Quick Fix (Resolves 70% of cases)
```
1. Update position with sensor fix: Nav → Sensors → Position Update
2. Recalibrate gyroscopes: Nav → Calibration → Gyro Cal (5 min)
3. Check for external forces: Solar wind, gravity anomalies
4. Verify thruster response: May be asymmetric thrust causing drift
```

### Full Diagnosis
- Check inertial measurement unit (IMU): May need recalibration
- Verify star tracker function: Should lock onto known stars
- Review thruster fuel consumption: Uneven usage indicates problem
- Check for gravitational sources: Nearby planets/asteroids affecting course

### Escalate If
- Position error > 100,000 km and growing
- Navigation computer reports hardware faults
- Ship near hazards (asteroid field, stellar corona)

**Reference:** [Navigation Manual](../manuals/navigation/navigation-overview.md) | [Error Codes: Navigation](../error-codes/error-codes-navigation.md)

---

## 13. AIRLOCK MALFUNCTION 🟡
**Frequency:** 3% of all calls | **Avg Resolution:** 10 minutes

### Symptoms
- Airlock won't cycle
- Door won't open/close
- Pressure equalization fails
- Safety interlocks preventing operation

### Quick Fix (Resolves 50% of cases)
```
1. Check both sides pressurized: Pressure differential must be < 0.1 kPa
2. Verify manual override is not engaged
3. Clear safety interlocks: May require manual reset on airlock panel
4. Use alternate airlock if available while troubleshooting
```

### Full Diagnosis
- Check pressure sensors: False readings prevent cycling
- Verify door seals: Damaged seals prevent proper seal detection
- Check hydraulic/pneumatic pressure for door operation
- Review safety logs: Recent near-miss or actual failures?

### Escalate If
- Person trapped in airlock
- Airlock showing signs of structural failure
- All airlocks malfunctioning (ship-wide system problem)

**Reference:** [Hull Integrity Manual](../manuals/hull-integrity/hull-integrity-overview.md)

---

## 14. FUEL LEVEL DISCREPANCY 🟢
**Frequency:** 3% of all calls | **Avg Resolution:** 4 minutes

### Symptoms
- Fuel gauge reading doesn't match logs
- "Fuel consumption anomaly detected" warning
- Range calculations inconsistent

### Quick Fix (Resolves 85% of cases)
```
1. Reset fuel sensors: Engineering → Fuel → Reset Sensors
2. Manual fuel measurement: Use dipstick or sight glass if accessible
3. Check for sensor drift: Compare multiple tank sensors
4. Verify no fuel transfer in progress causing confusion
```

### Full Diagnosis
- Check for leaks: Inspect fuel lines and tanks
- Review fuel consumption logs: Usage matches mission profile?
- Verify fuel quality: Contamination can affect sensor accuracy
- Check fuel tank temperature: Thermal expansion affects volume

### Escalate If
- Actual fuel leak detected (> 1 L/hour)
- Fuel critically low (< 10% remaining)
- Fuel contamination suspected

**Reference:** [Propulsion Manual](../manuals/propulsion/propulsion-overview.md)

---

## 15. TARGETING SYSTEM ERRORS 🟡
**Frequency:** 3% of all calls | **Avg Resolution:** 8 minutes

### Symptoms
- Weapons won't lock on target
- "WPN-015: Targeting Solution Failed" error
- Crosshairs don't track properly
- Fire control computer unresponsive

### Quick Fix (Resolves 60% of cases)
```
1. Verify sensors providing target data: Need active sensor lock
2. Check target is in weapons range: Different weapons, different ranges
3. Reset fire control computer: Weapons → Reset FCS
4. Manually designate target: Use backup manual targeting mode
```

### Full Diagnosis
- Check sensor-to-weapons data link: May be interrupted
- Verify weapons system power: Needs 15% reactor output minimum
- Check for target countermeasures: ECM, chaff, jamming
- Review targeting computer diagnostics: Hardware faults?

### Escalate If
- In active combat (expedite response)
- Multiple weapons systems affected
- Sensors and weapons both malfunctioning

**Reference:** [Weapons Manual](../manuals/weapons/weapons-overview.md) | [Point Defense](../manuals/weapons/point-defense-systems.md)

---

## 16. CARGO BAY DOOR WON'T OPEN/CLOSE 🟡
**Frequency:** 2% of all calls | **Avg Resolution:** 12 minutes

### Symptoms
- Door stuck partially open/closed
- "Cargo door motor overload" error
- Manual override doesn't work
- Unusual grinding/squealing sounds

### Quick Fix (Resolves 50% of cases)
```
1. Check for obstructions: Cargo blocking door track
2. Verify hydraulic pressure: Should be 15-20 MPa
3. Lubricate door tracks: Use provided maintenance kit
4. Reset door control computer: Cargo Panel → Door Controls → Reset
```

### Full Diagnosis
- Check door motor current draw: Overload indicates binding
- Inspect door tracks and rollers: Damage, wear, debris?
- Verify door sensors: False sensor readings prevent operation
- Check manual crank: Should be able to manually operate in emergency

### Escalate If
- Door stuck open in space (pressurization risk)
- Structural damage visible to door or frame
- Cargo needs urgent loading/unloading

**Reference:** [Cargo Bay Operations](../manuals/cargo/cargo-bay-operations.md)

---

## 17. MEDICAL BAY EQUIPMENT MALFUNCTION 🟡
**Frequency:** 2% of all calls | **Avg Resolution:** 10 minutes

### Symptoms
- Diagnostic scanner not working
- Medical readouts incorrect/inconsistent
- Equipment won't power on
- "Medical system calibration required" warning

### Quick Fix (Resolves 55% of cases)
```
1. Power cycle the affected equipment: Off 30 seconds, then on
2. Check calibration date: Recalibrate if > 90 days
3. Verify equipment is connected to correct power circuit
4. Clean sensors/contacts: Medical-grade cleaning solution
```

### Full Diagnosis
- Run equipment self-diagnostic: Most units have built-in test
- Check for software updates: May need updated medical database
- Verify environmental conditions: Temperature, humidity in spec?
- Review usage logs: Misuse or damage from recent incident?

### Escalate If
- Medical emergency in progress (patient critical)
- Multiple pieces of equipment failing
- Life support equipment (ventilator, etc.) malfunction

**Reference:** [Medical Bay Operations](../manuals/medical/medical-bay-operations.md)

---

## 18. ENCRYPTION KEY EXCHANGE FAILURE 🟢
**Frequency:** 2% of all calls | **Avg Resolution:** 5 minutes

### Symptoms
- "COM-156: Encryption Handshake Failed" error
- Secure communications won't establish
- Key exchange timeout
- Authentication failure messages

### Quick Fix (Resolves 75% of cases)
```
1. Verify both parties using compatible encryption protocol
2. Check system time/date: Must be within 5 minutes of actual time
3. Regenerate encryption keys: Comms → Security → New Keys
4. Retry handshake: May be temporary network issue
```

### Full Diagnosis
- Check encryption module status: May need reset
- Verify certificate validity: Expired certificates cause failures
- Check for man-in-the-middle attack: Security protocols tripped?
- Review network latency: High latency causes timeouts

### Escalate If
- Security breach suspected
- Unable to establish any secure communications
- Involves classified or sensitive transmissions

**Reference:** [Encryption Systems](../manuals/communications/encryption-systems.md) | [Error Codes: Communications](../error-codes/error-codes-communications.md)

---

## 19. WASTE MANAGEMENT SYSTEM FULL/BLOCKED 🟡
**Frequency:** 2% of all calls | **Avg Resolution:** 15 minutes

### Symptoms
- "Waste tank at 95% capacity" warning
- Backups or odors in head facilities
- Waste processing offline
- Tank pumps not operating

### Quick Fix (Resolves 40% of cases)
```
1. Check if holding tanks can be emptied: Docked or have waste processor?
2. If docked: Connect to station waste system and empty tanks
3. If in space: Engage waste processing (recycle water, compact solids)
4. Check for clogs: Access panels near head facilities
```

### Full Diagnosis
- Check waste pump operation: Should cycle regularly
- Verify waste processing chemical levels: May need resupply
- Check for frozen waste lines: Can occur in cold compartments
- Review crew count vs. system capacity: Overloaded?

### Escalate If
- System completely blocked (health hazard)
- Waste processing contaminating water supply
- No ability to empty or process waste for > 48 hours

**Reference:** [Life Support: Water Processing](../manuals/life-support/water-processing.md)

---

## 20. INTERMITTENT SYSTEM RESETS 🔴
**Frequency:** 2% of all calls | **Avg Resolution:** Escalate - Complex

### Symptoms
- Random system restarts
- "Watchdog timer reset" errors
- Data corruption
- Systems cycling off/on without input

### Quick Fix (Diagnostic only - usually escalate)
```
1. Note which systems affected and frequency of resets
2. Check for pattern: Same time of day? During specific operations?
3. Review error logs: System → Logs → Filter by "Reset"
4. Check power quality: Voltage fluctuations cause resets
```

### Full Diagnosis
- Check for software bugs: Recent updates or configuration changes?
- Verify power supply stability: Oscilloscope test on power lines
- Check for overheating: Computers reset at high temperature
- Look for electromagnetic interference: Can cause spurious resets
- Review memory diagnostics: Faulty RAM causes random crashes

### Escalate If
- Critical systems affected (navigation, life support, propulsion)
- Resets increasing in frequency
- Data loss occurring
- **MOST INTERMITTENT RESET ISSUES NEED SPECIALIST DIAGNOSIS**

**Reference:** [Power Distribution](../manuals/power/power-distribution-networks.md) | [Error Codes: Multiple Systems](../error-codes/)

---

## QUICK REFERENCE SUMMARY

### By Resolution Time
**< 5 minutes (Green):**
- #3 Low Oxygen Alert
- #4 Communications Interference
- #7 Sensor Ghost Contacts
- #8 Temperature Extremes
- #12 Navigation Drift
- #14 Fuel Level Discrepancy
- #18 Encryption Key Failure

**5-15 minutes (Yellow):**
- #1 Reactor Won't Start
- #2 FTL Jump Fails
- #5 Cargo Restraints Failed
- #6 Power Fluctuations
- #9 Water System Issues
- #10 Shields Not Activating
- #13 Airlock Malfunction
- #15 Targeting System Errors
- #16 Cargo Bay Door Issues
- #17 Medical Equipment Malfunction
- #19 Waste Management

**Escalate Immediately (Red):**
- #11 Coolant System Warnings
- #20 Intermittent System Resets

### By Success Rate (Quick Fix)
**Highest Success Rate (>70%):**
- #3 Low Oxygen - 80%
- #4 Communications - 75%
- #8 Temperature - 80%
- #14 Fuel Discrepancy - 85%
- #18 Encryption - 75%

**Lowest Success Rate (<60%):**
- #16 Cargo Door - 50%
- #19 Waste Management - 40%
- #20 System Resets - N/A (escalate)

### By System
- **Power:** #1, #6, #11
- **Navigation/FTL:** #2, #12
- **Life Support:** #3, #8, #9, #19
- **Communications:** #4, #18
- **Cargo:** #5, #16
- **Sensors:** #7
- **Defensive/Weapons:** #10, #15
- **Hull/Structure:** #13
- **Medical:** #17
- **Multi-System:** #20

---

## USAGE NOTES FOR SUPPORT AGENTS

### Best Practices
1. **Always try the quick fix first** - It works 60%+ of the time
2. **Time yourself** - If approaching resolution time limit, escalate
3. **Document what you tried** - Next agent or specialist needs to know
4. **Pattern recognition** - If you see same issue repeatedly, report for trending
5. **Update the customer** - Every 5 minutes, let them know status

### When to Deviate from This Guide
- **Emergency situations** - Safety first, always
- **Customer expertise** - Experienced crew may have already tried basics
- **Special circumstances** - Military, medical, law enforcement ships may have unique configurations
- **Recent service** - If just serviced, recent work may be culprit

### Red Flags (Always Escalate)
- Customer says "I smell something burning"
- Multiple unrelated systems failing simultaneously
- Customer reports "I've never seen this error before"
- Radiation, fire, or hull breach involved
- Situation deteriorating despite your actions

---

**Quick Links:**
- [Help Desk Index](./HELP-DESK-INDEX.md)
- [First Responder Checklist](./first-responder-checklist.md)
- [Escalation Guide](./escalation-triage-guide.md)
- [All KB Articles](../kb-articles/)
- [All Error Codes](../error-codes/)

---

**Document Version:** 1.0 | **Last Updated:** Stardate 2438.11
**Feedback:** Report issues or suggested additions to Technical Documentation Team
