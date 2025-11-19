# Training Scenario: Q-Core Reactor Coolant Leak Emergency

**Scenario ID:** TRAIN-PWR-005
**Category:** Power Systems - Q-Core Reactor
**Difficulty Level:** Intermediate
**Training Purpose:** Emergency response to active coolant leak during reactor operation
**Estimated Duration:** 30-45 minutes
**Prerequisites:** Q-Core reactor basics, emergency procedures training

## Scenario Overview

Support agent receives emergency call from vessel experiencing active coolant leak from Q-Core reactor. Agent must guide customer through leak identification, emergency shutdown decision, leak isolation, and temporary repair while preventing reactor damage or radiation hazard.

**Learning Objectives:**
- Diagnose coolant leak severity and location
- Guide emergency shutdown procedures under pressure
- Assess radiation safety during leak
- Provide leak isolation and temporary repair guidance
- Manage customer panic during reactor emergency

## Initial Contact

### Customer Opening Statement

**Vessel:** Mining support ship "Salvage King"
**Location:** Asteroid belt mining zone, 4 hours from nearest station
**Crew:** 5 (Captain, 2 Engineers, 2 Mining Operators)
**Reactor:** Q-Core Model 3 (industrial)
**Current Status:** Operating, powering mining operations

**Customer (Engineer, panicked):**

> "Emergency! We've got coolant spraying everywhere in the reactor compartment! There's silver fluid all over the deck, pressure's dropping, and the temperature alarm just went off. My captain wants to know if we should shut down the reactor or if it'll explode. What do we do?!"

### Initial Information Display

**Reactor Status (per customer):**
- Core Temperature: 2,400°C (normal is 2,000-2,500°C)
- Coolant Pressure: 68 PSI (normal is 90-110 PSI)
- Coolant Level: 72% (normal is 95-100%)
- Power Output: 85% capacity
- Radiation Level: 0.4 mSv/h (normal is <0.3 mSv/h)
- Warning: E-PWR-260 (Coolant Pressure Low)
- Warning: E-PWR-262 (Coolant Loss Detected)

**Visual Report:**
- Silver-gray coolant pooling on deck (approximately 20 liters visible)
- Active spray visible from somewhere in piping
- Steam/vapor rising from hot surfaces

## Phase 1: Immediate Safety Assessment (3-5 minutes)

### Key Questions to Ask

**Agent should gather:**

1. **"First, is anyone in the reactor compartment right now?"**
   - **Answer**: "Yes, I'm in here! I was checking the reactor when it started spraying."
   - **Purpose**: Immediate crew safety concern

2. **"Are you wearing radiation protection? Check your dosimeter reading."**
   - **Answer**: "No protection, just work coveralls. Dosimeter says 0.5 mSv/h. Is that bad?"
   - **Purpose**: Assess radiation exposure risk

3. **"What's the current core temperature reading?"**
   - **Answer**: "2,400°C. It was 2,200 a few minutes ago. Rising."
   - **Purpose**: Determine if losing coolant is causing overheating

4. **"How fast is the coolant pressure dropping? What was it 1 minute ago?"**
   - **Answer**: "It was 75 PSI a minute ago. Now 66 PSI. So losing about 10 PSI per minute."
   - **Purpose**: Calculate leak severity and time to critical pressure

5. **"Can you see where the coolant is spraying from?"**
   - **Answer**: "Looks like it's coming from a pipe fitting near the heat exchanger. Right side of the reactor, about chest height."
   - **Purpose**: Identify leak location for repair planning

### Expected Agent Response

**Agent should immediately prioritize:**

1. **Crew safety first**:
   > "Listen carefully. Your radiation exposure is elevated but not immediately dangerous. However, I need you to evacuate the reactor compartment NOW. Exit and close the hatch behind you. The leak may worsen and radiation could increase. We'll work this from outside the compartment."

2. **Acknowledge urgency but remain calm**:
   > "This is a serious situation but it's manageable. You're losing coolant at approximately 10 PSI per minute. At this rate, you have maybe 6-7 minutes before pressure reaches critical levels where we'll need to shut down the reactor."

