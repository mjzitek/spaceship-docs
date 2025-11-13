# KB-056: Antenna Damage and Replacement

**Category:** Communications Systems - Hardware
**Difficulty:** Intermediate to Advanced
**Est. Time to Resolve:** 2-6 hours (includes EVA)
**Last Updated:** 2847.09.14

## Issue Description

Communications antenna physically damaged, broken, or non-functional. May have been caused by docking incident, micrometeorite impact, debris collision, or combat damage. Requires inspection and possible replacement.

## Symptoms

- Cannot transmit or receive on specific frequency bands
- Communications range significantly reduced
- Antenna status showing "FAILED" or "DISCONNECTED" on panel
- Visible damage to antenna when inspected
- Error codes E-COM-201 through E-COM-210

## Antenna Types and Coverage

**Typical vessel has 8-12 antennas covering different frequency bands:**

### EM Radio Antennas (Local Communications, 0-250,000 km)
- **VHF/UHF Antennas**: 4-8 antennas (100-500 MHz)
  - Part #: ANT-EM-VHF-A (VHF) or ANT-EM-UHF-A (UHF)
  - Whip or stub style, 0.3-1.5 meters long
  - Location: Distributed around hull for omnidirectional coverage
  - Most vulnerable to damage (extends from hull)

### Subspace Antennas (Long Range, 0-15 light years)
- **Subspace Array**: 2-4 phased array panels
  - Part #: ANT-SUB-ARRAY-A
  - Flat panels, 1x2 meters typically
  - Location: Usually dorsal and ventral surfaces
  - More protected (flush with hull), but larger area to damage

### Specialized Antennas
- **Emergency Beacon Antenna**: 1 antenna
  - Part #: ANT-EMER-A
  - Small stub, usually protected location
  - Critical: Used for distress calls
- **Q-Link Antenna**: (if equipped)
  - Quantum entangled, cannot be "damaged" in traditional sense
  - Single-use system, not repairable

## Quick Diagnostic Questions

Ask the customer:

1. **"Which communication systems are affected?"**
   - EM radio only: VHF/UHF antenna issue
   - Subspace only: Subspace array issue
   - All systems: Multiple antennas damaged or internal issue (not antenna)

2. **"When did the communications stop working?"**
   - During docking: Docking collision damaged antenna
   - During flight: Micrometeorite or debris impact
   - After combat: Weapons fire damage
   - Gradual: Connector corrosion or mechanical wear

3. **"Can you visually inspect the antennas from outside the ship?"**
   - If docked: Look from docking port or station
   - If in flight: Use external cameras
   - Look for: Bent, broken, missing, burn marks

4. **"What does the antenna status panel show?"**
   - Access: Comms Panel > System > Antenna Status
   - Shows each antenna: Green (OK), Yellow (degraded), Red (failed)

5. **"How many antennas are showing as failed?"**
   - One antenna: Specific damage to that unit
   - Multiple in same area: Hull section damaged
   - All antennas: NOT antenna damage, internal system issue (see KB-033)

## Visual Inspection

### From Inside Ship (Using External Cameras)

**Steps:**
1. Access external camera views
   - Bridge panel or security system
   - Cycle through cameras to view all hull surfaces
2. Locate antennas:
   - **VHF/UHF**: Small protrusions (whip or stub style)
   - **Subspace**: Rectangular panels flush or slightly raised
3. Look for damage:
   - **Broken**: Antenna bent or snapped off
   - **Missing**: Antenna completely gone (torn off)
   - **Burn marks**: Scorched area around antenna base (lightning, weapons)
   - **Debris**: Foreign object lodged against antenna

### From Outside Ship (EVA or Docked Inspection)

**If safely able to conduct external inspection:**

**Safety Requirements:**
- Docked at station (safest) OR
- EVA with full suit, safety tether, and spotter
- Ship stable (not maneuvering)

