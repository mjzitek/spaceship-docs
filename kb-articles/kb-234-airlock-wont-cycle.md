# KB-234: Airlock Won't Cycle or Complete Sequence
**Category:** Hull Systems / Airlocks | **Severity:** High | **Avg Resolution Time:** 15 minutes

## ISSUE SUMMARY
Customer reports airlock will not complete cycling sequence, preventing entry or exit from ship. This can strand crew members or prevent EVA operations.

**Common Symptoms:**
- Airlock stuck between cycles (partially pressurized/depressurized)
- Inner or outer door won't open after cycle complete
- "Pressure equalization failed" error
- Safety interlocks preventing door operation
- Airlock control panel unresponsive

**Related Issues:**
- For hull breach situations, see [EMERG-001: Hull Breach](../emergency-procedures/emerg-001-hull-breach.md)
- For pressure loss issues, see [Life Support](../manuals/life-support/atmospheric-processing.md)

---

## ⚠️ SAFETY FIRST

### CRITICAL SAFETY CHECKS BEFORE TROUBLESHOOTING

**Ask customer IMMEDIATELY:**

1. **Is anyone currently in the airlock?**
   - If YES → Priority escalation, use Manual Override section below
   - If NO → Proceed with troubleshooting

2. **What is the current pressure state?**
   - Pressurized (matches ship interior) → Safer to troubleshoot
   - Depressurized (matches exterior/space) → More caution required
   - Partially pressurized → DANGEROUS, see Section A

3. **Which door(s) are involved?**
   - Inner door (to ship) → Less critical
   - Outer door (to space/exterior) → More critical
   - Both stuck → System-wide issue

**⚠️ NEVER override safety interlocks unless:**
- Life is in immediate danger
- You understand the specific risk you're accepting
- No other options exist

---

## QUICK DIAGNOSTIC QUESTIONS

1. **When did this start?**
   - During normal cycle → Likely pressure/sensor issue
   - After recent use → May be incomplete previous cycle
   - Never worked / first use → Installation or configuration issue

2. **What happens when you try to cycle?**
   - Nothing (no response) → Power or control issue
   - Starts but stops → Sensor or pressure issue
   - Error message → Note exact message
   - Partial cycle → Pump or valve issue

3. **Recent maintenance or repairs?**
   - If YES → May be related to service work

4. **Any visible damage to airlock or doors?**
   - If YES → May require physical repair

---

## DIAGNOSTIC FLOWCHART

```
Airlock Won't Cycle
         ↓
Is anyone trapped in airlock?
         ↓ YES                ↓ NO
[Go to EMERGENCY          Is control panel responsive?
 SECTION]                      ↓ NO              ↓ YES
                         [Section A:         Does cycle start?
                          Power/Control]          ↓ NO           ↓ YES
                                            [Section B:        [Section C:
                                             Door/Interlock]    Pressure System]
```

---

## 🆘 EMERGENCY: PERSON TRAPPED IN AIRLOCK

**If someone is in the airlock and in danger:**

### Step 1: Assess Situation (30 seconds)
```
Customer: Quickly determine:
1. Person's current condition (conscious, suited, time remaining)
2. Current airlock pressure (full, partial, none)
3. Which side person needs to go (back in ship, or out to space)
```

### Step 2: Manual Override (If Safe)
```
⚠️ Only if:
- Person is suited and has air (if going to space)
- OR airlock has some pressure and person can survive brief exposure

Customer Action:
1. Locate manual override panel (usually yellow cover near airlock)
2. Open cover (may need tool to break seal)
3. Follow embossed instructions on panel
4. Most common: Pull manual release lever for desired door
```

**⚠️ WARNING:** Manual override bypasses ALL safety checks. Only use in emergency.

### Step 3: Notify Emergency Services
```
Support Agent: Immediately page emergency response
- Continue assisting customer
- Emergency team may have additional override procedures
- Document all actions taken
```

**After person is safe, continue with standard troubleshooting to prevent recurrence.**

---

## SECTION A: POWER & CONTROL ISSUES

### Symptoms
- Airlock control panel completely unresponsive
- No lights or displays
- No sounds when buttons pressed

### Step 1: Check Power to Airlock
**Customer Action:**
```
1. Check airlock control panel indicators:
   - Any lights illuminated?
   - Display showing anything?
2. Check ship's power distribution:
   - Main Panel → Systems → Airlocks → Status
   - Should show "Online" and power percentage
```