3. **Establish plan**:
   > "Once you're out of the reactor compartment, we'll assess whether we can isolate the leak or if we need to do an emergency shutdown. Either way, we have a few minutes to work with."

## Phase 2: Leak Assessment and Initial Response (5-10 minutes)

### From Safe Position Outside Reactor Compartment

**Customer (now outside reactor compartment):**
> "Okay, I'm out. Hatch is closed. What now?"

**Agent should guide:**

### Step 1: Monitor from External Panel

**Agent Instruction:**
> "Good. Now go to your external reactor monitoring panel. This should be outside the reactor compartment. Read me the current status."

**Customer provides updated readings:**
- Core Temperature: 2,500°C (rising)
- Coolant Pressure: 62 PSI (continuing to drop)
- Coolant Level: 68%
- Power Output: 85%
- Radiation (external sensors): 0.3 mSv/h (normal, radiation contained to compartment)

**Agent Analysis:**
> "Temperature is rising because coolant flow is reduced. We're at 62 PSI - that gives us about 5 minutes before we hit 40 PSI, which is our mandatory shutdown threshold."

### Step 2: Attempt Leak Isolation

**Agent Instruction:**
> "You said the leak appeared to be from a fitting near the heat exchanger, right side. Let me check the coolant system schematic... Okay, there should be isolation valves that can close off sections of the coolant loop. Do you have access to the coolant control valves outside the reactor compartment?"

**Customer:**
> "Yes, there's a panel here with valve controls."

**Agent Instruction:**
> "Look for the valve labeled 'Heat Exchanger Section Isolation' or 'HX Isolation.' Can you locate it?"

**Customer:**
> "Found it. It's currently set to 'Open.'"

**Agent Instruction:**
> "Before we close it, understand that this will bypass the heat exchanger. Coolant will stop flowing through that section, which should stop the leak. However, cooling efficiency will drop by about 30%. Core temperature will rise, so we'll need to reduce reactor power to compensate. Are you ready to do this?"

**Customer:**
> "Yes, tell me what to do."

### Step 3: Isolate Leak Section

**Agent provides sequence:**

**Agent Instruction:**
> "First, reduce reactor power demand. On your reactor control panel, reduce fuel injection rate to 60% of current."

**Customer:**
> "Done. Power output dropping... now at 55%."

**Agent Instruction:**
> "Good. Now temperature should stop rising shortly. Next, close the Heat Exchanger Isolation valve. Turn it clockwise until it stops."

**Customer:**
> "Closing... closed. Pressure stopped dropping! We're holding at 58 PSI."

**Agent:**
> "Excellent! You've isolated the leak. The leaking section is now bypassed. Monitor your temperature closely."

**2 minutes later:**

**Customer:**
> "Temperature peaked at 2,650°C but it's coming back down now. Currently at 2,550°C and still dropping slowly."

**Agent:**
> "Perfect. That's the reactor stabilizing at lower power with reduced cooling. You should see it settle around 2,400-2,500°C at this power level. The leak is isolated, and the reactor is stable for now."

## Phase 3: Assessment and Next Steps (10-15 minutes)

### Evaluate Situation

**Agent should explain:**

> "Okay, here's the situation: You've successfully isolated the leak by bypassing the damaged heat exchanger section. Your reactor is stable but operating at reduced capacity - about 55% instead of the normal 85% you were using. This means you can't run all your mining equipment at full power. You have several options..."

### Present Options

**Option 1: Continue Operations at Reduced Power**
- **Pro**: Can continue some mining work
- **Pro**: Reactor remains online for life support and basic ship functions
- **Con**: Mining operations limited (reduced power available)
- **Con**: Temporary fix only - still need repair at station
- **Timeline**: Can operate for days/weeks until scheduled maintenance

**Option 2: Emergency Repair Attempt**
- **Pro**: Could restore full cooling capacity
- **Pro**: Return to full power operations
- **Con**: Requires entering reactor compartment (radiation exposure)
- **Con**: Repair may not be possible without parts
- **Con**: Risk of making leak worse
- **Timeline**: 2-4 hours if successful

