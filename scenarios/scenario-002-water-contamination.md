# Training Scenario: Water System Contamination Emergency

**Scenario ID:** TRAIN-LIFE-002
**Category:** Life Support Systems - Water Quality
**Difficulty Level:** Intermediate
**Training Purpose:** Diagnosing and resolving water contamination with time pressure
**Estimated Duration:** 30-45 minutes
**Prerequisites:** Life support basics, WRMS operations

## Scenario Overview

Support agent receives call from vessel reporting crew illness and water quality alarm. Agent must guide customer through identifying contamination type, isolating the problem, and restoring safe water supply while managing crew health crisis.

**Learning Objectives:**
- Diagnose water contamination from symptoms
- Prioritize crew safety vs. system repair
- Guide through emergency water rationing
- Understand WRMS failure modes
- Apply proper decontamination procedures

## Initial Contact

### Customer Opening Statement

**Vessel:** Cargo hauler "Rusty Venture"
**Location:** In transit between stations, 4 days from nearest port
**Crew:** 6 (Captain, First Mate, Engineer, 3 Cargo Handlers)
**Ship Class:** Medium freighter with APU-Standard, WRMS-Standard

**Customer (First Mate, voice concerned):**

> "Support, we have a problem. Three of our crew are sick - vomiting, diarrhea, one has a fever. Started about 6 hours ago. Our water quality monitor just went off with an alarm. The panel is showing 'BACTERIAL CONTAMINATION DETECTED' and error code E-LIFE-210. We're 4 days from the nearest station. What do we do?"

### Initial Information Display

**Water System Status (per customer):**
- Potable tank level: 65%
- Water quality: FAILED
- TDS: 180 ppm (normal)
- pH: 7.2 (normal)
- Bacterial count: 150 CFU/100ml (CRITICAL - should be 0)
- UV sterilizer: Status shows "OPERATING"
- Last water processing: 18 hours ago

**Crew Status:**
- 3 crew sick (nausea, vomiting, diarrhea, one with fever)
- Symptoms started 6 hours ago
- 3 crew still healthy (including engineer)

**Emergency Supplies:**
- Emergency water ration: 50 liters (stored, sealed containers)
- Medical supplies: Basic first aid kit

## Phase 1: Immediate Crew Safety (5 minutes)

### Key Questions to Ask

**Agent should gather:**

1. **"STOP all water consumption immediately. Has anyone drunk water in the last 2 hours?"**
   - **Answer**: "Yes, the three sick crew drank water earlier. The healthy ones haven't had any in past few hours - they were working on cargo loading."
   - **Purpose**: Establish exposure pattern

2. **"Check your emergency water ration - the sealed containers stored separately. Are they intact?"**
   - **Answer**: "Yes, we have 50 liters in sealed bottles. Not contaminated."
   - **Purpose**: Verify safe water source available

3. **"How are the sick crew doing right now? Anyone unconscious or getting worse?"**
   - **Answer**: "They're miserable but conscious. Lots of vomiting and trips to the head. One guy has a fever of 38.5°C."
   - **Purpose**: Assess medical severity

4. **"How many days until you reach port?"**
   - **Answer**: "Four days at current speed. We could push the engines and maybe make it in three."
   - **Purpose**: Calculate if emergency supply sufficient

### Expected Agent Response

**Agent should:**

1. **Immediate water prohibition**:
   > "CRITICAL: Do NOT let anyone drink tap water. Post warnings at all water outlets. Everyone drinks ONLY from the emergency ration bottles."

2. **Calculate emergency supply**:
   > "You have 50 liters emergency water for 6 people for 4 days. That's about 2 liters per person per day - bare minimum for survival. You'll need strict rationing. Priority is drinking water only - no washing, cooking with minimal water."

3. **Medical guidance**:
   > "The sick crew likely have bacterial gastroenteritis from contaminated water. Keep them hydrated with safe water, rest, and monitor. If anyone gets severely dehydrated or fever goes above 39°C, that's a medical emergency - you may need to divert to closer port."

4. **System assessment**:
   > "We need to figure out why your UV sterilizer isn't killing bacteria. But crew safety first - don't drink the water until we fix this and verify it's safe."

## Phase 2: Diagnosis (10-15 minutes)

### Diagnostic Questions

**Agent should guide through systematic diagnosis:**