**If no power to airlock system:**
```
Diagnosis: Power distribution issue
→ Check main power allocation (airlock needs ~5% minimum)
→ Check circuit breaker for airlock system
→ If power issues across multiple systems, see [System Interaction Matrix](../quick-reference/system-interaction-matrix.md)
→ If power present at main panel but not airlock, escalate (wiring issue)
```

---

### Step 2: Restart Airlock Control Computer
**Customer Action:**
```
1. Locate airlock control panel
2. Press and hold reset button (usually small recessed button)
   - Hold for 5 seconds
   - OR find "System Reset" in menu if accessible
3. Wait for system reboot (30-60 seconds)
4. Panel should show initialization sequence
5. Try cycling airlock again
```

**If restart resolves issue:**
```
Diagnosis: Software glitch or computer crash
→ Issue resolved
→ Document what led to crash (for tracking)
→ If happens frequently, escalate for software investigation
```

**If restart doesn't help or system won't restart:**
```
→ Proceed to Step 3
```

---

### Step 3: Use Backup/Alternative Airlock
**Customer Action:**
```
If ship has multiple airlocks:
1. Identify alternate airlock location
2. Test if alternate airlock functions
3. Use alternate for EVA operations while troubleshooting primary
```

**If alternate airlock works:**
```
Diagnosis: Primary airlock-specific issue
→ Continue troubleshooting primary (less urgency)
→ Customer can continue operations via alternate
```

**If no alternates work:**
```
Diagnosis: Ship-wide airlock control issue
→ Escalate to hull systems specialist
```

---

## SECTION B: DOOR & INTERLOCK ISSUES

### Symptoms
- Control panel responsive
- System shows "Interlock Active" or "Safety Override Required"
- Specific door won't open even after cycle completes
- Mechanical resistance or stuck door

### Step 1: Check Safety Interlocks
**Customer Action:**
```
1. Airlock Panel → Status → Interlocks
2. Check which interlocks are active:
   - Pressure Differential → Doors won't open if pressure not equalized
   - Door Position → One door must be closed before other opens
   - Seal Integrity → Door seals must be intact
   - Manual Override Active → Someone may have engaged manual mode
3. Note which interlocks are preventing operation
```

**Common Interlock Issues:**

**"Pressure Differential Too High"**
```
→ Go to Section C: Pressure System Issues
```

**"Opposite Door Not Secured"**
```
→ Verify opposite door is fully closed and latched
→ Check door sensor (may be dirty or misaligned)
→ Clean sensor and try again
```

**"Manual Override Engaged"**
```
→ Check if someone manually operated airlock
→ Disengage manual override (usually lever near door)
→ System should return to automatic mode
```

**"Seal Integrity Failure"**
```
→ Proceed to Step 2 (Door Seal Issues)
```

---

### Step 2: Check Door Seals and Sensors
**Customer Action:**
```
1. Visually inspect door seal (rubber/gasket around door):
   - Any visible damage, tears, or gaps?
   - Any debris or objects preventing seal?
   - Seal appears properly seated?

2. Check door sensors (usually magnetic or optical):
   - Small sensor units around door frame
   - Clean any that appear dirty
   - Check for physical damage
```

**If seal damaged:**
```
Diagnosis: Physical seal damage
→ Door will not cycle until seal replaced
→ Seal can be temporarily patched for emergency use:
  - Use pressure-rated tape (NOT regular tape)
  - This is temporary only - schedule seal replacement
→ If no repair possible, mark airlock as unusable
→ Escalate for seal replacement
```

**If sensors dirty or damaged:**
```
→ Clean sensors with clean cloth
→ Retry airlock cycle
→ If sensor damaged, may need replacement or can be bypassed temporarily
  (requires specialist authorization)
```

---

### Step 3: Test Door Movement (Manual Mode)
**Customer Action:**
```
⚠️ Only if airlock is fully pressurized or fully depressurized (not in between)

1. Engage manual door mode:
   - Airlock Panel → Manual Mode
   - OR locate manual control lever
2. Try opening door manually:
   - Some airlocks have mechanical assist
   - Should require moderate force, not excessive
3. Observe:
   - Does door move at all?
   - Any grinding, squealing, or resistance?
   - Does door move smoothly or bind?
```

**If door won't move or binds:**
```
Diagnosis: Mechanical obstruction or hardware failure
→ Check for:
  - Foreign objects in door track
  - Ice formation (if exterior door in cold environment)
  - Structural damage to door frame
  - Hinge or motor failure
→ If obstruction visible, remove it
→ If hardware failure, escalate for repair
```

**If door moves smoothly in manual mode but won't work in auto:**
```
Diagnosis: Door motor or control system failure
→ Can use manual mode temporarily (requires crew to manually cycle)
→ Escalate for motor/control repair
```

