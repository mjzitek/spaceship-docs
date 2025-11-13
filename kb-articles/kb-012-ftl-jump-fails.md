# KB-012: FTL Jump Fails to Execute - Common Causes

**Category:** Navigation Systems
**Difficulty:** Intermediate
**Est. Time to Resolve:** 20-45 minutes
**Last Updated:** 2847.09.14

## Issue Description

Customer has completed FTL charge sequence but jump won't execute when "EXECUTE JUMP" button is pressed. System may display "JUMP ABORTED" or specific error codes in E-NAV-500 series.

## Symptoms

- Charge completes to 100% but jump doesn't initiate
- "EXECUTE JUMP" button pressed with no response
- Charge sequence aborts at 90-99%
- Error messages related to navigation lock, mass shadow, or field stability
- Countdown begins but cancels before reaching zero

## Quick Diagnostic Questions

Ask the customer:

1. **"What error code is displayed, if any?"**
   - E-NAV-501: Power insufficient → See Solution A
   - E-NAV-502: Mass shadow detected → See Solution B
   - E-NAV-503: Cooldown timer active → See Solution C
   - E-NAV-504: Navigation lock failed → See Solution D
   - E-NAV-505: Tachyon emitter failure → See Solution E

2. **"What does the navigation lock indicator show?"**
   - Red/Failed: Computer can't calculate valid tunnel vector
   - Yellow/Pending: Still calculating (may resolve in moments)
   - Green/Locked: Navigation ready (check other systems)

3. **"What is your current distance from the nearest stellar body?"**
   - Less than minimum safe distance → Mass shadow issue
   - Adequate distance → Not a proximity problem

4. **"How long ago did you complete your last FTL jump?"**
   - Recent (within cooldown period) → Cooldown issue
   - Long ago or first jump → Not a cooldown issue

## Common Solutions

### Solution A: Insufficient Power (E-NAV-501)

**Cause**: Q-Core reactor not producing minimum 80% capacity required for FTL jump.

**Resolution Steps**:
1. Check Q-Core reactor output:
   - View reactor control panel
   - Verify power output percentage
   - Must show ≥ 80% available capacity

2. If reactor below 80%:
   - Check reactor status for issues:
     - Temperature in normal range (1,800-2,400°C)?
     - Fuel supply adequate?
     - Coolant system functioning?

3. Increase reactor output:
   - If at low power by design, increase throttle
   - Bring reactor to Standard Operation mode (60-85% output)
   - Allow reactor to stabilize (5-10 minutes)

4. Disable non-essential systems to free power:
   - Reduce sublight engine load (should be at idle anyway)
   - Dim non-critical lighting
   - Suspend non-urgent computations
   - Typical FTL power requirements:
     - Horizon-1: 20-25 MW
     - Horizon-2: 70-80 MW
     - Horizon-3: 160-180 MW

5. Wait for "FTL READY" indicator before attempting jump
6. Restart charge sequence if charge was aborted

**Expected Result**: With adequate power, charge and jump should proceed normally.

**If unresolved**: Reactor may have performance issue. Refer to KB-015 (Low Reactor Power Output).

### Solution B: Mass Shadow Detected (E-NAV-502)

**Cause**: FTL drive cannot activate within gravity well of large stellar objects. Safety system prevents jump that would cause catastrophic failure.

**Minimum Safe Distances:**
- From star: 2 AU (Astronomical Units)
- From planet: 100,000 km
- From station/large asteroid: 1,000 km

**Resolution Steps**:
1. Check navigation display for mass shadow warning:
   - Red zones on display indicate gravity wells
   - Current position should be outside all red zones

2. Identify interfering object:
   - Usually the planet/station customer is departing from
   - Sometimes a celestial body they didn't account for
   - Nav computer will identify source of interference

3. Move to safe distance:
   - Engage sublight engines
   - Plot course away from interfering mass
   - Use navigation computer's "Clear Zone Calculator"
     - Input: Current position and interfering object
     - Output: Nearest safe jump point and heading

4. Travel to clear zone:
   - May take minutes to hours depending on proximity
   - Monitor navigation display for green "CLEAR FOR JUMP" status

5. Once clear, reinitiate FTL charge sequence

**Expected Result**: From clear zone, jump should execute normally.

**Special Cases:**
- **Binary star systems**: Must clear both stars' gravity wells
- **Dense asteroid fields**: Computer may detect cumulative mass, requiring wide berth
- **Hidden masses**: Rogue planets, black holes not on charts can cause unexpected interference

**If unresolved**: Navigation sensors may be miscalibrated. Run sensor diagnostic.

### Solution C: Cooldown Timer Active (E-NAV-503)

**Cause**: FTL drive has mandatory cooldown period between jumps. QFM core must return to safe temperature before another jump.

**Cooldown Periods:**
- Horizon-1: 8 hours minimum
- Horizon-2: 6 hours minimum
- Horizon-3: 4 hours minimum

**Resolution Steps**:
1. Check FTL control panel for cooldown timer:
   - Displays time remaining (e.g., "04:37:22")
   - Timer counts down to 00:00:00

2. **There is no override for cooldown timer**
   - Safety feature preventing QFM thermal damage
   - Attempting jump during cooldown can destroy drive
   - Must wait for timer to expire

3. While waiting:
   - Verify no other prep issues (fuel, navigation, etc.)
   - Use time for crew rest, maintenance, route planning
   - Monitor QFM temperature (should be declining steadily)

4. When timer reaches 00:00:00:
   - "FTL READY" indicator will illuminate
   - May now initiate new charge sequence

**Expected Result**: After cooldown complete, drive operates normally.

