# KB-189: Power Fluctuations and Electrical Instability

**Document ID:** KB-189
**System:** Power Distribution / Q-Core Reactor
**Severity:** CAUTION - WARNING
**Applies To:** All vessels with Q-Core reactor and power distribution systems
**Related Error Codes:** E-PWR-201, E-PWR-220, E-PWR-250, E-PWR-400
**Last Updated:** 2847.10.05

## Overview

Power fluctuations are variations in electrical power output or distribution that cause lights to flicker, equipment to behave erratically, or systems to reset unexpectedly. While often not immediately dangerous, power instability can damage equipment, interrupt critical operations, and indicate underlying problems that could escalate.

**Common Manifestations:**
- Lights dimming or flickering
- Equipment restarting randomly
- Display screens flickering or distorting
- Error messages appearing and clearing
- Power meters showing unstable readings
- Audible changes in equipment operation (humming, clicking)

**Frequency:**
- Minor fluctuations: Common, usually harmless (1-2% variance)
- Moderate fluctuations: Concerning, requires investigation (3-5% variance)
- Severe fluctuations: Immediate action needed (>5% variance or repeated)

## Understanding Power Fluctuations

### Normal vs. Problematic Fluctuations

**Normal (No Action Required):**
- <1% voltage variance during load changes
- Brief (<1 second) dip when large equipment starts
- Slight variation during reactor power adjustments
- These are compensated by voltage regulation systems

**Problematic (Investigate):**
- >3% voltage variance sustained
- Repeated fluctuations (multiple per minute)
- Random fluctuations with no apparent load change
- Progressive worsening over time

**Critical (Immediate Action):**
- >10% voltage swings
- Complete power dropouts (even momentary)
- Burning smell, sparking, smoke
- Multiple systems affected simultaneously

### Power System Basics

**Your ship's power path:**
```
Reactor Core → Power Conditioning → Distribution Bus → Circuit Breakers → Equipment
```

**Problems can occur at any point in this chain.**

## Common Causes and Diagnosis

### Cause 1: Reactor Output Instability

**Symptoms:**
- Fluctuations affect entire ship
- Power meters at main distribution show variation
- May be accompanied by reactor error codes (E-PWR-201, E-PWR-250)
- Correlates with reactor parameter changes

**Diagnosis:**
1. Check reactor output meter: Should be steady at set point
2. Check reactor core temperature: Should be stable (±50°C variation is normal, ±200°C is not)
3. Check plasma density: Should be steady
4. Check error logs for reactor faults
5. Monitor fuel pressure: Should be steady

**Common Reactor-Related Causes:**
- Contaminated fuel (see KB-167)
- Dirty or clogged fuel injectors
- Magnetic containment instability
- Control system malfunction
- Failing reactor sensors giving false readings

**Solutions:**
- Clean fuel injectors (monthly maintenance)
- Check fuel quality, replace if contaminated
- Calibrate reactor control system
- Check and replace failing sensors
- Run reactor diagnostic (PWR-SYS-004)
- If severe: Reactor may need professional servicing

**Time to Fix:** 1-4 hours for basic fixes; professional service if complex

---

### Cause 2: Power Conditioning Failure

**Symptoms:**
- Fluctuations affect entire ship OR specific zones
- Reactor output is stable but distribution is not
- Power conditioning unit (PCU) shows faults or warnings
- May hear unusual sounds from PCU (buzzing, clicking)

**Diagnosis:**
1. Check reactor output: Stable? (If yes, problem is downstream)
2. Check PCU status panel: Any error lights?
3. Check PCU output: Should be regulated 120V DC or 240V AC (depending on your system)
4. Monitor PCU temperature: Should be <70°C
5. Listen for unusual sounds from PCU

**Power Conditioning Unit (PCU):**
- Part #: PCU-STD-50KW (Scout/Small Freighter) or PCU-STD-150KW (Large Freighter)
- Cost: 3,000-8,000 credits
- Function: Converts/regulates reactor output to usable power
- Contains: Transformers, voltage regulators, filters, protection circuits

**Common PCU Problems:**
- Aging capacitors (typical lifespan: 10-15 years)
- Overheating from poor ventilation
- Component failure from power surges
- Dust/debris causing shorts
- Loose connections

**Solutions:**
- Check ventilation, clean dust from PCU
- Tighten all connections (power off first!)
- Replace aging capacitors (if comfortable with electronics)
- Replace entire PCU if multiple component failures
- Reset PCU (power cycle with proper procedure)