---

## SECTION C: PRESSURE SYSTEM ISSUES

### Symptoms
- Cycle starts but doesn't complete
- "Pressure equalization timeout" error
- Takes much longer than normal to cycle
- Unusual sounds during cycle (hissing, rushing air)

### Step 1: Check Current Pressure Status
**Customer Action:**
```
1. Airlock Panel → Pressure Display
2. Note:
   - Current airlock pressure: _____ kPa
   - Ship interior pressure: _____ kPa (should be ~101 kPa)
   - Target pressure: _____ kPa
   - Pressure trend: Rising / Falling / Stable?
```

**Normal values:**
- Ship interior: ~101 kPa (1 atmosphere)
- Space/exterior: 0 kPa
- Cycle should complete pressure change in 2-5 minutes

**If pressure stuck between extremes:**
```
Diagnosis: Pump or valve issue
→ Proceed to Step 2
```

---

### Step 2: Check Airlock Pumps and Valves
**Customer Action:**
```
1. During cycle attempt, listen for:
   - Pump operating (should hear motor/pump sound)
   - Air rushing (valves opening/closing)
   - Any unusual sounds (grinding, squealing, clicking)

2. Airlock Panel → Diagnostics → Pump Status:
   - Vacuum Pump: Online/Offline?
   - Pressurization Valve: Open/Closed?
   - Vent Valve: Open/Closed?
```

**If pump not operating:**
```
Diagnosis: Pump power or hardware failure
→ Check power to pump
→ Check pump circuit breaker
→ If power present but pump not running, escalate for pump repair
```

**If valves not operating:**
```
Diagnosis: Valve control or mechanical failure
→ Manual valve override may be possible (specialist guidance required)
→ Escalate to hull systems specialist
```

---

### Step 3: Check for Pressure Leaks
**Customer Action:**
```
1. During pressurization attempt, listen around door seals for:
   - Hissing sound (indicates leak)
   - Location of sound (which seal)

2. If safe, use portable pressure gauge:
   - Monitor airlock pressure over 1 minute with all valves closed
   - Should hold steady within 1-2 kPa
   - Dropping = leak present

3. Visual inspection:
   - Look for any gaps around doors
   - Check emergency blow-out panels (should be intact)
   - Check any viewports or access panels
```

**If leak detected:**
```
Diagnosis: Seal or structural breach
→ Identify leak location
→ Small leaks may be temporarily sealable (pressure tape)
→ Large leaks require professional repair
→ If major leak, airlock may be unusable until repair
→ Escalate to hull systems specialist
```

**If no leak but pressure won't equalize:**
```
Diagnosis: Insufficient pump capacity or valve blockage
→ Pump may be degraded (old, dirty, damaged)
→ Valve may be partially blocked
→ Escalate for pump service or valve cleaning
```

---

### Step 4: Manual Pressure Equalization
**Customer Action (temporary workaround):**
```
To pressurize airlock manually (if pump failed):
1. Ensure outer door is closed and sealed
2. Locate manual pressurization valve (usually red valve near airlock)
3. Slowly open valve to allow ship air into airlock
4. Monitor pressure gauge
5. When pressure equals ship interior (~101 kPa), close valve
6. Inner door should now open

To depressurize airlock manually (if pump failed):
1. Ensure inner door is closed and sealed
2. Locate manual vent valve (usually blue valve near airlock)
3. SLOWLY open valve to vent air (rapid vent can damage equipment)
4. Monitor pressure gauge
5. When pressure equals exterior (0 kPa in space), close valve
6. Outer door should now open
```

**⚠️ CAUTION:** Manual operation is slow and should be done carefully. Rapid pressure changes can damage airlock components.

---

## SECTION D: SENSOR & CONTROL FAILURES

### Symptoms
- System reports incorrect pressure readings
- Doors show "Open" when clearly closed (or vice versa)
- Conflicting status information
- Cycle completes but system won't allow door opening

### Step 1: Calibrate Pressure Sensors
**Customer Action:**
```
1. Ensure airlock is in known state:
   - Fully pressurized (doors closed, equal to ship) OR
   - Fully depressurized (doors closed, equal to exterior)

2. Airlock Panel → Diagnostics → Calibrate Sensors

3. Follow calibration procedure:
   - System will ask to confirm current pressure state
   - Confirm actual state (pressurized or depressurized)
   - System will calibrate sensors to current reading

4. Try cycling airlock again
```

**If calibration resolves issue:**
```
Diagnosis: Sensor drift or miscalibration
→ Issue resolved
→ Schedule regular sensor calibration (quarterly recommended)
→ If drift happens frequently, sensors may need replacement
```

