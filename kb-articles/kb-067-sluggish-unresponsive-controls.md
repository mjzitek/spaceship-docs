# KB-067: Sluggish or Unresponsive Ship Controls

**Category:** Ship Operations / Control Systems
**Difficulty:** Basic to Intermediate
**Est. Time to Resolve:** 10-45 minutes
**Last Updated:** 2847.10.15

## Issue Description

Customer reports that ship controls are slow to respond, inputs are delayed, or controls feel "laggy." This may affect maneuvering thrusters, flight controls, system interfaces, or all ship systems simultaneously.

## Symptoms

- Controls take several seconds to respond to input
- Thruster response delayed when piloting
- System menus slow to load or navigate
- Multiple button presses required to register command
- Controls work but "feel wrong" - sluggish or unresponsive
- May be intermittent or constant

## Impact Assessment

**Ask customer: "Which controls are affected?"**

- **Flight controls only** (thrusters, steering) → Solution A (Thruster Response Lag)
- **All ship systems slow** (menus, displays, everything) → Solution B (Computer Performance)
- **Specific systems only** (weapons, sensors, etc.) → Solution C (System-Specific Issues)
- **Intermittent lag spikes** → Solution D (Network/Bus Interference)

## Common Solutions

### Solution A: Thruster Response Lag (Flight Controls Only)

**Cause**: Thruster control system delay, low pressure, or valve issues.

**Diagnostic Questions:**

1. **"Does the ship eventually respond, just slowly? Or do some commands not work at all?"**
   - Delayed response → Control signal delay (see steps below)
   - Some commands don't work → Mechanical issue (specific thruster failure)

2. **"Is this a recent problem, or has it been getting worse over time?"**
   - Recent/sudden → Software glitch or sensor issue
   - Gradual worsening → Mechanical degradation (valves, lines)

**Resolution Steps:**

1. **Check thruster pressure:**
   - Navigate to: Propulsion > Thrusters > System Status
   - Verify fuel pressure to thrusters: Should be 200-300 PSI
   - If low (<150 PSI):
     - Check fuel tank level
     - Check fuel pump operation
     - Inspect for fuel leaks
   - Low pressure causes delayed thruster response (takes time to build thrust)

2. **Recalibrate thruster response:**
   - Navigate to: Propulsion > Thrusters > Calibration
   - Run auto-calibration sequence (takes 5-10 minutes)
   - This resets thruster control timing and response curves
   - Test response after calibration completes

3. **Check for sensor lag:**
   - Navigate to: Flight Controls > Diagnostics
   - Check "Control Loop Frequency"
   - Should be 50-100 Hz (updates per second)
   - If below 20 Hz: Sensor or computer performance issue
     - Reboot flight control computer (see Solution B)
     - Check gyroscope and accelerometer calibration

4. **Verify control mode settings:**
   - Some ships have "precision" vs "responsive" control modes
   - Navigate to: Flight Controls > Control Mode
   - Try switching mode: "Responsive" gives faster reaction, "Precision" is deliberately slower
   - Confirm mode matches user expectation

**Expected Result**: Thrusters should respond within 0.5-1.0 seconds of control input.

**If unresolved**: Check for mechanical thruster issues (stuck valves, clogged lines) - escalate to maintenance.

### Solution B: Overall System Slowness (All Systems Affected)

**Cause**: Main computer performance degraded due to overload, memory issues, or failing hardware.

**Diagnostic Questions:**

1. **"How long has the ship been running since the last full reboot?"**
   - Days/weeks without reboot → Memory leak/fragmentation (see reboot solution)
   - Recent reboot, still slow → Hardware or software problem

2. **"Are any systems showing high CPU usage or resource warnings?"**
   - Navigate to: System > Performance Monitor
   - Check CPU, Memory, Storage usage
   - Any component > 90% → Identify and address

**Resolution Steps:**

1. **Check system resource usage:**
   - Navigate to: System > Performance Monitor
   - Look for:
     - CPU usage >80% sustained
     - Memory usage >90%
     - Storage nearly full (>95%)
   - Identify what's consuming resources

2. **Common resource hogs:**
   - **High CPU**: Background diagnostics, sensor processing, mining/cargo automation
   - **High Memory**: Too many applications open, memory leak in software
   - **Full Storage**: Logs, sensor recordings, cargo manifests
   - Close unnecessary applications
   - Clear old log files: System > Maintenance > Clear Logs (keep last 7 days)

3. **Perform system reboot:**
   - Save all work and close applications
   - Navigate to: System > Power > Restart Ship Computer
   - **NOTE**: This reboots computer only, not reactor or life support (those stay running)
   - Wait 2-3 minutes for full reboot
   - Test system responsiveness after reboot

4. **If still slow after reboot:**
   - Run system diagnostic: System > Diagnostics > Full Scan
   - Check for:
     - Corrupted system files
     - Failing storage drive
     - Memory module errors
   - May require software repair or hardware replacement

**Expected Result**: Fresh reboot typically resolves 70% of system slowness issues.

**If unresolved**: Hardware failure possible - escalate for diagnostics and potential component replacement.

### Solution C: Specific System Lag (One System Slow, Others Normal)

**Cause**: Individual system overloaded, misconfigured, or hardware issue.

**Resolution Steps:**

1. **Identify which system is affected:**
   - Weapons system slow? → Check weapons computer and targeting
   - Sensors laggy? → Check sensor processing load
   - Navigation delayed? → Check navigation computer
   - Communications slow? → Check comm system bandwidth

