# KB-301: Docking Port Alignment and Connection Issues

**Category:** Navigation / Docking Systems
**Difficulty:** Intermediate
**Est. Time to Resolve:** 15-60 minutes
**Last Updated:** 2847.11.01

## Issue Description

Customer unable to successfully dock with station or other vessel due to alignment problems, connection failures, or docking mechanism malfunctions. May result in bouncing off docking port, misalignment warnings, or failed seal.

## Symptoms

- Ship approaches docking port but won't connect
- Docking clamps won't engage or won't hold
- Alignment sensors show "MISALIGNMENT" error
- Ship bounces off port or slides past
- Docking successful but airlock seal fails
- Repeated docking attempts unsuccessful
- Error codes: E-NAV-400 series (docking system errors)

## Impact Assessment

**Ask customer: "What happens when you attempt to dock?"**

- **Can't get aligned** → Solution A (Alignment and Approach)
- **Alignment looks good but won't connect** → Solution B (Docking Mechanism)
- **Connects but seal fails** → Solution C (Airlock Seal)
- **Ship bounces or slides off** → Solution D (Velocity and Position)
- **Auto-dock fails** → Solution E (Auto-Dock System)

## Common Solutions

### Solution A: Alignment and Approach Issues

**Cause**: Ship not properly aligned with docking port axis, angle, or rotation.

**Diagnostic Questions:**

1. **"Are you using auto-dock or manual docking?"**
   - Auto-dock failing → See Solution E
   - Manual docking → Continue with alignment steps

2. **"What does the alignment indicator show?"**
   - Check docking display for alignment guides
   - Should show position and angle relative to port
   - Green = aligned, Yellow = close, Red = misaligned

**Resolution Steps:**

1. **Verify correct docking port:**
   - Confirm you're approaching the assigned/correct port
   - Station: Check assignment (may have specific bay number)
   - Ship-to-ship: Confirm which port (bow, aft, port, starboard)
   - Some ports are different sizes (your ship may not fit)

2. **Check alignment indicators:**
   - **Position alignment**: Center crosshair on docking port
     - X-axis (left-right): Should be within ±0.5 meters
     - Y-axis (up-down): Should be within ±0.5 meters
     - Z-axis (forward-back): Approach at correct distance
   - **Rotational alignment**: Roll indicator shows ship rotation
     - Must match port rotation (within ±5 degrees)
     - Rotate ship to align orientation markers