**Inspection Procedure:**
1. **Locate antenna** using diagram in Communications Manual
2. **Visual check:**
   - Antenna physically intact?
   - Mounting secure (not loose)?
   - Connector at base intact?
   - Coax cable visible and undamaged?
3. **Tactical check** (if safe):
   - Gently wiggle antenna (should be firm, not loose)
   - Look for cracks in mounting base
   - Check for corrosion on connector

**Document with photos** (for insurance, repair records)

## Common Damage Types and Solutions

### Damage Type A: Antenna Bent but Intact

**Cause**: Impact from docking, debris, or low-velocity collision

**Assessment:**
- Antenna still attached
- Bent at angle (not original position)
- May still partially function (degraded)

**Solution:**
1. **Test functionality:**
   - Try communications on affected band
   - If working (even poorly): Temporary operation possible
2. **Attempt to straighten** (if accessible):
   - **CAUTION**: May break if bent too much
   - Gently bend back toward original position
   - Do not force (better bent than broken off)
3. **Test after straightening:**
   - Check VSWR (should be <2.0:1)
   - If >3.0:1, antenna damaged internally, replace
4. **If communications restored to acceptable level:**
   - Can defer replacement until next scheduled maintenance
5. **If still poor or high VSWR:**
   - Replace antenna (see Replacement Procedure below)

**Temporary Operation:**
- Bent antenna usually works at 40-70% efficiency
- Reduced range but often adequate for local communications
- Plan replacement at next port

---

### Damage Type B: Antenna Broken (Partial Detachment)

**Cause**: High-velocity impact, combat damage, structural failure

**Assessment:**
- Antenna partially separated from base
- Hanging by cable or partially torn off
- Not functioning

**Solution:**
1. **Safety concern:**
   - Loose antenna may detach fully during maneuvers
   - Could impact hull or other components
   - Priority: Remove or secure
2. **If in flight and safe to EVA:**
   - Remove damaged antenna completely
   - Disconnect coax at base
   - Stow damaged antenna inside (or jettison if dangerous)
   - Cap coax connector to prevent moisture/debris
3. **If unable to EVA:**
   - Monitor during maneuvers (use camera)
   - If antenna detaches, track it (may impact ship)
   - Proceed to port for removal/replacement
4. **Install replacement antenna** (see Replacement Procedure)

**Operate without this antenna:**
- Communications degraded but other antennas may compensate
- Select working antennas manually: Comms Panel > Settings > Antenna Selection

---

### Damage Type C: Antenna Completely Missing

**Cause**: High-impact collision, torn off during docking, combat

**Assessment:**
- Antenna gone (only mounting base remains)
- Coax cable may be exposed or torn
- Obvious gap where antenna was

**Solution:**
1. **Immediate safety:**
   - If coax exposed, cover with tape or sealant (prevent moisture intrusion)
   - If hole in hull (rare), apply emergency sealant
2. **Assess communications capability:**
   - Can still communicate using remaining antennas?
   - May have reduced coverage (blind spot where antenna was)
3. **Compensate with remaining antennas:**
   - Access: Comms Panel > Settings > Antenna Selection
   - Select antenna in working direction
   - Orient ship to use working antennas (e.g., if forward antenna missing, face away from station to use aft antenna)
4. **Install replacement antenna** at next opportunity (see Replacement Procedure)

**Insurance/Liability:**
- If torn off during docking at station, station may be liable
- Document damage immediately (photos, timestamp, witnesses)
- File incident report with station authority

---

### Damage Type D: Burn Damage (Lightning, Weapons, Electrical)

**Cause**: Lightning strike in atmosphere, energy weapons, electrical surge

**Assessment:**
- Antenna may look intact but blackened or scorched
- Burn marks around base
- May have damaged connector or coax cable
- Often damages multiple antennas (electrical surge propagated)

**Solution:**
1. **Safety concern:**
   - Electrical surge may have damaged communications electronics
   - Before replacing antenna, verify internal systems OK
