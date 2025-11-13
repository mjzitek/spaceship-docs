# KB-045: Sublight Engines Producing Low Thrust

**Category:** Navigation Systems - Sublight Propulsion
**Difficulty:** Intermediate
**Est. Time to Resolve:** 30-90 minutes
**Last Updated:** 2847.09.14

## Issue Description

Customer reports Model-3 Sublight Impeller producing less thrust than commanded. Throttle set to 70-100% but actual thrust output significantly lower, resulting in poor acceleration and extended travel times.

## Symptoms

- Throttle indicator shows 70-100% but thrust gauge shows 40-60%
- Slower acceleration than normal
- Extended time to reach destination
- Ship feels "sluggish" during maneuvers
- Error code E-NAV-102 may be displayed

## Quick Diagnostic Questions

Ask the customer:

1. **"What's your throttle setting and what thrust percentage are you actually getting?"**
   - Quantify the gap (e.g., 80% throttle → 50% thrust = 30% loss)
   - Helps identify severity

2. **"Is this affecting all engines equally, or just one?"**
   - Single engine: Specific engine problem
   - All engines: System-wide issue (fuel, power, etc.)
   - Dual/quad config: Compare engine performance

3. **"What's your plasma chamber temperature?"**
   - Should be 600-900°C at standard thrust
   - If low: Insufficient fuel or power
   - If high: Possible cooling issue or efficiency problem

4. **"How long has this been occurring?"**
   - Gradual: Likely maintenance issue (clogged injectors, worn coils)
   - Sudden: Possible component failure or fuel problem
   - Since last maintenance: Check recent work done

5. **"Any recent changes? New fuel source? Maintenance performed?"**
   - Contaminated fuel from new supplier
   - Incorrectly performed maintenance
   - Damaged components during service

## Common Solutions

### Solution A: Clogged Fuel Injectors (Most Common - 40% of cases)

**Cause**: Carbon buildup on injector nozzles restricts fuel flow to plasma chamber.

**Symptoms Specific to This Cause:**
- Gradual thrust loss over weeks/months
- Uneven exhaust pattern (if visible)
- Plasma chamber temperature lower than expected
- All engines affected equally (if all overdue for cleaning)

**Resolution Steps:**

1. **Check Last Injector Cleaning**
   - Review maintenance logs
   - Should be cleaned monthly
   - If overdue (>6 weeks): Almost certainly the cause

2. **Run Injector Diagnostic**
   - Engine control panel: Diagnostics > Fuel System > Injector Test
   - System tests each of 12 injectors
   - Look for:
     - Weak spray pattern
     - Pressure drop across injectors
     - Uneven fuel distribution

