# Quick Reference: Common Maintenance Tasks

**Document ID:** QR-MAINT-001
**Last Updated:** 2847.10.06
**Audience:** All crew members, DIY operators
**Purpose:** Quick step-by-step guides for frequent maintenance tasks

## How to Use This Guide

This quick reference provides abbreviated procedures for common maintenance tasks. For complete procedures, consult the full system manuals.

**Skill Levels:**
- ⭐ **Basic:** Anyone can do with minimal tools
- ⭐⭐ **Intermediate:** Requires mechanical aptitude and some tools
- ⭐⭐⭐ **Advanced:** Requires technical knowledge and specialized tools

**Time Estimates:** Approximate time for experienced operator. Add 50-100% if first time.

**Safety First:** If you're uncomfortable with any task, seek professional help. No shame in that.

---

## DAILY MAINTENANCE

### Visual System Inspection (⭐ Basic, 10 minutes)

**Frequency:** Daily
**Why:** Catch problems early before they become emergencies

**Quick Checklist:**
- [ ] Reactor status panel: All green lights?
- [ ] Life support display: O₂ 19-23%, CO₂ <0.5%, pressure 14-15 PSI?
- [ ] Navigation systems: No error codes?
- [ ] Communications: Self-test passing?
- [ ] Hull integrity: No pressure drops?
- [ ] Unusual sounds, smells, vibrations?

**If anything abnormal:** Investigate immediately using relevant troubleshooting guide.

---

### Reactor Parameter Logging (⭐ Basic, 5 minutes)

**Frequency:** Daily
**Why:** Trend analysis helps predict failures
**Tool:** Logbook (paper or digital)

**Steps:**
1. Record core temperature
2. Record plasma density
3. Record coolant pressure
4. Record coolant temperature
5. Record power output
6. Record radiation level (at 1m from reactor)
7. Note any anomalies or error codes

**Normal Values:** See QR-PWR-001 (Reactor Normal Parameters)

**Trend to Watch:**
- Gradual temperature increase (cooling degradation)
- Gradual pressure decrease (coolant loss)
- Increasing fuel consumption (efficiency loss)

---

## WEEKLY MAINTENANCE

### Life Support Filter Check (⭐ Basic, 15 minutes)

**Frequency:** Weekly
**Why:** Clogged filters reduce efficiency and can fail
**Tools:** None (visual inspection)

**Steps:**
1. Open life support panel (usually in corridor or crew area)
2. Locate filter access door
3. Open filter housing
4. Visually inspect filters:
   - **HEPA filters:** Should be white/off-white; Replace if gray or black
   - **Carbon filters:** Check weight; Replace if feel light or saturated
   - **Pre-filters:** Should be clean; Replace if visibly dirty
5. Check filter pressure differential gauge (if equipped):
   - **Green zone:** OK
   - **Yellow zone:** Replace soon
   - **Red zone:** Replace immediately
6. Note filter condition in log
7. Replace if needed (see filter replacement below)

**Filter Lifespan:**
- Pre-filters: 30-60 days
- HEPA filters: 6-12 months
- Carbon filters: 6-12 months

**Part Numbers:**
- FILT-HEPA-A (Standard HEPA)
- FILT-CARBON-B (Carbon filter)
- FILT-PRE-STD (Pre-filter)

---

### Coolant Level Check (⭐ Basic, 5 minutes)

**Frequency:** Weekly
**Why:** Low coolant causes reactor overheating
**Tools:** None (visual gauge)
**Location:** Reactor compartment, coolant reservoir

**Steps:**
1. Locate coolant reservoir sight glass
2. Check level:
   - **92-98%:** Optimal, no action
   - **85-92%:** Adequate, monitor
   - **<85%:** Add coolant soon
   - **<80%:** Add coolant immediately
3. Check for leaks (look for puddles, stains)
4. Log level in maintenance record

**If Level Low:**
- See "Coolant Top-Off" procedure below
- Investigate for leaks if dropping repeatedly