**Temporary Workaround:**
- Reduce total ship power consumption
- Bypass damaged zones if PCU has zone failures
- Run on backup battery for critical systems while repairing

**Time to Fix:** 2-8 hours depending on issue

---

### Cause 3: Overloaded Circuit

**Symptoms:**
- Fluctuations in specific area or systems only
- Occurs when certain equipment is running
- Circuit breaker may trip repeatedly
- Wiring may be warm to touch (CAUTION: Fire hazard)

**Diagnosis:**
1. Identify affected area/systems
2. Check circuit breaker panel: Any tripped or warm breakers?
3. Calculate load: Add up wattage of all equipment on circuit
4. Compare to circuit rating (usually marked on breaker)
5. Check for recently added equipment

**Circuit Capacity Examples:**
- **15A circuit @ 120V:** 1,800W maximum (safe load: 1,440W or 80%)
- **20A circuit @ 120V:** 2,400W maximum (safe load: 1,920W or 80%)
- **30A circuit @ 120V:** 3,600W maximum (safe load: 2,880W or 80%)

**Common Overload Scenarios:**
- Multiple high-power devices on one circuit (microwave + heater + power tools)
- Added equipment without considering circuit capacity
- Daisy-chained extension cords/power strips
- Equipment malfunction drawing excessive current

**Solutions:**
- Redistribute load: Move some equipment to different circuits
- Upgrade circuit: Install higher-rated breaker and wiring (requires electrical work)
- Replace equipment: More efficient alternatives
- Schedule usage: Don't run all high-power equipment simultaneously
- Remove daisy-chains: Direct connection to outlets only

**SAFETY WARNING:**
- Overloaded circuits are FIRE HAZARDS
- If wiring feels hot, shut off circuit immediately
- If you smell burning, shut off circuit and inspect
- Don't bypass circuit breakers or use higher-rated breakers without upgrading wiring

**Time to Fix:** 1-3 hours for load balancing; 4-8 hours for circuit upgrade

---

### Cause 4: Loose or Corroded Connections

**Symptoms:**
- Intermittent fluctuations
- May affect single device, multiple devices, or whole zones
- Worsens with vibration (during acceleration, rough maneuvering)
- May hear crackling or see sparking

**Diagnosis:**
1. **POWER OFF AFFECTED CIRCUIT FIRST**
2. Visual inspection of connections
3. Look for: Discoloration, corrosion, loose terminals, damaged insulation
4. Gently tug on wires to check security (power off!)
5. Use multimeter to check continuity

**Common Problem Areas:**
- Junction boxes (especially in high-vibration areas)
- Circuit breaker connections
- Equipment terminals
- Cable connectors that are frequently disconnected/reconnected

**Corrosion Risk Factors:**
- High humidity areas (near galley, head, life support)
- Temperature cycling (causes condensation)
- Age (ships >10 years more prone)
- Poor initial installation

**Solutions:**
- Clean corrosion: Use electrical contact cleaner and wire brush
- Tighten loose connections: Follow torque specifications
- Replace damaged terminals or connectors
- Apply anti-corrosion compound to connections
- Replace damaged wiring
- Improve environmental sealing in humid areas

**Prevention:**
- Annual inspection of electrical connections
- Apply dielectric grease to exposed connections
- Address humidity issues in ship
- Secure wiring properly to reduce vibration

**Time to Fix:** 1-4 hours depending on number and location of bad connections

---

### Cause 5: Failing Equipment Drawing Unstable Current

**Symptoms:**
- Fluctuations occur when specific equipment is running
- Equipment may behave erratically
- Equipment may be older or showing other signs of failure
- Circuit for that equipment may be overloading

**Diagnosis:**
1. Identify which equipment correlates with fluctuations
2. Isolate equipment: Run it alone on circuit
3. Monitor current draw: Should be steady and match specifications
4. Inspect equipment: Signs of damage, burning smell, unusual sounds?
5. Test with known-good equipment if possible

**Common Culprits:**
- Aging motors with worn bearings (erratic current draw)
- Failing power supplies in computers/electronics
- Damaged heaters with partial shorts
- Pumps with blocked impellers or failing seals

**Solutions:**
- Repair equipment if possible
- Replace failing equipment
- Disconnect equipment if not critical until repair possible
- May need professional diagnosis for complex equipment

**Time to Fix:** Varies by equipment

---

### Cause 6: Damaged Wiring

**Symptoms:**
- Intermittent fluctuations or complete power loss
- May worsen over time
- Visual damage may be visible (if accessible)
- May be localized to specific areas