**Customer Education:**
- Plan multi-jump routes accounting for cooldown periods
- Total travel time = (jump times) + (cooldown periods)
- Example: 3 jumps on Horizon-2 requires:
  - Jump 1: 8 hours transit
  - Cooldown: 6 hours
  - Jump 2: 6 hours transit
  - Cooldown: 6 hours
  - Jump 3: 10 hours transit
  - Total: 36 hours

**If unresolved**: Timer malfunction is rare but possible. Escalate to FTL specialist.

### Solution D: Navigation Lock Failed (E-NAV-504)

**Cause**: Navigation computer unable to calculate stable tunnel vector to destination. Multiple possible causes.

**Resolution Steps**:
1. Check destination coordinates:
   - Verify coordinates entered correctly
   - Common mistake: Wrong decimal place in coordinates
   - Cross-reference with star chart
   - Typo in coordinates can cause nav lock failure

2. Verify destination is within jump range:
   - Calculate distance to destination
   - Compare to drive's maximum range:
     - Horizon-1: 20 light-years maximum
     - Horizon-2: 50 light-years maximum
     - Horizon-3: 100 light-years maximum
   - If destination too far, plan intermediate waypoint

3. Check for spatial interference:
   - Navigation computer scans tunnel path for:
     - Quantum turbulence (near black holes, neutron stars)
     - Gravitational anomalies
     - Dense nebulae
   - If interference detected, may need alternate destination or timing

4. Update star charts:
   - Outdated charts can cause navigation failures
   - Download latest charts from ORSM navigation database
   - Stellar positions drift over years; old data causes errors

5. Try alternate destination:
   - Input coordinates for nearby system
   - If lock succeeds, original destination likely problematic
   - If still fails, navigation computer or sensors may be faulty

6. Manual navigation input:
   - Experienced operators can manually specify tunnel vector
   - **CAUTION**: Only for certified navigators
   - Incorrect manual vector extremely dangerous

**Expected Result**: With valid coordinates and clear path, navigation lock should succeed.

**If unresolved**: Navigation computer may require recalibration or repair. Escalate.

### Solution E: Tachyon Emitter Failure (E-NAV-505)

**Cause**: One or more of 16 tachyon emitters not functioning. All 16 required for safe jump.

**Resolution Steps**:
1. Access emitter status display:
   - FTL control panel > Emitters > Status
   - Shows status of all 16 emitters
   - Green: Operating normally
   - Yellow: Degraded performance
   - Red: Failed

2. Identify failed emitter(s):
   - Note emitter number (1-16)
   - Note position (forward/aft, port/starboard, dorsal/ventral)

3. Attempt emitter reset:
   - Select failed emitter on panel
   - Press "RESET" button
   - System will power cycle emitter
   - Wait 30 seconds for emitter to reinitialize
   - Check if status changes to green

4. Check emitter power supply:
   - Verify emitter receiving power (voltage should be 420 VDC)
   - Check circuit breaker for that emitter
   - Reset breaker if tripped

5. Inspect physical emitter (if accessible):
   - Some emitters in accessible hull locations
   - Look for physical damage, burn marks
   - Check mounting and electrical connections
   - Tighten any loose connections

6. If emitter cannot be repaired:
   - FTL jump impossible with failed emitter
   - Requires emitter replacement (Part #: TAC-EM-H series)
   - Customer must use sublight engines to reach repair facility
   - **OR** limp along if close to destination

**Expected Result**: If emitter can be reset or repaired, jump proceeds normally.

**If unresolved**: Failed emitter requires professional replacement. Cannot jump until repaired.

## Multiple Errors

If customer experiencing multiple error codes:

1. Address in order of severity:
   - E-NAV-502 (Mass shadow) - First, move to safe location
   - E-NAV-501 (Power) - Second, ensure adequate reactor output
   - E-NAV-505 (Emitter) - Third, critical system failure
   - E-NAV-504 (Nav lock) - Fourth, navigation issue
   - E-NAV-503 (Cooldown) - Last, just need to wait

2. Solving one error may reveal others
3. Recheck all systems after each fix

## Escalation Criteria

Escalate to FTL specialist if:

- All common solutions attempted without success
- Error codes not covered in this article
- Physical damage to FTL drive components
- Customer reports unusual sounds, vibrations, or smells from FTL drive
- QFM temperature not declining during cooldown
- Tunnel stability issues during charge sequence
- Customer requires emergency jump despite system warnings

## Prevention Tips

- **Pre-flight planning**: Calculate mass shadow clear zones before attempting departure
- **Fuel management**: Ensure adequate reactor fuel for FTL power requirements
- **Route planning**: Account for cooldown periods in multi-jump routes
- **Navigation updates**: Keep star charts current (update quarterly minimum)
- **Emitter inspection**: Monthly emitter status checks catch failures early
- **Coordinate verification**: Always double-check destination coordinates before charging

## Related Articles

- KB-023: FTL Drive Overheating
- KB-034: Navigation Computer Errors
- KB-045: Mass Shadow Calculations
- KB-067: Emergency FTL Abort Procedures
- KB-089: Tachyon Emitter Replacement

## Related Manuals

- NAV-FTL-001: FTL Drive System Overview
- NAV-FTL-002: FTL Jump Procedures
- NAV-FTL-004: FTL Drive Troubleshooting
- EMERG-006: FTL Emergency Procedures

---

**Support Note**: E-NAV-502 (mass shadow) and E-NAV-503 (cooldown) account for 60% of "jump won't execute" calls. Always check these first. Many customers don't realize cooldown is mandatory and non-overridable.