---

### Communication System Test (⭐ Basic, 10 minutes)

**Frequency:** Weekly
**Why:** Verify your lifeline is functional
**Tools:** None

**Steps:**
1. **EM Radio Test:**
   - Transmit test message on open frequency
   - Self-test: Receive on second radio if equipped
   - Or ask nearby ship/station for radio check
   - Should receive clear reply

2. **Subspace Test (if equipped):**
   - Send test message via subspace
   - Verify link stability indicator >90%
   - Check for error codes

3. **Emergency Beacon Test:**
   - Press TEST button on beacon
   - Should receive "TEST PASSED" confirmation within 5 seconds
   - If no confirmation: Troubleshoot immediately (critical safety equipment)

4. **Log Results:**
   - Date and time
   - All systems tested: PASS or FAIL
   - Any issues noted

**If Test Fails:** See ERR-COMM error codes and troubleshooting.

---

## MONTHLY MAINTENANCE

### Fuel Injector Cleaning (⭐⭐ Intermediate, 45 minutes)

**Frequency:** Monthly
**Why:** Dirty injectors reduce efficiency, cause instability
**Tools:** Injector cleaning kit (Part #: KIT-CLEAN-INJ)
**Safety:** Reactor must be in STANDBY (not full shutdown, not full power)

**Steps:**

1. **Prepare Reactor:**
   - Reduce to standby mode (see PWR-SYS-002)
   - Wait 5 minutes for stabilization
   - Verify core temp 600-800°C

2. **Access Injectors:**
   - Open injector access panel (reactor compartment)
   - Disconnect injector power (4 connectors)
   - Remove 4 mounting bolts (10mm socket)
   - Carefully pull injector assembly

3. **Disassemble Injectors:**
   - 6 nozzles per assembly (typically)
   - Unscrew each nozzle (hand-tight, no tools needed)
   - Place in cleaning tray

4. **Clean:**
   - Pour injector cleaning solvent into tray
   - Soak nozzles for 15 minutes
   - Use small brush to scrub each nozzle
   - Focus on tip openings (should be clear, no blockage)
   - Rinse with isopropyl alcohol
   - Dry with compressed air or lint-free cloth

5. **Inspect:**
   - Look for cracks, damage, wear
   - Check o-rings (replace if cracked or hard)
   - If damaged: Replace nozzle (Part #: NOZ-INJ-Q)

6. **Reassemble:**
   - Screw nozzles back into injector assembly (hand-tight)
   - Reinstall assembly into reactor
   - Torque 4 mounting bolts (12 Nm)
   - Reconnect power connectors
   - Close access panel

7. **Test:**
   - Return reactor to normal operation
   - Monitor for 15-30 minutes
   - Check for leaks, unusual sounds
   - Performance should improve (steadier plasma density)

**Cost:** Cleaning solvent ~50 credits, replacement nozzles ~100 credits each if needed

---

### Hull Inspection (⭐⭐ Intermediate, 30-60 minutes)

**Frequency:** Monthly interior, Quarterly exterior (EVA)
**Why:** Detect micrometeorite damage, corrosion, stress cracks
**Tools:** Flashlight, inspection mirror (for tight spots)

**Interior Hull Inspection:**

1. **Walk all accessible compartments:**
   - Look at walls, ceiling, floor
   - Feel for temperature variations (hot/cold spots)
   - Listen for unusual sounds (hissing = leak)

2. **Check for:**
   - Cracks or bulges
   - Discoloration or staining
   - Rust or corrosion
   - Frost formation (indicates breach nearby)
   - Loose panels or fasteners

3. **High-Risk Areas (inspect carefully):**
   - Forward sections (most impacts)
   - Around hatches and doors (stress points)
   - Near equipment with vibration
   - Areas with moisture (galley, head)

4. **Document Any Issues:**
   - Photo if possible
   - Note location precisely
   - Estimate size and severity
   - Schedule repair

**Exterior Hull Inspection (EVA Required):**

1. **Plan EVA:** Two-person team, proper safety
2. **Walk exterior methodically:**
   - Forward to aft, top to bottom
   - Look for impact craters, cracks, missing plates
3. **Focus on:**
   - Armor plating condition
   - Antenna integrity
   - Sensor arrays
   - Heat shield (if present)
   - Weld seams
4. **Mark any damage** for repair
5. **Photos** for maintenance records

**If Breach Found:** See KB-145 (Micrometeorite Impact Response)

---

### Backup Battery Check (⭐ Basic, 10 minutes)

**Frequency:** Monthly
**Why:** Emergency power is critical for survival
**Tools:** Multimeter (optional)
**Location:** Usually near reactor or bridge

**Steps:**
1. Locate backup battery bank
2. Check charge level indicator:
   - **Green:** >80%, good
   - **Yellow:** 50-80%, charging OK
   - **Red:** <50%, investigate
3. Check charging indicator (should show "CHARGING" when reactor running)
4. If equipped with multimeter:
   - Measure voltage across battery terminals
   - Should match rated voltage (typically 24V, 48V, or 120V system)
   - If significantly low, batteries may need replacement
5. Check battery age:
   - Lead-acid: Replace every 5 years
   - Lithium: Replace every 10 years
   - If past lifespan, schedule replacement
6. Log battery status

**If Batteries Not Charging:**
- Check charging circuit breaker
- Check charging system connections
- May need professional diagnosis

**Part Numbers (example, varies by ship):**
- BATT-BACKUP-24V-200AH (24V system)
- BATT-BACKUP-48V-100AH (48V system)

---

## QUARTERLY MAINTENANCE

### Magnetic Field Calibration (⭐⭐⭐ Advanced, 60 minutes)

**Frequency:** Quarterly
**Why:** Magnetic field drift causes plasma instability
**Tools:** Calibration test equipment (Part #: KIT-CAL-MAG)
**Skill:** Advanced - Professional recommended if uncomfortable

**Summary Steps:**
1. Reactor to standby mode
2. Connect calibration equipment to magnetic coil test points
3. Measure field strength of each coil (should be equal, within 0.1 Tesla)
4. Adjust coils as needed via control panel calibration menu
5. Verify all coils balanced
6. Return reactor to normal operation
7. Monitor stability

**Full Procedure:** See PWR-SYS-003, Section 4.2

**Cost:** Calibration kit rental ~500 credits or purchase ~2,000 credits

---

### Coolant Flush and Replacement (⭐⭐ Intermediate, 2-3 hours)

**Frequency:** Quarterly (or annually if low usage)
**Why:** Contaminated coolant loses effectiveness
**Tools:** Drain pan, coolant pump (optional), funnel
**Parts:** Coolant (Part #: COL-NAK-100)

**WARNING: Coolant is hazardous. Sodium-potassium alloy reacts with water. Use proper safety equipment.**

**Steps:**

1. **Prepare:**
   - Full reactor shutdown (not just standby)
   - Wait 2 hours for coolant to cool (<100°C)
   - Verify temperature before proceeding

2. **Drain Old Coolant:**
   - Place drain pan under drain valve (holds ~50-100L depending on system)
   - Open drain valve slowly
   - Let drain completely (30-60 minutes)
   - Dispose of old coolant properly (hazardous waste)

3. **Inspect System:**
   - Look inside reservoir (if transparent)
   - Check for sludge, particles, discoloration
   - If heavily contaminated: Flush with inert gas before refilling

4. **Refill:**
   - Close drain valve
   - Pour new coolant into fill port
   - Fill to 95% line (allow for expansion)
   - DO NOT OVERFILL

5. **Purge Air:**
   - Pressurize coolant system (hand pump usually provided)
   - Bring to 150 PSI
   - Open bleed valve at high point of system
   - Close when coolant flows with no bubbles
   - Top off coolant if needed

6. **Test:**
   - Restart reactor (see PWR-SYS-002)
   - Monitor coolant pressure (should stabilize at 120-140 PSI)
   - Check for leaks
   - Monitor temperature regulation

**Coolant Quantity Needed:**
- Mark III Reactor: 40-60 liters
- Mark V Reactor: 80-120 liters
- Mark VII Reactor: 150-200 liters

**Cost:** Coolant ~50-80 credits per liter

**Disposal:** Contact local hazmat disposal service. DO NOT dump in space, on planets, or in recycling systems.

---

### Full System Diagnostic (⭐⭐ Intermediate, 2-3 hours)

**Frequency:** Quarterly
**Why:** Comprehensive health check catches hidden issues
**Tools:** Ship's diagnostic system
**Procedure:** Varies by ship, but generally:

**Run Diagnostics For:**
1. **Reactor:** PWR-SYS diagnostic routine
2. **Life Support:** LIFE-SYS diagnostic
3. **Navigation:** NAV-SYS diagnostic
4. **Communications:** COM-SYS diagnostic
5. **Hull Integrity:** HULL-SYS scan
6. **Propulsion:** PROP-SYS diagnostic

**For Each System:**
- Start diagnostic from control panel
- Diagnostic runs 15-30 minutes per system
- Review results for errors, warnings, cautions
- Address any issues found
- Document results in maintenance log

**Look For:**
- Sensor drift (requires calibration)
- Component degradation (schedule replacement)
- Performance decline (investigate cause)
- Error codes (troubleshoot)

---

## ANNUAL MAINTENANCE

### Complete System Overhaul (⭐⭐⭐ Advanced / Professional)

**Frequency:** Annually
**Why:** Comprehensive maintenance extends equipment life
**Duration:** 2-5 days depending on ship size
**Recommendation:** Professional service at certified station

**Major Tasks Include:**
- Complete reactor service
- Full life support system service
- Navigation system calibration
- Communication system overhaul
- Hull structural inspection
- Propulsion system service
- All safety systems verification
- Firmware and software updates
- Certification inspection (if required by regulations)

**Cost:** 5,000-25,000 credits depending on ship size and condition

**Can Be Done DIY:** If highly skilled and have time, but most operators use professional service annually.

**Certification:** Many jurisdictions require annual certified inspection for commercial vessels.

---

## COMMON QUICK FIXES

### Coolant Top-Off (⭐⭐ Intermediate, 15 minutes)

**When:** Coolant level 85-92% (below optimal)

**Steps:**
1. Reactor can stay online (standby or normal operation)
2. Locate coolant reservoir fill port
3. Check current level (sight glass)
4. Open fill port carefully
5. Add coolant slowly until level reaches 95% line
6. Close fill port securely
7. Monitor pressure for 15 minutes (should stabilize)

**How Much:** Usually 1-5 liters to top off

---

### Emergency Filter Replacement (⭐ Basic, 10 minutes)

**When:** Life support efficiency dropping, CO₂ rising, filter clogged

**Steps:**
1. Life support can stay online (will run on reserves during replacement)
2. Open filter access panel
3. Turn filter housing counterclockwise to unlock
4. Pull out old filter (dispose properly)
5. Insert new filter (note airflow direction arrow)
6. Turn housing clockwise to lock
7. Verify system returns to normal operation

**Cost:** 50-150 credits per filter depending on type

---

### Circuit Breaker Reset (⭐ Basic, 1 minute)

**When:** Breaker trips, cutting power to equipment

**Steps:**
1. Turn off equipment that was running on that circuit
2. Locate tripped breaker (will be in middle position, not fully "ON")
3. Push breaker fully to "OFF" position
4. Wait 10 seconds
5. Push breaker to "ON" position
6. Turn on equipment one device at a time

**If Breaker Trips Again:**
- You have an overload or short circuit
- Do NOT keep resetting - find and fix problem
- See KB-189 (Power Fluctuations) for diagnosis

---

### Antenna Alignment (⭐⭐ Intermediate, 15 minutes)

**When:** Communication range reduced, signal weak

**Steps:**
1. Access antenna control panel (usually at communications station)
2. Select antenna to align
3. Choose "Auto-Align" if available:
   - System will scan and optimize
   - Takes 5-10 minutes
4. Manual alignment:
   - Point antenna at target (station, ship, relay)
   - Adjust azimuth and elevation
   - Watch signal strength meter
   - Optimize for maximum signal
5. Lock antenna position
6. Test communication

**Note:** Moving antennas may require EVA for external antennas

---

## MAINTENANCE RECORD KEEPING

### What to Log:

**Every Maintenance Task:**
- Date and time
- Task performed
- Parts replaced (with part numbers)
- Who performed it
- Any anomalies noted
- Next due date

**Why Log Everything:**
- Trend analysis (predict failures)
- Warranty claims (proof of maintenance)
- Resale value (well-maintained ship worth more)
- Troubleshooting (history helps diagnosis)
- Compliance (commercial vessels need records)

**Log Format:**
- Paper logbook (traditional, reliable)
- Digital log (searchable, backups important)
- Both (redundancy)

---

## SPARE PARTS TO STOCK

### Essential Spares (Always Have These):

**Consumables:**
- Life support filters (1 set)
- Reactor fuel canister (1 backup)
- Coolant (20L)
- Lubricants
- Electrical tape, wire, connectors

**Common Failure Items:**
- Fuses (assorted)
- Circuit breakers (common sizes for your ship)
- Emergency hull patches (12-pack)
- O-rings (assorted)
- Injector nozzles (2-4)

**Emergency:**
- Emergency masks (ensure all stations stocked)
- Fire extinguishers (charged and accessible)
- First aid supplies
- Emergency beacon batteries (backup)

**Total Investment:** 2,000-5,000 credits for basic spare parts inventory

---

## WHEN TO CALL A PROFESSIONAL

**You should seek professional help if:**
- Task is rated "Advanced" and you're not comfortable
- You don't have proper tools or parts
- Problem is beyond troubleshooting guides
- Safety is at risk
- Warranty work (DIY may void warranty)
- Certification required (annual inspections)

**No shame in calling for help. Professionals exist for a reason.**

---

## MAINTENANCE SCHEDULE SUMMARY

| Task | Frequency | Skill | Time |
|------|-----------|-------|------|
| Visual inspection | Daily | ⭐ | 10 min |
| Parameter logging | Daily | ⭐ | 5 min |
| Filter check | Weekly | ⭐ | 15 min |
| Coolant level check | Weekly | ⭐ | 5 min |
| Communication test | Weekly | ⭐ | 10 min |
| Injector cleaning | Monthly | ⭐⭐ | 45 min |
| Hull inspection (interior) | Monthly | ⭐⭐ | 30-60 min |
| Battery check | Monthly | ⭐ | 10 min |
| Magnetic calibration | Quarterly | ⭐⭐⭐ | 60 min |
| Coolant flush | Quarterly | ⭐⭐ | 2-3 hrs |
| Full diagnostic | Quarterly | ⭐⭐ | 2-3 hrs |
| Hull inspection (exterior) | Quarterly | ⭐⭐ | 60 min |
| Complete overhaul | Annually | ⭐⭐⭐ | 2-5 days |

---

## Related Documents

- **Preventive Maintenance Guide:** Complete maintenance schedules
- **PWR-SYS-003:** Reactor Maintenance Guide (detailed)
- **LIFE-SYS-003:** Life Support Maintenance (detailed)
- **Various KB Articles:** Specific troubleshooting and repair guides
- **Parts Catalog:** Part numbers and specifications

---

**MAINTENANCE IS NOT OPTIONAL. IT'S YOUR LIFE.**

**A well-maintained ship is a safe ship. A neglected ship is a coffin.**

**10 hours of maintenance prevents 100 hours of repairs.**

---

**Questions? Need detailed procedures? Consult full system manuals or contact ORSM Support 24/7.**