**Diagnosis:**
1. Trace affected circuits
2. Visual inspection for: Damaged insulation, pinched wires, rodent damage, heat damage
3. Continuity testing with multimeter (power off!)
4. Insulation resistance testing (advanced)

**Common Damage Causes:**
- Crushing (cargo shifted, improper installation)
- Chafing (vibration against sharp edges)
- Overheating (from overload or poor connections)
- Age (insulation degrades over decades)
- Accidental damage during repairs

**Solutions:**
- Repair minor damage: Electrical tape, heat shrink tubing (temporary)
- Replace damaged section: Splice in new wire (proper connectors)
- Replace entire wire run: Safest for severe damage
- Re-route wiring: Away from damage sources

**SAFETY WARNING:**
- Damaged wiring can cause fires
- If insulation is compromised, risk of shorts and sparks
- Priority repair for any visible wire damage

**Time to Fix:** 2-6 hours depending on location and extent

---

## Systematic Diagnostic Procedure

**If you're experiencing power fluctuations and aren't sure of the cause:**

### Step 1: Characterize the Fluctuations (10 minutes)

**Answer these questions:**
1. Whole ship or specific area? (Whole = reactor/PCU; Specific = downstream)
2. Constant or intermittent? (Constant = steady problem; Intermittent = loose connection or triggered by load)
3. When do they occur? (Always, with certain equipment, during maneuvers, random)
4. How severe? (Minor annoyance to system shutdowns)
5. How long has it been happening? (Just started, days, weeks)
6. Did anything change recently? (New equipment, repairs, route changes)

**Your answers will point you toward likely causes.**

### Step 2: Check the Source (15 minutes)

**Check Reactor:**
- Reactor output meter reading: Stable?
- Reactor error codes: Any present?
- Core temperature, plasma density: Stable?

**If reactor is stable:**
- Problem is likely in power conditioning or distribution

**If reactor is unstable:**
- Address reactor issue first (see PWR-SYS-004)

### Step 3: Check Power Conditioning (15 minutes)

**Check PCU:**
- Status indicators: All green?
- Output voltage: Stable and correct value?
- Temperature: Normal (<70°C)?
- Sounds: Any unusual buzzing, clicking, humming?

**If PCU is fine:**
- Problem is in distribution or loads

**If PCU shows issues:**
- Address PCU (see Cause 2 above)

### Step 4: Check Distribution (30 minutes)

**Check Circuit Breakers:**
- Any tripped? (Reset and monitor)
- Any warm? (Indicates overload)
- Connections tight?

**Check Affected Circuits:**
- Calculate load vs. capacity
- Inspect connections in junction boxes
- Look for visible damage to wiring

### Step 5: Isolate Problem (30-60 minutes)

**Systematic Shutdown:**
1. Turn off all non-essential systems
2. Monitor: Do fluctuations stop?
3. If yes: Turn systems back on one by one
4. When fluctuations return: Last system turned on is likely the cause
5. Investigate that system specifically

**This process identifies problem equipment or circuits.**

### Step 6: Resolve (Time Varies)

- Address specific cause identified above
- Test thoroughly before considering resolved
- Monitor for 24 hours to confirm fix

## Emergency Procedures

### If Fluctuations Are Severe or Worsening

**Immediate Actions:**

1. **Reduce Load**
   - Turn off non-essential systems
   - Minimum load: Life support, basic propulsion, communications

2. **Isolate Problem If Possible**
   - If localized, trip breaker to affected area
   - Operate on remaining systems

3. **Monitor Critical Systems**
   - Life support status
   - Navigation/propulsion capability
   - Communications

4. **Prepare for Power Loss**
   - Charge batteries if possible
   - Ready emergency lighting
   - Prepare backup systems
   - Don EVA suits if decompression risk

5. **Call for Assistance**
   - If unsafe to continue
   - If unable to diagnose/fix
   - ORSM emergency support available 24/7

### If Complete Power Loss Occurs

**See emergency procedures for reactor shutdown and emergency power:**
- EMER-PROC-005: Reactor Emergency Procedures
- PWR-SYS-002: Emergency Restart Procedures
- Emergency battery power provides 4-12 hours (ship dependent)

## Prevention

### Regular Maintenance

**Monthly:**
- Visual inspection of electrical systems
- Check for loose connections
- Clean reactor fuel injectors
- Monitor power consumption trends

**Quarterly:**
- Thorough electrical connection inspection
- Clean PCU and check ventilation
- Check circuit breaker panel
- Calibrate power monitoring systems

