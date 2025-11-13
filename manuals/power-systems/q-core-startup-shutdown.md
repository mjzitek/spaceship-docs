# Q-Core Reactor Startup and Shutdown Procedures

**Document ID:** PWR-SYS-002
**Revision:** 3.1
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document outlines standard procedures for safe startup and shutdown of Q-Core Reactor systems. These procedures apply to all Q-Core models (Mark III, V, and VII) unless otherwise noted.

**CRITICAL**: Improper startup or shutdown can result in plasma instability, containment breach, or reactor damage. Follow all steps in sequence.

## Pre-Startup Checklist

Before initiating reactor startup, verify:

- [ ] Coolant system filled to minimum 85% capacity
- [ ] Magnetic containment coils energized and stable
- [ ] Fuel pellet canisters installed and sealed
- [ ] Radiation shielding integrity at 100%
- [ ] Emergency shutdown systems functional
- [ ] Backup power available for startup sequence
- [ ] All maintenance locks and safety tags removed
- [ ] Cooling vents clear of obstructions
- [ ] Crew notified of impending reactor activation

## Standard Startup Procedure (Cold Start)

**Duration:** Approximately 12-18 minutes
**Power Required:** External or battery backup (minimum 5 kW)

### Phase 1: System Initialization (0-3 minutes)

1. **Enable Reactor Control Panel**
   - Switch main breaker to ON position
   - Verify all status indicators illuminate
   - Confirm diagnostic display shows "READY FOR STARTUP"

2. **Activate Coolant Circulation**
   - Open primary coolant valve
   - Start coolant pumps at 30% flow rate
   - Verify coolant temperature below 40°C
   - Monitor for leaks or pressure anomalies

3. **Energize Magnetic Containment**
   - Initialize superconducting magnets
   - Ramp field strength from 0 to 4.5 Tesla over 90 seconds
   - Confirm field stability within ±0.1 Tesla variance
   - Monitor coil temperature (should remain below 80°C)

### Phase 2: Plasma Ignition (3-8 minutes)

4. **Prepare Fuel Injection System**
   - Verify fuel canister pressure (should read 150-200 PSI)
   - Prime plasma injectors
   - Set initial injection rate to minimum (0.1 pellets/second)

5. **Initiate Fusion Reaction**
   - Press "IGNITION" button on control panel
   - Injectors will fire startup sequence automatically
   - Plasma temperature will rise from ambient to 800°C in 60 seconds
   - Monitor plasma density (target: 2.0-2.5 g/cm³)

6. **Stabilize Initial Fusion**
   - Increase magnetic field to 5.5 Tesla
   - Adjust fuel injection to 0.3 pellets/second
   - Core temperature should reach 1,200°C
   - Power output will begin at approximately 5-10% capacity

### Phase 3: Ramp to Operating Power (8-15 minutes)

7. **Gradual Power Increase**
   - Increase coolant flow to 60% pump capacity
   - Ramp magnetic field to 6.5 Tesla
   - Increase fuel injection to 0.8 pellets/second
   - Monitor core temperature rise (should not exceed 200°C per minute)

8. **Reach Standard Operating Mode**
   - Target core temperature: 1,800-2,000°C
   - Target plasma density: 3.5-4.0 g/cm³
   - Target power output: 60-70% capacity
   - Magnetic field: 6.0-7.0 Tesla

9. **Final System Checks**
   - Verify all parameters within normal range
   - Check for unusual vibrations or sounds
   - Confirm power distribution to all ship systems
   - Log startup completion in ship's record

**Startup Complete**: Reactor is now in Standard Operation mode.

## Quick Startup Procedure (Hot Start)

If reactor has been in Standby Mode (not fully shut down), startup is faster:

**Duration:** 3-5 minutes

1. Verify reactor is in Standby Mode (10% power output)
2. Increase coolant flow from 20% to 60%
3. Ramp magnetic field from 4.5 to 6.5 Tesla over 2 minutes
4. Increase fuel injection from standby rate to standard operation
5. Monitor temperature rise and power output increase
6. Confirm parameters reach normal operating range

## Standard Shutdown Procedure (to Full Stop)

**Duration:** Approximately 15-25 minutes

### Phase 1: Power Reduction (0-5 minutes)

1. **Notify Crew**
   - Announce reactor shutdown over ship-wide comm
   - Ensure all non-essential systems powered down
   - Verify backup power systems online

2. **Reduce Power Output**
   - Decrease fuel injection rate by 50%
   - Reduce magnetic field strength to 5.0 Tesla
   - Allow core temperature to drop below 2,000°C
   - Power output should decrease to 30-40% capacity

