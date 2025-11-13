# KB-001: Q-Core Reactor Won't Start - Quick Resolution

**Category:** Power Systems
**Difficulty:** Basic
**Est. Time to Resolve:** 15-30 minutes
**Last Updated:** 2847.09.14

## Issue Description

Customer reports that Q-Core reactor ignition sequence fails or plasma won't form when attempting startup. Error codes E-PWR-101 or E-PWR-102 may be displayed.

## Symptoms

- Ignition button pressed but reaction doesn't initiate
- Plasma forms briefly then dissipates
- Control panel shows "IGNITION FAILED" message
- Temperature remains at ambient, doesn't rise
- Error code E-PWR-101 (fuel system) or E-PWR-102 (magnetic containment)

## Quick Diagnostic Questions

Ask the customer:

1. **"What is your fuel canister pressure reading?"**
   - If below 100 PSI → Fuel system issue (see Solution A)
   - If 150-200 PSI → Fuel pressure adequate, check other causes

2. **"Are all tachyon emitters showing green status?"**
   - Wait, wrong system. For reactor: **"Are all magnetic containment coils powered?"**
   - If any coils dark/red → Magnetic system issue (see Solution B)
   - If all green → Coils powered, check field strength

3. **"What is your coolant system status?"**
   - If coolant low or pumps not running → Coolant issue (see Solution C)
   - If coolant normal → Check other systems

4. **"How long since last reactor shutdown?"**
   - If less than rated cooldown interval → Drive still in cooldown (see Solution D)
   - If adequate time elapsed → Not a cooldown issue

## Common Solutions

### Solution A: Low Fuel Pressure (E-PWR-101)

**Cause**: Insufficient fuel pressure prevents injectors from delivering fuel to fusion chamber.

**Resolution Steps**:
1. Check fuel canister pressure gauge
   - Should read 150-200 PSI
   - If below 100 PSI, canister is depleted or defective

2. Replace fuel canister:
   - Close main fuel valve
   - Depressurize fuel line
   - Disconnect empty canister
   - Install fresh canister (verify seal gasket present)
   - Open main fuel valve
   - Verify pressure reads 150-200 PSI

3. If pressure still low after canister replacement:
   - Check for fuel line leaks
   - Inspect fuel valve (may be partially closed or stuck)
   - Test fuel pressure regulator function

4. Retry reactor startup

**Expected Result**: Reactor should complete ignition sequence normally.

**If unresolved**: Escalate to Level 2 support for fuel system diagnosis.

### Solution B: Magnetic Containment Failure (E-PWR-102)

**Cause**: Magnetic coils not generating sufficient field strength to contain plasma.

**Resolution Steps**:
1. Check coil power supply:
   - Verify voltage at coil terminals: Should be 380-420 VDC
   - If no voltage: Check power circuit breaker (may be tripped)
   - Reset breaker and retry

2. Verify magnetic field strength:
   - Should reach 4.5 Tesla during startup initialization
   - If below 4.0 Tesla: Possible coil damage or power supply issue

3. Test individual coils:
   - Access diagnostic menu: System > Magnetic > Coil Test
   - System tests each of 12 coils sequentially
   - Note any failed coils

4. If single coil failed:
   - **Temporary workaround**: Some reactors can operate with 11/12 coils at reduced capacity
   - Enable degraded mode if available (reduces max power to 70%)
   - Schedule coil replacement ASAP

