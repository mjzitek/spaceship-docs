# TRAIN-NAV-004: Navigation Computer Failure During FTL Jump

**Training Module:** Navigation Systems - Emergency Response
**Difficulty:** Expert
**Duration:** 120 minutes
**Prerequisites:** FTL Jump Procedures Certification, Emergency Navigation Training
**Last Updated:** 2847.09.14

## Scenario Overview

**Situation**: Mid-jump through hyperspace, navigation computer crashes. Crew must complete jump manually, navigate to destination without computer assistance, and restore systems. Tests crew's understanding of FTL mechanics, manual navigation skills, and crisis management.

**Learning Objectives:**
- Understand FTL jump phases and what happens if computer fails
- Execute manual jump completion procedures
- Navigate without computer assistance
- Diagnose and restore computer systems under pressure
- Make critical decisions about jump abort vs. continuation

**Ship Configuration:**
- Model: Pathfinder-Class Long-Range Explorer
- Crew: 5 (Captain, Pilot, Navigator, Engineer, Science Officer)
- FTL Drive: Horizon-2 (40 light-year range)
- Location: Mid-jump, 18 light-years from origin, 22 light-years to destination
- Jump Status: 45% complete (approx. 27 minutes into 60-minute jump)

## Initial Conditions (T+0:00)

**Time**: 14:27 ship time
**Jump Status**: Stable tunnel, routine transit

**Crew Stations:**
- Captain: Bridge command chair, monitoring overall status
- Pilot: Flight controls (minimal input needed during stable jump)
- Navigator: Navigation console, monitoring jump parameters
- Engineer: Engineering, monitoring FTL drive and reactor
- Science Officer: Science station, monitoring quantum field

**Alarm Triggers:**

```
WARNING - NAVIGATION COMPUTER FAULT
System: NAV-CPU-MAIN
Status: CRITICAL ERROR - PROCESSOR HALT
Backup: SWITCHING TO NAV-CPU-BACKUP
Backup Status: ONLINE... FAULT... OFFLINE
Result: NO NAVIGATION COMPUTER AVAILABLE
Jump Control: MANUAL MODE
```

**Bridge Display:**
```
FTL JUMP STATUS - MANUAL CONTROL REQUIRED
Jump Progress: 45% (18 LY traveled, 22 LY remaining)
Tunnel Stability: 94% (DEGRADING - manual stabilization needed)
Estimated Time Remaining: 33 minutes (if stabilized)
Navigation Computer: OFFLINE
Jump Abort Available: YES (next 8 minutes only)
```

**Initial Information Available:**

Navigator reports: "Captain, both nav computers are down! Primary crashed, backup failed to initialize. We're flying blind in hyperspace!"

Engineer reports: "FTL drive is stable for now, but without computer control, tunnel stability is dropping. Down to 94% and falling."

Pilot reports: "I've got manual controls, but I need navigation data to keep us on course. How do I know where we're going?"

## Critical Decision Point #1 (T+0:00 to T+8:00)

**Immediate Situation:**
- In hyperspace tunnel, 45% through jump
- No navigation computer (cannot calculate corrections automatically)
- Tunnel stability degrading (94% → 92% → 90%...)
- 8-minute window to abort jump and return to origin
- If abort window closes, must complete jump to destination

**Captain must decide:**

### Option A: Abort Jump, Return to Origin (Safe but Costly)

**Process:**
1. Pilot executes emergency jump abort (while still in 8-minute window)
2. FTL drive reverses quantum tunnel
3. Ship returns to origin system
4. 18 light-years of fuel and 27 minutes wasted
5. Must repair computers, then re-attempt jump (hours delay)

**Advantages:**
- Safest option (known system, familiar space)
- Can repair computers in safe environment
- Eliminates risk of lost-in-space scenario

**Disadvantages:**
- Wastes 18 LY worth of fuel (expensive: ~45,000 credits)
- Major time delay (6+ hours to repair and re-jump)
- Destination may be time-critical (cargo spoilage, passenger schedules, emergency)
- Aborting stresses FTL drive components (wear and tear)