### Phase 2: Plasma Shutdown (5-12 minutes)

3. **Terminate Fusion Reaction**
   - Cease fuel pellet injection completely
   - Maintain magnetic containment at 5.0 Tesla
   - Allow residual plasma to decay naturally
   - Core temperature will drop to 1,000°C over 4-6 minutes

4. **Coolant Stabilization**
   - Maintain coolant flow at 60% until core drops below 800°C
   - Monitor coolant temperature (should not exceed 180°C)
   - Prevent thermal shock by controlling cooling rate

### Phase 3: System Deactivation (12-25 minutes)

5. **Deactivate Magnetic Containment**
   - Once core temperature below 500°C, begin field reduction
   - Decrease magnetic field from 5.0 to 0 Tesla over 3 minutes
   - Monitor for any residual plasma (should be zero)

6. **Coolant System Shutdown**
   - Continue coolant circulation until core reaches 200°C
   - Reduce pump speed gradually to zero
   - Close coolant valves
   - Allow system to equalize to ambient temperature

7. **Final Deactivation**
   - Power down reactor control panel
   - Switch main breaker to OFF position
   - Engage maintenance locks if reactor will be offline extended period
   - Log shutdown completion in ship's record

**Shutdown Complete**: Reactor is now fully offline and safe for maintenance.

## Emergency Shutdown (SCRAM)

Use ONLY in critical situations: containment failure, coolant loss, or imminent danger.

**Duration:** 30-90 seconds

1. **Press red EMERGENCY SCRAM button** (located on main control panel)
2. System will automatically:
   - Immediately cease fuel injection
   - Dump magnetic containment field
   - Activate emergency coolant flood
   - Vent residual plasma through emergency exhaust
   - Engage reactor lockdown

**WARNING**: Emergency shutdown causes thermal stress and may damage reactor components. Use only when necessary. Reactor requires full inspection before restart after SCRAM event.

## Shutdown to Standby Mode

For temporary shutdown (less than 48 hours), use Standby Mode:

**Duration:** 5 minutes

1. Reduce fuel injection to 10% of normal rate
2. Decrease magnetic field to 4.5 Tesla
3. Lower coolant flow to 20%
4. Power output will stabilize at 10% capacity
5. Reactor maintains minimal fusion reaction

**Benefits:** Faster restart, reduced thermal cycling stress, maintains emergency power capability.

## Troubleshooting Startup/Shutdown Issues

### Reactor Won't Start

**Symptoms:** Ignition sequence fails, plasma won't stabilize
**Check:**
- Fuel canister pressure (must be 150+ PSI)
- Magnetic containment field strength
- Coolant flow and temperature
- Backup power availability

**See:** PWR-SYS-004 Troubleshooting Manual, Error Code E-PWR-101

### Reactor Won't Shut Down

**Symptoms:** Fusion reaction persists after fuel injection stopped
**Action:**
- Maintain magnetic containment
- Continue coolant circulation
- Contact Outer Rim Support immediately
- Prepare for possible SCRAM if reaction intensifies

**See:** EMERG-005 Reactor Emergency Procedures

### Abnormal Temperature During Startup

**Symptoms:** Temperature rises too quickly or exceeds limits
**Action:**
- Immediately reduce fuel injection rate
- Increase coolant flow to maximum
- Hold at current power level until temperature stabilizes
- If temperature continues rising, initiate shutdown

### Coolant System Failure During Shutdown

**Symptoms:** Coolant pump failure, leak detected
**Action:**
- Activate backup coolant system immediately
- Accelerate shutdown procedure
- If backup unavailable, initiate emergency SCRAM
- Evacuate reactor compartment if radiation levels rise

## Post-Startup Monitoring Period

After successful startup, monitor reactor for first 30 minutes:

- Check all parameters every 5 minutes
- Listen for unusual sounds (grinding, high-pitched whines)
- Monitor vibration levels
- Watch for coolant leaks
- Verify stable power delivery to ship systems

## Related Documents

- PWR-SYS-001: Q-Core Reactor System Overview
- PWR-SYS-003: Q-Core Maintenance and Inspection Guide
- PWR-SYS-004: Q-Core Troubleshooting Manual
- EMERG-005: Reactor Emergency Procedures
- ERR-PWR-100: Power System Error Codes

---

**CERTIFICATION REQUIRED**: Reactor startup and shutdown should only be performed by qualified personnel with current Q-Core operation certification. Training available through ORSM Technical Academy.
