# KB-078: Acceleration Coil Replacement Guide

**Category:** Navigation Systems - Sublight Propulsion
**Difficulty:** Advanced
**Est. Time to Resolve:** 4-8 hours per engine
**Last Updated:** 2847.09.14

## Issue Description

Electromagnetic acceleration coils in Model-3 Sublight Impeller have failed or degraded, causing reduced thrust output. Coils accelerate ionized plasma to generate thrust. When coils fail, thrust decreases proportionally. This guide covers testing, diagnosis, and replacement of failed coils.

## Background: Acceleration Coil Function

### How Coils Work

**Model-3 Sublight Impeller uses electromagnetic acceleration:**

1. **Fuel injection**: Deuterium injected into plasma chamber
2. **Plasma formation**: Fuel ionized by high voltage (becomes conductive plasma)
3. **Electromagnetic acceleration**: 24 coils arranged in series accelerate plasma
   - Each coil creates magnetic field
   - Plasma (conductive) pushed by magnetic field
   - Acceleration cumulative through 24 coil stages
4. **Exhaust**: Accelerated plasma exits through thrust nozzle

**Each coil contributes ~4% of total thrust:**
- 1 failed coil: ~4% thrust loss
- 2 failed coils: ~8% thrust loss
- 3 failed coils: ~12% thrust loss
- 6 failed coils: ~25% thrust loss (significant degradation)

### Coil Specifications (Model-3)

**Per Coil:**
- Coil current: 80-180 A (depending on thrust setting)
- Coil voltage: 400-800 VDC
- Magnetic field strength: 1.5-3.5 Tesla
- Coil resistance: 0.5-1.0 Ω (when healthy)
- Temperature: 60-80°C (normal operation)
- Weight: 12 kg each
- Lifespan: 3-5 years (50,000-100,000 hours) depending on use

**Per Engine:**
- Total coils: 24 coils arranged in 3 rings of 8 coils
- Total current: 80-180 A (coils in series, same current through all)
- Total voltage: 9,600-19,200 VDC across all 24 coils
- Power consumption: 10-50 kW per engine (depending on thrust setting)

## Symptoms of Failed or Degraded Coils

**Performance Symptoms:**
- Reduced thrust output (throttle 100% gives 75-95% thrust)
- Gradual thrust loss over months (as coils degrade with age)
- Sudden thrust loss (if coil fails catastrophically)
- Uneven thrust between multiple engines (if ship has 2-4 engines)

**Diagnostic Symptoms:**
- Error code E-NAV-102 (Low Thrust) or E-NAV-124 (Coil Failure)
- Coil diagnostic shows failed coil(s)
- High resistance in specific coil(s) (>1.5 Ω)
- No current through specific coil (infinite resistance, open circuit)
- Hot spot on specific coil (>100°C) during operation

## When to Suspect Coil Failure vs. Other Issues

**Suspect Coil Failure if:**
- Thrust loss gradual (weeks/months) - typical of coil degradation
- Single engine affected (if multi-engine ship) - coil failure localized
- Coil diagnostic identifies specific coil(s) failed
- Engine several years old (coils near end of life)
- Other systems (fuel, power, cooling) test normal

**Likely NOT Coil Failure if:**
- Thrust loss sudden (minutes/hours) - more likely fuel or injector issue
- All engines equally affected - system-wide issue (power, fuel, computer)
- Recent maintenance or impact - may be connector or alignment issue
- Engine new or recently serviced - coils should last years

**See related articles for alternative causes:**
- KB-045: Sublight Engines Low Thrust (comprehensive differential diagnosis)
- KB-015: Low Reactor Power Output (if power issue)
- KB-062: Fuel System Troubleshooting (if fuel quality issue)

## Diagnostic Procedure

### Step 1: Run Coil Diagnostic

**Access:** Engine Control Panel > Diagnostics > Propulsion > Coil Test

**What the test does:**
- Applies test current to each coil individually
- Measures:
  - Coil resistance (should be 0.5-1.0 Ω)
  - Current draw (should be proportional to voltage)
  - Magnetic field strength (measured by Hall effect sensors)
  - Temperature (should be uniform across all coils)

