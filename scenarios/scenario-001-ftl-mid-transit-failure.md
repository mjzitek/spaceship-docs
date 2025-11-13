# Training Scenario: FTL Mid-Transit Emergency

**Scenario ID:** TRAIN-NAV-001
**Category:** Navigation Systems - FTL Drive
**Difficulty Level:** Advanced
**Training Purpose:** Emergency response to FTL tunnel instability during transit
**Estimated Duration:** 45-60 minutes
**Prerequisites:** FTL operation certification, emergency procedures training

## Scenario Overview

Support agent receives distressed call from vessel experiencing tunnel stability degradation during active FTL jump. Agent must guide customer through assessment, stabilization attempts, and possible emergency abort decision while vessel is mid-transit in quantum tunnel.

**Learning Objectives:**
- Diagnose FTL system issues during active transit
- Guide customer through real-time emergency decision making
- Understand FTL emergency abort risks vs. continuing deteriorating jump
- Apply troubleshooting under extreme time pressure
- Manage customer stress during life-critical situation

## Initial Contact

### Customer Opening Statement

**Vessel:** Independent freighter "Dust Runner"
**Location:** In FTL transit, 18 hours into 36-hour jump
**Crew:** 3 (Captain, Engineer, Cargo Handler)
**FTL Drive:** Horizon-2 (commercial)
**Destination:** Kepler Station, 42 light-years from origin

**Customer (Captain, voice stressed):**

> "Support, this is Captain Vex of the Dust Runner, we need help NOW. We're in the middle of an FTL jump and something's wrong. The tunnel stability indicator dropped from 97% to 89% about ten minutes ago and it's still falling. We're at 87% now. The ship's shaking worse than I've ever felt, and my engineer says we've never seen it this bad. What do we do? Should we abort the jump?"

### Initial Information Display

**FTL Drive Status (per customer):**
- Tunnel Stability: 87% (and decreasing slowly)
- Tachyon Field Intensity: 520 TU (normal is 450-600)
- QFM Core Temperature: 1,350°C (normal is 800-1,200)
- Graviton Compensator Load: 78% (normal is 40-70%)
- Power Draw: 75 MW (normal for Horizon-2)
- Time in Transit: 18 hours
- Estimated Time Remaining: 18 hours
- Vibrations: Significant, increasing

**Q-Core Reactor:**
- Output: 80% capacity
- Temperature: 2,200°C (normal)
- All other parameters normal

## Phase 1: Immediate Assessment (5 minutes)

### Key Questions to Ask

**Agent should gather:**

1. **"What's your current tunnel stability reading right now?"**
   - **Answer**: "86%... no wait, 85%. It just dropped again."
   - **Purpose**: Establish baseline and rate of decline

2. **"How fast is the stability dropping? Approximately how much per minute?"**
   - **Answer**: "Started at 97% ten minutes ago, now 85%. So about 1% every minute or so."
   - **Purpose**: Calculate time until critical threshold (85% = emergency abort required)

3. **"What's your QFM core temperature reading?"**
   - **Answer**: "1,350°C and it's been creeping up. Started this jump at 1,100°C."
   - **Purpose**: Identify if QFM overheating is contributing

4. **"Have any error codes appeared on the FTL panel?"**
   - **Answer**: "Yes, E-NAV-515 - Tunnel Stability Below Minimum. And... E-NAV-520 just appeared - Graviton Compensator Overload."
   - **Purpose**: Confirm diagnostics and identify multiple system stress

5. **"Is your Q-Core reactor maintaining steady power output?"**
   - **Answer**: "Yes, holding at 80%. No fluctuations."
   - **Purpose**: Rule out power supply issues

### Expected Agent Response

Based on information gathered, agent should:

1. **Acknowledge severity**: "Captain, I understand this is a serious situation. Tunnel stability at 85% is approaching the critical threshold. We need to work quickly but carefully."

2. **Establish timeline**: "At the current rate of decline, you have approximately 5-10 minutes before stability reaches 85%, which is our abort threshold. However, stability can sometimes stabilize on its own. Let's try some corrective actions first."

3. **Reassure but be honest**: "The good news is your reactor is stable and you still have options. The risk is if we can't stabilize the tunnel, you'll need to make an abort decision soon."

## Phase 2: Stabilization Attempts (10-15 minutes)

### Corrective Action 1: Increase Tachyon Field Intensity

**Agent Instruction:**
> "First, let's try to strengthen the tunnel. Go to your FTL control panel, find the Tachyon Field Intensity control. What's your current reading?"

**Customer:** "520 TU."

**Agent Instruction:**
> "Increase it by 50 TU to 570. Do this gradually - use the up arrow to increase by 10 TU every 10 seconds or so."

**Customer Actions (via engineer):**
- Increase field intensity 520 → 570 TU
- Monitor stability response

**Expected Result:**
- Tunnel stability drop rate slows
- Stability at 84% and holding (stopped declining for now)
- QFM temperature increases slightly to 1,380°C
- Vibrations reduce somewhat