**Outcome if chosen:**
- Ship safely returns to origin
- Scenario ends (repairs made, jump re-attempted later)
- **Score: 60/100** (safe but unimaginative, did not attempt manual navigation)

---

### Option B: Continue Jump, Manual Navigation (Challenging but Optimal)

**Process:**
1. Navigator and Pilot manually stabilize quantum tunnel
2. Navigator calculates course corrections using manual instruments
3. Engineer maintains FTL drive without computer automation
4. Complete jump to destination (22 LY remaining)
5. Repair computers after safe arrival

**Advantages:**
- Completes jump (no fuel waste, no delay)
- Demonstrates crew skill and resourcefulness
- Maintains schedule

**Disadvantages:**
- High crew workload (continuous manual input required)
- Risk of tunnel collapse if crew makes errors
- Risk of navigation error (emerging off-course)
- Stressful for crew (33 minutes of intense focus)

**Challenges:**
- Tunnel stability degrading: Requires active stabilization
- No computer: All calculations manual (math, charts, instruments)
- Jump completion: Must precisely time tunnel collapse at destination

**Outcome if chosen:**
- Proceed to Manual Navigation Phase (see below)
- **Score potential: 80-100/100** depending on crew performance

---

### Option C: Continue Jump, Attempt Computer Repair Mid-Jump (Very Risky)

**Process:**
1. Engineer attempts to reboot or repair navigation computer during jump
2. Simultaneously, Pilot and Navigator maintain jump manually
3. If computer restored, jump continues with automation
4. If repair fails, continues as Option B

**Advantages:**
- If successful, restores full automation (reduces crew workload)
- Addresses root problem immediately

**Disadvantages:**
- Diverts Engineer from FTL drive monitoring (dangerous)
- Computer repair unlikely to succeed mid-jump (unstable power, vibration)
- If repair attempt causes additional failures, situation worsens
- Low probability of success (20-30%)

**Outcome if chosen:**
- 70% chance: Repair fails, must continue with Option B (but with distracted Engineer, higher risk)
- 30% chance: Repair succeeds, computer online, jump continues normally
- **Score: 50-90/100** depending on outcome and secondary issues

---

### Option D: Do Nothing / Hesitate (Catastrophic)

**If Captain does not make decision within 8 minutes:**
- Jump abort window closes (cannot return to origin)
- Tunnel stability continues degrading without intervention
- Tunnel stability <70%: Jump tunnel collapses
- Ship drops out of hyperspace at random location (mid-interstellar space)
- Crew must navigate conventionally (sublight) to nearest system (could take months or years)
- FTL drive damaged by uncontrolled collapse (expensive repairs)

**Outcome:**
- Ship lost in deep space
- Training scenario FAILED
- **Score: 0/100**

---

## Scenario Branch: Option B Selected (Manual Navigation - Optimal Path)

**T+1:00**: Captain decides to continue jump with manual navigation

Captain orders: "We're committed. Navigator, Pilot - take manual control. Engineer, keep that drive stable. We're going to finish this jump the old-fashioned way."

### Phase 1: Stabilize Quantum Tunnel (T+1:00 to T+5:00)

**Current Status:**
- Tunnel stability: 89% and falling (1% per minute)
- Below 70%: Tunnel collapse imminent
- Crew has ~15-20 minutes to stabilize before critical

**Navigator Actions:**

1. **Switch to Manual Tunnel Stabilization**
   - Access: FTL Panel > Manual Controls > Tunnel Stabilization
   - Displays real-time tunnel geometry (3D visualization)
   - Shows quantum field distortions, gravitational perturbations

2. **Identify Instability Causes**
   - Tunnel wobble: Caused by gravitational anomaly (star system passing nearby hyperspace route)
   - Field asymmetry: One side of tunnel stronger than other
   - Tachyon flow uneven: Needs rebalancing

3. **Manual Corrections** (Navigator inputs)
   - **Adjust tachyon emitter power**: Increase starboard emitters by 8% (rebalances field)
   - **Compensate for gravitational pull**: Apply lateral thrust correction (0.3° offset)
   - **Monitor field harmonics**: Adjust QFM phase alignment (requires continuous tweaking)