**Question 1: UV Sterilizer Check**

**Agent**: "Go to your WRMS panel. Access the UV sterilizer status. What does it show for UV lamp output?"

**Customer (Engineer investigating)**: "It says... UV lamp output is 42% of rated intensity."

**Teaching Point**: UV lamps degrade over time. At 42%, not enough UV radiation to kill bacteria. Should be >70% minimum.

**Question 2: Lamp Age**

**Agent**: "Check your maintenance log. When was the UV lamp last replaced?"

**Customer**: "Uh... looking at the log... oh man, it was replaced 18 months ago. The log says replace every 12 months."

**Teaching Point**: UV lamps have finite lifespan (~8,000-10,000 operating hours or 12 months). This lamp is overdue, which explains low output.

**Question 3: System History**

**Agent**: "Has your water tasted or smelled odd recently, before the alarm?"

**Customer**: "Actually, yeah. Past week or so the water has tasted a bit off. Not horrible, just... not quite right. We figured it was just the usual recycled water taste."

**Teaching Point**: Gradual UV lamp degradation meant bacterial contamination was building up slowly. Crew was drinking low levels of bacteria for days, then it reached critical threshold triggering alarm.

**Question 4: Why Now?**

**Agent**: "UV lamps don't suddenly fail. This has been degrading for months. Why did the alarm just go off?"

**Customer**: "Good question. Let me check... Oh, we ran a water processing cycle 18 hours ago. Processed a bunch of wastewater."

**Agent**: "That's it. Fresh wastewater from biological reactor entered the system with high bacterial load. The weak UV lamp couldn't sterilize it all. The bacteria multiplied overnight and reached alarm threshold."

### Root Cause Identified

**Cause**: UV sterilizer lamp degraded below effective level (42% output)
**Contributing Factor**: Overdue lamp replacement (18 months vs 12 month spec)
**Trigger**: Large processing cycle with inadequate sterilization
**Result**: Bacterial contamination of potable water supply

## Phase 3: Emergency Response Decision (5 minutes)

### Options Presentation

**Agent must present choices:**

**Option 1: Continue to Port on Emergency Water**
- **Pro**: Safe, no risk of continued exposure
- **Pro**: Professional repair at port
- **Con**: 4 days on bare minimum water (2L per person/day)
- **Con**: No washing, very uncomfortable
- **Con**: If emergency water runs out, life-threatening

**Option 2: Decontaminate and Restore Water System**
- **Pro**: Access to full water supply if successful
- **Pro**: Crew comfort improved
- **Con**: Takes time and effort
- **Con**: If decontamination fails, used up time/resources
- **Con**: Requires UV lamp replacement (do they have spare?)

**Agent should ask**:
> "Do you have a spare UV lamp aboard? Part number UV-LAMP-254."

**Customer**: "Let me check the parts locker... Yes! We have one spare, still in the sealed package."

**Agent**: "Good. That changes things. With a new lamp and proper decontamination, you can restore your water system. But it's going to take 6-8 hours of work. The alternative is 4 days of strict rationing. What does your captain want to do?"

**Customer (checks with captain)**: "Captain says restore the water if possible. We need the water, and people are going to be miserable for 4 days without showers."

## Phase 4: Decontamination Procedure (15-20 minutes to explain)

### Step-by-Step Guidance

**Agent walks customer through complete procedure:**

**Step 1: Isolate Potable Water Tank (Immediate)**

**Agent**: "First, we're isolating the contaminated potable tank so no one accidentally uses it. Go to the WRMS panel, select 'Potable Tank' and press 'ISOLATE'. This closes all outlet valves."

**Customer**: "Done. Panel shows 'Potable Tank Isolated - No Water Flow'."

**Agent**: "Good. Now even if someone turns on a tap, nothing comes out. All 6 crew are drinking emergency rations only until we're done."

**Step 2: Replace UV Lamp**

**Agent**: "Get your spare UV lamp. You'll need to access the UV sterilizer housing. It's usually in the main WRMS compartment."

**Customer**: "Found it. There's a cylindrical housing with a quartz sleeve inside."

