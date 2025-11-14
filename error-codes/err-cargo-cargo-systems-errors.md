# ERR-CARGO: Cargo Systems Error Codes

**System:** Cargo Management and Handling Systems
**Error Code Range:** E-CARGO-100 through E-CARGO-999
**Manufacturer:** Outer Rim Starship Manufacturing (ORSM)
**Document Version:** 2.1
**Last Updated:** 2847.09.14

## Purpose

This document provides complete reference for all cargo system error codes. Use this to diagnose issues with cargo bay doors, environmental controls, loading systems, and cargo monitoring.

## Error Code Format

**E-CARGO-XXX**
- **E**: Error
- **CARGO**: Cargo systems
- **XXX**: Specific error number

**Severity Levels:**
- **INFO**: Informational, no action required
- **CAUTION**: Monitor, may require attention
- **WARNING**: Requires action soon (hours to days)
- **CRITICAL**: Immediate action required

---

## E-CARGO-100 Series: Cargo Bay Door Errors

### E-CARGO-101: Door Failed to Open
**Severity:** WARNING
**Description:** Cargo bay door did not open when commanded

**Possible Causes:**
- Door mechanism jammed (cargo blocking, debris)
- Door motor failure
- Control system fault
- Power supply issue
- Manual lock engaged

**Diagnostic Steps:**
1. Check manual lock: Is it engaged? (Disengage if needed)
2. Check power: Is power reaching door motor? (Verify circuit breaker)
3. Check for obstructions: Visual inspection through viewport
4. Check motor: Listen for motor sound when opening commanded
5. Check control system: Try manual controls vs. automatic

