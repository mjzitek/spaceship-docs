# KB-027: Low Oxygen Alert - Life Support Emergency

**Category:** Life Support Systems
**Difficulty:** Critical - Time Sensitive
**Est. Time to Resolve:** 5-20 minutes
**Last Updated:** 2847.09.14

## CRITICAL NOTICE

This is a life-threatening emergency. Response time is critical. If oxygen level below 16%, crew may lose consciousness within minutes.

**PRIORITY**: Resolve immediately. Escalate to emergency support if unable to quickly stabilize O₂ levels.

## Issue Description

Atmospheric Processing Unit (APU) showing low oxygen alarm. O₂ level below normal range (19.5-21%) and potentially dropping.

## Oxygen Levels and Danger

| O₂ Level | Status | Crew Effects | Timeframe |
|----------|--------|--------------|-----------|
| 19.5-21% | Normal | None | Normal operations |
| 18-19.5% | Low (Warning) | Mild symptoms | Hours before critical |
| 16-18% | Critically Low | Impaired judgment, fatigue | 30-60 minutes before severe |
| 14-16% | Dangerous | Rapid breathing, confusion, weakness | 15-30 minutes before unconsciousness |
| <14% | Life-Threatening | Loss of consciousness, organ damage | Minutes before death |

## Immediate Questions

**FIRST QUESTION: "What is your current oxygen level reading?"**
- This determines urgency of response
- If <16%: Follow CRITICAL EMERGENCY protocol (see below)
- If 16-18%: Follow URGENT protocol
- If 18-19.5%: Follow STANDARD protocol

**SECOND QUESTION: "Is the oxygen level stable, rising, or falling?"**
- Falling: Most urgent, system failing or leak present
- Stable: Still dangerous but not worsening
- Rising: Emergency actions working, maintain course

**THIRD QUESTION: "How many crew members aboard?"**
- More crew = faster oxygen consumption
- Determines how quickly situation will deteriorate
- Oxygen consumption: ~0.84 kg per person per day

## CRITICAL EMERGENCY Protocol (O₂ < 16%)

If oxygen below 16%, every second counts:

### Step 1: Activate Emergency Oxygen (IMMEDIATE)

**Customer Action:**
1. Locate "EMERGENCY O₂" button on APU control panel
   - Large red button, clearly labeled
   - May be under protective cover (lift cover first)

2. Press and hold for 3 seconds
   - System will release oxygen from emergency tanks
   - Audible hiss as O₂ flows into cabin atmosphere

3. Verify emergency O₂ flowing:
   - Check pressure gauge on emergency tanks (should be dropping)
   - Oxygen level reading should stop dropping or start rising
   - Crew should feel relief within 1-2 minutes

**Expected Result:** O₂ level stabilizes or begins rising within 2-3 minutes.

**Emergency Tank Capacity:**
- APU-Compact: 6-12 hours of emergency O₂
- APU-Standard: 12-24 hours of emergency O₂
- APU-Industrial: 24-48 hours of emergency O₂

### Step 2: Reduce Crew Activity

**Customer Action:**
1. Alert all crew to minimize physical activity
   - Sit or lie down
   - Avoid exertion
   - Speak only when necessary
   - No running, heavy lifting, or strenuous tasks

2. Seal off unused compartments:
   - Close hatches to cargo bays, storage areas
   - Concentrates oxygen in occupied areas
   - Reduces volume of air that needs oxygen

**Expected Result:** Reduces oxygen consumption by 30-50%, extending emergency supply.

### Step 3: Diagnose While Stabilized

Once emergency O₂ deployed and crew safe, diagnose root cause:
- Proceed to URGENT Protocol diagnostics below
- Emergency tanks buy time but don't fix underlying problem
- Must resolve issue before emergency supply exhausted

## URGENT Protocol (O₂ 16-18%)

Dangerous but minutes available to diagnose and fix:

### Diagnostic A: Check Electrolysis Unit

**Cause**: Oxygen generation system not producing O₂ at required rate.

**Customer Questions:**
1. "Look at your APU control panel. What does it say for 'O₂ Generation Rate'?"
   - Should match crew consumption: ~0.84 kg per person per day
   - If zero: Electrolysis unit completely offline
   - If low: Unit running but degraded

2. "Is the electrolysis unit powered on?"
   - Check status light (should be green)
   - If dark: Unit has no power
   - If red: Unit in fault state

**Resolution Steps:**

**If electrolysis unit offline:**
1. Check power supply to unit
   - Verify Q-Core reactor producing power
   - Check circuit breaker for electrolysis unit
   - Reset breaker if tripped

2. Restart electrolysis unit:
   - APU control panel > Oxygen System > Restart
   - Unit takes 5-10 minutes to begin producing O₂
   - Monitor generation rate, should reach rated output

**If electrolysis unit degraded:**
1. Check water supply:
   - Unit requires purified water to generate O₂
   - Verify water tank not empty
   - Check water feed line not blocked

2. Check electrodes:
   - Degraded electrodes reduce efficiency
   - APU panel shows electrode health percentage
   - If <70% efficiency, electrodes likely failing
   - Can increase power to electrodes as temporary measure (increases output)

3. Increase electrolysis power:
   - APU panel > Oxygen System > Power Level
   - Increase from standard (usually 70-80%) to maximum (100%)
   - May compensate for degraded efficiency
   - Monitor QFM core temperature (uses more power)

**Expected Result:** Electrolysis unit restarts or increases output. O₂ level begins rising.

### Diagnostic B: Check for Hull Breach

