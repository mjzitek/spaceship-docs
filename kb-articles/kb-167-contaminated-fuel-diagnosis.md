# KB-167: Contaminated Reactor Fuel Diagnosis and Response

**Document ID:** KB-167
**System:** Power Systems / Q-Core Reactor
**Severity:** WARNING - CRITICAL
**Applies To:** All Q-Core reactor models (Mark III, V, VII)
**Related Error Codes:** E-PWR-101, E-PWR-201, E-PWR-250, E-PWR-405
**Last Updated:** 2847.10.02

## Overview

Contaminated reactor fuel is a serious but often overlooked problem that can cause reactor performance issues, instability, and potential safety hazards. Contamination can occur during manufacturing, storage, handling, or from on-board system failures.

**Contamination Sources:**
- Moisture infiltration during storage or transfer
- Foreign particles (dust, metal shavings, organic material)
- Degraded canister seals allowing air exposure
- Cross-contamination from improper storage
- Manufacturing defects (rare but possible)
- Chemical breakdown from improper storage temperature

**Frequency:**
- **Rare** in properly maintained systems (1-2% of fuel issues)
- **More common** with discount/off-brand fuel sources (5-10%)
- **Increased risk** when refueling at small outpost stations with poor fuel handling

## Symptoms of Contaminated Fuel

### Performance Symptoms

**Primary Indicators:**
1. **Inconsistent Power Output**
   - Power fluctuates ±10% without control input
   - Cannot maintain steady state
   - Error: E-PWR-201 (Insufficient power output)

2. **Plasma Instability**
   - Plasma density varies erratically
   - Magnetic containment compensation working overtime
   - Error: E-PWR-250 (Plasma instability)

3. **Increased Fuel Consumption**
   - Consuming 20-40% more fuel than specifications
   - Fuel canister pressure drops faster than normal
   - Reach "refuel required" threshold much earlier

4. **Unusual Reactor Behavior During Startup**
   - Longer than normal startup time (>5 minutes extra)
   - Multiple failed startup attempts
   - Error: E-PWR-101 (Fuel system fault)

### Physical/Sensor Symptoms

1. **Temperature Irregularities**
   - Core temperature spikes and dips unpredictably
   - Temperature 100-300°C below expected for power level
   - Or sudden spikes with no corresponding power increase

2. **Pressure Anomalies**
   - Fuel canister pressure behaving strangely
   - Pressure drops in irregular patterns
   - Pressure higher or lower than expected for fuel level

3. **Radiation Fluctuations**
   - Radiation levels varying without cause
   - Unexpected radiation spikes during normal operation
   - Usually small (0.1-0.3 mSv/h variance) but noticeable

4. **Visual/Audible Changes**
   - Unusual humming or vibration from reactor
   - Magnetic coil activity lights flickering more than normal
   - Coolant pumps working harder (louder)

### Diagnostic Readings

**Check reactor diagnostic panel for:**
- Injector efficiency: <85% (normal is 90-95%)
- Plasma purity index: <92% (normal is 97-99%)
- Combustion efficiency: <80% (normal is 85-90%)
- Ash/residue buildup: Elevated (>5% higher than expected for runtime)

## Diagnostic Procedure

### Step 1: Confirm Contamination (15-30 minutes)

**Rule Out Other Causes First:**

Before assuming fuel contamination, verify:

1. **Injector Condition**
   - When was last cleaning? (Should be monthly)
   - Could be clogged injector, not bad fuel
   - Quick test: Manually cycle injectors, watch performance
   - If cleaning injectors resolves issue, fuel is probably OK

2. **Magnetic Coil Function**
   - Check all 12 coils (or 8 for Mark III)
   - Failing coil causes similar instability
   - Error code E-PWR-102 may accompany coil failure

3. **Coolant System**
   - Coolant level adequate? (Should be 92-98%)
   - Coolant quality OK? (Not degraded or contaminated itself)
   - Poor cooling can mimic fuel issues

4. **Control System Calibration**
   - Last calibration date?
   - Run diagnostic: "System → Reactor → Calibration Check"
   - Miscalibrated sensors give false readings

**If All Above Are Normal, Proceed with Fuel Testing:**

### Step 2: Fuel Canister Inspection (10 minutes)

**Visual Inspection:**

1. **Remove Current Fuel Canister**
   - SAFELY: Follow standard fuel change procedures (PWR-SYS-002)
   - Reduce reactor to standby first
   - Allow 5-minute cooldown
   - Depressurize fuel line
   - Remove canister

2. **Inspect Canister Exterior**
   - Check seals: Cracked? Damaged? Discolored?
   - Check pressure gauge: Should match expected level
   - Check temperature: Should be -250°C ±10°C
   - Look for frost or condensation (indicates seal leak)