**Pilot Actions:**

1. **Manual Flight Control**
   - Ship must maintain precise centerline of quantum tunnel
   - Tunnel width: ~500 meters (ship is 60 meters long, some margin)
   - Deviation >200 meters from center: Tunnel walls contact hull (catastrophic)

2. **Instrument Flying** (no external visual references in hyperspace)
   - Use tunnel position indicator (shows ship position relative to tunnel center)
   - Adjust attitude: Pitch ±0.1°, Yaw ±0.1° (tiny corrections, very sensitive)
   - Throttle: Maintain constant 0.45c relative velocity in tunnel

3. **Respond to Navigator Corrections**
   - When Navigator adjusts tunnel geometry, Pilot must compensate
   - Example: Navigator shifts tunnel 10 meters port → Pilot must adjust heading 0.05° port

**Engineer Actions:**

1. **Monitor FTL Drive Health**
   - Tachyon emitter temperature: Should be <400°C (manual mode runs hotter)
   - QFM coolant flow: Verify adequate (manual mode, no automatic adjustments)
   - Graviton compensator load: Should be <85% (overload risk if tunnel unstable)

2. **Reactor Power Management**
   - FTL drive consuming 180 MW (higher than normal due to manual stabilization)
   - Ensure reactor maintaining output
   - Divert power from non-essentials if needed (life support to minimum, lights dimmed)

3. **Emergency Preparations**
   - If tunnel collapses: Must emergency-stop FTL drive (SCRAM button ready)
   - Coolant bypass ready (if QFM overheats, emergency cooling)

**Progress Report T+5:00:**

After 4 minutes of manual corrections:

```
TUNNEL STABILITY: 91% (stabilized, no longer degrading)
Tachyon Flow: BALANCED
Field Geometry: SYMMETRIC ±2%
Ship Position: Centerline ±5 meters (excellent)
Crew Status: High workload but managing
Time Remaining: 28 minutes
```

Navigator: "Tunnel is stable, Captain. We've got it under control."

Engineer: "FTL drive is running hot but within limits. We can maintain this for 28 minutes."

Pilot: "I've got the feel for it now. We're holding centerline."

Captain: "Good work. Now, how do we make sure we arrive at the right place?"

---

### Phase 2: Manual Navigation to Destination (T+5:00 to T+33:00)

**Challenge:** Without navigation computer, crew must manually calculate and navigate to destination.

**What the computer normally does:**
- Tracks position in hyperspace (dead reckoning based on velocity and time)
- Calculates course corrections for gravitational perturbations
- Times tunnel collapse to emerge at precise destination coordinates

**What crew must do manually:**

**Navigator Duties:**

1. **Dead Reckoning Position**
   - Jump started 27 minutes ago, traveled ~18 light-years
   - Current velocity: 0.45c in tunnel (constant)
   - Remaining distance: 22 light-years
   - Estimated time: 28 minutes (need to refine)

2. **Calculate Precise Destination Coordinates**
   - Pull out star charts (physical backups, not computer)
   - Destination: Kepler Station, orbit around star HD 189733
   - Coordinates: RA 20h 00m 43s, Dec +22° 42' 39" (relative to galactic center)
   - Distance from origin: 40.2 light-years (Navigator measures on chart)

3. **Account for Stellar Motion**
   - Stars move! During 60-minute jump, destination star moves
   - HD 189733 proper motion: 0.52 arcseconds/year (toward galactic north)
   - During 60-min jump: Star moves ~60,000 km
   - Must aim for where star WILL BE, not where it WAS at jump start

4. **Gravitational Corrections**
   - Massive objects curve space, affect hyperspace route
   - Mid-route, ship passed near binary star system (gravitational pull)
   - Pull caused ~0.3 light-year deflection (must correct course)
   - Navigator calculates correction: 1.2° heading adjustment, apply over next 10 minutes

