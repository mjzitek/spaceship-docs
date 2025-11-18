# KB-045: Cargo Shifted During Transit - Detection and Response

**Article ID:** KB-045
**Category:** Cargo Management
**Severity:** High
**Last Updated:** 2847.09.14
**Author:** ORSM Technical Support

## Problem Description

Cargo has shifted position during flight, causing load imbalance, potential damage, and safety hazards. This typically occurs during acceleration, deceleration, or course changes when cargo restraints fail or are inadequate.

## Symptoms

- CMS load balance warning (yellow, orange, or red alert)
- Unusual sounds from cargo bay (thuds, sliding, crashes)
- Vessel handling changes (pull to one side, difficulty maneuvering)
- Visible cargo out of position (if cameras or visual inspection available)
- Cargo bay pressure changes (if cargo damaged pressure seal)
- Acceleration response anomalies (vessel doesn't respond as expected to thrust)

## Affected Vessels

All vessel classes carrying cargo, particularly:
- Freighters with heavy or bulk cargo
- Vessels with inadequate restraint systems
- Ships experiencing emergency maneuvers
- Vessels with improperly loaded cargo

## Root Causes

### Restraint Failure
- Cargo straps broke or loosened
- Magnetic locks disengaged
- Cargo bars shifted or collapsed
- Restraint system not rated for cargo weight

### Improper Loading
- Cargo not secured properly during loading
- Weight distribution errors
- Center of mass not calculated correctly
- Incompatible cargo stacked together

### Excessive Acceleration
- Emergency maneuvers exceeded safe limits for loaded cargo
- Combat maneuvers
- Collision avoidance
- Rapid course changes

### Equipment Failure
- Deck plating failure
- Magnetic lock power loss
- Automated restraint system malfunction
- Structural damage to cargo bay

## Immediate Actions

### Step 1: Reduce Acceleration (0-30 seconds)

**CRITICAL**: Continuing high acceleration with shifted cargo is extremely dangerous.

1. **Reduce thrust to minimum safe level**
   - Lower main engine power
   - Disable automated maneuvering
   - Minimize attitude adjustments
   - Coast if safe to do so

2. **Disable artificial gravity in cargo bay** (if equipped and safe)
   - Prevents cargo from continuing to fall/slide
   - Makes cargo "float" reducing stress on structure
   - WARNING: Only if cargo bay unpressurized or crew evacuated

3. **Sound alarm**
   - Alert all crew to cargo shift
   - Order crew to stay clear of cargo bay
   - Do not enter bay while vessel maneuvering

### Step 2: Assess Situation (1-5 minutes)

1. **Check CMS load balance display**
   - How far off-center is center of mass?
   - Yellow: Minor shift, manageable
   - Orange: Significant shift, restrict maneuvering
   - Red: Critical shift, vessel control compromised

2. **Review cargo bay sensors**
   - Weight distribution map
   - Shift detection alerts
   - Which cargo items moved
   - Extent of movement

3. **Visual inspection (if safe)**
   - Use internal cameras
   - View through cargo bay windows
   - Do NOT enter bay yet (cargo may still be moving)

4. **Check for secondary damage**
   - Hull integrity (shifted cargo may have damaged hull)
   - Pressure seals
   - Power systems
   - Adjacent compartments

### Step 3: Stabilize Vessel (5-15 minutes)

1. **Compensate for imbalance (if possible)**
   - Shift fuel between tanks to counter cargo imbalance
   - Adjust thrust vectoring
   - Use RCS (reaction control system) for attitude control
   - May need asymmetric thrust to maintain course

2. **Bring vessel to stable condition**
   - Match velocity with nearby objects (eliminate relative motion)
   - Orient vessel to minimize stress from imbalance
   - Hold position and attitude

3. **Calculate safe maneuvering envelope**
   - Maximum safe acceleration with current imbalance
   - Turning limits
   - Braking distance

## Detailed Response Procedures

### If Load Imbalance is Minor (Yellow Alert)

**Characteristics**:
- Center of mass off by <10%
- Vessel still handles normally with care
- No immediate danger

**Actions**:
1. Reduce speed by 30-50%
2. Avoid sharp maneuvers
3. Plan to inspect and re-secure cargo at next stop or when safe
4. Continue transit cautiously
5. Monitor continuously for worsening

**Timeline**: Can defer re-securing for hours to days if monitored

### If Load Imbalance is Significant (Orange Alert)

**Characteristics**:
- Center of mass off by 10-25%
- Vessel handling noticeably affected
- Maneuvering restricted

**Actions**:
1. Reduce speed significantly (50-70% reduction)
2. Limit acceleration and turns
3. Plot course avoiding hazards (cannot maneuver aggressively)
4. Plan to re-secure cargo within hours
5. Consider diverting to nearest port if cannot safely re-secure

**Timeline**: Must address within 2-6 hours

### If Load Imbalance is Critical (Red Alert)

**Characteristics**:
- Center of mass off by >25%
- Vessel control severely compromised
- May be tumbling or unable to maintain attitude
- Structural stress warning

**Actions**:
1. **EMERGENCY STOP**
   - Cut all main engines
   - Use RCS only for stabilization
   - Do not attempt maneuvering

2. **Assess whether vessel controllable**
   - If yes: Hold position, proceed to re-securing immediately
   - If no: May need to jettison cargo to regain control

3. **Immediate cargo re-securing**
   - Cannot defer, must fix now
   - See detailed procedure below

4. **Consider jettison if necessary**
   - If cannot re-secure
   - If structural failure imminent
   - If crew safety at risk

**Timeline**: Must address immediately (minutes, not hours)

## Re-Securing Cargo Procedure

### Preparation

1. **Ensure vessel stable**
   - All acceleration stopped
   - Attitude control only
   - Artificial gravity off in cargo bay

2. **Assemble team and equipment**
   - Minimum 2 crew (safety requirement)
   - Cargo straps, bars, and restraints
   - Tether lines for crew
   - Portable terminals showing CMS data
   - Emergency patch supplies (in case hull damaged)

3. **Safety briefing**
   - Identify shifted cargo
   - Plan for re-securing
   - Escape routes if cargo shifts again
   - Communication protocols

### Entering Cargo Bay

1. **Don safety equipment**
   - Tether to secure points
   - Hard hats (falling cargo risk)
   - Gloves
   - Emergency respirator nearby

2. **Enter cautiously**
   - Watch for unstable cargo
   - Listen for creaking or shifting sounds
   - Stay near exits

3. **Initial assessment**
   - Which items shifted
   - Damage to cargo or bay
   - Broken restraints
   - Hull damage

### Re-Securing Process

**For Small Cargo Shifts** (<1 meter movement):

1. **Reposition cargo if needed**
   - Use grav-lift or manual pushing (in zero-G)
   - Return to original position
   - Check against load plan

2. **Inspect old restraints**
   - Why did they fail?
   - Replace if broken
   - Tighten if loosened

3. **Apply new restraints**
   - Use additional straps/bars
   - Over-secure (better safe than sorry)
   - Test by pulling (should not budge)

**For Large Cargo Shifts** (>1 meter movement):

1. **Reassess load distribution**
   - May not be able to return to original position
   - Recalculate center of mass with new positions
   - Plan new securing layout

2. **Redistribute other cargo if needed**
   - Move other items to balance shifted cargo
   - CMS computer can suggest new arrangement
   - May need to shift multiple items

3. **Secure in new positions**
   - Use maximum restraints
   - Consider emergency welding or bolting for heavy items
   - Verify load balance restored

4. **Update cargo manifest**
   - Log new positions
   - Update CMS database

### Verification

1. **Visual check**
   - All cargo secured
   - Restraints tight
   - No loose items

2. **CMS computer verification**
   - Run load balance calculation
   - Should show green (balanced)
   - All items accounted for

3. **Test maneuver**
   - Small acceleration (10% thrust)
   - Monitor for any movement
   - Listen for sounds
   - Check CMS continuously

4. **Full test**
   - Gradually increase to normal acceleration
   - Try gentle turns
   - Monitor for 15-30 minutes
   - If stable, resume transit

## If Cannot Re-Secure

### Jettison Procedure (Emergency Only)

**WARNING**: Jettison only as last resort. Creates navigation hazard and cargo loss.

**When to jettison**:
- Cannot re-secure and imbalance critical
- Structural damage imminent
- Crew safety at risk
- No other option

**Procedure**:
1. Calculate which cargo to jettison (minimum needed to restore balance)
2. Verify safe to jettison (no vessels nearby, not in orbit of inhabited planet)
3. Seal remaining cargo
4. Open cargo bay doors or airlock
5. Push/eject cargo into space
6. Close bay doors
7. Verify load balance restored
8. Mark jettison location (navigation hazard warning)
9. Report to authorities

### Request Assistance

If cannot handle alone:
- Call for tug assistance (can stabilize vessel)
- Request docking with station (repair in controlled environment)
- Emergency services if critical

## Prevention

### Proper Loading Procedures

1. **Follow load plan**
   - CMS computer calculates optimal positions
   - Heavy cargo low and centered
   - Balanced port/starboard
   - Secure as you load (not after)

2. **Adequate restraints**
   - Use restraints rated for cargo weight
   - Multiple redundant restraints
   - Inspect restraints before loading

3. **Post-loading inspection**
   - Visual check all cargo secured
   - Test restraints (pull test)
   - CMS verification
   - Log in manifest

### During Transit

1. **Monitor CMS continuously**
   - Regular checks of load balance
   - Watch for shift warnings
   - Trend analysis (is balance degrading?)

2. **Limit acceleration**
   - Don't exceed rated limits for cargo type
   - Smooth acceleration/deceleration
   - Avoid sharp maneuvers unless emergency

3. **Periodic inspections**
   - Check cargo bay during long transits
   - Listen for unusual sounds
   - Re-tighten restraints if needed

### Regular Maintenance

1. **Inspect restraint systems**
   - Check straps for wear
   - Test magnetic locks
   - Verify structural integrity
   - Replace worn components

2. **CMS sensor calibration**
   - Ensures accurate load balance data
   - Monthly calibration recommended
   - Replace failed sensors

## Related Issues

- **KB-001**: Reactor Won't Start (power loss may cause magnetic lock failure)
- **KB-027**: Low Oxygen Alert (hull damage from shifted cargo)
- **ERR-CARGO-200**: Load Imbalance Warning
- **EMERG-011**: Cargo Bay Emergency Procedures

## Technical Support

**If you need assistance**:
- **ORSM Support Line**: Load planning and re-securing guidance
- **Emergency Services**: If situation critical
- **Cargo Specialist**: Complex cargo issues

---

## Success Story

*"Our freighter 'Dusty Runner' had 200 tons of ore shift during emergency evasion maneuver. Load balance went red, vessel nearly uncontrollable. Followed KB-045 procedure: stopped acceleration, assessed damage, spent 3 hours carefully re-distributing and re-securing cargo. CMS went back to green. Slow trip to port, but we made it. Could've been disaster if we'd tried to keep flying with that imbalance."*

— Captain Rodriguez, Asteroid Belt Freight Services

---

**Remember**: Shifted cargo is not just an inconvenience—it's a serious safety hazard that can lead to loss of control, structural failure, or collision. Always secure cargo properly before departure and respond immediately to shift warnings.