**Option 3: Shutdown and Return to Station**
- **Pro**: Safest option for reactor
- **Pro**: Professional repair at station
- **Con**: Lose all power (must use battery backup)
- **Con**: 4-hour trip on battery power (tight for life support)
- **Con**: Mission delay, lost mining revenue
- **Timeline**: 4 hours to station

**Agent should ask:**
> "What's your mission priority? Can you complete your mining work at reduced power, or do you need full power? How critical is it to stay on station here versus returning for repairs?"

### Customer Decision

**Customer (after consulting captain):**
> "We can complete the current mining contract at reduced power - it'll just take longer. Can we safely operate like this for the next 3-4 days? Then we'll return to station for proper repairs."

**Agent Response:**
> "Yes, that's safe as long as you maintain these conditions. Let me give you the operating parameters and monitoring requirements..."

## Phase 4: Continued Operations Guidance (5-10 minutes)

### Operating Restrictions

**Agent should specify:**

1. **Power Limitations:**
   > "Keep reactor power output at 60% maximum. This translates to about 48 MW available power for your systems. You'll need to prioritize which mining equipment to run."

2. **Temperature Monitoring:**
   > "Core temperature should stay below 2,600°C. If it exceeds this, reduce power immediately. Check temperature every hour."

3. **Coolant Monitoring:**
   > "Coolant pressure should remain stable at 55-60 PSI. If it drops below 50 PSI, you may have a second leak - shut down immediately and call us back."

4. **Radiation Checks:**
   > "The sealed reactor compartment should contain any radiation. Check external radiation levels every 4 hours. If readings exceed 0.5 mSv/h outside the compartment, evacuate adjacent areas and shut down."

5. **No Entry to Reactor Compartment:**
   > "Do not enter the reactor compartment until you've reached the station and can coordinate with radiation safety personnel. The leaked coolant may be contaminated with radioactive material."

### Cleanup and Coolant Loss

**Customer asks:**
> "What about all that coolant that leaked out? Do we need to refill it?"

**Agent Response:**
> "Your coolant level is at 68%, which is low but acceptable for short-term operation at reduced power. Ideally you'd refill to 80%+ for safety margin. Do you have reserve coolant aboard?"

**Customer:**
> "We have one 50-liter emergency reserve tank."

**Agent:**
> "Good. You lost approximately 25-30 liters from the leak. I recommend adding 20 liters from your reserve to bring the level up to about 88%. This gives you a safety buffer. I'll walk you through the coolant fill procedure..."

### Coolant Fill Procedure (Step by Step)

**Agent guides customer through:**

1. Connect emergency coolant tank to fill port (outside reactor compartment)
2. Open fill valve slowly
3. Monitor coolant level gauge
4. Fill until level reaches 85-90%
5. Close fill valve
6. Check for pressure increase (should rise to 65-70 PSI)
7. Monitor for 5 minutes to ensure no additional leaks

**Result:**
- Coolant level: 87%
- Coolant pressure: 67 PSI (stable)
- Core temperature: 2,480°C (stable)
- Power output: 58%
- All parameters within safe range

## Phase 5: Documentation and Follow-Up (5 minutes)

### What to Document

**Agent instructs:**

> "Before we finish, you need to document this incident for the repair station and for safety records. Record the following:"

1. **Incident Details:**
   - Time of leak discovery
   - Maximum radiation exposure (0.5 mSv/h for engineer)
   - Leak location (heat exchanger section, right side fitting)
   - Actions taken (section isolation, power reduction, coolant refill)

2. **Current Configuration:**
   - Heat exchanger section isolated (bypassed)
   - Operating at 60% power maximum
   - Coolant level 87%, pressure 67 PSI

3. **Repair Requirements:**
   - Replace/repair heat exchanger section piping
   - Full coolant system inspection
   - Radiation survey of reactor compartment (contamination check)
   - Coolant system pressure test before returning to service

### Station Arrival Procedures

**Agent provides advance guidance:**

> "When you arrive at the station in 3-4 days:"

1. **Before docking:**
   - Notify station of reactor leak incident
   - Request radiation safety team for compartment entry