**Agent Instructions**:
> "Power OFF the WRMS completely. The UV lamp has 220V power - don't touch it while hot or powered.
>
> Remove the housing endcap - usually 4 bolts.
> Carefully pull out the old UV lamp. It'll be a long tube, about 50cm.
> While it's out, clean the quartz sleeve with vinegar solution - removes mineral deposits that block UV.
> Install the new lamp - make sure it's seated properly in the power socket.
> Replace the endcap, torque bolts evenly.
> Power the WRMS back on.
> Check the UV lamp status - should show 95-100% output now."

**Customer (15 minutes later)**: "OK, new lamp is in. Panel shows UV output at 98%. That's way better than 42%!"

**Step 3: Shock Treatment of Potable Tank**

**Agent**: "Now we need to kill all bacteria in the contaminated potable tank. We're going to shock treat it with chlorine."

**Customer**: "We don't have chlorine aboard."

**Agent**: "Check your emergency supplies. You might have water purification tablets - those contain chlorine. Or check the medical kit for chlorine-based disinfectant."

**Customer**: "Found water purification tablets! Package says 'chlorine dioxide tablets'."

**Agent Instructions**:
> "Perfect. Here's the procedure:
>
> 1. Calculate chlorine dose: You have a 500L potable tank at 65% = 325 liters of contaminated water.
> 2. Target concentration: 50 ppm (parts per million) chlorine.
> 3. Read the tablet package - tells you how much water per tablet. Usually one tablet per liter for drinking water, but we want stronger.
> 4. Add 50 tablets (makes 50 ppm in 325L) directly into the potable tank.
> 5. Mix by running the circulation pump for 30 minutes.
> 6. Let sit for 4 hours minimum - chlorine kills bacteria over time.
> 7. After 4 hours, flush the entire tank contents out through the drain port.
> 8. DO NOT drink this water - it's chlorinated and full of dead bacteria."

**Customer**: "Add 50 tablets, circulate 30 minutes, wait 4 hours, then drain. Got it."

**Step 4: Flush and Sanitize System**

**Agent (4 hours later - customer calls back)**:
> "Now we flush the chlorine and dead bacteria out, then sanitize the entire water system.
>
> 1. Open the potable tank drain valve - drain all 325 liters. Yes, all of it. It's contaminated.
> 2. Close drain valve.
> 3. Run a water processing cycle - takes wastewater and makes new fresh water.
> 4. This new water goes through the NEW UV lamp - will be sterile.
> 5. Process 100 liters initially for flushing.
> 6. Use this 100L to flush all pipes: Run every tap for 2 minutes, run shower, flush toilets.
> 7. Drain potable tank again - this flushes chlorine residue and dead bacteria from pipes.
> 8. Process another 300 liters of water - this becomes your clean drinking water supply.
> 9. With new UV lamp, this water should be safe."

**Step 5: Verification Testing**

**Agent**:
> "Before anyone drinks, we test the water:
>
> 1. Check water quality panel - TDS, pH, bacterial count.
> 2. Bacterial count should be 0 CFU/100ml.
> 3. If bacteria still detected: More sterilization needed.
> 4. If bacteria at 0: Water is safe.
> 5. Also do taste/smell test - should not smell like chlorine (if it does, flush more).
> 6. Have one healthy crew member (not the sick ones) drink a small glass - wait 2 hours - if no illness, water is safe."

**Customer (8 hours after starting procedure)**: "Water quality panel shows 0 bacteria! TDS and pH both normal. Water smells and tastes fine. Engineer just tried a glass - so far so good."

**Agent**: "Excellent. Wait the 2-hour observation period. If engineer shows no symptoms, water system is restored. Resume normal water usage."

## Phase 5: Follow-Up and Prevention (5 minutes)

### Post-Decontamination Care

**Agent provides final guidance:**

**Medical Follow-Up**:
> "The three sick crew will recover in 24-48 hours with rest and hydration. Keep them hydrated with safe water. Monitor for signs of severe dehydration: confusion, dizziness, very dark urine, reduced urination. If anyone gets worse, consider diverting to closer port for medical care."

**System Monitoring**:
> "For the next 24 hours, check water quality every 4 hours. Make sure bacterial count stays at 0. If bacteria returns, the decontamination didn't fully work."

**Maintenance Schedule**:
> "Update your maintenance log - UV lamp replaced TODAY. Set a reminder for 12 months from now. Don't defer this again - bacterial contamination is serious."

**Crew Education**:
> "Share with your crew: Water tasting 'off' is an early warning sign. Don't ignore it. Report to engineer immediately. Could have caught this before people got sick."