---

### Step 2: Test Door Position Sensors
**Customer Action:**
```
1. With door fully closed:
   - Airlock Panel → Status → Door Position
   - Should show "Closed" and "Sealed"

2. If showing incorrect status:
   - Physically verify door is actually closed
   - Clean door position sensor (usually magnetic sensor on frame)
   - Check sensor alignment

3. Manually open door slightly (if safe):
   - Status should change to "Open"
   - If doesn't change, sensor failed
```

**If sensor failed or misaligned:**
```
Diagnosis: Position sensor malfunction
→ Sensor can sometimes be manually aligned
→ May be able to bypass temporarily with override
→ Escalate to hull systems specialist for sensor replacement
```

---

## ESCALATION CRITERIA

**Escalate to Hull Systems Specialist if:**
- [ ] Person trapped in airlock (immediate - emergency response)
- [ ] Physical damage to airlock doors or seals
- [ ] Pump or valve hardware failure identified
- [ ] Pressure leak that cannot be sealed
- [ ] Sensor failures that cannot be calibrated
- [ ] Issue not resolved after 20 minutes
- [ ] All airlocks on ship affected (system-wide issue)
- [ ] Customer needs EVA operations urgently

**Escalate to Power Systems if:**
- [ ] Multiple systems offline (not just airlock)
- [ ] Power distribution issue identified

---

## WORKAROUNDS & ALTERNATIVES

### If Airlock Unusable

**Option 1: Use Alternate Airlock**
- Most ships have 2+ airlocks
- May be less conveniently located
- Fully functional alternative

**Option 2: Docking for EVA**
- If at station or near another ship
- Request docking for personnel transfer
- Avoid EVA until airlock repaired

**Option 3: Manual Cycle Operation**
- If automatic systems failed but hardware intact
- Crew can manually operate valves and doors
- Requires training and is slower
- Temporary solution until automatic systems restored

**Option 4: Emergency Egress System**
- If EVA is critical emergency
- Some ships have emergency egress hatches
- Usually one-way (can get out, can't get back in same way)
- Last resort only

---

## PREVENTION & MAINTENANCE

### Regular Maintenance
**Recommended schedule:**
1. **Monthly:**
   - Visual inspection of seals
   - Test cycle with no personnel
   - Clean door sensors

2. **Quarterly:**
   - Pressure sensor calibration
   - Lubricate door mechanisms
   - Check pump operation

3. **Annually:**
   - Replace door seals (even if appear OK)
   - Full system diagnostic
   - Pressure test (leak check)

### Warning Signs
- Cycle time increasing (taking longer)
- Unusual sounds during operation
- Doors require more force to open/close
- Intermittent sensor errors
- Visible seal wear or damage

**Address these early to prevent complete failure.**

---

## RELATED DOCUMENTATION

**Emergency Procedures:**
- [EMERG-001: Hull Breach Response](../emergency-procedures/emerg-001-hull-breach.md)

**Technical Manuals:**
- [Hull Integrity Overview](../manuals/hull-integrity/hull-integrity-overview.md)
- [Hull Inspection Procedures](../manuals/hull-integrity/hull-inspection-procedures.md)
- [Hull Repair Procedures](../manuals/hull-integrity/hull-repair-procedures.md)

**Quick Reference:**
- [Top 20 #13: Airlock Malfunction](../quick-reference/top-20-common-issues.md#13-airlock-malfunction)
- [System Interaction Matrix](../quick-reference/system-interaction-matrix.md)

**Help Desk Resources:**
- [Help Desk Index](../quick-reference/HELP-DESK-INDEX.md)
- [Escalation Guide](../quick-reference/escalation-triage-guide.md)
- [First Responder Checklist](../quick-reference/first-responder-checklist.md)

---

## DOCUMENT INFORMATION

**KB Article:** KB-234
**Version:** 1.0
**Last Updated:** Stardate 2438.11
**Author:** Technical Documentation Team
**Applies To:** All ship classes with standard airlock systems

**Revision History:**
| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Stardate 2438.11 | Initial publication |

---

**Success Rate:** Following this procedure resolves approximately 65% of airlock cycling failures at Level 1 support.

**Average Resolution Time:** 15 minutes

**Common Root Causes:**
1. Seal deterioration/damage (30%)
2. Sensor calibration drift (25%)
3. Pump or valve failure (20%)
4. Control computer crash (15%)
5. Power issues (10%)

**Safety Note:** Airlocks are safety-critical systems. When in doubt, escalate rather than risk crew safety.