3. **Correct common alignment errors:**

   **If ship drifting left/right or up/down:**
   - Use lateral thrusters to center
   - Small adjustments (tap controls, don't hold)
   - Wait for ship to stabilize after each adjustment
   - Approach slowly (0.1-0.3 m/s) to allow time for correction

   **If ship rotated wrong:**
   - Check rotation indicator (shows roll angle)
   - Use roll thrusters or RCS to rotate ship
   - Match your "up" to port's "up"
   - Many ships: Green light on port = "top" alignment marker

   **If ship at wrong angle (pitched or yawed):**
   - Ship nose must point directly at port (±2 degrees)
   - Use pitch/yaw controls to align
   - Check from multiple camera angles if available

4. **Approach procedure for difficult alignments:**
   - Stop at 10 meters from port
   - Make all alignment corrections while stationary
   - Get alignment indicators all green
   - Only then approach slowly (0.1 m/s)
   - Maintain alignment during approach (small corrections only)
   - Final 1 meter: Hands off controls, let momentum carry you in

**Expected Result**: Proper alignment allows docking mechanism to engage automatically.

**If unresolved**: Ship may have thruster malfunction preventing fine control - escalate to propulsion diagnostics.

### Solution B: Docking Mechanism Won't Connect

**Cause**: Mechanical failure of docking clamps, latches, or magnetic capture system.

**Diagnostic Questions:**

1. **"Do you hear or feel the docking clamps trying to engage?"**
   - Mechanical sound/vibration → Clamps trying but failing (mechanical issue)
   - No sound → Clamps not activating at all (electrical/control issue)

2. **"What does the docking status display show?"**
   - Check: Docking > System Status
   - Shows status of clamps, magnets, seals

**Resolution Steps:**

1. **Check docking system power:**
   - Navigate to: Docking > System Status
   - Verify power to docking system (should show "POWERED")
   - If no power:
     - Check docking circuit breaker (may be tripped)
     - Reset and retry

2. **Cycle docking system:**
   - Navigate to: Docking > System Reset
   - Powers down then restarts docking mechanisms
   - Wait 30 seconds after reset
   - Retry docking

3. **Manual docking clamp activation:**
   - If auto-engage failed, try manual:
   - Approach port until very close (<0.5 meters)
   - Hold position
   - Navigate to: Docking > Manual Controls
   - Activate "ENGAGE CLAMPS" manually
   - Should hear/feel clamps grabbing port

4. **Check for physical obstructions:**
   - If possible, use external camera to view docking port on your ship
   - Look for:
     - Debris in docking ring
     - Damaged or bent clamps
     - Stuck latches
     - Ice buildup (if in cold environment)
   - May need EVA to clear obstruction or repair damage

5. **Compatibility check:**
   - Some older ships use non-standard docking mechanisms
   - Confirm your ship's docking standard matches station/port:
     - Standard: Universal Docking Collar (UDC)
     - Commercial: CommDock-3
     - Military: MilSpec-D
     - Industrial: HeavyDock
   - If incompatible, may need adapter collar or different port

**Expected Result**: Functional docking mechanism engages and holds ship firmly.

**If unresolved**: Mechanical damage likely - may need repair before successful docking. Escalate to maintenance.

### Solution C: Airlock Seal Failure

**Cause**: Docking successful (clamps holding) but airlock won't seal or pressurize.

**Diagnostic Questions:**

1. **"Are the docking clamps engaged and holding the ship?"**
   - Yes → Seal problem (continue steps below)
   - No → Connection problem (see Solution B)

2. **"What happens when you try to pressurize the docking tunnel?"**
   - Pressure won't rise → Leak in seal
   - Pressure rises then drops → Seal failing intermittently
   - Error message → System detecting unsafe condition

**Resolution Steps:**

1. **Check seal status:**
   - Navigate to: Docking > Airlock Status
   - Check "Seal Integrity" reading
   - Should show "SEALED" or "GOOD"
   - If shows "UNSEALED" or "LEAK": Seal not making contact

2. **Verify both hatches are closed:**
   - **Your ship's hatch**: Must be closed before pressurizing tunnel
   - **Station/other ship's hatch**: Should also be closed
   - Opening sequence:
     - Close both hatches
     - Pressurize tunnel
     - Equalize pressure
     - Then both hatches can open

3. **Check seal alignment:**
   - Seal ring must make even contact all the way around
   - If docking slightly misaligned, seal may not contact properly
   - Try disconnecting and re-docking with better alignment
   - Small position errors may allow clamps to engage but prevent seal

4. **Inspect seal ring condition:**
   - If accessible (external camera or EVA):
     - Look for:
       - Damaged/torn seal
       - Debris preventing seal contact
       - Ice or frost on seal (prevents contact)
       - Seal ring retracted (should extend when docked)
   - Clean or repair as needed

5. **Manual seal pressurization:**
   - Some systems allow manual seal inflation:
   - Navigate to: Docking > Seal Controls
   - "MANUAL SEAL PRESSURE": Increase to 120% for better seal
   - May allow tunnel pressurization even with marginal seal

**Expected Result**: Good seal allows tunnel to pressurize fully, enabling hatch opening.

**If unresolved**: Seal damage may require replacement. May need to use EVA suits to transfer if tunnel can't pressurize.

### Solution D: Ship Bounces or Slides Off Port

**Cause**: Approach velocity too high, incorrect angle, or thruster firing during final approach.

**Diagnostic Questions:**

1. **"How fast are you approaching the docking port?"**
   - Velocity should be <0.5 m/s for final approach
   - If faster: Reduces collision speed

2. **"Are any thrusters firing during the final contact?"**
   - Thrusters active → Pushing ship away from port
   - Should be "hands off" for final contact

**Resolution Steps:**

1. **Reduce approach velocity:**
   - Recommended approach speeds:
     - 10 meters out: 0.5 m/s
     - 5 meters out: 0.3 m/s
     - 2 meters out: 0.1 m/s
     - Final 1 meter: Drift (no thrust)
   - Slower is better - be patient

2. **Disable auto-stabilization for final approach:**
   - Many ships have RCS auto-stabilization
   - This can fire thrusters during docking contact (bad)
   - Navigate to: Flight Controls > RCS Settings
   - Set to "MANUAL" or "DOCKING MODE"
   - Final approach: No thrust inputs, let ship coast in

3. **Correct bounce recovery:**
   - If ship bounces off port:
     - Don't chase it immediately
     - Back off to 10 meters
     - Stabilize ship (stop all rotation and drift)
     - Re-align carefully
     - Retry approach slower

4. **Check magnetic capture (if equipped):**
   - Some ports use magnetic capture to pull ships in gently
   - Navigate to: Docking > Mag Capture
   - Should show "ACTIVE" when <3 meters from port
   - If not active:
     - Check power to mag system
     - May need to activate manually
   - Mag capture allows slightly faster approach (ship caught and slowed)

5. **Station/port rotation:**
   - If docking with rotating station/ship:
     - Must match rotation before docking
     - Rotate ship at same rate as port
     - Maintain rotation match during approach
     - If rotation mismatched, ship slides off port

**Expected Result**: Slow, stable approach allows docking mechanism to engage softly.

**If unresolved**: May need docking practice or pilot training. Consider requesting tugboat assistance.

### Solution E: Auto-Dock System Failure

**Cause**: Automatic docking system malfunction, misconfiguration, or incompatibility.

**Diagnostic Questions:**

1. **"What does the auto-dock display show when you engage it?"**
   - Check for error messages
   - Note specific error code (E-NAV-4XX series)

2. **"At what point does auto-dock fail?"**
   - Won't engage → System not operational
   - Engages but doesn't approach → Sensor issue
   - Approaches but aborts → Safety threshold triggered

**Resolution Steps:**

1. **Verify auto-dock prerequisites:**
   - **Distance**: Must be within 100 meters of port (typically)
   - **Velocity**: Relative velocity <1 m/s
   - **Alignment**: Rough alignment required (within 20 degrees)
   - **Clearance**: No obstacles between ship and port
   - **Permission**: Station must grant docking clearance (transmits docking beacon)

2. **Check docking beacon reception:**
   - Navigate to: Docking > Beacon Status
   - Should show "RECEIVING" when near assigned port
   - If no beacon:
     - Confirm docking clearance from station
     - Check if approaching correct port (wrong port = no beacon)
     - Communications issue (repair comms)

3. **Restart auto-dock system:**
   - Disengage auto-dock
   - Navigate to: Docking > Auto-Dock > System Reset
   - Wait 30 seconds
   - Re-engage auto-dock
   - Retry

4. **Check sensor functionality:**
   - Auto-dock uses sensors to judge distance and alignment
   - Navigate to: Sensors > Proximity Sensors
   - All proximity sensors should show "OPERATIONAL"
   - If sensors failed, auto-dock cannot work (use manual docking)

5. **Try manual docking:**
   - If auto-dock unreliable, manual docking is backup
   - Many pilots prefer manual for better control
   - Follow Solution A (Alignment) for manual procedure

6. **Software update:**
   - Outdated auto-dock software may have bugs
   - Navigate to: Docking > Software Version
   - Check for updates: System > Updates > Check Now
   - Install docking system updates if available

**Expected Result**: Functional auto-dock completes docking without pilot input.

**If unresolved**: Auto-dock system may need repair. Use manual docking as workaround. Escalate for software/sensor diagnostics.

## Advanced Diagnostics

### Docking Sensor Test

Navigate to: Docking > Diagnostics > Sensor Test

Tests all docking-related sensors:
- Proximity sensors (distance to port)
- Alignment sensors (angle and position)
- Seal sensors (seal contact detection)
- Pressure sensors (tunnel pressurization)

Note any failed sensors - must be repaired for reliable docking.

### Docking Mechanism Test

Navigate to: Docking > Diagnostics > Mechanism Test

Tests mechanical components:
- Clamps (extend, retract, grip strength)
- Latches (engage, disengage)
- Seal inflation (extend, pressure)
- Magnetic capture (if equipped)

Note any failed components - must be repaired.

## Escalation Criteria

Escalate to Level 2 support or technician if:

- Multiple docking attempts fail despite following procedures
- Docking mechanism mechanically damaged (collision, wear)
- Sensor failures preventing accurate alignment
- Auto-dock system unrecoverable
- Compatibility issues between ship and port standards
- Urgent docking needed (low fuel, medical, etc.) and cannot achieve

## Emergency Docking

**If docking needed urgently (fuel, medical, life support):**

1. **Request assistance:**
   - Contact station: Request tugboat/docking assistance
   - Tug can grab ship and position it precisely
   - Or station may have docking arms to pull ship in

2. **EVA transfer option:**
   - If docking impossible but ship can hold position near station:
   - Crew can EVA across gap
   - Use tether for safety
   - Transfer through airlock without ship docking

3. **Emergency coupling:**
   - Some stations have flexible coupling tubes
   - Can extend to poorly-aligned ship
   - Allows crew transfer even without hard dock

## Prevention Tips

- **Practice docking**: Improves skill, reduces failed attempts
- **Maintain docking equipment**: Monthly mechanism test, annual seal replacement
- **Slow approaches**: Patience prevents bouncing and damage
- **Sensor calibration**: Quarterly sensor check ensures accurate alignment
- **Update software**: Keep auto-dock software current for bug fixes
- **Clean docking ring**: Debris and ice interfere with seal - inspect and clean regularly

## Related Articles

- KB-067: Sluggish or Unresponsive Controls (may affect docking precision)
- KB-404: Station Won't Grant Docking Clearance
- KB-531: Proximity Sensor Malfunction

## Related Manuals

- DOCK-SYS-001: Docking Systems Overview
- NAV-OPS-005: Docking Procedures and Best Practices
- DOCK-SYS-003: Docking Mechanism Maintenance

---

**Support Note**: Docking issues frustrate customers because they're "so close" to their destination. Most cases resolve with patient, slower approach and attention to alignment. Auto-dock is convenient but manual docking is more reliable - teach customers manual procedure as backup. Docking is skill-based - more practice = better success rate.