3. **Check Manufacturing Date and Batch**
   - Fuel canisters have 5-year shelf life
   - Batch number on label: Record it
   - Check ORSM recall list if concerned

4. **Inspect Viewport (if equipped)**
   - Fuel should be clear/translucent with slight blue glow
   - Contaminated fuel may show:
     - Cloudiness or opacity
     - Particulate matter visible
     - Discoloration (brown, yellow, or dark)
     - Separation (if mixed with heavier elements)

### Step 3: Fuel Sample Testing (30-45 minutes)

**REQUIRES:** Fuel sampling kit (Part #: TEST-FUEL-Q)
**Cost:** 200 credits per kit (single use)
**Available:** Most stations, ORSM service centers

**Procedure:**

1. **Extract Sample**
   - Follow kit instructions exactly
   - Use provided sample valve adapter
   - Extract 5mL sample into test vial
   - Seal immediately

2. **Run Test Strips (included in kit)**

   **Test A: Moisture Content**
   - Insert moisture test strip
   - Wait 30 seconds
   - Compare color to chart
   - **Normal:** <0.1% moisture (light blue)
   - **Contaminated:** >0.5% moisture (dark blue to purple)

   **Test B: Particulate Count**
   - Insert filter paper into sample
   - Wait 60 seconds
   - Count visible particles on paper
   - **Normal:** 0-5 particles per sample
   - **Contaminated:** >20 particles per sample

   **Test C: Chemical Purity**
   - Add reagent A to sample (3 drops)
   - Shake gently
   - Observe color change
   - **Normal:** Clear or very light yellow
   - **Contaminated:** Orange, brown, or cloudy

   **Test D: Isotope Ratio**
   - Use included spectrometer attachment (if kit has one)
   - Or visual spectral test (basic kits)
   - D-T ratio should be 50:50 ±2%
   - **Normal:** 48-52% deuterium, 48-52% tritium
   - **Contaminated:** Ratio off by >5%, or other elements present

3. **Interpret Results**

   | Test Result | Interpretation | Action |
   |-------------|----------------|--------|
   | All tests normal | Fuel is OK | Look for other causes |
   | Moisture high | Water contamination | Discard fuel, check storage |
   | Particulates high | Physical contamination | Discard fuel, clean system |
   | Chemical impure | Manufacturing defect or mixing | Discard fuel, contact supplier |
   | Isotope ratio off | Wrong fuel type or degraded | Discard fuel, verify specifications |

### Step 4: System Contamination Check (30-60 minutes)

**If fuel is contaminated, the reactor internals may also be contaminated:**

1. **Inspect Fuel Injectors**
   - Remove injector assembly (Part #: INJ-FUEL-Q-MK[model])
   - Look for:
     - Residue buildup (brown/black deposits)
     - Clogged nozzles
     - Discoloration
   - Clean thoroughly with injector cleaning solvent (Part #: SOLV-INJ-Q)
   - Or replace if heavily contaminated

2. **Check Fuel Lines**
   - Inspect fuel line filters (Part #: FILT-FUEL-Q)
   - If clogged or discolored, replace
   - Flush fuel lines with inert gas (nitrogen recommended)

3. **Inspect Plasma Chamber (if accessible)**
   - This is advanced/optional
   - Requires reactor cooldown and partial disassembly
   - Look for unusual residue on chamber walls
   - May need professional cleaning

## Response Actions

### Immediate Actions (If Contamination Confirmed)

**1. Stop Using Contaminated Fuel**
- Switch to backup canister if available
- If no backup, operate on batteries/minimum power until resolved

**2. Quarantine Contaminated Canister**
- Label clearly: "CONTAMINATED - DO NOT USE"
- Store separately from good fuel
- Document: Batch number, supplier, date purchased

**3. Clean Reactor System**
- Clean or replace injectors
- Replace fuel filters
- Flush fuel lines
- See detailed cleaning procedure below

**4. Install Known-Good Fuel**
- Use fuel from reputable source
- Verify seal integrity before installation
- Test canister pressure and temperature
- Verify batch number is not on recall list

**5. Test Reactor Operation**
- Startup procedure per PWR-SYS-002
- Monitor closely for 2-3 hours
- Document performance improvement

### Detailed System Cleaning Procedure

**TIME REQUIRED:** 2-4 hours
**SKILL LEVEL:** Intermediate to Advanced
**REQUIRED TOOLS:** Basic tool kit, fuel system tools, cleaning supplies

**Step-by-Step:**

1. **Prepare Reactor**
   - Full shutdown (not just standby)
   - Cooldown: 30 minutes minimum
   - Remove contaminated fuel canister
   - Depressurize all fuel lines

2. **Remove and Clean Injectors** (45 minutes)
   - Remove injector assembly (4 bolts, disconnect fuel line)
   - Disassemble injectors (6 nozzles typically)
   - Soak in injector cleaning solvent for 15 minutes
   - Use injector cleaning brush (Part #: BRUSH-INJ-Q) to scrub
   - Rinse with isopropyl alcohol
   - Dry with compressed air
   - Inspect for damage; replace if needed
   - Reassemble and reinstall

3. **Replace Fuel Filters** (15 minutes)
   - Locate fuel line filters (usually 2: primary and secondary)
   - Disconnect fuel lines (wipe connections first)
   - Remove old filters
   - Install new filters (Part #: FILT-FUEL-Q)
   - Verify o-rings seated properly
   - Reconnect fuel lines, torque to spec (12 Nm)

4. **Flush Fuel Lines** (30 minutes)
   - Connect nitrogen purge kit (Part #: KIT-PURGE-FUEL)
   - Pressurize lines with nitrogen (30 PSI)
   - Open purge valves at both ends
   - Flush for 5 minutes
   - Repeat 3 times
   - Final flush: 10 minute duration
   - Seal lines

5. **Optional: Combustion Chamber Cleaning** (60+ minutes, advanced)
   - **Only if contamination was severe**
   - Requires partial reactor disassembly
   - Use chamber cleaning tool (Part #: TOOL-CHAMBER-CLEAN)
   - Follow chamber access procedure in PWR-SYS-003
   - Apply cleaning compound (Part #: CLEAN-CHAMBER-Q)
   - Scrub gently (do not damage chamber walls)
   - Vacuum out residue
   - Reassemble carefully

6. **System Verification**
   - Pressure test all fuel lines (150 PSI for 5 minutes, no drop)
   - Verify all connections tight
   - Install known-good fuel canister
   - Run startup checklist
   - Monitor first 3 hours of operation closely

## Prevention Strategies

### Fuel Purchasing Best Practices

**1. Source from Reputable Suppliers**
- Certified ORSM fuel vendors preferred
- Avoid "discount" or "economy" fuel unless absolutely necessary
- Check supplier reviews on spacer forums

**2. Inspect Before Purchase**
- Check seal integrity on every canister
- Verify manufacturing date (not older than 4 years)
- Check batch number against recall lists
- Verify part number matches your reactor model

**3. Test Sample (if possible)**
- Some stations allow test sampling
- Small stations may not have testing equipment
- Carry your own test kit if regularly visiting small outposts

### On-Board Storage Best Practices

**1. Proper Storage Environment**
- Temperature: -245 to -255°C (cryogenic storage)
- Pressure: Maintain canister external pressure (150-200 PSI)
- Location: Isolated from heat sources, vibration, radiation
- Orientation: Upright, labels visible

**2. Storage Container/Bay Requirements**
- Insulated fuel storage bay (most ships have this)
- Temperature monitoring (alarm if temp rises above -240°C)
- Separate from other cargo (especially organics, chemicals)
- Secure mounting (prevent impact damage)

**3. Rotation and Tracking**
- Use oldest fuel first (First In, First Out)
- Log fuel batch numbers and install dates
- Track consumption rates (helps identify contamination early)
- Inspect canisters monthly for seal integrity

### System Maintenance to Prevent Contamination Issues

**Monthly:**
- Clean fuel injectors (even if no issues)
- Inspect fuel line connections for leaks
- Check fuel filter condition

**Quarterly:**
- Replace fuel filters (proactive)
- Calibrate fuel system sensors
- Full diagnostic of fuel delivery system

**Annually:**
- Replace fuel lines (Part #: LINE-FUEL-Q-KIT)
- Replace all seals and o-rings in fuel system
- Professional inspection of combustion chamber

## Supplier Issues and Reporting

### If You Receive Bad Fuel

**1. Document Everything**
- Batch number, canister serial numbers
- Supplier name and location
- Purchase date and price
- Test results
- Photos of contamination if visible
- Reactor performance logs showing issue

**2. Contact Supplier**
- Report the issue
- Request refund/replacement
- Most reputable suppliers will honor this
- Keep records of communication

**3. Report to Authorities (if severe)**
- Outer Rim Fuel Safety Board (ORFSB)
- ORSM if fuel was branded as "ORSM Certified"
- Helps prevent others from receiving bad batches

**4. File Insurance Claim (if applicable)**
- Damage caused by bad fuel may be covered
- Cleaning costs, replacement parts
- Lost income from downtime
- Need documentation from steps above

### Known Problem Suppliers (Example)

*Note: This is fictional for the scenario*

- **RedLine Fuels (Theta Station):** Multiple contamination reports 2846-2847
- **Discount Fusion (various):** Moisture contamination issues, poor storage
- **Nova-Tek Generic:** Isotope ratio inconsistent, manufacturing QA issues

**Recommended Suppliers:**
- ORSM Certified dealers (official parts distributors)
- Atlas Energy Systems (major stations)
- CoreFuel Industries (certified, premium pricing)

## Cost Analysis

### Costs of Contaminated Fuel Issue

**Direct Costs:**
- Contaminated fuel (wasted): 800-2,400 credits per canister
- Fuel test kit: 200 credits
- Replacement fuel: 800-2,400 credits
- Cleaning supplies: 100-300 credits
- Replacement filters: 150 credits
- Replacement injectors (if needed): 600 credits

**Labor Costs (if not DIY):**
- Station service cleaning: 1,500-3,000 credits
- Professional chamber cleaning: 4,000-8,000 credits

**Indirect Costs:**
- Downtime (mission delays)
- Potential cargo penalties for late delivery
- Reduced reactor efficiency during contamination period
- Increased wear on reactor components

**Total:** 3,000-15,000 credits for a contamination event

### Prevention Investment

**Monthly:**
- Injector cleaning: 0 credits (DIY) or 200 credits (service)
- Fuel testing (if suspicious): 200 credits

**Quarterly:**
- Fuel filter replacement: 150 credits

**Annually:**
- Full fuel system service: 1,000-2,000 credits

**Total Prevention Cost:** ~1,500-3,000 credits/year

**ROI:** One contamination event costs more than a year of prevention. Prevention wins.

## Emergency Workarounds

### If You Have No Alternative Fuel Available

**Scenario:** You're in deep space, contaminated fuel, no replacement available.

**Options (in order of preference):**

**1. Battery/Reserve Power**
- Reduce to minimal power consumption
- Essential systems only (life support, basic propulsion)
- Can run 24-72 hours depending on ship size
- Navigate to nearest fuel source

**2. Filtered Operation**
- Install additional fuel filters in series (improvised)
- Run reactor at reduced power (60% max)
- Monitor constantly
- Increases injector clogging but may work short-term
- Clean injectors every 6-12 hours

**3. Dilution with Good Fuel**
- If you have small amount of good fuel, mix with contaminated
- Reduces contamination concentration
- 25% good / 75% contaminated may be workable
- Run at reduced power, monitor closely

**4. Call for Assistance**
- Emergency fuel delivery (expensive but available)
- Tow to nearest station (if you have no power)
- ORSM emergency support can arrange

## Frequently Asked Questions

**Q: Can I clean and reuse contaminated fuel?**
A: Generally no. Home filtration is not reliable. Contaminated fuel should be disposed of properly. Some specialized facilities can reprocess fuel, but it's expensive and usually not worth it.

**Q: How can I tell good fuel from bad before buying?**
A: Check seals, manufacturing date, batch number, and supplier reputation. Test sampling if possible. If it's suspiciously cheap, there's probably a reason.

**Q: Will contaminated fuel damage my reactor permanently?**
A: Usually no, if addressed promptly. Severe contamination left untreated can cause premature wear or damage to injectors and chamber. Clean system thoroughly and damage is usually minimal.

**Q: My fuel was fine yesterday, can it go bad that fast?**
A: Not usually. More likely: seal failed and contamination entered quickly, or contamination was present but symptoms just became noticeable. Check seal integrity.

**Q: Can I run my reactor on "80% pure" fuel?**
A: Not recommended. Reactor specifications require minimum 95% purity. Lower purity causes instability, inefficiency, and potential safety issues. Use proper fuel only.

**Q: Is expensive fuel worth it?**
A: Yes. Premium/certified fuel is more expensive (10-20% more) but worth it. Cheaper fuel risks contamination, poor performance, and expensive cleaning/repairs.

## Related Documents

- **PWR-SYS-001:** Q-Core Reactor Overview
- **PWR-SYS-002:** Reactor Startup and Shutdown Procedures
- **PWR-SYS-003:** Reactor Maintenance Guide
- **PWR-SYS-004:** Reactor Troubleshooting Manual
- **QR-PWR-001:** Q-Core Reactor Normal Parameters
- **ERR-PWR:** Power System Error Codes Reference
- **WARRANTY-POLICY:** Warranty exclusions include contaminated fuel damage

## Emergency Contacts

**ORSM Fuel Technical Support:**
- Can help diagnose fuel issues remotely
- 24/7 availability
- Can arrange emergency fuel delivery

**Outer Rim Fuel Safety Board:**
- Report contaminated fuel batches
- Safety recalls and advisories
- Consumer protection

---

**BOTTOM LINE: Buy good fuel from reputable sources. Your reactor will thank you. Your wallet will thank you. Your crew will thank you.**

**Don't be penny-wise and pound-foolish. Cheap fuel is expensive in the long run.**