**Annually:**
- Professional electrical system inspection
- Reactor comprehensive maintenance
- Replace aging components (capacitors, contactors)
- Update firmware on control systems

### Early Warning Signs

**Watch for these indicators of impending power issues:**
- Gradual increase in minor fluctuations
- New sounds from equipment (buzzing, humming)
- Breakers tripping more frequently
- Equipment behaving slightly erratically
- Reactor parameters drifting

**Address early signs immediately. Prevention is cheaper and safer than emergency repairs.**

## Tools and Parts to Keep On Board

### Diagnostic Tools:
- Multimeter (Part #: TOOL-MULTI-DIG) - 150 credits
- Clamp ammeter (Part #: TOOL-AMP-CLAMP) - 200 credits
- Non-contact voltage tester - 40 credits
- Inspection flashlight

### Repair Supplies:
- Electrical tape (proper spacecraft-rated)
- Heat shrink tubing (assorted sizes)
- Wire nuts / connectors
- Dielectric grease
- Contact cleaner
- Spare circuit breakers (common sizes for your ship)
- Spare wire (common gauges: 14AWG, 12AWG, 10AWG)

### Cost: ~800-1,200 credits for complete electrical repair kit

## When to Call for Professional Help

**Call ORSM Support or Local Electrician If:**
- You can't identify the source after systematic diagnosis
- Problem requires PCU replacement (complex)
- Problem requires major wiring work
- Reactor issues beyond basic maintenance
- Electrical fire has occurred (even if extinguished)
- You're not comfortable working with electrical systems

**Better to call for help than:**
- Risk electrical shock
- Cause electrical fire
- Damage expensive equipment
- Create bigger problem

## Cost Estimates

**Typical Repair Costs:**
- DIY connection tightening/cleaning: 0-50 credits (supplies)
- Circuit rebalancing: 0-200 credits (time)
- PCU component replacement: 500-1,500 credits (parts + labor)
- PCU full replacement: 3,000-8,000 credits
- Wiring repair/replacement: 200-2,000 credits depending on extent
- Professional diagnosis: 200-500 credits
- Reactor service: 2,000-10,000 credits depending on issue

**Cost of Ignoring the Problem:**
- Damaged equipment from unstable power: 1,000-50,000+ credits
- Electrical fire: Ship lost
- Reactor damage from instability: 10,000-100,000+ credits

**Prevention and early intervention are always cheaper.**

## Related Documents

- **PWR-SYS-001:** Q-Core Reactor Overview
- **PWR-SYS-002:** Reactor Startup and Shutdown Procedures
- **PWR-SYS-003:** Reactor Maintenance Guide
- **PWR-SYS-004:** Reactor Troubleshooting Manual
- **KB-167:** Contaminated Fuel Diagnosis
- **ERR-PWR:** Power System Error Codes Reference
- **EMER-PROC-005:** Reactor Emergency Procedures

## Frequently Asked Questions

**Q: Can power fluctuations damage my equipment?**
A: Yes. Modern electronics have some tolerance, but severe or repeated fluctuations can damage power supplies, corrupt data, and shorten equipment lifespan. Address fluctuations promptly.

**Q: Is it normal for lights to dim slightly when large equipment starts?**
A: Minor, brief (<1 second) dimming during startup of large motors or equipment is normal. If it's severe (>20% dimming) or sustained (>2 seconds), you have a problem.

**Q: My reactor output is stable but I still have fluctuations. Why?**
A: The problem is downstream from the reactor: power conditioning, distribution, wiring, or load issues. Follow the diagnostic procedure starting at Step 3.

**Q: Can I just install a bigger circuit breaker to stop it from tripping?**
A: NO. Circuit breakers protect the WIRING. Installing a higher-rated breaker without upgrading the wiring is a fire hazard. If a breaker trips repeatedly, you have an overload or short that must be fixed.

**Q: Should I stock spare PCU?**
A: For small ships, probably not (expensive). For commercial ships on long routes, consider it if you can afford it. At minimum, know where you can get one quickly.

**Q: How do I know if I should DIY or call for help?**
A: If you're comfortable with electrical basics, have proper tools, and can diagnose the issue, many fixes are DIY-able. If you're uncomfortable, the issue is complex, or involves high voltages/currents, call a professional. No shame in calling for help - better safe than sorry.

---

**BOTTOM LINE: Power fluctuations are usually fixable. Diagnose systematically, fix promptly, maintain regularly, and your electrical systems will serve you reliably.**

**Stable power = stable operations = safe ship.**