2. **After docking:**
   - Connect to station power before shutting down reactor
   - Controlled reactor shutdown (not emergency)
   - Radiation survey of reactor compartment before cleanup
   - Professional repair of heat exchanger piping

3. **Before restart:**
   - Full coolant system pressure test
   - Reactor safety inspection
   - Verify all repairs complete

**Agent:**
> "You did a great job handling this emergency. The quick isolation prevented a forced shutdown and possible reactor damage. Operate conservatively for the next few days, monitor closely, and you'll make it to the station safely."

## Post-Scenario Debrief

### Key Learning Points

1. **Coolant leak severity assessment:**
   - Pressure drop rate indicates leak size
   - Temperature rise indicates cooling loss
   - Radiation levels indicate if leak is external to shielding

2. **Immediate priorities:**
   - Crew safety (radiation exposure, hot coolant hazard)
   - Prevent reactor damage (shutdown before critical pressure)
   - Isolate leak if possible (minimize coolant loss)

3. **Leak isolation strategy:**
   - Use isolation valves to bypass leaking section
   - Reduce reactor power to compensate for reduced cooling
   - Monitor temperature carefully after isolation

4. **Operating with degraded cooling:**
   - Reduced power output maintains safe temperatures
   - Coolant level must be adequate even if pressure low
   - Short-term operation acceptable, plan for repair

5. **Radiation safety:**
   - Even "low" radiation adds up over time
   - Minimize time in elevated radiation areas
   - Sealed compartments contain radiation effectively

### Common Mistakes to Avoid

- **Immediate SCRAM**: Not always necessary if leak can be isolated
- **Entering reactor compartment unnecessarily**: Work from external controls when possible
- **Ignoring radiation exposure**: Low levels are still significant over time
- **Attempting repair without proper assessment**: May make situation worse
- **Not considering operational alternatives**: Reduced power may allow mission continuation

### Technical Details

**Why isolation worked:**
- Q-Core reactor has redundant cooling loops
- Heat exchanger section is parallel path (can be bypassed)
- Reduced power requires less cooling capacity
- Core loop cooling remains functional

**Why SCRAM wasn't required:**
- Leak isolated before pressure reached critical 40 PSI
- Core temperature remained below emergency threshold (3,000°C)
- No radiation containment threat
- Reactor remained stable after isolation

## Scenario Variations

**Variation 1: Leak Cannot Be Isolated**
- Isolation valves are frozen/failed
- Must choose between emergency SCRAM or accepting continued coolant loss
- May need emergency coolant refill while leak ongoing
- Teaches SCRAM decision-making

**Variation 2: Multiple Leaks**
- Second leak develops after isolating first
- Coolant pressure continues dropping despite isolation
- Forces emergency shutdown decision
- Teaches cascading failure response

**Variation 3: Radiation Hazard**
- Leak is inside reactor shielding
- Radiation levels rising ship-wide
- Must SCRAM immediately and evacuate areas
- Teaches radiation emergency procedures

## Assessment Criteria

**Agent Performance Evaluation:**

**Excellent:**
- Immediately prioritized crew safety (evacuation from reactor compartment)
- Correctly calculated leak severity and timeline
- Identified isolation option and guided customer through procedure
- Reduced reactor power before isolating leak (prevented temperature spike)
- Provided clear operating restrictions for continued operations
- Gave thorough documentation and follow-up guidance

**Good:**
- Managed safe outcome (leak isolated, reactor stable)
- Customer able to continue limited operations
- Provided basic follow-up guidance

**Needs Improvement:**
- Did not address crew radiation exposure promptly
- Failed to calculate pressure drop timeline
- Did not reduce power before isolation (temperature spike risk)
- Recommended SCRAM when isolation possible (overly conservative)
- Incomplete operating restrictions or follow-up guidance

---

**Instructor Notes**: This scenario teaches that not all reactor emergencies require immediate SCRAM. System isolation and power reduction can often stabilize situation and allow continued (reduced) operations. Emphasize crew safety, careful assessment, and working from external controls when possible.