**Customer:** "Okay, stability stopped dropping. We're holding at 84%. Temperature went up a bit to 1,380. Is that okay?"

**Agent Response:**
> "Yes, that's within acceptable range. The increased field is drawing more power and generating more heat, but it's stabilizing the tunnel. Monitor closely for the next few minutes. Let me know immediately if stability starts dropping again or if QFM temperature exceeds 1,400°C."

### Corrective Action 2: Verify Power Stability

**Agent Instruction:**
> "While we monitor, let's make sure your reactor is maintaining adequate power. Check your Q-Core reactor output. It should still be at 80% or higher."

**Customer:** "Reactor's at 79%, dropped 1% since we increased the field."

**Agent Instruction:**
> "That's normal - the increased tachyon field requires more power. As long as it stays above 75%, you're fine. If it drops below 75%, we'll need to reduce non-essential power consumption."

### Situation Development (Complication)

**After 3 minutes of apparent stability:**

**Customer (increasingly concerned):**
> "Uh, support... stability just dropped to 83%. And compensator load is at 82% now. Temperature is 1,400°C. What's happening?"

**Teaching Point:**
- Initial corrective action bought time but didn't solve root cause
- Graviton compensator overload suggests external gravitational interference
- Temperature at upper limit of safe range
- Stability continuing to degrade despite increased field

## Phase 3: Critical Decision Point (5-10 minutes)

### Advanced Diagnosis

**Agent should deduce:**

The combination of:
- Graviton compensator overload (82%, normal is 40-70%)
- Rising QFM temperature
- Continuing stability degradation despite increased tachyon field
- Mid-transit location (18 hours into 36-hour jump)

**Likely indicates:** Vessel is passing through unexpected gravitational field - possibly uncharted stellar object, rogue planet, or dense dark matter region.

**Agent Instruction:**
> "Captain, the graviton compensator overload tells me you're encountering gravitational interference along your jump path. This could be an uncharted mass or dense region. The question is whether you'll pass through it and conditions will improve, or if it will get worse."

**Customer:** "Can we tell which?"

**Agent Instruction:**
> "Not with certainty. If it's a localized mass, compensator load should peak and then decrease as you move past it. If it's a large region or conditions worsen, we may not be able to maintain the tunnel. "

### Abort vs. Continue Decision

**Agent must present options:**

**Option 1: Continue and Monitor**
- **Pro**: May pass through interference zone, conditions improve
- **Pro**: Avoids rough emergency abort
- **Con**: If conditions worsen, may be forced to abort at even worse conditions
- **Con**: Risk of tunnel collapse if stability drops below 85%

**Option 2: Emergency Abort Now**
- **Pro**: Exit tunnel while still have some control (84% stability)
- **Pro**: Avoid worse conditions if interference increasing
- **Con**: Rough exit, spatial position uncertain
- **Con**: FTL drive will need inspection before next jump
- **Con**: Will be stranded far from destination and origin

**Agent should ask:**
> "Captain, this is your decision, but I can provide guidance. If you abort now at 84% stability, you'll have a rough but manageable exit. If you continue and stability drops below 85%, you may be forced into a worse abort. However, if you pass through this interference, you could complete the jump normally. What are your mission priorities? Is your cargo time-sensitive? Do you have adequate supplies for a delay?"

**Customer Response:**
> "We're carrying medical supplies to Kepler Station - they're expecting us. But crew safety is priority. How long do we have to decide?"

**Agent Calculation:**
> "At current decline rate, maybe 5 minutes before you reach 85%. But decline could accelerate. I recommend deciding in the next 2-3 minutes."

### Scenario Branch Point

**BRANCH A: Customer Chooses to Continue**

**Customer:** "We'll continue. Monitor closely and tell me if I need to abort."

**Agent Response:**
> "Understood. Watch your displays constantly. If stability hits 85% or compensator reaches 90%, abort immediately. If QFM temperature hits 1,500°C, abort immediately. I'll stay on the line with you."

**30 seconds later:**

**Customer:** "Stability is 82%. Compensator is 85%. Should we abort?"

**Agent:** "Not yet, but you're very close to threshold. Prepare your hand on the abort button. If either gets worse in the next 30 seconds, press abort."

**Another 30 seconds:**

**Customer:** "Wait... compensator load is dropping. 84%... 82%... 80%. Stability stopped dropping - holding at 82%."

**Agent:** "Excellent! You're passing through the interference. Continue monitoring. Compensator load should continue decreasing."

**Resolution:** Vessel successfully passes through gravitational anomaly. Over next 10 minutes, tunnel stability gradually improves to 88%, compensator load returns to normal 65%, temperature decreases to 1,250°C. Jump completes normally.

**Agent Debrief:**
> "Captain, you made the right call. You've cleared the interference zone. I recommend logging this location and gravitational anomaly for the navigation database. When you arrive at Kepler Station, have your FTL drive inspected to ensure no damage from the stress. The elevated temperatures and compensator load can cause component wear."