**Test Duration:** 10-15 minutes per engine

**Results Interpretation:**

| Parameter | Healthy Coil | Degraded Coil | Failed Coil |
|-----------|--------------|---------------|-------------|
| Resistance | 0.5-1.0 Ω | 1.0-1.5 Ω | >1.5 Ω or ∞ (open) |
| Current | 80-180 A | 50-79 A | 0 A (open) or >200 A (short) |
| Field Strength | 1.5-3.5 T | 0.8-1.4 T | 0 T (no field) |
| Temperature | 60-80°C | 80-120°C | Cold (no current) or >120°C (short) |

**Document results:**
- Note which coils failed (e.g., "Ring 2, Position 3" or "Coil #11")
- Note degraded coils (may fail soon, consider replacing proactively)

### Step 2: Visual Inspection (If Possible)

**Access to coils:**
- Requires removal of engine cowling (outer cover)
- Tools: 10mm hex driver, remove 12-24 bolts around cowling
- Coils visible once cowling removed

**Look for:**
- **Discoloration**: Blackened coil indicates overheating (insulation burned)
- **Physical damage**: Cracks, dents, impact damage
- **Loose mounting**: Coil vibrating loose from mounts
- **Burned connectors**: Electrical connection overheated or arced
- **Coolant leaks**: Coolant residue on coil (causes corrosion, failure)

**Document with photos** (for records, insurance if applicable)

### Step 3: Decision - Replace or Continue Operation?

**Replace immediately if:**
- 3+ coils failed (12%+ thrust loss)
- Safety-critical mission (need full thrust capability)
- Failed coil showing physical damage (fire hazard)
- Progressive failures (1 coil this week, another next week - indicates systemic issue)

**Can defer replacement if:**
- 1-2 coils failed (4-8% thrust loss, manageable)
- Not on time-critical mission
- Can reach port safely with reduced thrust
- No physical damage or safety concerns

**Consider replacing degraded coils proactively:**
- If coil resistance >1.2 Ω, likely to fail within 6-12 months
- Replacing now during scheduled maintenance cheaper than emergency replacement later
- "While you're in there" logic - cowling already removed, might as well replace degraded coils

## Parts and Tools Required

### Replacement Parts

**Per Coil:**
- Acceleration coil: Part #: ACC-COIL-M3-series (model-specific)
  - Cost: 400-800 credits each
  - Weight: 12 kg
  - Lead time: Usually in stock, 1-3 days if not
- Coil gasket/seal: Part #: GSK-COIL-M3 (if equipped)
  - Cost: 15-30 credits
- Thermal paste: Part #: PASTE-THERM-A (if coil heat sink)
  - Cost: 25 credits per tube

**Quantity:**
- Replace only failed coils (minimum)
- Replace failed + degraded coils (recommended)
- Replace all 24 coils (if engine old, preventive maintenance)

