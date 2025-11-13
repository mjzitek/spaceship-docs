# Q-Core Reactor Troubleshooting Manual

**Document ID:** PWR-SYS-004
**Revision:** 3.8
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Purpose

This manual provides systematic troubleshooting procedures for Q-Core Reactor issues. Follow decision trees and diagnostic steps to identify and resolve common problems.

**When in doubt, contact Outer Rim Support.** Incorrect troubleshooting can worsen reactor problems or create safety hazards.

## General Troubleshooting Approach

1. **Identify symptoms**: What is the reactor doing (or not doing)?
2. **Check error codes**: Review control panel for specific error codes
3. **Verify parameters**: Compare current readings to normal operating ranges
4. **Follow decision tree**: Use appropriate troubleshooting flowchart
5. **Implement solution**: Apply recommended fix
6. **Verify resolution**: Confirm problem is resolved
7. **Document**: Log issue and solution in maintenance records

## Safety First

Before troubleshooting:

- Ensure adequate radiation protection
- Verify emergency shutdown accessible
- Have fire suppression ready
- Clear non-essential personnel from reactor compartment
- Notify crew of troubleshooting activities

## Problem Category Index

### Power Generation Issues
- [Reactor Won't Start](#reactor-wont-start)
- [Insufficient Power Output](#insufficient-power-output)
- [Power Fluctuations](#power-fluctuations)
- [Unexpected Shutdown](#unexpected-shutdown)

### Thermal Management Issues
- [Overheating](#overheating)
- [Temperature Fluctuations](#temperature-fluctuations)
- [Coolant System Problems](#coolant-system-problems)

### Plasma Containment Issues
- [Plasma Instability](#plasma-instability)
- [Magnetic Field Problems](#magnetic-field-problems)
- [Containment Warnings](#containment-warnings)

### Fuel System Issues
- [Fuel Injection Problems](#fuel-injection-problems)
- [High Fuel Consumption](#high-fuel-consumption)
- [Fuel Pressure Issues](#fuel-pressure-issues)

---

## Reactor Won't Start

### Symptoms
- Ignition sequence fails
- Plasma won't form or immediately dissipates
- Error code E-PWR-101 or E-PWR-102

### Diagnostic Steps

**Step 1: Check Prerequisites**

Verify all startup conditions met:
- [ ] Coolant level ≥ 85%
- [ ] Backup power available (≥ 5 kW)
- [ ] Fuel canisters installed and pressurized
- [ ] Magnetic containment energized
- [ ] No active error codes from previous operation

**Step 2: Test Fuel System**

1. Check fuel canister pressure gauge
   - Should read 150-200 PSI
   - If below 100 PSI: Replace fuel canister
   - If zero: Check fuel line connection

2. Verify fuel valve open
   - Visual check of valve position indicator
   - Should be in "OPEN" position
   - If closed, open valve and retry startup

3. Test injector operation
   - Access diagnostic menu: System > Fuel > Injector Test
   - Run "Dry Fire Test" (no fuel injection)
   - Listen for clicking sound (12 clicks in sequence)
   - If no clicks or irregular pattern: Injectors faulty, see [Fuel Injection Problems](#fuel-injection-problems)

**Step 3: Verify Magnetic Containment**

1. Check field strength reading
   - Should reach 4.5 Tesla during startup initialization
   - If below 4.0 Tesla: Magnetic coils may be damaged
   - Error code E-PWR-115 indicates coil failure

2. Test coil power supply
   - Measure voltage at coil terminals: Should be 380-420 VDC
   - If low voltage: Check power distribution from backup system
   - If no voltage: Coil power circuit breaker may be tripped

3. Inspect coil physical condition
   - Look for burn marks, discoloration
   - Check for unusual heat (coils should be cool before startup)
   - If coils damaged: Replacement required, contact ORSM service

**Step 4: Check Control System**

1. Verify control panel receives power
   - All indicator lights should illuminate
   - Display should show "READY FOR STARTUP"
   - If dark or flickering: Control board power issue

2. Reset control computer
   - Switch reactor main breaker OFF
   - Wait 30 seconds
   - Switch main breaker ON
   - Allow control system to boot (60 seconds)
   - Retry startup sequence

3. Check for software errors
   - Connect diagnostic tablet
   - Navigate to: System > Logs > Error History
   - Look for controller errors (E-PWR-300 series)
   - If software error: Update firmware or reset to factory defaults

**Step 5: Manual Diagnostic Test**

If automated startup still fails:

1. Enable manual mode on control panel
2. Manually energize magnetic containment to 4.5 Tesla
3. Manually open fuel valve and fire single injector pulse
4. Observe if plasma forms even briefly
   - If plasma forms but dissipates: Containment field issue
   - If no plasma forms: Fuel delivery or ignition system problem
   - If plasma forms and is stable: Automated control system issue

### Common Solutions

| Symptom | Likely Cause | Solution |
|---------|--------------|----------|
| E-PWR-101 error | Low fuel pressure | Replace fuel canister |
| E-PWR-102 error | Magnetic field failure | Check coil power supply, inspect coils |
| E-PWR-103 error | Coolant flow insufficient | Prime coolant pumps, check for blockages |
| Injectors don't fire | Clogged nozzles | Clean injectors (see PWR-SYS-003) |
| Plasma forms then dies | Weak magnetic field | Calibrate containment system |

---

## Insufficient Power Output

### Symptoms
- Reactor running but producing less than expected power
- Unable to bring reactor above 60-70% capacity
- Ship systems starved for power
- Error code E-PWR-201

### Diagnostic Steps

**Step 1: Verify Load Requirements**

1. Calculate actual power demand
   - Add up all active ship systems power draw
   - Compare to reactor current output
   - Ensure demand doesn't exceed reactor rating

2. Check for parasitic loads
   - Disable non-essential systems
   - Monitor if power output improves
   - Identify any systems drawing excessive power

**Step 2: Check Fuel Delivery**

1. Measure fuel consumption rate
   - Should match expected rate for power output level
   - Mark III: 0.4 kg/day at 60% power
   - Mark V: 1.2 kg/day at 60% power
   - Mark VII: 2.8 kg/day at 60% power

2. If consumption is low:
   - Check fuel injector operation (see Step 3)
   - Verify fuel canister pressure (150-200 PSI)
   - Inspect fuel lines for restrictions

3. If consumption is normal but power low:
   - Problem is in energy conversion, not fuel delivery
   - See Step 4 (thermal efficiency)

**Step 3: Inspect Fuel Injectors**

1. Monitor plasma density
   - Normal range: 3.5-4.2 g/cm³
   - If below 3.0 g/cm³: Insufficient fuel reaching chamber

2. Test individual injectors
   - Diagnostic menu: System > Fuel > Individual Injector Test
   - Each of 12 injectors tested separately
   - Verify consistent fuel spray pattern
   - Replace any failed injectors

3. Check for carbon buildup
   - Clogged injectors reduce fuel flow
   - Perform injector cleaning (see PWR-SYS-003)
   - May restore 10-15% power output

**Step 4: Assess Thermal Efficiency**

1. Check core temperature
   - Should be 1,800-2,400°C for standard operation
   - If below 1,800°C: Fusion reaction suboptimal
   - If above 2,400°C but power low: Cooling system removing too much heat

2. Inspect coolant system
   - Verify coolant flow rate matches reactor output level
   - Check coolant temperature differential (inlet vs outlet)
   - Normal differential: 80-120°C
   - If differential too high: Coolant flowing too fast, stealing heat
   - If differential too low: Coolant not extracting heat efficiently

3. Test thermoelectric converters
   - These convert thermal energy to electrical power
   - Diagnostic menu: System > Power > Converter Efficiency Test
   - Should show ≥ 85% efficiency
   - If below 80%: Converters degraded, replacement needed

**Step 5: Magnetic Containment Optimization**

1. Check field strength
   - Should be 6.0-7.5 Tesla during standard operation
   - If low: Increase field strength in 0.5 Tesla increments
   - Monitor power output after each adjustment

2. Verify field uniformity
   - Uneven field reduces fusion efficiency
   - Run field calibration (see PWR-SYS-003, Monthly Maintenance)
   - Calibration may restore 5-10% power output

3. Inspect for field distortions
   - Nearby magnetic equipment can interfere
   - Damaged coils create field irregularities
   - Use diagnostic tablet to map field geometry

### Solutions by Cause

**Dirty Injectors**
- Clean injectors per PWR-SYS-003
- Expected improvement: 10-15% power increase
- Time required: 2 hours

**Low Magnetic Field**
- Recalibrate containment system
- Increase field strength setting
- Expected improvement: 5-10% power increase
- Time required: 1 hour

**Degraded Converters**
- Replace thermoelectric converter modules
- Part #: TEC-QCR-series (model specific)
- Expected improvement: 20-25% power increase
- Time required: 6-8 hours

**Excessive Coolant Flow**
- Reduce coolant pump speed by 10-20%
- Monitor core temperature (must stay below 2,800°C)
- Expected improvement: 5-8% power increase

---

## Overheating

### Symptoms
- Core temperature exceeds 2,800°C
- Temperature rising rapidly
- Warning lights and alarms
- Error code E-PWR-220 or E-PWR-221

### IMMEDIATE ACTIONS

1. **Reduce reactor load immediately**
   - Decrease fuel injection rate by 30%
   - Increase coolant flow to maximum
   - Reduce power demand by shutting down non-essential systems

2. **Monitor temperature trend**
   - If temperature stabilizes: Continue reduced operation
   - If temperature continues rising: Prepare for emergency shutdown
   - If temperature exceeds 3,000°C: SCRAM immediately

3. **DO NOT** shut down coolant system while reactor is hot

### Diagnostic Steps

**Step 1: Check Coolant System**

1. Verify coolant flow
   - Pump should be operating
   - Flow indicator should show movement
   - If no flow: Check for pump failure or blockage

2. Check coolant level
   - Must be ≥ 85% capacity
   - If low: Top off immediately with emergency coolant supply
   - If critically low: May explain overheating

3. Inspect for coolant leaks
   - Look for wet spots, steam, or puddles
   - Check coolant pressure (should be 120-140 PSI)
   - If pressure dropping: Active leak present
   - Follow leak to source and repair

4. Verify coolant temperature
   - Inlet temperature should be 40-80°C
   - Outlet temperature should be 120-200°C
   - If outlet temp above 250°C: Coolant absorbing excessive heat

**Step 2: Check Heat Exchanger**

1. Verify heat exchanger operation
   - This radiates waste heat to space
   - Check radiator panels deployed (if retractable type)
   - Verify heat exchanger pump operating

2. Inspect for blockages
   - Coolant must flow freely through heat exchanger
   - Mineral buildup can reduce cooling efficiency
   - May require system flush (see PWR-SYS-003)

**Step 3: Assess Fusion Reaction**

1. Check if reactor operating above rated capacity
   - Verify power output level
   - If at 100% for extended period: Thermal overload possible
   - Reduce to 85% maximum for normal operation

2. Monitor plasma density
   - Excessive density increases heat generation
   - Normal range: 3.5-4.2 g/cm³
   - If above 5.0 g/cm³: Reduce fuel injection rate

3. Check magnetic containment efficiency
   - Weak field allows plasma to contact chamber walls
   - Creates hot spots and rapid heating
   - Increase field strength or recalibrate

**Step 4: Inspect Thermal Sensors**

1. Verify temperature readings accurate
   - Cross-check multiple temperature sensors
   - If sensors disagree significantly: One may be faulty
   - Replace suspect sensors

2. Test sensor calibration
   - Diagnostic menu: System > Sensors > Temperature Calibration
   - Run auto-calibration sequence
   - If calibration fails: Sensor replacement required

### Solutions by Cause

**Coolant Leak**
- Locate and repair leak
- Refill coolant system
- Purge air from lines
- Resume normal operation

**Coolant Pump Failure**
- Switch to backup coolant pump (if equipped)
- Or replace primary pump (Part #: PMP-COL-Q series)
- Verify flow restored before increasing reactor load

**Blocked Heat Exchanger**
- Perform coolant system flush
- Use descaling solution if mineral deposits present
- May require heat exchanger replacement if severely clogged

**Over-Fueling**
- Reduce fuel injection rate
- Decrease magnetic field slightly to reduce plasma density
- Operate at lower power output until situation resolved

**Damaged Containment Field**
- Recalibrate magnetic field
- Replace damaged coils if necessary
- May require reactor shutdown for repairs

---

## Plasma Instability

### Symptoms
- Plasma density fluctuating rapidly
- Core temperature swings ±200°C or more
- Power output oscillating
- Vibrations or unusual sounds from reactor
- Error codes E-PWR-250 through E-PWR-259

### DANGER

Unstable plasma can lead to containment breach. Take seriously.

### Immediate Actions

1. Reduce reactor to minimum stable output
2. Decrease fuel injection rate to half
3. Increase magnetic field strength by 0.5 Tesla
4. Monitor for stabilization (should occur within 2 minutes)
5. If instability continues: Initiate shutdown sequence

### Diagnostic Steps

**Step 1: Magnetic Field Analysis**

1. Check field strength uniformity
   - Use diagnostic tablet field mapping function
   - Field should be smooth and symmetrical
   - Irregularities indicate coil problems

2. Look for field fluctuations
   - Field should be stable within ±0.05 Tesla
   - If varying more than ±0.2 Tesla: Power supply issue or coil damage
   - Check error logs for E-PWR-115 (coil malfunction)

3. Verify all coils operating
   - There are 12 containment coils in standard configuration
   - Test each individually: Diagnostic > Magnetic > Coil Test
   - Failed coil creates asymmetric field = instability

**Step 2: Fuel Delivery Analysis**

1. Check injector consistency
   - All 12 injectors should fire at same rate
   - Irregular injection creates plasma density variations
   - Test injectors: System > Fuel > Injector Pattern Test

2. Verify fuel pressure stability
   - Pressure should be constant at 150-200 PSI
   - Fluctuating pressure = fluctuating fuel delivery
   - Check fuel canister regulator function

3. Inspect for fuel contamination
   - Impure fuel can cause erratic fusion
   - Check fuel quality certification on canister
   - If suspect contamination: Replace fuel canister

**Step 3: Resonance Check**

1. Measure reactor vibration frequency
   - Use vibration analyzer or diagnostic tablet
   - Normal vibration: 30-50 Hz, low amplitude
   - If vibration at 180-220 Hz: Resonance condition

2. Identify resonance source
   - Coolant pump speed can create resonance
   - Adjust pump speed ±10% to shift frequency
   - Magnetic field modulation can also cause resonance

3. Dampen vibrations
   - Check reactor mounting bolts torqued properly
   - Verify vibration dampeners not worn out
   - May need to replace mounting isolation system

**Step 4: External Interference**

1. Check for nearby electromagnetic sources
   - FTL drive charging can create interference
   - Shield generators operating near reactor
   - Communication array high-power transmission

2. Verify reactor shielding integrity
   - Electromagnetic shielding prevents external interference
   - Check shielding panels properly installed
   - Test shielding effectiveness with EM scanner

### Solutions by Cause

**Failed Magnetic Coil**
- Identify failed coil via diagnostic test
- Replace coil (Part #: MAG-COIL-Q series)
- Recalibrate magnetic containment system
- Downtime: 8-12 hours

**Irregular Fuel Injection**
- Clean or replace faulty injectors
- Verify fuel pressure regulator operating correctly
- Check fuel line filters not clogged

**Resonance Vibration**
- Adjust coolant pump speed to different operating point
- Install additional vibration dampers
- May require reactor remounting if mounts degraded

**Contaminated Fuel**
- Replace fuel canister with certified clean fuel
- Flush fuel lines
- Clean injectors to remove contaminant residue

---

## Fuel Injection Problems

### Symptoms
- Low plasma density despite adequate fuel supply
- Uneven power output
- Some injectors not firing
- Error codes E-PWR-180 through E-PWR-189

### Diagnostic Steps

**Step 1: Test All Injectors**

1. Access injector diagnostic mode
   - Diagnostic menu: System > Fuel > Individual Injector Test
2. Test each of 12 injectors sequentially
3. Record results:
   - PASS: Injector fires cleanly, pressure spike visible
   - FAIL: No response or weak response
   - INTERMITTENT: Sometimes fires, sometimes doesn't

**Step 2: Inspect Failed Injectors**

For each failed injector:

1. Check electrical connection
   - Verify connector firmly seated
   - Test voltage at injector terminal: Should be 24 VDC pulse
   - If no voltage: Wiring or control board issue

2. Remove and inspect injector nozzle
   - Look for carbon buildup on tip
   - Check nozzle opening not deformed or clogged
   - Measure nozzle opening: Should be 3.0mm ±0.1mm

3. Test injector mechanically
   - Remove from reactor
   - Manually trigger with test rig
   - Listen for clean click and observe fuel spray pattern
   - If mechanical failure: Replace injector

**Step 3: Check Fuel Supply to Injectors**

1. Verify fuel pressure at injector manifold
   - Should be 150-200 PSI
   - If low: Check fuel line from canister to manifold
   - Look for kinks, blockages, or leaks

2. Inspect fuel filters
   - Located between canister and manifold
   - Can become clogged with fuel contaminants
   - Replace if dirty or if pressure drop across filter >20 PSI

3. Test fuel valve operation
   - Main fuel valve should be fully open during operation
   - Partial closure reduces pressure
   - Verify valve actuator functioning

**Step 4: Examine Injector Control System**

1. Check control board output signals
   - Each injector has dedicated control channel
   - Use oscilloscope or diagnostic tablet to verify pulses
   - Pulse frequency should match fuel injection rate setting

2. Test control board processor
   - Diagnostic menu: System > Control > Processor Test
   - Verifies CPU, memory, I/O functions
   - If test fails: Control board replacement required

3. Update injector control firmware
   - Ensure latest version installed
   - Available from ORSM service portal
   - Some injection issues resolved by firmware updates

### Solutions by Cause

**Clogged Injector Nozzles**
- Clean per PWR-SYS-003 maintenance procedures
- Use 3mm titanium cleaning rods
- Replace O-rings when reinstalling
- Time required: 2 hours

**Damaged Injector**
- Replace injector (Part #: INJ-ASM-Q3/Q5/Q7)
- Torque to 15 Nm
- Test after installation
- Time required: 30 minutes per injector

**Fuel Filter Blockage**
- Replace fuel filters (Part #: FLT-FUL-30)
- Installed in pairs (primary and secondary)
- Always replace both simultaneously
- Time required: 45 minutes

**Low Fuel Pressure**
- Check fuel canister valve fully open
- Replace fuel pressure regulator if faulty (Part #: REG-FUL-200)
- Verify no leaks in fuel delivery system

**Control Board Failure**
- Replace injector control board (Part #: CTL-INJ-Q)
- Requires firmware installation after replacement
- Recalibrate injection timing
- Time required: 4 hours

---

## Error Code Quick Reference

For complete error code list, see ERR-PWR-100.

### Critical Errors (Immediate Action Required)

- **E-PWR-220**: Core temperature critical (>3,000°C) - SCRAM recommended
- **E-PWR-251**: Plasma containment failure imminent - SCRAM immediately
- **E-PWR-260**: Coolant loss detected - Emergency shutdown
- **E-PWR-270**: Radiation levels critical - Evacuate reactor compartment

### Warning Errors (Investigate Promptly)

- **E-PWR-101**: Startup failure - fuel system issue
- **E-PWR-102**: Startup failure - magnetic containment issue
- **E-PWR-115**: Magnetic coil malfunction
- **E-PWR-201**: Insufficient power output
- **E-PWR-221**: Core temperature elevated (>2,800°C)

### Advisory Errors (Monitor and Schedule Maintenance)

- **E-PWR-180**: Injector performance degraded
- **E-PWR-305**: Control system minor fault
- **E-PWR-350**: Coolant quality outside optimal range
- **E-PWR-400**: Routine maintenance due

## When to Contact Support

Contact Outer Rim Support if:

- Multiple troubleshooting attempts unsuccessful
- Error code not listed in documentation
- Problem intermittent and cannot be reproduced
- Repair requires parts not available on ship
- Safety concern about proceeding

**Support available 24/7** via emergency hotline or service portal.

## Related Documents

- PWR-SYS-001: Q-Core Reactor System Overview
- PWR-SYS-002: Q-Core Startup and Shutdown Procedures
- PWR-SYS-003: Q-Core Maintenance and Inspection Guide
- ERR-PWR-100: Power System Error Codes (Complete)
- EMERG-005: Reactor Emergency Procedures

---

**Remember:** When in doubt, shut it down. A delayed schedule is better than a damaged reactor or injured crew.