**BRANCH B: Customer Chooses to Abort**

**Customer:** "No, this is too risky. We're aborting. How do we do this?"

**Agent Response:**
> "Understood. Locate the red FTL ABORT button. Press and hold for 3 seconds until you hear a confirmation tone. Brace for rough exit - make sure all crew are secured."

**Customer:** "Pressing now... holding... confirmation tone. Here we go!"

**Expected Sequence:**
- Significant vibration for 5-10 seconds
- Visual distortion as tunnel collapses
- Sharp "snap back" sensation as vessel returns to normal space
- Some crew nausea or disorientation (normal)

**30 seconds later:**

**Customer:** "We're out. That was rough but everyone's okay. Where the hell are we?"

**Agent Response:**
> "Check your navigation computer for position. You'll likely be off your planned route - emergency aborts can cause spatial displacement."

**Customer:** "Navigation says we're... 26 light-years from our origin point, 23 light-years from Kepler Station. We're in empty space between systems."

**Agent Response:**
> "That's within expected range for emergency abort. Your FTL drive will now enter cooldown for 6 hours minimum. Do not attempt another jump until cooldown complete AND you've run a full diagnostic on the FTL system. The stress from the abort may have damaged components. Check tachyon emitters especially."

**Resolution:** Vessel safe but stranded in interstellar space. Must wait 6 hours for FTL cooldown, then run diagnostics. Depending on diagnostic results, may be able to continue to Kepler Station (additional 23 light-year jump) or may need to return to origin for repairs.

## Post-Scenario Debrief

### Key Learning Points

1. **FTL tunnel instability** can be caused by:
   - Gravitational interference (uncharted masses)
   - QFM degradation or overheating
   - Tachyon emitter failures
   - Power fluctuations

2. **Corrective actions** during transit:
   - Increase tachyon field intensity (first response)
   - Ensure adequate reactor power
   - Monitor all parameters continuously
   - Identify trends (improving vs. worsening)

3. **Abort decision criteria**:
   - Tunnel stability <85%: Mandatory abort
   - QFM temperature >1,600°C: Abort recommended
   - Graviton compensator >90%: Abort recommended
   - Multiple deteriorating parameters: Strongly consider abort

4. **Emergency abort consequences**:
   - Spatial displacement (unpredictable exit location)
   - Component stress/damage requiring inspection
   - Mandatory cooldown before next jump
   - Possible mission delay or failure

5. **Customer stress management**:
   - Acknowledge severity honestly
   - Provide clear options with pros/cons
   - Give customer control of decision while guiding
   - Stay calm and methodical even under pressure
   - Remain on line during crisis for support

### Common Mistakes to Avoid

- **Overriding customer's abort decision**: Agent should guide but customer has final say
- **Failing to establish timelines**: Customer needs to know how long they have to decide
- **Ignoring multiple warning signs**: Compensator overload + temperature + stability = serious
- **Not explaining abort consequences**: Customer needs full picture to decide
- **Panicking or showing uncertainty**: Agent must project calm competence

### Follow-Up Actions

**If Jump Completed:**
- Recommend FTL drive inspection at destination
- File navigation anomaly report (gravitational interference location)
- Check for component wear from elevated stress

**If Aborted:**
- Run full FTL diagnostic (required before next jump)
- Inspect tachyon emitters and QFM
- Report spatial displacement (for navigation database accuracy)
- Coordinate rescue/repair if FTL damaged

## Scenario Variations (for repeated training)

**Variation 1**: Root cause is failing tachyon emitter, not gravitational interference
- Customer must identify which emitter failing
- Must decide if can continue with degraded field
- May need to replace emitter mid-transit (if accessible and spare available)

**Variation 2**: QFM overheating is primary issue
- Caused by inadequate cooling system
- Must reduce field intensity (accepting lower speed) or abort
- Teaches tradeoff between jump completion and component safety

**Variation 3**: Power fluctuation from reactor
- Reactor experiencing issues during jump
- Must balance reactor stability with FTL power demands
- May need to fix reactor issue while maintaining jump

## Assessment Criteria

**Agent Performance Evaluation:**

**Excellent:**
- Quickly gathered all relevant parameters
- Identified gravitational interference as likely cause
- Presented clear abort vs. continue options
- Gave customer agency while providing expert guidance
- Maintained calm, professional demeanor
- Provided appropriate follow-up recommendations

**Good:**
- Gathered most relevant information
- Applied appropriate corrective actions
- Helped customer make informed decision
- Managed situation to safe conclusion

**Needs Improvement:**
- Missed key diagnostic questions
- Failed to calculate abort timeline
- Did not clearly explain options
- Showed uncertainty or panic
- Gave incomplete follow-up guidance

---

**Instructor Notes**: This scenario tests agent's ability to manage time-critical emergencies with incomplete information and high customer stress. Emphasize that real support calls may not always have perfect outcomes - goal is safe resolution, which might mean aborted jump and mission delay rather than catastrophic failure.