**Other Supplies:**
- Electrical contact cleaner (Part #: CLN-ELEC-A)
- Torque wrench lubricant (Part #: LUBE-BOLT-A)

### Tools Required

- **10mm hex driver** (remove cowling bolts)
- **8mm hex driver** (remove coil mounting bolts, 4 per coil)
- **Torque wrench** (12 Nm for coil bolts)
- **Multimeter** (verify continuity, resistance)
- **Thermal imaging camera** (optional, locate hot spots)
- **Lifting tool or hoist** (coils are 12 kg, awkward to handle)

### Safety Equipment

- **Lockout/tagout**: Ensure engine cannot start during work
- **Insulated gloves**: Coils may have stored charge
- **Safety glasses**: Metal fragments possible during removal

## Replacement Procedure

### Phase 1: Preparation (30 minutes)

1. **Shutdown engine completely:**
   - Engine panel: Shutdown
   - Wait for engine to cool (<100°C before touching)
   - Verify reactor not providing power to engine
   - Lockout/tagout: Ensure engine cannot be started

2. **Remove engine cowling:**
   - Locate cowling bolts (typically 12-24 around perimeter)
   - Remove bolts with 10mm hex driver
   - Lift cowling away (may be heavy, 20-40 kg)
   - Set aside safely

3. **Access coil compartment:**
   - Coils now visible
   - May need to remove additional panels to access specific coil
   - Take photos for reference (shows correct routing of wires)

4. **Discharge coils (safety):**
   - Even with power off, coils may hold charge
   - Use discharge tool (short coil terminals with resistor)
   - Or wait 10 minutes after power off for self-discharge

5. **Identify failed coil(s):**
   - Reference diagnostic results (e.g., "Ring 2, Position 3")
   - Locate on engine (may be numbered or use diagram)
   - Mark with tape or label (prevents replacing wrong coil)

### Phase 2: Remove Failed Coil (30-60 minutes per coil)

1. **Disconnect electrical:**
   - Each coil has 2 electrical connections (input and output in series)
   - Note which wire goes where (take photo or label wires)
   - Disconnect connectors:
     - Push-on connectors: Pull straight off
     - Bolted connectors: Remove bolt, lift wire off terminal
   - **IMPORTANT**: Do not mix up wires (reverses polarity, damages coil)

2. **Disconnect coolant (if liquid-cooled coils):**
   - Some coils have coolant loop for thermal management
   - Close isolation valves on coolant lines
   - Disconnect coolant lines from coil
   - Expect small amount of coolant spillage (have rag ready)

3. **Unbolt coil from mounting:**
   - Typically 4 bolts per coil (8mm hex)
   - May be difficult to access (tight space)
   - Use wobble extension or flex head wrench
   - Keep bolts (reuse if not damaged)

4. **Remove coil from engine:**
   - Coil may be wedged in place
   - Gently wiggle or pry (don't force)
   - Lift coil out (12 kg, use hoist or helper if needed)
   - Watch for sharp edges

5. **Inspect mounting location:**
   - Clean mounting surface (remove debris, old thermal paste)
   - Check for damage (cracks, corrosion)
   - Inspect electrical connections (corrosion, wear)

### Phase 3: Install New Coil (30-60 minutes per coil)

1. **Prepare new coil:**
   - Unbox and inspect (no shipping damage)
   - Verify part number correct
   - Check orientation (some coils have specific polarity/direction)
   - Apply thermal paste if coil has heat sink mounting

2. **Position new coil:**
   - Lower coil into mounting location
   - Align with bolt holes
   - Ensure coil seated fully (flush with mounting surface)

3. **Bolt coil to mounting:**
   - Install 4 bolts (hand-tighten first)
   - Then torque in cross pattern (prevents uneven pressure):
     - Torque sequence: 1, 3, 2, 4 (opposite corners)
   - Torque specification: 12 Nm
   - Verify coil doesn't move (firmly mounted)

4. **Reconnect electrical:**
   - Reference photo of original wiring
   - Connect input wire to input terminal
   - Connect output wire to output terminal
   - **Verify polarity**: Getting this wrong damages coil
   - Push-on connectors: Push firmly until click
   - Bolted connectors: Torque to 5 Nm

5. **Reconnect coolant (if applicable):**
   - Connect coolant lines to coil
   - Open isolation valves
   - Check for leaks (wipe dry, wait 5 min, check again)
   - Top off coolant if needed

6. **Double-check:**
   - All bolts tight?
   - All electrical connections secure?
   - No tools or parts left in engine?
   - Coil oriented correctly?

### Phase 4: Test and Calibration (60-90 minutes)

1. **Reinstall cowling:**
   - Position cowling over engine
   - Install bolts (hand-tight, then torque to 15 Nm)
   - Ensure all bolts installed (don't miss any)

2. **Remove lockout/tagout:**
   - Verify work area clear
   - Restore power to engine

3. **Run coil diagnostic:**
   - Access: Engine Control Panel > Diagnostics > Coil Test
   - Test all coils (including new ones)
   - **Verify new coil(s) test normal:**
     - Resistance: 0.5-1.0 Ω
     - Current: Appropriate for test voltage
     - Field strength: 1.5-3.5 T
     - Temperature: Should warm during test but not overheat

4. **Calibrate coil system:**
   - After replacement, magnetic field must be rebalanced
   - Access: Engine Control Panel > Propulsion > Coil Calibration
   - **Auto-calibration procedure:**
     - System energizes all coils at various levels
     - Measures field uniformity
     - Adjusts current distribution to equalize fields
     - Takes 15-20 minutes
     - Do not interrupt (will need to restart if interrupted)
   - **Result should show:** "Field uniformity >95%"
   - If <95%, may indicate installation issue (recheck connections)

5. **Static thrust test:**
   - With ship secured (docked or in stable orbit)
   - Increase throttle gradually: 10%, 20%, 40%, 70%, 100%
   - Verify thrust output matches throttle setting
   - Listen/feel for abnormal vibration or sounds
   - Monitor coil temperatures (should be uniform)

6. **Flight test (if possible):**
   - Conduct short maneuvering test
   - Verify full thrust available
   - Verify engine responds smoothly to throttle changes
   - Check for any anomalies

**If any issues during test:**
- Shut down immediately
- Recheck installation (connections, bolts, orientation)
- Run diagnostics again
- May need to remove and reinstall coil

### Phase 5: Documentation (15 minutes)

1. **Update maintenance log:**
   - Date and location of repair
   - Coils replaced (which ones, part numbers)
   - Test results (thrust output, calibration)
   - Technician name

2. **Update ship's inventory:**
   - Spare coils used (order replacements)
   - Parts consumed (gaskets, thermal paste, etc.)

3. **File warranty claim (if applicable):**
   - If coils failed prematurely (<2 years or <25,000 hours)
   - ORSM may cover under warranty
   - Need proof of failure (diagnostic report, photos)

## Multiple Coil Replacement

**If replacing multiple coils (common if engine old):**

**Efficient approach:**
1. Remove cowling (once)
2. Disconnect all electrical for coils being replaced
3. Remove all failed/degraded coils
4. Install all new coils
5. Reconnect all electrical
6. Reinstall cowling (once)
7. Test and calibrate

**Time saving:**
- Removing cowling once vs. multiple times saves 1-2 hours
- Can do in assembly-line fashion (remove all, then install all)

**Replacing all 24 coils (complete overhaul):**
- If engine >5 years old or >75,000 hours
- Prevents future failures (all coils same age)
- Time: 8-12 hours for all 24 coils
- Cost: 9,600-19,200 credits (24 coils × 400-800 credits each)
- Essentially remanufactures engine to like-new thrust performance

## Troubleshooting Installation Issues

### Issue: New Coil Tests as Failed

**Possible causes:**
1. **Wrong part number**: Coil not compatible with Model-3
   - Verify part number: ACC-COIL-M3-series
   - Some coils look similar but have different specs
2. **Reversed polarity**: Input/output swapped
   - Recheck wiring against photo/diagram
   - Swap if needed, retest
3. **Defective new coil**: Rare but possible
   - Test coil with multimeter (should measure 0.5-1.0 Ω between terminals)
   - If open (∞) or short (0 Ω), coil defective - return for replacement
4. **Poor electrical connection**: Connector not fully seated
   - Disconnect and reconnect firmly
   - Check for corrosion or damaged pins

### Issue: Calibration Fails (Field Uniformity <95%)

**Possible causes:**
1. **Mixed coil types**: If replacing multiple coils, all must be same model
   - Verify all coils same part number
2. **Mounting misalignment**: Coil not seated correctly
   - Recheck all coils firmly bolted, flush with mounting surface
3. **Computer glitch**: Calibration software error
   - Reboot engine control system, try calibration again
4. **Pre-existing damage**: Other coils (not replaced) may be degraded
   - Re-run diagnostics, may need to replace additional coils

### Issue: Abnormal Vibration or Noise After Replacement

**Possible causes:**
1. **Loose coil**: Not fully bolted down
   - Recheck torque on all bolts
2. **Foreign object**: Tool or part left in engine
   - Remove cowling, inspect thoroughly
3. **Coil hitting cowling**: Coil orientation wrong or cowling misaligned
   - Check clearances, realign cowling
4. **Unbalanced magnetic field**: Calibration needed
   - Run calibration procedure

## Cost-Benefit Analysis

### Cost of Replacement (DIY)

**Single coil:**
- Part: 400-800 credits
- Supplies: 50 credits (gaskets, paste, cleaner)
- Time: 4-6 hours
- **Total: 450-850 credits + time**

**Multiple coils (e.g., 6 coils):**
- Parts: 2,400-4,800 credits
- Supplies: 100 credits
- Time: 8-12 hours (not 6× longer, more efficient in batch)
- **Total: 2,500-4,900 credits + time**

**All 24 coils (complete overhaul):**
- Parts: 9,600-19,200 credits
- Supplies: 200 credits
- Time: 12-16 hours
- **Total: 9,800-19,400 credits + time**

### Cost of Professional Service

**Single coil:**
- Parts: 400-800 credits
- Labor: 800-1,200 credits (4-6 hours @ 200 credits/hour)
- **Total: 1,200-2,000 credits**

**All 24 coils:**
- Parts: 9,600-19,200 credits
- Labor: 2,400-3,200 credits (12-16 hours @ 200 credits/hour)
- **Total: 12,000-22,400 credits**

### Cost of NOT Replacing (Continued Operation with Failed Coils)

**Operational impact:**
- Reduced thrust = longer travel times = higher fuel cost
- May not be able to escape hazards (need full thrust for emergency maneuvers)
- Progressive failure (one coil fails, then another) = stranded risk
- Insurance may not cover incident if known deficiency not repaired

**Financial:**
- Deferred maintenance often more expensive later (cascading failures)
- Emergency repair more expensive than scheduled maintenance

**Recommendation:**
- If 1-2 coils failed: Can defer to scheduled maintenance if not safety-critical
- If 3+ coils failed: Replace soon (within weeks, not months)
- If engine >5 years old: Consider replacing all 24 coils proactively (overhaul)

## Warranty and Lifespan

**ORSM Warranty on Acceleration Coils:**
- **Standard warranty**: 2 years or 25,000 operating hours, whichever first
- **Extended warranty** (if purchased): 5 years or 75,000 hours
- **Warranty covers**: Manufacturing defects, premature failure
- **Warranty does NOT cover**: Normal wear, abuse, improper maintenance

**Expected Lifespan:**
- **Typical**: 3-5 years or 50,000-100,000 hours
- **Heavy use** (freight, long-haul): 2-3 years
- **Light use** (personal, short hops): 5-7 years
- **Aggressive operation** (frequent high-thrust, combat): 1-2 years

**Maintenance to Extend Lifespan:**
- Avoid prolonged full-thrust operation (run at 70-80% when possible)
- Keep cooling system maintained (prevents overheating)
- Annual coil inspection (catch degradation early)
- Proper shutdown procedures (gradual throttle-down, not instant off)

## Related Articles

- KB-045: Sublight Engines Producing Low Thrust
- KB-051: Sublight Engine Overheating
- KB-062: Fuel System Troubleshooting
- NAV-SUB-002: Sublight Engine Maintenance Guide

## Related Manuals

- NAV-SUB-001: Sublight Engine System Overview (includes coil theory)
- NAV-SUB-003: Sublight Engine Troubleshooting
- ERR-NAV-100: Sublight Propulsion Error Codes

---

**Support Note**: Acceleration coil replacement is ADVANCED repair. Walk customer through diagnostics to confirm coil failure first (not fuel, power, or other issue). If coils confirmed failed, assess customer skill level:
- **Experienced mechanic**: Can guide through replacement procedure
- **Moderate skill**: Recommend yard service unless very confident
- **No experience**: Strongly recommend professional service (easy to make costly mistakes)

Most coil failures are age-related. If engine >5 years old and multiple coils failing, recommend complete overhaul (replace all 24) rather than piecemeal replacement. Up-front cost higher but more economical long-term.

**Time estimate guidance**: First-time coil replacement: 6-8 hours. Experienced: 4-6 hours. Professional mechanic: 3-4 hours. Don't rush - improper installation causes more problems.