5. If multiple coils failed or field strength critically low:
   - Reactor inoperable until repair
   - Requires coil replacement (Part #: MAG-COIL-Q series)
   - Escalate to certified technician

**Expected Result**: With working coils, reactor should start normally (possibly at reduced capacity).

**If unresolved**: Escalate for magnetic system diagnostics and repair.

### Solution C: Coolant System Issue (E-PWR-103)

**Cause**: Reactor won't start if coolant system unable to handle thermal load.

**Resolution Steps**:
1. Check coolant level:
   - Must be ≥ 85% capacity to allow startup
   - Top off with Grade-A sodium-potassium coolant if low
   - **WARNING**: Only use approved coolant type (Part #: COL-NAK-100)

2. Verify coolant pumps operating:
   - Listen for pump motor sound
   - Check pump status indicator (should show "RUNNING")
   - If pump not starting:
     - Check pump power supply
     - Reset pump controller
     - Manually start pump if auto-start failed

3. Check coolant flow:
   - Verify coolant pressure 80-120 PSI (standby level)
   - Flow indicator should show movement
   - If no flow despite pump running: Possible blockage or valve closed

4. Inspect for leaks:
   - Look for coolant puddles or wet spots
   - Check coolant pressure over time (shouldn't drop)
   - Repair any leaks before startup

5. Retry reactor startup once coolant system operational

**Expected Result**: With adequate coolant and pumps running, startup should proceed.

**If unresolved**: Check for coolant system blockages or pump mechanical failure.

### Solution D: Cooldown Timer Still Active

**Cause**: Reactor has minimum cooldown interval between runs. Attempting startup before timer expires will fail.

**Resolution Steps**:
1. Check control panel cooldown timer:
   - Horizon-1: 8 hours minimum
   - Horizon-2: 6 hours minimum
   - Horizon-3: 4 hours minimum
   - Wait, this is for FTL drives not reactors

2. For Q-Core reactor, there's no standard cooldown timer
   - However, if reactor was emergency SCRAM'd, startup lockout active
   - Check for "SCRAM LOCKOUT" indicator
   - Requires inspection and manual reset by qualified technician

3. If SCRAM lockout present:
   - Reactor must be inspected before restart
   - Check for thermal damage
   - Verify containment integrity
   - Reset lockout only after inspection confirms safe operation

**Expected Result**: If lockout due to previous SCRAM, requires manual intervention.

**Action**: Escalate to qualified technician for post-SCRAM inspection.

### Solution E: Control System Reset

**Cause**: Sometimes control computer in error state preventing startup.

**Resolution Steps**:
1. Perform control system reset:
   - Switch reactor main breaker to OFF position
   - Wait 30 seconds (allows capacitors to discharge)
   - Switch main breaker to ON position
   - Wait 60 seconds for control system to boot

2. Check status indicators:
   - All lights should illuminate during boot
   - Display should show "READY FOR STARTUP" when boot complete
   - If error messages persist, note error codes

3. Retry startup sequence

**Expected Result**: Often resolves transient software glitches.

**If unresolved**: May indicate control board failure, escalate for diagnostics.

## Escalation Criteria

Escalate to Level 2 support if:

- Multiple solutions attempted without success
- Customer reports physical damage to reactor components
- Error codes other than E-PWR-101, 102, 103 displayed
- Customer uncomfortable performing diagnostic steps
- Safety concerns (radiation, leaks, unusual sounds/smells)

## Prevention Tips

Share with customer to avoid future issues:

- **Maintain fuel supply**: Don't let canisters run below 100 PSI before replacement
- **Regular coolant checks**: Weekly coolant level verification prevents startup issues
- **Scheduled maintenance**: Monthly coil calibration keeps magnetic system healthy
- **Avoid emergency SCRAM**: Causes thermal stress; use controlled shutdown when possible
- **Keep spares**: Stock fuel canisters, coolant, and critical components

## Related Articles

- KB-015: Low Reactor Power Output
- KB-023: Reactor Overheating Issues
- KB-042: Coolant System Maintenance
- KB-087: Understanding Reactor Error Codes

## Related Manuals

- PWR-SYS-001: Q-Core Reactor System Overview
- PWR-SYS-002: Q-Core Startup and Shutdown Procedures
- PWR-SYS-004: Q-Core Troubleshooting Manual

---

**Support Note**: This is one of the most common support calls. 80% of cases resolve with Solutions A (fuel pressure) or E (control reset). Always check fuel pressure first.