5. **Update Course Every 5 Minutes**
   - Continuous dead reckoning (velocity × time = distance traveled)
   - Mark position on chart
   - Recalculate heading to destination
   - Feed corrections to Pilot

**Pilot Duties:**

1. **Execute Navigator's Course Corrections**
   - Navigator calls out: "Come left 0.5 degrees over 2 minutes"
   - Pilot makes gradual heading change (not abrupt, destabilizes tunnel)
   - Confirm new heading achieved

2. **Maintain Tunnel Stability During Maneuvers**
   - Turning in hyperspace stresses tunnel
   - Must turn slowly, smoothly
   - Monitor stability, if drops below 85%, pause turn until restabilized

**Science Officer Duties:**

1. **Monitor for Gravitational Anomalies**
   - Use gravitational sensors to detect nearby massive objects
   - Warning: Detect star system 2 light-years off course → Alert Navigator (may need correction)

2. **Assist Navigator with Calculations**
   - Manual math required (slide rule, calculator, or mental math)
   - Two people calculating reduces errors
   - Cross-check Navigator's work

**Progress Report T+15:00:**

Halfway through manual navigation phase:

```
Jump Progress: 68% (27.2 LY traveled, 12.8 LY remaining)
Tunnel Stability: 88-92% (varying, manual adjustments maintaining)
Course Accuracy: ±0.2 LY from ideal track (acceptable)
Crew Fatigue: Moderate (18 minutes remaining)
```

Navigator: "We're on course, Captain. Estimate arrival at Kepler Station in 18 minutes, plus or minus 2 minutes."

Captain: "What's our accuracy? How close will we be?"

Navigator: "Best estimate, we'll emerge within 50,000 kilometers of station. That's within sensor range, we can navigate conventionally from there."

Pilot: "50,000 klicks? With a computer we'd hit within 500. But I'll take it."

---

### Phase 3: Jump Completion and Tunnel Collapse (T+31:00 to T+33:00)

**Critical Final Phase:**

**Challenge:** Timing tunnel collapse to emerge at destination.

**What happens at jump completion:**
1. FTL drive stops generating quantum tunnel (tachyon emitters power down)
2. Tunnel collapses in ~2 seconds
3. Ship "drops out" of hyperspace, returns to normal space
4. Location of drop-out depends on WHEN tunnel collapsed

**Timing is everything:**
- Collapse too early: Emerge short of destination (millions of km away)
- Collapse too late: Overshoot destination (fly past at high speed)
- Collapse at right time: Emerge at destination

**Without computer, Navigator must manually time collapse:**

**T+31:00** - Navigator announces: "2 minutes to destination."

**Navigator Calculations:**