2. **Test communications system:**
   - Access: Comms Panel > Diagnostics > System Test
   - Check for errors in transmitter, receiver, or interface
   - If internal damage, repair before replacing antennas (or waste new antenna)
3. **If internal systems OK, inspect antenna:**
   - Check VSWR (likely very high, >10:1, indicating damage)
   - Check connector for carbon tracking or melting
4. **Replace burned antenna and cable:**
   - Antenna: Part # per type (ANT-EM-xxx or ANT-SUB-xxx)
   - Coax cable: Part #: COAX-EM-A or COAX-SUB-A
   - May need to replace entire cable run if surge damage extends into ship
5. **Ground system properly:**
   - Ensure lightning/surge protection installed (Part #: SURGE-PROT-COM)
   - May prevent future damage

**Prevention:**
- Avoid atmospheric flight during electrical storms
- Install surge protection on all antenna feeds
- Some regions of space have electrical hazards (plasma storms, etc.) - avoid if possible

---

### Damage Type E: Connector Corrosion or Loose Connection

**Cause**: Age, moisture intrusion, vibration, poor installation

**Assessment:**
- Antenna looks intact
- Antenna status shows "DISCONNECTED" or intermittent
- Recent vibration or rough maneuvering?

**Solution:**
1. **If accessible from interior (no EVA needed):**
   - Locate antenna connection point (usually near hull, inside access panel)
   - Inspect connector:
     - Corrosion (green/white deposits)
     - Loose (not fully seated)
     - Damaged pins
2. **Clean connector:**
   - Disconnect coax
   - Clean both male and female connectors with electrical contact cleaner
   - Use fine brush or swab to remove corrosion
   - Do not use abrasives (damages plating)
3. **Reconnect firmly:**
   - Ensure connector fully seated
   - Torque to specification (typically 0.5-1.0 Nm for N-type connectors)
   - Apply corrosion preventive compound (Part #: COMP-CORR-A)
4. **Test communications:**
   - Should show "CONNECTED" on antenna status
   - Check VSWR (should be <2.0:1)

**Preventive Maintenance:**
- Inspect antenna connectors annually
- Apply corrosion preventive compound
- Ensure proper seal (moisture barrier)

---

## Antenna Replacement Procedure

**Requires:**
- Replacement antenna (correct part number for frequency band and ship model)
- EVA capability (if antenna external) OR docked with external access
- Tools: Wrench (sizes vary), torque wrench, coax crimping tool (if replacing cable)

### Step 1: Preparation

1. **Power OFF communications system**
   - Prevents electrical damage during replacement
   - Prevents RF burn risk (transmitter can injure if transmitting while handling antenna)
2. **Verify replacement antenna correct:**
   - Check part number matches
   - Check frequency band matches (VHF, UHF, subspace, etc.)
3. **Gather tools and equipment:**
   - Wrench for antenna mount (typically 10mm or 13mm hex)
   - Torque wrench
   - Replacement antenna
   - Replacement gasket (Part #: GSK-ANT-A)
   - Coax cable (if damaged, Part #: COAX-EM-A or COAX-SUB-A)
   - Sealant (Part #: SEAL-ANTH-A)

### Step 2: Remove Damaged Antenna

**If EVA required:**
1. Suit up, tether, safety check
2. Exit airlock, navigate to antenna location
3. Work with spotter (monitor from inside)

**Removal Steps:**
1. **Disconnect coax cable at antenna base:**
   - Usually N-type connector or similar
   - Turn counterclockwise to loosen
   - Pull straight out (don't bend)
2. **Unbolt antenna from mount:**
   - Typically 3-4 bolts
   - Size varies (10mm, 13mm common)
   - Keep bolts (may reuse if not damaged)
3. **Remove antenna and gasket:**
   - Lift antenna away from hull
   - Remove old gasket (usually rubber or silicone)
   - Inspect mounting surface for damage

### Step 3: Install New Antenna

1. **Clean mounting surface:**
   - Remove old sealant residue
   - Wipe with solvent if needed
   - Surface should be smooth and clean
2. **Install new gasket:**
   - Place gasket on mounting base
   - Ensure alignment with bolt holes
3. **Position new antenna:**
   - Align antenna with mounting holes
   - Ensure correct orientation (if directional antenna)
   - Some antennas have alignment mark (e.g., "FORWARD")
4. **Install bolts:**
   - Hand-tighten all bolts first
   - Then torque in star pattern (prevents uneven pressure)
   - Torque specification: Typically 8-12 Nm (check antenna manual)
5. **Connect coax cable:**
   - Align connector (don't force)
   - Push firmly, then turn clockwise to tighten
   - Torque: 0.5-1.0 Nm (hand-tight plus 1/8 turn)
6. **Apply sealant around base** (if required):
   - Some antennas need additional sealant for waterproofing
   - Apply bead around base perimeter
   - Do not obstruct any drain holes

### Step 4: Test and Verification

1. **Return to interior** (if EVA)
2. **Power ON communications system**
3. **Check antenna status:**
   - Access: Comms Panel > System > Antenna Status
   - New antenna should show GREEN (connected, functioning)
4. **Measure VSWR:**
   - Access: Comms Panel > Diagnostics > Antenna Test
   - Select replacement antenna
   - Run VSWR test
   - Should be <2.0:1 (ideally 1.2-1.5:1)
   - If >3.0:1, issue with installation (loose connector, wrong antenna, damaged coax)
5. **Test communications:**
   - Transmit on affected frequency band
   - Verify reception
   - Check range and signal quality

**If VSWR high or communications not working:**
- Check coax connection (most common issue)
- Verify antenna type correct for frequency band
- Check for damage to coax cable
- May need to re-seat antenna or replace coax

### Step 5: Documentation

1. **Record in maintenance log:**
   - Date, time, location
   - Antenna replaced (part number, frequency band, location on hull)
   - Reason for replacement (damage type, cause if known)
   - VSWR measurement after installation
   - Technician name
2. **Update ship's inventory:**
   - Note spare antenna used (order replacement spare)
3. **File insurance claim** (if applicable):
   - Photos of damage
   - Repair invoice
   - Incident report

## Special Considerations

### Subspace Array Replacement

**More complex than EM antenna:**

- **Phased array**: Multiple elements, must be aligned precisely
- **Calibration required**: After replacement, system must calibrate (15-30 minutes)
- **Professional recommended**: Unless experienced, consider yard service

**If field-replacing subspace array:**
1. Follow same removal/installation steps as EM antenna
2. After installation, run calibration:
   - Access: Comms Panel > Subspace > Array Calibration
   - System tests all elements, adjusts phase
   - Takes 15-30 minutes
   - Do not interrupt
3. Test subspace communications after calibration

### Emergency Beacon Antenna

**Critical system:**

- Used for distress calls
- Must be functional
- Some jurisdictions require functional beacon for legal operation

**If emergency beacon antenna damaged:**
- **Priority replacement**
- Test after replacement:
  - Access: Emergency Panel > Beacon Test (NOT Activate!)
  - Test mode verifies antenna without actually transmitting distress
  - Should show "READY" after test

### Multiple Antenna Damage

**If several antennas damaged (e.g., collision affected one side of ship):**

1. **Prioritize replacement:**
   - Emergency beacon: First priority
   - VHF/UHF for local comms: Second priority
   - Subspace for long-range: Third priority
   - Redundant antennas: Replace as able
2. **May need multiple EVA sessions:**
   - Replace most critical first
   - Schedule additional EVAs for remaining antennas
3. **Temporary operation:**
   - Use intact antennas
   - Orient ship to use working antennas
   - Reduced coverage/range acceptable temporarily

## Temporary Workarounds

**If unable to replace antenna immediately (no spare, no EVA capability, etc.):**

### Workaround A: Use Remaining Antennas
- Most ships have 8-12 antennas (redundancy)
- Loss of 1-2 antennas reduces coverage but doesn't eliminate communications
- **Mitigation:**
  - Manually select working antennas
  - Orient ship to use working antennas (e.g., if port antenna broken, keep port side away from station)
  - Operate at reduced range (stay closer to stations, ships)

### Workaround B: Improvised Antenna (Emergency Only)
- Can create crude antenna from wire
- **ONLY if ALL antennas damaged and communications critical**
- **Procedure:**
  - Cut appropriate length wire (1/4 wavelength for frequency)
    - VHF 150 MHz: 0.5 meter wire
    - UHF 450 MHz: 0.17 meter wire
  - Connect to center pin of coax connector
  - Extend wire outside hull (through airlock, hatch, window)
  - Very inefficient but may allow short-range communications
- **Not a permanent solution**, replace with proper antenna ASAP

### Workaround C: Relay Through Other Ship
- If another vessel nearby:
  - Request they relay messages to station/destination
  - Ship-to-ship radio often shorter range (easier with damaged antenna)
  - They can communicate long-range on your behalf

## Parts and Supplies

**Stock aboard as spares:**

- VHF antenna: Part #: ANT-EM-VHF-A (1-2 spares)
- UHF antenna: Part #: ANT-EM-UHF-A (1-2 spares)
- Antenna gaskets: Part #: GSK-ANT-A (5-10 pieces, cheap, common failure)
- Coax cable: Part #: COAX-EM-A, 5-10 meter lengths (2-3 pieces)
- Connectors: N-type connectors, male and female (5-10 pieces)
- Sealant: Part #: SEAL-ANTH-A (1 tube)

**Subspace arrays:**
- Expensive (1,500-5,000 credits each)
- Large (difficult to store)
- Most ships do not stock as spare (order when needed)

**Where to purchase:**
- ORSM parts department
- Most station ship supply stores (generic antennas compatible)
- Emergency: Salvage from derelict ships (test before installing)

## Cost Estimates

**Parts:**
- VHF/UHF antenna: 200-500 credits
- Subspace array: 1,500-5,000 credits
- Emergency beacon antenna: 800-1,200 credits
- Coax cable: 50-150 credits per meter
- Gaskets: 5-20 credits each

**Labor (if professional installation):**
- EM antenna replacement: 500-1,000 credits (2-3 hours)
- Subspace array replacement: 1,500-3,000 credits (4-6 hours, includes calibration)
- EVA surcharge: +500 credits (if ship in flight)

**Insurance:**
- May cover damage if not due to negligence
- Collision damage usually covered (less deductible)
- Combat damage may require special coverage

## Prevention Tips

- **Careful docking**: Most antenna damage occurs during docking
  - Approach slowly, verify clearances
  - Use docking computer/sensors
  - If uncertain, request tug assistance
- **Pre-flight inspection**: Visually check antennas before departure
- **Avoid hazards**: Debris fields, combat zones, electrical storms
- **Proper maintenance**: Annual connector inspection, corrosion prevention
- **Surge protection**: Install on all antenna feeds

## Related Articles

- KB-033: Complete Loss of Communications
- KB-092: Communications System Preventive Maintenance
- KB-134: Docking Damage Assessment and Claims
- ERR-COM-200: Antenna Error Codes

## Related Manuals

- COMM-SYS-001: Communications System Overview
- COMM-SYS-004: Antenna Installation and Maintenance
- EVA-001: Extravehicular Activity Procedures

---

**Support Note**: Most antenna calls are bent or loose connectors, not full replacement needed. Walk customer through visual inspection and status panel check first. If antenna physically broken, advise on temporary operation with remaining antennas. Replacement may be deferred to scheduled maintenance if not critical. Reserve EVA guidance for experienced crews only; recommend yard service for inexperienced.

**Safety Reminder**: Antennas can carry high RF power when transmitting. Always power OFF communications before handling antennas. RF burns are serious injuries.
