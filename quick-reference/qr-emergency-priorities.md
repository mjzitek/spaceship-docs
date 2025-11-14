# Quick Reference: Emergency Response Priorities

**Document ID:** QR-EMER-001
**Classification:** CRITICAL REFERENCE
**Post This At:** Bridge, Engineering, Crew Quarters
**Last Updated:** 2847.09.29

## The Rule of Survival

**In ANY emergency, this is your priority order. NEVER DEVIATE.**

```
1. CREW SAFETY
2. SHIP INTEGRITY
3. CARGO / MISSION
```

**Explanation:**
- Dead crew can't save the ship
- A destroyed ship can't complete the mission
- Cargo can be replaced; people cannot

**If you must choose, choose in this order. Every time.**

## Emergency Classification

### CRITICAL (Red Alert)
- Immediate threat to life
- Catastrophic system failure
- Hull breach with rapid decompression
- Fire out of control
- Reactor containment failure
- Collision imminent

**Response:** Drop everything. All hands to emergency stations. Execute emergency procedures immediately.

### URGENT (Yellow Alert)
- Potential threat to life or ship
- Major system degradation
- Small contained fire
- Life support issues
- Navigation failure
- Power system problems

**Response:** All hands to stations. Assess and respond. May have minutes to hours to resolve.

### IMPORTANT (Amber Advisory)
- Reduced capability
- Minor system failures
- Non-critical damage
- Supply concerns

**Response:** Address when able. Monitor closely. May escalate.

### ROUTINE (Green)
- Normal operations
- Minor issues
- Scheduled maintenance

**Response:** Normal procedures. Log and address during standard work.

## Critical Emergencies: First 60 Seconds