**Solutions:**
- **If jammed:** Remove obstruction, then retry
- **If no power:** Reset circuit breaker
- **If motor failed:** Replace door motor (Part #: DOOR-MOTOR-CARGO)
- **If control fault:** Reboot control system or use manual override

**Related:** KB-134 (Cargo Door Troubleshooting)

---

### E-CARGO-102: Door Failed to Close
**Severity:** CRITICAL
**Description:** Cargo bay door did not close when commanded

**Possible Causes:**
- Door mechanism jammed
- Door seals damaged (preventing full closure)
- Sensor detecting obstruction (safety interlock)
- Motor or control failure

**Diagnostic Steps:**
1. Check sensors: Is safety sensor detecting obstruction? (Override if false alarm)
2. Check seals: Visual inspection for damage or misalignment
3. Check for obstructions: Cargo protruding beyond door line?
4. Check motor: Listen for motor attempting to close

**Solutions:**
- **If obstruction:** Remove or reposition cargo
- **If sensor false alarm:** Clean sensor, recalibrate, or temporarily override (use caution)
- **If seals damaged:** Replace door seals (Part #: SEAL-DOOR-CARGO)
- **If motor failed:** Replace motor or use manual crank

**CRITICAL:** Cannot depressurize bay or enter vacuum with door open. Repair immediately if in space.

---

### E-CARGO-103: Door Position Unknown
**Severity:** CAUTION
**Description:** Control system cannot determine if door is open, closed, or partially open

**Possible Causes:**
- Position sensor failure
- Sensor wiring damaged
- Control computer fault

**Diagnostic Steps:**
1. Visual check: Is door actually open or closed?
2. Check position sensors: Located at door hinges, check for damage or disconnection
3. Check wiring: Trace from sensors to control panel

**Solutions:**
- **If sensor failed:** Replace position sensor (Part #: SENS-POS-DOOR)
- **If wiring damaged:** Repair or replace wiring
- **If computer fault:** Reboot control system

**Workaround:** Operate door manually using visual confirmation of position

---

### E-CARGO-104: Door Partially Open (Unexpected)
**Severity:** WARNING
**Description:** Door stopped mid-travel (not fully open or closed)

**Possible Causes:**
- Motor overload (door binding)
- Power loss during operation
- Control commanded stop (possibly erroneous)
- Mechanical failure (broken gear, linkage)

**Diagnostic Steps:**
1. Check door mechanism: Manually inspect for binding or damage
2. Check power: Was power interrupted during door movement?
3. Check motor current: High current indicates binding

**Solutions:**
- **If binding:** Lubricate door mechanism, remove obstruction
- **If power loss:** Restore power, complete door operation
- **If mechanical failure:** Inspect linkage, gears; replace broken components

**Safety:** Do not leave door partially open (unstable, may close unexpectedly)

---

### E-CARGO-105: Door Opening/Closing Too Slowly
**Severity:** CAUTION
**Description:** Door movement taking longer than expected

**Possible Causes:**
- Motor degraded (worn brushes, bearings)
- Door mechanism needs lubrication
- Power supply voltage low
- Overload (door very heavy, warped)

**Diagnostic Steps:**
1. Time door operation: Normal is 10-30 seconds depending on size
2. Listen to motor: Sounds labored? Smooth?
3. Check voltage: Should be 380-420 VDC
4. Inspect door: Warped? Bent? Binding on track?

**Solutions:**
- **If motor worn:** Replace motor
- **If needs lubrication:** Apply grease to hinges, tracks (Part #: GREASE-DOOR-A)
- **If voltage low:** Check power system, increase priority
- **If door damaged:** Straighten or replace door panels

**Acceptable:** Some slowness is OK if door functions. Replace motor before complete failure.

---

### E-CARGO-106: Door Seal Pressure Test Failed
**Severity:** CRITICAL (if need to depressurize)
**Description:** Door seal not maintaining pressure (leaking)

**Possible Causes:**
- Seal damaged or worn
- Seal misaligned
- Door not closing fully
- Seal contaminated (debris preventing seal)

**Diagnostic Steps:**
1. Pressurize bay slightly (if safe): Monitor pressure decay rate
2. Visual inspection: Look for gaps, damaged seal sections
3. Check door closure: Is door fully closed and latched?

**Solutions:**
- **If seal worn:** Replace door seals (Part #: SEAL-DOOR-CARGO)
- **If contaminated:** Clean seal surface and door mating surface
- **If door not closing fully:** Adjust door alignment or latches
- **If seal misaligned:** Re-seat seal in channel

**CRITICAL:** Cannot operate in vacuum with leaking door. Repair before departing station or exposing bay to vacuum.

---

## E-CARGO-200 Series: Environmental Control Errors

### E-CARGO-201: Bay Temperature Out of Range
**Severity:** CAUTION or WARNING (depends on cargo)
**Description:** Cargo bay temperature outside acceptable range

**Possible Causes:**
- HVAC system malfunction
- Heater or cooler failure
- Thermostat misconfigured
- External environment extreme (near star, deep space)

**Diagnostic Steps:**
1. Check current temperature: What is actual temperature?
2. Check target temperature: What should it be for cargo type?
3. Check HVAC status: Running? Adequate capacity?
4. Check for heat sources: Equipment in bay generating heat?

**Solutions:**
- **If HVAC failed:** See KB-018 (Temperature Control Failure)
- **If target wrong:** Adjust thermostat to cargo requirements
- **If capacity insufficient:** Reduce heat load (turn off equipment) or increase HVAC capacity
- **If external:** Adjust ship orientation (minimize solar exposure or maximize)

**Cargo Damage Risk:**
- Temperature-sensitive cargo may spoil, degrade, or become dangerous if temperature not maintained
- Check cargo manifest for temperature requirements

---

### E-CARGO-202: Bay Pressure Abnormal
**Severity:** WARNING
**Description:** Cargo bay pressure not at expected level

**Possible Causes:**
- Pressure leak (door seal, hull breach)
- Pressurization system malfunction
- Incorrect pressure setting

**Diagnostic Steps:**
1. Check current pressure: Reading in kPa or PSI
2. Check expected pressure: Should bay be pressurized (101 kPa) or vacuum (0 kPa)?
3. Check for leaks: Pressure slowly dropping? (indicates leak)
4. Check pressurization system: Working? Valves open?

**Solutions:**
- **If leak:** Locate and seal (see E-CARGO-106 for door seals)
- **If system malfunction:** Check valves, compressor, lines
- **If wrong setting:** Adjust pressure to correct level for cargo type

**Safety:** Some cargo requires vacuum (prevents oxidation, combustion). Some requires pressure (liquid cargo, biologicals). Verify cargo requirements.

---

### E-CARGO-203: Bay Humidity Too High
**Severity:** CAUTION
**Description:** Relative humidity in bay exceeding acceptable level

**Possible Causes:**
- Dehumidifier failure
- Water leak into bay
- Cargo releasing moisture (organic materials)
- External environment humid (rare in space, possible in atmosphere)

**Diagnostic Steps:**
1. Check humidity level: Normal is 30-60% RH
2. Check dehumidifier: Running? Draining?
3. Check for water: Leaks from pipes, condensation on walls?
4. Check cargo: Is cargo wet or releasing moisture?

**Solutions:**
- **If dehumidifier failed:** Repair or replace
- **If water leak:** Locate and repair leak
- **If cargo issue:** Ventilate bay, dry cargo, or isolate moisture source
- **If high ambient:** Seal bay, run dehumidifier continuously

**Damage Risk:** High humidity causes corrosion (metal cargo), mold (organic cargo), electronic damage

---

### E-CARGO-204: Bay Atmosphere Contaminated
**Severity:** WARNING
**Description:** Air quality sensors detecting contaminants (toxins, particles, vapors)

**Possible Causes:**
- Cargo leaking (chemicals, fuels)
- Fire or smoke
- Off-gassing from materials
- Ventilation system failure

**Diagnostic Steps:**
1. Check sensor readings: What contaminant detected? (CO, VOC, particulates?)
2. Visual inspection: Smoke? Spills? Damaged cargo?
3. Check ventilation: Is system running and exchanging air?

**Solutions:**
- **If leak:** Contain leaking cargo, clean spill
- **If fire/smoke:** Suppress fire (see KB-089), ventilate thoroughly
- **If off-gassing:** Increase ventilation, seal cargo if possible
- **If ventilation failed:** Repair ventilation system

**Safety:** Do not enter bay with high contamination without breathing apparatus

---

## E-CARGO-300 Series: Loading and Securing Errors

### E-CARGO-301: Center of Gravity Out of Limits
**Severity:** CRITICAL
**Description:** Cargo loading has shifted ship's center of gravity outside safe range

**Possible Causes:**
- Cargo loaded unevenly
- Heavy cargo positioned too far fore/aft or port/starboard
- Cargo shifted during flight

**Diagnostic Steps:**
1. Check CG display: Shows current CG position and safe limits
2. Review cargo manifest: Where is heavy cargo located?
3. Check cargo securing: Is cargo tied down or loose?

**Solutions:**
- **If unbalanced loading:** Redistribute cargo (move heavy items to opposite side or toward center)
- **If cargo shifted:** Re-secure cargo in proper position
- **If cannot rebalance:** Off-load some cargo or accept restricted flight envelope (limited maneuverability)

**Flight Risk:**
- CG too far forward: Nose-heavy, difficulty pitching up, hard landing
- CG too far aft: Tail-heavy, pitch instability, possible uncontrollable
- CG too far lateral: Roll tendency, asymmetric thrust required
**Do not depart with CG out of limits** (flight safety issue)

---

### E-CARGO-302: Cargo Restraint Failure Detected
**Severity:** WARNING
**Description:** Sensor indicating cargo tie-down or restraint has failed

**Possible Causes:**
- Strap broken
- Attachment point failed
- Sensor detecting slack or tension loss

**Diagnostic Steps:**
1. Identify location: Which restraint sensor triggered?
2. Visual inspection: Check that specific restraint
3. Assess cargo: Is cargo actually loose or about to shift?

**Solutions:**
- **If restraint broken:** Replace strap or chain (Part #: STRAP-CARGO-5M)
- **If attachment failed:** Repair or use alternate attachment point
- **If cargo loose:** Re-secure immediately (especially if in flight)
- **If sensor false alarm:** Verify cargo actually secure, then reset alarm

**Shifting cargo hazards:**
- CG change (affects flight stability)
- Damage to cargo or bay
- Injury to crew if near cargo
- Fire risk (friction from shifting)

---

### E-CARGO-303: Overweight Cargo Bay
**Severity:** CRITICAL
**Description:** Total cargo weight exceeds bay or ship rating

**Possible Causes:**
- Cargo weighed incorrectly at loading
- Undeclared cargo added
- Scale calibration error

**Diagnostic Steps:**
1. Check total weight: Bay scales show current weight
2. Compare to limits: Maximum cargo weight from ship specs
3. Review manifest: Does declared weight match scale weight?

**Solutions:**
- **If overweight:** Off-load cargo until within limits
- **If scale error:** Recalibrate scale (Part #: SCALE-CARGO-10T)
- **If slightly over:** May be acceptable if other factors compensate (low fuel, no passengers), consult flight engineer

**Flight Risk:**
- Structural stress (bay floor, ship frame may not handle weight)
- Propulsion inadequate (ship underpowered for weight)
- Braking distance increased (cannot stop as quickly)
**Do not depart overweight** (structural failure or crash risk)

---

### E-CARGO-304: Hazmat Incompatibility Detected
**Severity:** CRITICAL
**Description:** Incompatible hazardous materials stored in proximity

**Possible Causes:**
- Loading error (incompatible materials placed together)
- Manifest error (materials mislabeled)
- Insufficient separation

**Diagnostic Steps:**
1. Identify materials: What hazmat classes involved?
2. Check separation: Physical distance and barriers between them
3. Review incompatibility chart: Which materials cannot be together?

**Common Incompatibilities:**
- **Oxidizers (Class 5) + Flammables (Class 3)**: Fire/explosion risk
- **Acids + Bases**: Violent reaction, heat, fumes
- **Water-reactive (Class 4.3) + Liquids**: Explosion risk
- **Oxidizers + Organics**: Spontaneous combustion

**Solutions:**
- **If incompatible:** Separate materials (minimum 3 meters + barrier)
- **If cannot separate:** Off-load one material type
- **If uncertain:** Consult hazmat guide (Cargo Handling Manual, Section 8)

**CRITICAL:** Incompatible materials can cause fire, explosion, toxic gas release. Do not transport together.

---

## E-CARGO-400 Series: Cargo Monitoring Errors

### E-CARGO-401: Cargo Temperature Sensor Failed
**Severity:** CAUTION
**Description:** Temperature sensor monitoring cargo has failed

**Possible Causes:**
- Sensor damaged
- Sensor disconnected
- Wiring fault

**Diagnostic Steps:**
1. Check sensor location: Where is failed sensor?
2. Visual inspection: Sensor physically damaged?
3. Check wiring: Connected? Corroded?

**Solutions:**
- **If sensor damaged:** Replace sensor (Part #: SENS-TEMP-CARGO)
- **If disconnected:** Reconnect
- **If wiring damaged:** Repair or replace wiring

**Workaround:** Use handheld thermometer to periodically check cargo temperature manually

---

### E-CARGO-402: Cargo Movement Detected
**Severity:** WARNING
**Description:** Accelerometer or sensor detected cargo shifting

**Possible Causes:**
- Cargo not properly secured
- Restraints failed
- Ship maneuvering caused cargo to shift
- Collision or impact

**Diagnostic Steps:**
1. Visual inspection: Has cargo actually moved?
2. Check restraints: Are they intact and tight?
3. Review recent maneuvers: High-G turn or acceleration?

**Solutions:**
- **If cargo shifted:** Stop and re-secure before continuing flight
- **If restraints failed:** Replace and reinforce
- **If maneuvering too aggressive:** Reduce acceleration/turn rates with cargo aboard

**Flight Safety:** Shifting cargo changes CG (affects control), may damage ship or cargo

---

### E-CARGO-403: Cargo Radiation Level High
**Severity:** WARNING or CRITICAL
**Description:** Radiation sensor detecting elevated radiation from cargo

**Possible Causes:**
- Radioactive cargo (declared or undeclared)
- Cargo container damaged (shielding compromised)
- Natural radiation sources (some ores, materials)

**Diagnostic Steps:**
1. Check manifest: Is radioactive cargo declared?
2. Check radiation level: How high? (mSv/hr)
3. Identify source: Which specific cargo item?
4. Check shielding: Is cargo properly shielded?

**Solutions:**
- **If declared and properly shielded:** Verify shielding intact, monitor levels
- **If shielding damaged:** Repair or add additional shielding (lead blankets)
- **If undeclared:** Notify authorities, may need to off-load (illegal)
- **If crew exposure concern:** Limit time in bay, use distance and shielding

**Exposure Limits:**
- <2 mSv/hr: Safe for brief entry
- 2-10 mSv/hr: Limit time in bay, monitor exposure
- >10 mSv/hr: Evacuate bay, seek professional handling

---

## E-CARGO-500 Series: Cargo Handling Equipment Errors

### E-CARGO-501: Cargo Crane/Lift Failure
**Severity:** CAUTION
**Description:** Mechanical lift or crane not operating

**Possible Causes:**
- Motor failure
- Hydraulic system fault
- Control system issue
- Overload protection triggered

**Diagnostic Steps:**
1. Check power: Is lift receiving power?
2. Check hydraulics: Pressure OK? Leaks?
3. Check load: Is lift overloaded?
4. Check controls: Manual control working?

**Solutions:**
- **If motor failed:** Repair or replace motor
- **If hydraulic fault:** Repair hydraulics, check fluid level
- **If overloaded:** Reduce load to within lift capacity
- **If control fault:** Use manual controls or reboot system

**Workaround:** Manual cargo handling (slower, requires crew labor)

---

### E-CARGO-502: Cargo Roller/Conveyor Jam
**Severity:** CAUTION
**Description:** Cargo roller or conveyor system jammed

**Possible Causes:**
- Cargo stuck on rollers
- Foreign object in mechanism
- Roller bearing seized
- Motor overload

**Diagnostic Steps:**
1. Visual inspection: What's blocking rollers?
2. Check cargo: Too large, too heavy, or misaligned?
3. Check rollers: Rotating freely when unloaded?

**Solutions:**
- **If cargo stuck:** Remove cargo, clear jam
- **If foreign object:** Remove debris
- **If bearing seized:** Replace roller (Part #: ROLLER-CARGO-300MM)
- **If motor overload:** Reduce load or replace motor

**Workaround:** Manual cargo movement

---

### E-CARGO-503: Cargo Airlock Malfunction
**Severity:** CRITICAL (if needed for loading/unloading)
**Description:** Cargo airlock not cycling properly

**Possible Causes:**
- Door seal failure
- Pressure equalization fault
- Control system error
- Mechanical jam

**Diagnostic Steps:**
1. Check airlock status: At what stage did it fail?
2. Check pressures: Inner door pressure, outer door pressure, airlock pressure
3. Check seals: Both doors sealing properly?
4. Check controls: Manual override available?

**Solutions:**
- **If seal failure:** Replace seals (Part #: SEAL-AIRLOCK-CARGO)
- **If pressure fault:** Check pumps, valves, pressure sensors
- **If control error:** Reboot system or use manual controls
- **If jammed:** Clear obstruction

**Safety:** Cannot open both airlock doors simultaneously (would vent atmosphere). Airlock must function for safe cargo transfer in vacuum.

---

## E-CARGO-600 Series: Cargo Information/Tracking Errors

### E-CARGO-601: Cargo Manifest Mismatch
**Severity:** CAUTION
**Description:** Actual cargo does not match manifest

**Possible Causes:**
- Loading error (wrong cargo loaded)
- Manifest data entry error
- Undeclared cargo
- Cargo misidentified

**Diagnostic Steps:**
1. Physical inventory: Count and identify actual cargo
2. Compare to manifest: What's missing, extra, or wrong?
3. Review loading records: Where did discrepancy occur?

**Solutions:**
- **If loading error:** Update manifest to match actual cargo
- **If data entry error:** Correct manifest
- **If undeclared:** Notify authorities (may be illegal, smuggling)
- **If misidentified:** Correct identification and classification

**Legal/Insurance:** Manifest must be accurate for customs, insurance, safety. Undeclared cargo can void insurance and result in fines.

---

### E-CARGO-602: Cargo RFID Tag Not Responding
**Severity:** INFO
**Description:** RFID tag on cargo container not readable

**Possible Causes:**
- Tag damaged or removed
- Tag battery dead (active tags)
- RFID reader malfunction
- Electromagnetic interference

**Diagnostic Steps:**
1. Check tag physically: Present? Damaged?
2. Check reader: Working for other tags?
3. Check for interference: Nearby equipment causing EMI?

**Solutions:**
- **If tag damaged:** Replace tag (Part #: TAG-RFID-CARGO)
- **If battery dead:** Replace battery (passive tags have no battery, active tags do)
- **If reader failed:** Repair or replace reader
- **If interference:** Move cargo away from EMI source or shield

**Workaround:** Manual tracking (barcode, visual inspection, manifest)

---

## E-CARGO-700 Series: Emergency and Safety Errors

### E-CARGO-701: Fire Detected in Cargo Bay
**Severity:** CRITICAL
**Description:** Smoke or fire detected by sensors

**Possible Causes:**
- Electrical short
- Cargo fire (spontaneous combustion, chemical reaction)
- Friction/heat from cargo shifting
- External heat source

**Immediate Actions:**
1. **Seal bay:** Close all doors to cargo bay
2. **Alert crew:** Sound fire alarm
3. **Assess:** Fire size, type, cargo involved
4. **Suppress:** See KB-089 (Cargo Bay Fire Response)

**Suppression Options:**
- Extinguishers (manual)
- CO₂ flood (automatic)
- Decompression (last resort)

**CRITICAL:** Fire consumes oxygen, produces toxic smoke, can spread rapidly. Act immediately.

**See:** KB-089 for complete fire response procedures

---

### E-CARGO-702: Toxic Gas Detected in Cargo Bay
**Severity:** CRITICAL
**Description:** Gas sensors detecting hazardous gases

**Possible Causes:**
- Cargo leak (chemical vapors)
- Fire producing toxic smoke
- Container failure (pressurized gas release)
- Off-gassing from materials

**Immediate Actions:**
1. **Evacuate bay:** All crew exit immediately
2. **Seal bay:** Close all doors
3. **Identify gas:** What type? (CO, chlorine, ammonia, etc.)
4. **Ventilate:** If safe, vent to exterior (do not vent to ship interior)

**Gas Types and Responses:**
- **CO (Carbon Monoxide)**: Odorless, deadly. Ventilate, locate source (often fire)
- **Cl₂ (Chlorine)**: Yellow-green gas, corrosive. Ventilate, neutralize with soda ash
- **NH₃ (Ammonia)**: Pungent odor, corrosive. Ventilate, evacuate until dissipated
- **H₂S (Hydrogen Sulfide)**: Rotten egg odor, very toxic. Evacuate, ventilate, locate source

**Safety:** Do not enter bay without breathing apparatus. Some gases heavier than air (settle at bottom), some lighter (rise to ceiling).

---

### E-CARGO-703: Explosion Risk Detected
**Severity:** CRITICAL
**Description:** Conditions indicate explosion hazard

**Possible Causes:**
- Flammable gas accumulation
- Explosive cargo overheating
- Pressure buildup in sealed containers
- Incompatible materials reacting

**Immediate Actions:**
1. **Evacuate adjacent areas:** Crew to safe distance
2. **Assess risk:** What explosive material? How imminent?
3. **Reduce risk:** Cool cargo, ventilate gas, relieve pressure if possible
4. **If imminent:** Decompress bay (removes heat and oxygen) or jettison explosive cargo

**Explosive Materials:**
- **Class 1 Explosives**: Ammunition, fireworks, blasting caps
- **Compressed gases**: Can explode if overheated (propane, oxygen, etc.)
- **Flammable liquids**: Can form explosive vapor (gasoline, solvents)
- **Reactive chemicals**: Can explode if mixed or contaminated

**CRITICAL:** If explosion imminent and cannot prevent, decompress bay or evacuate ship and call for help.

---

### E-CARGO-704: Cargo Bay Depressurization Event
**Severity:** CRITICAL
**Description:** Cargo bay has lost pressure (hull breach or door open)

**Possible Causes:**
- Hull breach (micrometeorite, collision)
- Door opened unintentionally
- Airlock failure
- Explosive decompression (large breach)

**Immediate Actions:**
1. **Seal adjacent compartments:** Close bulkheads to prevent ship-wide decompression
2. **Verify crew safe:** All crew accounted for, none in bay?
3. **Assess breach:** Size, location, can it be sealed?
4. **Seal breach:** If possible, apply emergency sealant or patch

**See:** EMERG-007 (Hull Breach and Decompression) for complete procedures

**Safety:** Do not enter depressurized bay without pressure suit. Cargo may be damaged or ejected.

---

## Troubleshooting Quick Reference

| Error Code | Primary Cause | First Check | KB Article / Manual |
|------------|--------------|-------------|---------------------|
| E-CARGO-101/102 | Door mechanism | Power, obstructions, manual lock | KB-134 |
| E-CARGO-201 | HVAC failure | Temperature, HVAC status | KB-018 |
| E-CARGO-301 | Unbalanced loading | CG display, cargo positions | Cargo Manual |
| E-CARGO-304 | Hazmat incompatibility | Separation, hazmat classes | Cargo Manual Section 8 |
| E-CARGO-402 | Cargo shifted | Visual inspection, restraints | Cargo Manual Section 3 |
| E-CARGO-701 | Fire | Visual, smoke, cargo type | KB-089 |
| E-CARGO-702 | Toxic gas | Gas type, ventilation | EMERG-008 |
| E-CARGO-704 | Decompression | Pressure, breach location | EMERG-007 |

---

## Related Documentation

- KB-089: Cargo Bay Fire Response
- KB-134: Cargo Door Troubleshooting
- KB-018: Temperature Control Failure
- EMERG-007: Hull Breach and Decompression
- EMERG-008: Hazmat Incidents
- Cargo Handling Procedures Manual
- Hazmat Storage and Transportation Guide

---

**Support Note:** Cargo system errors range from minor (door slow, sensor failed) to critical (fire, decompression, explosion risk). Triage quickly: Ask "Is anyone in danger? Is ship in danger?" If yes, emergency response. If no, systematic troubleshooting. Most cargo calls are doors, temperature, or securing issues - straightforward with right procedures.

**Safety Reminder:** Cargo bays can contain hazardous materials. When troubleshooting, always ask "What cargo is in the bay?" and assess hazards before sending crew to investigate. Some issues (fire, gas, radiation) require specialized response, not routine troubleshooting.