**Cause**: Leak venting atmosphere to space faster than APU can replenish.

**Customer Questions:**
1. "Is your cabin pressure also dropping?"
   - Normal: 95-105 kPa
   - If dropping: Strong indication of hull breach
   - If stable: Breach less likely (small leaks may not affect pressure immediately)

2. "Do you hear any hissing sounds or feel air movement?"
   - Hissing: Air escaping through breach
   - Air current: Atmosphere being drawn toward leak

**Resolution Steps:**

1. Locate breach:
   - Check hull breach sensors (if equipped)
   - Listen carefully for hissing
   - Use smoke test: Release smoke, watch direction it moves
   - Check recent impact or damage sites

2. Seal breach:
   - Emergency hull patches (adhesive metal patches)
   - Emergency sealant foam for small cracks
   - Close bulkhead doors to isolate breached compartment

3. Monitor cabin pressure:
   - Should stabilize once leak sealed
   - O₂ level should stop dropping

**Expected Result:** With breach sealed, O₂ and pressure stabilize.

**If large breach cannot be sealed**: Evacuate affected compartment, seal it off completely.

### Diagnostic C: Check HEPA Filters

**Cause**: Severely clogged filters restrict airflow through APU, preventing oxygen from distributing.

**Customer Questions:**
1. "What color is your filter status indicator?"
   - Green: Filters OK
   - Yellow: Filters partially clogged
   - Red: Filters severely clogged

2. "Can you hear the circulation fans running?"
   - Should hear steady hum of fans
   - If silent: Fans may have failed
   - If loud/grinding: Fan mechanical issue

**Resolution Steps:**

1. Check filter airflow indicator:
   - Gauge shows airflow through filters
   - If in red zone: Filters blocking air circulation
   - Oxygen being generated but not distributed

2. Replace HEPA filters:
   - Access filter compartments
   - Remove old filters (may be visibly dirty/clogged)
   - Install spare filters
   - Close filter compartment securely

3. If no spare filters available:
   - Remove filters temporarily (very short term only)
   - Allows airflow but no filtration
   - Particulates will circulate (causes respiratory irritation)
   - Reinstall filters as soon as possible

4. Verify fan operation:
   - Fans should increase speed after filter replacement
   - Check airflow at vents throughout ship
   - O₂ reading should rise as generated oxygen distributes

**Expected Result:** With filters replaced and fans running, O₂ distributes properly and level rises.

## STANDARD Protocol (O₂ 18-19.5%)

Concerning but time available for thorough diagnosis:

1. **Review all URGENT protocol diagnostics above**
   - Even though less critical, same issues apply
   - Catching problem early prevents escalation to emergency

2. **Check crew count vs. APU capacity**:
   - APU-Compact: Rated for 1-4 crew
   - APU-Standard: Rated for 5-20 crew
   - APU-Industrial: Rated for 25-100 crew
   - If crew count exceeds rating, O₂ generation insufficient

3. **Review recent changes**:
   - Did more crew board recently?
   - New equipment consuming oxygen? (combustion devices, exothermic processes)
   - Changes to APU settings?

4. **Schedule APU maintenance**:
   - Low O₂ may indicate degrading system performance
   - Preventive maintenance can avoid future emergencies

## After Resolution

Once O₂ level restored to 19.5-21%:

1. **Monitor for 24 hours**:
   - Check O₂ level every hour
   - Verify remains stable in normal range
   - Watch for recurrence of drop

2. **Perform full APU diagnostic**:
   - Run complete system test
   - Identify any degraded components
   - Schedule repairs or part replacements

3. **Refill emergency O₂ tanks** (if used):
   - Emergency tanks must be refilled at station
   - Do not depart without refill
   - Emergency supply critical for safety

4. **Document incident**:
   - Log in ship's maintenance records
   - Note cause, resolution, and any component failures
   - Required for safety compliance

## Escalation Criteria

Escalate IMMEDIATELY if:

- O₂ level continues dropping despite emergency actions
- Multiple crew members showing symptoms (confusion, unconsciousness)
- Unable to identify cause of O₂ loss
- Electrolysis unit cannot be restarted
- Large hull breach cannot be sealed
- Emergency O₂ supply nearly exhausted

**EMERGENCY**: If situation not stabilizing, advise customer to:
- Send distress signal
- Prepare for emergency docking or evacuation
- Move to escape pods if vessel cannot maintain life support

## Prevention Tips

- **Daily O₂ monitoring**: Check level daily, catch trends early
- **Weekly filter checks**: Replace filters before they severely clog
- **Monthly electrolysis test**: Verify O₂ generation at rated capacity
- **Maintain emergency O₂**: Always keep tanks full and tested
- **Don't exceed capacity**: Crew count within APU rating
- **Hull integrity**: Regular hull inspections prevent leaks

## Related Articles

- KB-038: High CO₂ Emergency Response
- KB-044: APU Electrolysis Unit Failure
- KB-056: Hull Breach Detection and Repair
- KB-071: HEPA Filter Replacement Guide
- KB-092: Atmospheric Sensor Calibration

## Related Manuals

- LIFE-ATM-001: Atmospheric Processing Unit System
- LIFE-ATM-003: APU Troubleshooting Guide
- EMERG-008: Low Oxygen Emergency Procedures
- EMERG-007: Decompression Emergency Procedures

---

**CRITICAL SUPPORT NOTE**: This is a life-safety issue. Do not minimize urgency. If customer seems confused or irrational, they may already be suffering oxygen deprivation. Escalate immediately to emergency support and advise activating emergency O₂ while staying on the line.