**Parts Stock**:
> "You used your only spare UV lamp. Order replacements at next port - keep 2 spares aboard. Part number UV-LAMP-254. Cost is about 300 credits - a lot cheaper than a medical evacuation."

### Scenario Resolution

**SUCCESSFUL OUTCOME:**
- Water system decontaminated and restored after 8 hours
- Crew has safe water for remaining 4-day journey
- Sick crew recovering (uncomfortable but not life-threatening)
- New UV lamp installed and functioning at 98%
- Total emergency water used: 20 liters (30 liters remaining as safety margin)

**Agent Performance**: Successfully guided customer through complex decontamination without professional support, balanced crew health vs. system repair priorities.

## Alternative Scenario Branches

### Branch A: No Spare UV Lamp

**If customer answered "No spare lamp":**

**Agent**: "Without a spare lamp, you can't restore the UV sterilizer. Your only option is to continue on emergency water ration for 4 days."

**Adjusted Plan**:
- Strict water rationing (2L per person per day drinking only)
- No washing, minimal cooking water
- Monitor emergency supply carefully
- If supply runs critically low (<10L remaining), issue distress call
- Proceed directly to port at maximum safe speed

**Outcome**: Crew survives but very uncomfortable 4-day journey. Water system repaired at port.

### Branch B: Contamination Returns After Decontamination

**If bacterial count doesn't return to 0:**

**Possible Causes**:
1. Chlorine shock not strong enough (need second treatment)
2. Biofilm in pipes survived (need system flush with stronger disinfectant)
3. Contamination source not UV lamp - may be RO membrane failure or tank breach
4. New UV lamp defective (rare but possible)

**Agent Response**: Guide through troubleshooting, may ultimately need to rely on emergency water and professional repair at port.

### Branch C: Crew Member Becomes Critically Ill

**If fever spikes to >40°C or severe dehydration:**

**Agent**: "This is now a medical emergency. You need to divert to the nearest port immediately - even if it's off your route. Send a medical distress signal. Bacterial infection may be severe or crew member may have secondary complications."

**Outcome**: Emergency diversion, possible rescue, crew member receives medical treatment. Water system secondary priority.

## Post-Scenario Debrief

### Key Learning Points

1. **UV sterilizer maintenance is critical** - Deferred maintenance has serious health consequences
2. **Water quality changes (taste/odor) are early warnings** - Don't ignore
3. **Emergency water rationing calculations** - 2L per person per day minimum
4. **Decontamination procedures are complex** - Require time, materials, and careful execution
5. **Medical risk assessment** - When to repair vs. when to seek help
6. **Parts inventory importance** - Spare UV lamp saved the mission

### Common Mistakes to Avoid

- **Allowing continued water consumption** - Agent must immediately stop water use
- **Underestimating decontamination time** - 8 hours is significant commitment
- **Skipping verification testing** - Don't trust water until tested
- **Ignoring medical severity** - Bacterial gastroenteritis can become serious
- **Not calculating emergency supply** - Know if rationing will last until port

### Support Skills Demonstrated

- **Triage decision-making** (crew safety vs. system repair)
- **Technical guidance** (step-by-step decontamination)
- **Resource assessment** (spare parts, emergency supplies)
- **Medical awareness** (symptoms, severity, when to escalate)
- **Timeline management** (8-hour procedure vs. 4-day journey)

## Assessment Criteria

**Excellent Performance:**
- Immediately stopped water consumption
- Calculated emergency supply adequacy
- Diagnosed UV lamp failure correctly
- Guided complete decontamination procedure
- Provided medical guidance
- Emphasized preventive maintenance

**Good Performance:**
- Stopped water use
- Identified UV lamp issue
- Walked through most decontamination steps
- Ensured crew safety

**Needs Improvement:**
- Delayed stopping water consumption
- Missed UV lamp as root cause
- Incomplete decontamination procedure
- Didn't address medical concerns
- Failed to provide follow-up guidance

---

**Instructor Notes**: This scenario tests agent's ability to balance immediate health crisis with technical system repair. Emphasize that crew safety is always first priority - if agent is uncertain about decontamination success, defaulting to emergency ration and professional repair at port is the safer choice. Real support sometimes means saying "get to port for professional help" rather than attempting field repairs.