### DECOMPRESSION
1. **BREATHE OUT** (don't hold breath)
2. **DON MASK** (grab nearest emergency mask)
3. **ISOLATE BREACH** (close bulkhead doors)
4. Then: Locate and seal
   - See: EMER-PROC-003

### FIRE
1. **ALERT** ("Fire, fire, fire" + location)
2. **ASSESS** (size, type, location)
3. **EXTINGUISH or EVACUATE**
   - Small + safe = Fight it
   - Large or unsafe = Evacuate and seal compartment
4. Then: Ventilate or activate suppression
   - See: EMER-PROC-001

### REACTOR EMERGENCY
1. **CHECK TEMPERATURE** (>3,000°C = SCRAM now)
2. **CHECK PRESSURE** (<60 PSI = SCRAM now)
3. **CHECK CONTAINMENT** (unstable = SCRAM now)
4. **EXECUTE SCRAM** if any critical parameter
   - See: PWR-SYS-002, EMER-PROC-005
5. Then: Emergency power from batteries

### COLLISION / IMPACT
1. **BRACE** (grab something fixed)
2. **ASSESS INJURIES** (crew first)
3. **CHECK HULL** (any breaches?)
4. **CHECK SYSTEMS** (what's damaged?)
5. Then: Emergency repair as needed
   - See: KB-134, KB-145

### LIFE SUPPORT FAILURE
1. **CHECK O₂ LEVELS** (need 19%+)
2. **DON MASKS** if O₂ dropping
3. **ACTIVATE RESERVES** (emergency O₂)
4. **ISOLATE FAILURE** (which system failed?)
5. Then: Repair or workaround
   - See: LIFE-SYS-001

### MEDICAL EMERGENCY
1. **ASSESS PATIENT** (breathing? pulse? bleeding?)
2. **CALL FOR HELP** (alert all crew)
3. **BEGIN FIRST AID** (ABC - Airway, Breathing, Circulation)
4. **STABILIZE** (stop bleeding, immobilize injuries)
5. Then: Contact medical support or divert to station
   - See: Emergency Medical Guide

## Quick Decision Matrix

**Use this when you have seconds to decide:**

| Situation | Crew Safe? | Ship Safe? | Action |
|-----------|-----------|-----------|---------|
| Fire in cargo bay | YES | YES | Fight fire, protect cargo |
| Fire in cargo bay | YES | NO | Evacuate, seal, let burn, save ship |
| Fire in cargo bay | NO | YES | Rescue crew first, then fight fire |
| Fire in cargo bay | NO | NO | Rescue crew, abandon cargo bay, save ship |
| | | | |
| Hull breach in quarters | YES | YES | Seal and repair |
| Hull breach in quarters | YES | NO | Evacuate quarters, seal compartment |
| Hull breach in quarters | NO | YES | Rescue crew, then seal |
| Hull breach in quarters | NO | NO | Rescue crew, seal, damage control |
| | | | |
| Reactor overheating | YES | YES | Emergency shutdown procedure |
| Reactor overheating | YES | NO | SCRAM immediately |
| Reactor overheating | NO | YES | Evacuate engineering, then SCRAM |
| Reactor overheating | NO | NO | Evacuate engineering, SCRAM, prepare evacuation |

**Pattern:** Crew → Ship → Mission. Always.

## Communication Protocols

### Standard Emergency Call
```
"[EMERGENCY TYPE] [EMERGENCY TYPE] [EMERGENCY TYPE]"
"LOCATION: [Specific location]"
"STATUS: [Brief description]"
"ASSISTANCE: [What you need]"
```

**Examples:**

**Fire:**
```
"Fire, fire, fire!"
"Location: Cargo Bay 2, port side"
"Status: Electrical fire, spreading"
"Assistance: Need extinguisher, seal ventilation"
```

**Decompression:**
```
"Decompression, decompression, decompression!"
"Location: Crew quarters, section 3"
"Status: Hull breach, pressure dropping fast"
"Assistance: All hands, emergency seal team to crew quarters"
```

**Medical:**
```
"Medical emergency, medical emergency, medical emergency!"
"Location: Engine room"
"Status: Crew down, unconscious, possible electrical shock"
"Assistance: Need medic immediately"
```

### Universal Distress (External)
```
"MAYDAY MAYDAY MAYDAY"
"This is [VESSEL NAME] [VESSEL NAME] [VESSEL NAME]"
"Position: [Coordinates or reference]"
"Emergency: [Type]"
"Assistance Required: [Specific needs]"
"Crew: [Number] aboard, [number] casualties"
"Over."
```

## Evacuation Order

**Only Captain or Acting Captain can order ship evacuation.**

**Evacuation Order:**
```
"All hands, all hands, all hands."
"Abandon ship. Abandon ship. Abandon ship."
"This is not a drill."
"Report to evacuation pods immediately."
"Captain."
```

**Evacuation Priority:**
1. Injured/incapacitated crew (assisted by able crew)
2. Non-essential crew
3. Essential crew (maintain systems until last possible moment)
4. Captain (last off)

**What to Grab (30 seconds max):**
- Emergency beacon
- Medical supplies
- Water (if accessible)
- Emergency rations (if accessible)
- Nothing else matters

## Common Error Codes by Severity

### IMMEDIATE ACTION REQUIRED (CRITICAL)
- **E-PWR-220:** Reactor temperature critical
- **E-PWR-260:** Coolant loss
- **E-HULL-230:** Rapid decompression
- **E-HULL-240:** Catastrophic breach
- **E-LIFE-220:** Life support critical failure
- **E-NAV-330:** Collision imminent

### URGENT ACTION REQUIRED (WARNING)
- **E-PWR-201:** Insufficient power output
- **E-PWR-250:** Plasma instability
- **E-HULL-210:** Pressure drop detected
- **E-LIFE-201:** O₂ generator fault
- **E-LIFE-205:** CO₂ scrubber fault
- **E-NAV-301:** FTL drive instability

### MONITOR CLOSELY (CAUTION)
- **E-PWR-400:** Maintenance due
- **E-COM-101:** Antenna fault
- **E-NAV-201:** Sensor degradation
- **E-CARGO-200:** Environmental out of range

## Essential Supplies Locations

**Emergency Masks (15-30 min O₂):**
- Every compartment (red containers on walls)
- Minimum 2 per compartment

**Fire Extinguishers:**
- Every 10 meters of corridor
- Every compartment (at entrance)
- Color coded by type (Red=CO₂, Yellow=Foam, Blue=Powder)

**Hull Breach Repair:**
- Engineering: Full kit
- Bridge: Basic kit
- Cargo bays: Basic kit
- Contents: Patches, foam, epoxy, plates

**First Aid:**
- Bridge: Advanced kit
- Engineering: Advanced kit
- Each crew quarter: Basic kit
- Contents: Bandages, antiseptic, splints, meds

**Emergency Rations (per person, 7 days):**
- Bridge: Locker under helm
- Engineering: Storage near reactor controls
- Crew quarters: Under bunks

**Emergency Beacon:**
- Bridge: Mounted at communications
- Engineering: In emergency locker
- EVA suits: Integrated
- Escape pods: Integrated

## Chain of Command in Emergency

**Normal:**
1. Captain
2. Executive Officer / First Mate
3. Chief Engineer
4. Senior Crew Member (by seniority)

**If Captain Incapacitated:**
- Next in line assumes command immediately
- No debate, no delay
- Others must follow, even if they disagree

**If Ranking Officer Gives Order You Think Is Wrong:**
- Follow the order UNLESS it's clearly suicidal or illegal
- Voice objection: "Captain, I recommend [alternative] because [reason]"
- If overruled, follow order
- If order is clearly suicidal (will definitely kill crew), you may refuse and relieve officer
- This is EXTREME measure, only if absolutely certain

## When to Call for External Help

### Call IMMEDIATELY If:
- Multiple critical system failures
- Casualties beyond your medical capability
- Ship may be lost
- Catastrophic damage
- Unable to reach destination
- Reactor containment breach

### Call When Stable If:
- Single critical failure but contained
- Need technical guidance
- Need parts or supplies beyond your stock
- Repair is beyond your crew's skill

### How to Call:
1. **Emergency Channel:** 121.5 MHz (monitored 24/7)
2. **ORSM Emergency Hotline:** Via subspace if available
3. **Nearest Vessel:** Broadcast on standard frequencies
4. **Nearest Station:** Direct call if in range

**Don't Be a Hero:** Asking for help is smart, not weak.

## Critical Reminders

### Mindset
- **Stay Calm:** Panic kills. Breathe. Think. Act.
- **Work Together:** Crew is your greatest resource.
- **Adapt:** Plan A might fail. Have Plan B, C, D ready.
- **Survive:** Your goal is to survive. Period.

### Common Mistakes
- **Hesitation:** In critical emergencies, seconds matter. MOVE.
- **Tunnel Vision:** Don't fixate on one problem while others escalate.
- **Pride:** Ask for help. Use every resource.
- **Panic:** Control your fear. Fear is useful; panic is deadly.

### Success Principles
1. **Train:** Practice emergencies regularly.
2. **Prepare:** Check emergency supplies monthly.
3. **Know Your Ship:** Know where everything is.
4. **Trust Your Crew:** You survive together or not at all.

---

## POST THIS WHERE YOU'LL SEE IT DAILY

**Emergency Prep Checklist (Weekly):**
- [ ] Emergency masks charged and in place
- [ ] Fire extinguishers pressurized
- [ ] Breach repair supplies stocked
- [ ] First aid kits complete
- [ ] Crew knows evacuation routes
- [ ] Emergency drills scheduled

**Remember:**
- Crew first
- Ship second
- Cargo third

**You can replace cargo. You cannot replace crew.**

---

**For detailed procedures, see:**
- EMER-PROC-001: Fire Response
- EMER-PROC-002: Medical Emergency
- EMER-PROC-003: Rapid Decompression
- EMER-PROC-004: Emergency Evacuation
- EMER-PROC-005: Reactor Emergency

**ORSM Emergency Support: Available 24/7**

---

**Stay Sharp. Stay Ready. Stay Alive.**