2. **Restart affected system:**
   - Most systems can be restarted without ship-wide reboot
   - Navigate to affected system's control panel
   - Look for: System > Restart or Power > Cycle System
   - Wait for system to reinitialize
   - Test response

3. **Check system-specific settings:**
   - **Weapons**: Target tracking limit (tracking too many targets = lag)
   - **Sensors**: Scan resolution too high (reduce for faster response)
   - **Navigation**: Chart detail level (lower detail = faster plotting)
   - Reduce quality/detail settings to improve response

4. **Update system software:**
   - Navigate to: System > Software > Check for Updates
   - Install any available updates (may fix bugs causing lag)
   - Reboot after update installation

**Expected Result**: System-specific restarts and settings adjustments resolve most single-system lag.

**If unresolved**: System hardware may be failing - escalate for component diagnostics.

### Solution D: Intermittent Lag Spikes

**Cause**: Electrical interference, network congestion, or environmental factors.

**Diagnostic Questions:**

1. **"Does the lag happen at specific times or randomly?"**
   - Specific times → External trigger (environmental, scheduled tasks)
   - Random → Interference or hardware intermittent failure

2. **"Does the lag occur when specific systems are active?"**
   - During weapon fire → Electrical surge from weapons
   - During sensor sweeps → Sensor processing spikes
   - During communications → Comm system interference
   - Identify correlation

**Resolution Steps:**

1. **Check for electrical interference:**
   - Heavy power loads can cause voltage sag affecting computers
   - Common causes:
     - Weapon charging/firing
     - Thruster max burn
     - Mining equipment operation
   - Install/verify power filtering on computer circuits
   - Upgrade power supply if inadequate

2. **Check data bus congestion:**
   - All ship systems communicate via data bus (network)
   - Too much data traffic = lag
   - Navigate to: System > Network > Bus Utilization
   - Should be <70% average
   - If >80%: Some systems flooding bus with data
   - Identify chatty systems and reduce update frequency

3. **Environmental factors:**
   - Strong magnetic fields (near pulsars, planets)
   - Radiation (passing through radiation zones)
   - Extreme temperatures
   - Check if lag correlates with environment
   - May need better shielding or wait until clear of environmental hazard

4. **Scheduled background tasks:**
   - Some ships run diagnostics, backups, or maintenance automatically
   - These can cause periodic lag
   - Navigate to: System > Scheduled Tasks
   - Review what's running and when
   - Reschedule to off-peak times (during sleep shift, etc.)

**Expected Result**: Identifying and eliminating interference source restores normal response.

**If unresolved**: May need electrical system audit or shielding upgrades - escalate to electrical technician.

## Advanced Diagnostics

### If multiple solutions attempted without success:

1. **Control Input Test:**
   - Navigate to: Flight Controls > Input Test
   - Move control stick/yoke
   - Display should show immediate response to input
   - If input test responsive but ship still slow → Thruster/actuation issue (not computer)
   - If input test also slow → Computer/sensor issue

2. **Response Time Measurement:**
   - Use diagnostic tool to measure actual response time:
     - Input signal received → Output command sent: Should be <100 milliseconds
     - Output command sent → Thruster activation: Should be <500 milliseconds
   - Identify which stage is delayed

3. **Compare to backup systems:**
   - If ship has redundant computer: Switch to backup, test response
   - If backup responsive: Primary computer has problem
   - If backup also slow: System-wide issue (power, interference, etc.)

## Escalation Criteria

Escalate to Level 2 support or technician if:

- All basic solutions attempted without improvement
- Control lag is severe (>5 seconds) and dangerous
- Customer reports recent physical damage or electrical issues
- System diagnostics show hardware errors
- Intermittent lag cannot be correlated to any pattern
- Safety concern (unable to maneuver away from hazards)

## Quick Wins (Try First)

For fastest resolution, try these in order:

1. **Reboot ship computer** (5 minutes, fixes 70% of cases)
2. **Check thruster fuel pressure** (1 minute, common issue)
3. **Clear log files** (2 minutes, frees resources)
4. **Recalibrate thrusters** (10 minutes, fixes drift and lag)

## Prevention Tips

Share with customer to avoid future issues:

- **Weekly reboots**: Prevents memory fragmentation and software glitches
- **Monitor resources**: Check CPU/memory usage periodically, address hogs before they cause lag
- **Regular calibration**: Monthly thruster and sensor calibration maintains crisp response
- **Clean logs**: Don't let log files fill storage (automatic cleanup or monthly manual)
- **Power quality**: Ensure clean power to computer systems (filters, voltage regulation)
- **Software updates**: Keep systems updated (bug fixes improve performance)

## Related Articles

- KB-018: Thruster Not Firing or Weak Thrust
- KB-053: Computer Performance Degradation
- KB-091: Electrical System Interference Issues
- KB-134: Flight Control Calibration Procedures

## Related Manuals

- FLT-CTRL-001: Flight Control Systems Overview
- COMP-SYS-002: Ship Computer Maintenance
- PROP-SYS-003: Thruster System Troubleshooting
- ELEC-SYS-005: Electrical Interference and Filtering

---

**Support Note**: "Sluggish controls" is a common but vague complaint. First question should always be: "Which controls - flight, menus, specific systems, or everything?" This quickly narrows diagnosis. Most cases resolve with simple reboot, but safety-critical if affecting flight controls - prioritize accordingly.