3. **Clean Injectors**
   - Shutdown engine (must be cool, <200°C)
   - Remove injector assembly (Part location: plasma chamber access panel)
   - Use 3mm titanium cleaning rods (Part #: CLN-ROD-TI-3MM)
   - Push through each nozzle to remove carbon deposits
   - Inspect nozzles with magnification (should be perfectly circular, 3.0mm ±0.1mm)
   - If nozzle deformed or damaged, replace injector (Part #: INJ-ASM-M3)

4. **Reinstall and Test**
   - Replace injector O-rings (Part #: ORG-INJ-12) - ALWAYS replace when servicing
   - Torque mounting bolts to 15 Nm
   - Restart engine in standby mode
   - Test fire injectors (should see smooth plasma stream)
   - Gradually increase to full thrust
   - Verify thrust output matches throttle setting

**Expected Result:** Thrust restored to 90-100% of rated output. May see 10-15% improvement.

**Time Required:** 2-3 hours (all engines)

**If Unresolved:** Injectors may be permanently damaged (replace) or issue is elsewhere.

---

### Solution B: Degraded Acceleration Coils

**Cause**: Electromagnetic acceleration coils weakened due to age or damage, cannot accelerate plasma to full velocity.

**Symptoms Specific to This Cause:**
- Thrust loss gradual over months/years
- Coil current normal but exhaust velocity reduced
- May hear buzzing or humming from coils
- Thermal imaging shows coils running hotter than normal

**Resolution Steps:**

1. **Test Coil Performance**
   - Access: Diagnostics > Propulsion > Coil Test
   - System measures each of 24 coils per engine
   - Check for:
     - Coil current: Should be 80-180 A depending on thrust setting
     - Magnetic field strength: Should be proportional to current
     - Coil resistance: Should be 0.5-1.0 Ω per coil
     - Temperature: Should be 60-80°C at standard operation

2. **Identify Failed/Degraded Coils**
   - Failed: No current, infinite resistance, cold
   - Degraded: High resistance (>1.5 Ω), hotter than others, weak field

3. **Calculate Impact**
   - Single coil failure: ~4% thrust loss (24 coils total)
   - Two coils: ~8% loss
   - Three or more: ~12-15% loss
   - If customer reporting 20-30% loss, coils likely not sole cause

4. **Replace Failed Coils**
   - Shutdown engine completely
   - Access coil compartment (requires removal of engine cowling)
   - Disconnect failed coil(s) electrically
   - Unbolt from mounting (4 bolts per coil, 8mm hex)
   - Install replacement coil (Part #: ACC-COIL-M3-series)
   - Reconnect electrical
   - Torque bolts to 12 Nm

5. **Recalibrate Coil System**
   - After replacement, system must rebalance magnetic field
   - Access: Diagnostics > Propulsion > Coil Calibration
   - Run auto-calibration (takes 15-20 minutes)
   - Verify field uniformity >95%

**Expected Result:** Thrust improves by approximately 4% per replaced coil.

**Time Required:** 4-6 hours (includes cowling removal, calibration)

**Preventive Maintenance:** Coils typically last 3-5 years. Replace proactively if testing shows degradation.

---

### Solution C: Fuel Quality Issues

**Cause**: Contaminated or incorrect deuterium fuel causing inefficient plasma formation.

**Symptoms Specific to This Cause:**
- Sudden thrust loss (coincides with refueling)
- Fuel pressure normal but plasma density low
- Unusual exhaust color (should be blue-white, not yellow/orange)
- May have rough running or vibration

**Resolution Steps:**

1. **Check Fuel Source**
   - When was last refueling?
   - New fuel supplier or station?
   - Fuel grade correct? (Should be 99.8% pure deuterium)

2. **Test Fuel Quality**
   - Extract sample from fuel tank (10ml sample)
   - Use fuel purity tester (if available) or:
   - Send sample to testing facility at port
   - Contamination types:
     - Water (reduces combustion efficiency)
     - Heavy hydrogen isotopes (incorrect fuel)
     - Hydrocarbons (from contaminated storage tanks)

3. **If Fuel Contaminated:**
   - **Do NOT continue operations** with bad fuel
   - Drain fuel tank completely
   - Flush fuel system with clean deuterium (50-100 liters)
   - Clean fuel filters (Part #: FLT-FUL-M3)
   - Refill with certified pure fuel
   - Prime fuel system (purge air)

4. **Clean Injectors and Combustion Chamber**
   - Contaminated fuel leaves deposits
   - Follow injector cleaning procedure (Solution A above)
   - May need to clean plasma chamber interior:
     - Access through inspection port
     - Use soft brush and approved cleaning solvent
     - Do not use abrasives (damage chamber lining)

**Expected Result:** Thrust restored to normal after clean fuel installed and system cleaned.

**Cost Consideration:**
- May be able to return contaminated fuel for refund
- Document fuel quality issues for insurance/legal purposes
- Report to station authority (they may have bad batch affecting others)

**Prevention:**
- Only refuel at reputable stations
- Request fuel certification before accepting delivery
- Keep fuel testing kit aboard for spot checks

---

### Solution D: Insufficient Power Supply

**Cause**: Q-Core reactor not providing adequate power to engines.

**Symptoms Specific to This Cause:**
- All engines equally affected
- Reactor output indicator showing <60%
- Other ship systems also degraded
- May have reactor error codes

**Resolution Steps:**

1. **Check Reactor Output**
   - View Q-Core control panel
   - Current output: Should be 60-85% for normal flight operations
   - If <60%: Reactor issue, not engine issue

2. **Verify Power Demand**
   - Calculate total ship power demand:
     - Sublight engines: 10-50 kW per engine at full thrust
     - Life support: 8-15 kW
     - Other systems: 5-20 kW
   - Total should not exceed reactor capacity

3. **If Reactor Output Low:**
   - Refer customer to KB-015 (Low Reactor Power Output)
   - Common reactor issues:
     - Clogged fuel injectors (reactor, not engine)
     - Degraded thermoelectric converters
     - Low magnetic field strength
   - Fix reactor issue first, engine thrust should return to normal

4. **If Reactor Adequate but Power Not Reaching Engines:**
   - Check power distribution panel
   - Verify circuit breakers not tripped
   - Check voltage at engine power input: Should be 380-420 VDC
   - If low voltage: Power transmission issue (wiring, breakers, relays)

**Expected Result:** Once reactor restored to adequate output, engine thrust returns to normal.

**Escalate:** If reactor issue cannot be quickly resolved, customer should use reduced thrust and proceed to port for reactor service.

---

### Solution E: Exhaust Nozzle Blockage or Damage

**Cause**: Thrust nozzle partially blocked by debris or damaged, restricting exhaust flow.

**Symptoms Specific to This Cause:**
- Single engine affected (if one nozzle blocked)
- Visible damage or obstruction to nozzle
- Abnormal exhaust pattern
- May have impacted debris recently

**Resolution Steps:**

1. **Visual Inspection of Nozzle**
   - External inspection (if docked or safe to EVA)
   - Look for:
     - Debris lodged in nozzle
     - Dents or deformation
     - Cracks or burn-through
     - Discoloration indicating overheating

2. **Internal Inspection**
   - Access from engine compartment (rear access panel)
   - Look up into nozzle throat
   - Check for carbon buildup, foreign objects
   - Verify nozzle throat diameter (should be 200-400mm depending on engine size)

3. **Clear Blockage**
   - If debris: Remove with long tools (do not enter nozzle)
   - If carbon buildup: Clean with wire brush and solvent
   - Flush with compressed air

4. **Repair Damage**
   - Minor dents: May not affect performance significantly
   - Cracks: Require nozzle replacement (Part #: NOZ-EXH-M3-series)
   - Burn-through: Immediate replacement required (safety hazard)

5. **Nozzle Replacement** (if required):
   - Shutdown engine, allow to cool (< 100°C)
   - Disconnect thrust vectoring hydraulics
   - Unbolt nozzle assembly (12 bolts, 15mm hex)
   - Remove old nozzle and gasket
   - Install new gasket (Part #: GSK-NOZ-M3)
   - Install new nozzle
   - Torque bolts to 80 Nm in star pattern
   - Reconnect hydraulics
   - Test thrust vectoring before flight

**Expected Result:** Thrust restored to normal for affected engine.

**Time Required:**
- Clearing blockage: 30 minutes
- Nozzle replacement: 3-4 hours

---

### Solution F: Coolant System Inefficiency

**Cause**: Engine running too hot due to coolant issues, automatic thermal limiter reducing thrust.

**Symptoms Specific to This Cause:**
- Plasma chamber temperature elevated (>1,200°C at standard thrust)
- Thrust automatically reduces when temperature hits 1,400°C
- Coolant temperature higher than normal
- May see E-NAV-115 (coolant system malfunction)

**Resolution Steps:**

1. **Check Coolant Level**
   - View coolant reservoir sight glass
   - Should be 85-100% full
   - If low: Top off with approved coolant
   - If very low: Check for leaks

2. **Verify Coolant Flow**
   - Check coolant pumps running (should hear pump motor)
   - Verify coolant flow rate appropriate for thrust level:
     - Standby: 5 L/min
     - Standard (40-70%): 25-40 L/min
     - Maximum (70-100%): 60-80 L/min
   - If flow low: Pump degradation or blockage

3. **Check Heat Exchanger**
   - Heat exchanger radiates waste heat to space
   - Verify radiator panels deployed (if retractable type)
   - Check for micrometeorite damage to radiator fins
   - Ensure heat exchanger coolant flow not blocked

4. **Test Coolant Pump**
   - Access: Diagnostics > Cooling > Pump Test
   - Pump should produce rated pressure and flow
   - If degraded: Replace pump (Part #: PMP-COL-M3)

5. **Increase Cooling Capacity** (temporary workaround):
   - Increase coolant flow rate 10-20% above standard
   - May allow higher thrust before thermal limiter activates
   - Monitor temperature carefully
   - Plan permanent repair (pump replacement, heat exchanger cleaning)

**Expected Result:** With adequate cooling, thermal limiter no longer restricts thrust.

**Time Required:**
- Top off coolant: 15 minutes
- Pump replacement: 4-6 hours

---

## Escalation Criteria

Escalate to Level 2 support if:

- Multiple solutions attempted without improvement
- Customer reports recent collision or combat damage
- Thrust loss exceeds 50% (may indicate major component failure)
- Error codes other than E-NAV-102 or E-NAV-115
- Customer uncomfortable performing diagnostic procedures
- Structural damage to engine suspected

## Prevention Tips

Share with customer to prevent future issues:

- **Monthly injector cleaning**: Single most important maintenance item
- **Use quality fuel**: Only refuel at reputable stations, test quality
- **Monitor temperatures**: Elevated temps early indicator of problems
- **Annual coil inspection**: Replace before they fail
- **Keep spares**: Stock injector assemblies, coils, O-rings
- **Clean exhaust nozzles**: Every 6 months, check for carbon buildup
- **Coolant maintenance**: Check level weekly, flush system annually

## Multiple Concurrent Issues

Often low thrust caused by combination of factors:

**Example:** Customer has 35% thrust loss
- Clogged injectors: 15% loss
- Two failed coils: 8% loss
- Contaminated fuel: 10% loss
- Minor coolant inefficiency: 2% loss
- **Total: 35% loss**

**Strategy:**
- Address issues in order of ease/impact
- Cleaning injectors quick and often yields biggest improvement
- After each fix, retest to see if additional work needed

## Related Articles

- KB-015: Low Reactor Power Output
- KB-051: Sublight Engine Overheating
- KB-062: Fuel System Troubleshooting
- KB-078: Acceleration Coil Replacement Guide

## Related Manuals

- NAV-SUB-001: Sublight Engine System Overview
- NAV-SUB-002: Sublight Engine Maintenance Guide
- NAV-SUB-003: Sublight Engine Troubleshooting
- ERR-NAV-100: Sublight Propulsion Error Codes

---

**Support Note**: Clogged injectors cause 40% of low thrust calls. Always ask about last injector cleaning first. If overdue, recommend cleaning before investigating other causes. Can often resolve issue in 2 hours instead of spending all day chasing complex diagnostics.