1. **Estimate Time to Destination**
   - Current position: 39.1 LY from origin (Navigator's dead reckoning)
   - Destination: 40.2 LY from origin
   - Remaining: 1.1 LY
   - Velocity: 0.45c in tunnel
   - Time remaining: 1.1 LY ÷ 0.45 LY/year = 2.44 years if at normal speed...
   - **Wait, that's wrong!** In hyperspace, effective velocity much higher
   - Recalculate using hyperspace time dilation factor
   - Actual time remaining: 120 seconds

2. **Account for Tunnel Collapse Duration**
   - Tunnel doesn't collapse instantly, takes ~2 seconds
   - Must initiate collapse 2 seconds before desired drop-out point
   - Initiate collapse at: T+32:58 (118 seconds from now)

3. **Continuous Updates**
   - Every 10 seconds, recalculate based on latest position
   - Refine estimate: Now showing 115 seconds... 110... 105...

**T+32:00** - Navigator: "1 minute to collapse point."

**T+32:30** - Navigator: "30 seconds. Engineer, prepare to shut down tachyon emitters on my mark."

Engineer confirms: "Ready to power down emitters, standing by."

**T+32:50** - Navigator: "10 seconds... 9... 8..."

Pilot: "Throttle at zero, ready for drop-out."

**T+32:55** - Navigator: "5... 4... 3... 2... 1... MARK!"

Engineer: "Powering down tachyon emitters NOW!"

**T+32:57** - Tunnel begins collapse

```
TUNNEL COLLAPSE INITIATED
Tachyon Emitters: OFFLINE
Quantum Field: DISSIPATING
Tunnel Stability: 90% → 70% → 40% → 10%
Ship Status: TRANSITION TO NORMAL SPACE
```

**T+33:00** - Drop-out to normal space

```
FTL JUMP COMPLETE
Normal Space Coordinates: [CALCULATING...]
Distance to Kepler Station: [SCANNING...]
Ship Status: All systems nominal
Crew Status: [EXHAUSTED]
```

**Sensor Results:**

```
POSITION: Kepler System, HD 189733 orbit
DISTANCE TO KEPLER STATION: 47,300 km (within target range!)
ERROR: 0.19 LY lateral offset (acceptable for manual navigation)
CONVENTIONAL NAVIGATION TIME: 22 minutes at sublight
```

**Outcome: SUCCESS!**

Captain: "Outstanding work, everyone. Navigator, Pilot - that was textbook manual navigation. 47,000 klicks from station with no computer. I'm impressed."

Navigator: "Thank you, sir. I'll be honest, I was sweating that last 30 seconds."

Engineer: "FTL drive is secure, reactor nominal. We're ready for conventional approach to station."

Pilot: "Engaging sublight engines, plotting intercept with Kepler Station. ETA 22 minutes."

---

## Post-Jump Actions (T+33:00 to T+60:00)

### Immediate: Conventional Navigation to Station

**Pilot's Task:**
- Sublight engines to station (47,300 km at ~36 m/s average = 22 minutes)
- Standard docking approach
- Allows crew brief rest after intense jump

### Computer Diagnosis and Repair

**Engineer's Task:**

1. **Assess Damage**
   - Access navigation computer bay
   - Primary computer: Processor failure (motherboard fried)
   - Backup computer: Failed to initialize (software corruption)

2. **Root Cause Analysis**
   - Probable cause: Power surge during jump initialization
   - Surge damaged primary, corrupted backup
   - Surge protection circuit breaker tripped (found in electrical panel)

3. **Repair Options:**
   - **Option A**: Replace primary computer processor board (Part #: NAV-CPU-BOARD-A, 3,500 credits, 4-hour install)
   - **Option B**: Reload backup computer software from emergency backup (2 hours)
   - **Option C**: Both (most thorough, 6 hours total)

4. **Immediate Action:**
   - Reload backup software (gets one computer operational quickly)
   - Order replacement processor board for primary
   - Install surge protection upgrade (prevent recurrence)

### Crew Debriefing

**Captain conducts debriefing:**

**What went well:**
- Quick decision to continue jump (demonstrated confidence and skill)
- Effective teamwork (Navigator, Pilot, Engineer coordinated perfectly)
- Manual tunnel stabilization successful
- Navigation accuracy impressive (47,300 km error on 40 LY jump = 0.00001% error)

**What could improve:**
- Earlier recognition of power surge risk (should have caught during pre-flight)
- Backup computer should not fail if primary fails (need better isolation)
- Crew fatigue high (manual navigation exhausting, need periodic drills to build stamina)

**Lessons Learned:**
- Manual navigation still possible (critical skill, must maintain proficiency)
- Redundancy is not always redundant (backup failed too)
- Pre-flight power system checks critical (would have caught surge risk)

### Incident Report

**Required documentation:**

1. **Ship's Log Entry:**
   - Navigation computer failure during jump
   - Manual navigation successfully completed
   - Arrival time, position accuracy
   - Crew commendations for performance

2. **Maintenance Log:**
   - Primary nav computer: Failed, requires processor replacement
   - Backup nav computer: Software reloaded
   - Power surge protection: Upgraded

3. **ORSM Incident Report:**
   - Computer failure described
   - May be manufacturing defect (warranty claim)
   - Recommend other ships check surge protection

4. **Crew Training Records:**
   - Manual navigation proficiency demonstrated
   - Navigator, Pilot, Engineer: Commended for performance
   - Recommend manual navigation scenario for quarterly training

---

## Scenario Branch: Option A Selected (Jump Abort)

**T+3:00**: Captain decides to abort jump

Captain orders: "This is too risky without computers. Pilot, execute emergency jump abort, now!"

### Abort Procedure

**Pilot Actions:**

1. **Initiate Abort Sequence**
   - Access: FTL Panel > Emergency > ABORT JUMP
   - Confirm abort (requires two-button press to prevent accidental)
   - System begins abort procedures

2. **Tunnel Reversal**
   - FTL drive reverses tachyon flow
   - Quantum tunnel begins collapsing from forward end (instead of aft)
   - Ship decelerates in tunnel
   - Ship "backs out" to origin point

3. **Abort Duration**
   - 45% through jump, so 45% return time
   - Approximately 27 minutes to return to origin

**During Abort:**
- Crew monitors tunnel stability (abort stresses tunnel differently)
- High G-forces possible (up to 3g deceleration, crew uncomfortable but safe)
- FTL drive runs hot (abort is hard on components)

**T+30:00** - Ship emerges at origin system

```
JUMP ABORTED SUCCESSFULLY
Position: Origin system (Vega Station orbit)
Ship Status: All systems nominal (FTL drive elevated temperature)
Fuel Used: 18 LY worth (~45,000 credits wasted)
Time Lost: 60 minutes (jump + abort) + repair time + re-jump time
```

**Post-Abort:**

1. **Computer Repair** (6 hours at station, professional technicians)
2. **FTL Drive Cooldown** (2 hours, drive must cool before re-jump)
3. **Refuel** (replace used fuel, 45,000 credits)
4. **Re-Jump to Destination** (60 minutes for successful jump)

**Total Delay: 9+ hours, 45,000 credits cost**

**Outcome:**
- Safe return, successful computer repair
- Major delay and expense
- **Score: 60/100** (safe but costly, did not demonstrate manual navigation skill)

---

## Scenario Branch: Option C Selected (Repair Attempt Mid-Jump)

**T+2:00**: Captain orders Engineer to attempt computer repair during jump

Captain: "Engineer, get down to the computer bay and get those systems back online. We need that computer."

Engineer: "Sir, I should be monitoring the FTL drive during jump..."

Captain: "We'll manage. Get those computers fixed."

### Repair Attempt

**Engineer Actions:**

1. **Access Computer Bay** (2 minutes to reach from engineering)
2. **Diagnose Failure** (5 minutes):
   - Primary: Processor halt (motherboard damaged)
   - Backup: Software corruption
3. **Attempt Repair:**
   - Try rebooting primary (fails, hardware damage)
   - Try reloading backup software (difficulty: power unstable during jump, 30% success chance)

**Random Outcome Determination:**

**70% Chance - Repair Fails:**

T+10:00 - Engineer reports: "Captain, I can't get either computer online. Primary has hardware failure, backup won't reload software. The power is too unstable during jump."

Captain: "Return to engineering and monitor the drive. We'll finish this manually."

**Result:**
- 8 minutes wasted on failed repair
- Engineer distracted from FTL monitoring
- During engineer's absence, tunnel stability dropped to 84% (Pilot and Navigator struggling)
- Now must complete jump manually but with reduced tunnel stability (harder)

**Completion:**
- Continue as Option B scenario, but starting at 84% stability instead of 91%
- Higher risk of tunnel collapse
- If crew performs well, still successful
- **Score: 70-85/100** (successful but made situation harder)

**30% Chance - Repair Succeeds:**

T+12:00 - Engineer reports: "Captain, I got the backup computer online! Software reloaded successfully."

Captain: "Outstanding. Transferring jump control to computer."

**Result:**
- Computer resumes automated control
- Tunnel stability improves (computer better than manual)
- Jump completes normally
- Engineer returns to FTL monitoring

**Completion:**
- Jump completes successfully at T+33:00
- Computer-assisted, no manual navigation required
- **Score: 85/100** (successful and restored computer, but risky gamble)

---

## Debriefing and Assessment

### Scoring Criteria

**Optimal Performance (95-100 points):**
- Chose Option B (manual navigation)
- Successfully stabilized tunnel (>85% stability maintained)
- Accurate navigation (arrival within 100,000 km of station)
- Effective crew coordination (no errors, smooth communication)
- Tunnel collapse perfectly timed (±5 seconds)
- No damage to FTL drive or ship systems
- Crew fatigue managed (breaks for non-critical personnel)

**Excellent Performance (85-94 points):**
- Chose Option B, successful completion
- Tunnel stability 80-85% (some struggle but maintained)
- Arrival within 200,000 km of station
- Minor coordination issues but recovered quickly
- Tunnel collapse timing ±10 seconds (minor overshoot/undershoot)

**Acceptable Performance (70-84 points):**
- Chose Option B or C, successful completion
- Tunnel stability briefly dipped to 75-79% but recovered
- Arrival within 500,000 km of station (acceptable error)
- Communication issues but no critical mistakes

**Marginal Performance (60-69 points):**
- Chose Option A (abort) - safe but expensive
- Or chose Option B/C but struggled significantly
- Tunnel stability dropped below 75% temporarily
- Arrival >500,000 km from station (requires extended conventional navigation)
- Minor damage to FTL systems from stress

**Failure (<60 points):**
- Chose Option D (hesitation) or failed to stabilize tunnel
- Tunnel collapsed during jump
- Ship dropped out mid-space (random location)
- Crew errors caused FTL drive damage
- Unable to complete jump

### Key Learning Points

1. **Understand Computer Limitations**
   - Computers fail, crew must know manual procedures
   - Backup systems can fail simultaneously (common-mode failure)
   - Manual skills must be maintained through regular practice

2. **Decision Making Under Pressure**
   - Abort vs. Continue: Assess risk/benefit quickly
   - Time-limited decisions (8-minute abort window)
   - Balance safety vs. efficiency

3. **Manual Navigation Skills**
   - Dead reckoning in hyperspace (velocity × time)
   - Account for stellar motion, gravitational effects
   - Cross-check calculations (two people verify math)
   - Timing tunnel collapse precisely

4. **Crew Coordination**
   - Navigator calculates, Pilot executes
   - Engineer monitors systems, reports status
   - Science Officer assists with calculations, warns of hazards
   - Captain coordinates, makes final decisions

5. **Fatigue Management**
   - Manual navigation is exhausting (intense concentration 30+ minutes)
   - Crew must maintain performance despite stress
   - Training builds stamina for real emergencies

6. **Preventive Maintenance**
   - Pre-flight computer checks critical
   - Surge protection prevents failures
   - Regular computer diagnostics catch issues before critical failure

## Related Training Modules

- TRAIN-NAV-001: Basic Manual Navigation
- TRAIN-NAV-002: FTL Jump Emergency Procedures
- TRAIN-NAV-003: Computer System Diagnosis and Repair
- TRAIN-EMERG-001: Multi-System Failure Response

## Related Documentation

- KB-012: FTL Jump Fails (troubleshooting)
- FTL Jump Procedures Manual
- Navigation Computer Manual
- ERR-NAV-350: Computer Fault Error Codes

---

**Instructor Notes**: This scenario is EXPERT level. Most crews will struggle initially. The goal is not perfect performance first try, but rather demonstrating that manual navigation IS possible with training. Use this scenario to identify gaps in manual navigation skills and provide targeted follow-up training. Emphasize that while computers are reliable, manual backup skills are essential for long-range exploration where help may be days or weeks away.

**Recommended Frequency**: Run this scenario annually for all long-range/FTL-capable crews. More frequent practice (quarterly) for exploration vessels operating in uncharted space.

**Variations**:
- Vary jump distance (longer jumps = more fatigue, more errors accumulate)
- Add secondary failures (FTL drive overheating, gravitational anomaly)
- Vary crew experience (mix experienced and novice, see how mentoring works under pressure)
- Time-critical cargo (adds pressure to continue rather than abort)
