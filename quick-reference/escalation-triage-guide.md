# ESCALATION & TRIAGE GUIDE
**When and How to Route Issues to Specialists**

## PURPOSE
This guide helps you decide when to escalate issues beyond Level 1 support and how to route them to the appropriate specialist or team.

**Key Principle:** When in doubt, escalate UP. It's better to engage specialists unnecessarily than to waste time on issues beyond your scope.

---

## 🎯 SUPPORT LEVEL DEFINITIONS

### Level 1 Support (You)
**Scope:**
- Common issues covered in Top 20 guide
- Issues resolvable with KB articles
- Standard troubleshooting procedures
- Basic parameter checks and resets
- Filter replacements and routine maintenance guidance
- Error code interpretation and basic resolution

**Time Limit:** 15 minutes
- If not resolved or clearly diagnosable within 15 minutes → Escalate to Level 2

**Tools:**
- KB articles
- Error code references
- Quick reference guides
- Standard troubleshooting procedures

---

### Level 2 Support (Specialists)
**Scope:**
- Complex troubleshooting requiring deep system knowledge
- Issues requiring configuration changes
- Multi-system cascade failures
- Hardware diagnostics beyond basic checks
- Intermittent issues requiring detailed analysis
- Performance tuning and optimization

**Teams:**
- Power Systems Specialist
- Navigation/FTL Specialist
- Life Support Specialist
- Communications Specialist
- Weapons & Defense Specialist
- Hull & Structural Engineer

---

### Level 3 / Emergency Response
**Scope:**
- Life-threatening emergencies
- Ship-threatening system failures
- Situations requiring immediate expert intervention
- Evacuation coordination
- Emergency on-site service dispatch

**Teams:**
- Emergency Response Coordinator
- On-Site Service Dispatch
- Rescue & Recovery Services

---

## 🚦 TRIAGE DECISION TREE

```
                    ISSUE REPORTED
                         ↓
            Is anyone in immediate danger?
                    ↙       ↘
                  YES        NO
                   ↓          ↓
         [LEVEL 3 EMERGENCY]  Can ship operate safely?
                              ↙              ↘
                            YES               NO
                             ↓                 ↓
                  Is it a Top 20 issue?    [ESCALATE TO LEVEL 2]
                     ↙            ↘
                   YES             NO
                    ↓               ↓
         Follow Top 20 guide    Can you diagnose system?
                                ↙              ↘
                              YES               NO
                               ↓                 ↓
                 Try standard KB/troubleshooting    Use Symptom Guide
                              ↓                         ↓
                 Resolved in 15 min?         Identified system?
                     ↙        ↘                  ↙         ↘
                   YES         NO               YES         NO
                    ↓           ↓                ↓           ↓
                [CLOSE]  [ESCALATE L2]   Try troubleshooting  [ESCALATE L2]
```

---

## 🔴 IMMEDIATE ESCALATION (Level 3 Emergency)

**Escalate IMMEDIATELY without troubleshooting if:**

### Life Safety Threats
- ☐ Fire on board
- ☐ Hull breach with decompression
- ☐ Reactor radiation leak
- ☐ Life support complete failure (< 30 minutes of air)
- ☐ Toxic atmosphere
- ☐ Crew medical emergency requiring evacuation
- ☐ Ship on collision course (unable to maneuver)

### Ship-Critical Failures
- ☐ Total power loss (reactor offline, no backup)
- ☐ FTL failure while in hyperspace
- ☐ Complete propulsion failure in hazardous location
- ☐ Multiple cascading system failures
- ☐ Fire suppression system failed during active fire

### Hostile Situations
- ☐ Under attack with defensive systems down
- ☐ Stranded in immediately hostile environment
- ☐ Hijacking or security breach

**Escalation Process:**
1. **Immediately** page Emergency Response: "Priority 1 - [Type] - [Ship Name]"
2. **Stay on line** with customer
3. Begin emergency procedures while help is en route
4. Update emergency team every 2 minutes
5. DO NOT transfer call - maintain continuous contact

---

## 🟠 URGENT ESCALATION (Level 2 Specialist)

**Escalate to Level 2 after basic diagnostics if:**

### Time-Based Triggers (15-Minute Rule)
- ☐ Issue not resolved after 15 minutes of troubleshooting
- ☐ Issue not clearly diagnosed after 10 minutes
- ☐ Customer has already tried everything in KB article

### Complexity Indicators
- ☐ Intermittent issue with no clear pattern
- ☐ All standard fixes have failed
- ☐ Multiple related systems failing (cascade)
- ☐ Error codes not in standard documentation
- ☐ Requires parameter changes beyond basic resets
- ☐ Requires hardware diagnostics you cannot perform remotely

### System-Specific Triggers
- ☐ Reactor issues beyond startup troubleshooting
- ☐ Coolant system problems (always escalate)
- ☐ FTL drive calibration needs
- ☐ Navigation computer programming issues
- ☐ Sensor array hardware problems
- ☐ Communications encryption deep diagnostics
- ☐ Weapons system integration issues
- ☐ Structural damage assessment needs

### Criticality Triggers
- ☐ Ship is stranded (cannot move)
- ☐ Ship in hazardous location (not immediate danger, but risky)
- ☐ Mission-critical system down
- ☐ Commercial ship losing revenue due to downtime
- ☐ VIP or priority customer

**Escalation Process:**
1. Document all troubleshooting already performed
2. Prepare summary for specialist (ticket notes)
3. Inform customer: "I'm bringing in our [System] specialist who can diagnose this further"
4. Page appropriate specialist
5. Brief specialist on findings
6. Transfer call with warm handoff

---

## 🟡 STANDARD HANDLING (Level 1)

**You should handle these:**
- ☐ Issues clearly covered in Top 20 guide
- ☐ Issues with clear KB article match
- ☐ Standard error codes with documented resolutions
- ☐ Routine maintenance questions
- ☐ Filter replacements, basic parameter checks
- ☐ User education and training
- ☐ Simple sensor calibrations
- ☐ Basic power cycles and resets

**Continue troubleshooting if:**
- Making progress toward diagnosis
- Customer is cooperative and available
- Within your knowledge scope
- Under 15 minutes elapsed
- Ship is safe to continue operations

---

## 📋 ESCALATION CRITERIA BY SYSTEM

### POWER SYSTEMS

**Escalate If:**
- Coolant pressure/temperature abnormal (always)
- Radiation levels elevated (always)
- Reactor won't start after standard KB-001 procedure
- Multiple power-related systems failing
- Control rods not responding
- Power fluctuations continue after basic checks

**You Can Handle:**
- Standard reactor startup troubleshooting (KB-001)
- Basic power distribution issues
- Simple load balancing
- Filter replacement guidance
- Basic parameter verification

**Specialist:** Power Systems Specialist

---

### NAVIGATION / FTL

**Escalate If:**
- FTL drive won't charge above 80%
- Navigation computer reports hardware faults
- Star tracker calibration needed
- Coordinate validation repeatedly fails with valid coordinates
- FTL failure in transit (immediate - Level 3)
- Gyroscope hardware issues

**You Can Handle:**
- Standard FTL jump troubleshooting (KB-012, checklist)
- Basic navigation drift (KB, Top 20 #12)
- Coordinate format issues
- Basic position updates
- Pre-jump checklist guidance

**Specialist:** Navigation/FTL Specialist

---

### LIFE SUPPORT

**Escalate If:**
- O2 levels below 18% or CO2 above 1%
- Atmospheric scrubber failure
- Water contamination detected
- Life support failure cascade
- Environmental controls completely non-functional
- Biological hazards detected

**You Can Handle:**
- Sensor calibration (KB-027)
- Filter replacement guidance
- Basic O2 level troubleshooting
- Temperature control (Top 20 #8)
- Water system basics (Top 20 #9)

**Specialist:** Life Support Specialist

---

### COMMUNICATIONS

**Escalate If:**
- Encryption system failures
- Hardware damage to antenna array
- All frequencies failing equally
- Security protocol issues
- Signal processing unit failures
- Need relay satellite diagnosis

**You Can Handle:**
- Frequency selection
- Power level adjustments
- Antenna orientation
- Basic interference troubleshooting (Top 20 #4)
- Encryption key regeneration (Top 20 #18)
- Range verification

**Specialist:** Communications Specialist

---

### SENSORS

**Escalate If:**
- Multiple sensor nodes failing
- Calibration failures
- Sensor array hardware damage
- Systematic blind spots
- Sensor fusion errors
- Advanced interference issues

**You Can Handle:**
- Basic sensor calibration
- Ghost contact troubleshooting (KB-089)
- Sensitivity adjustments
- Single sensor node issues
- Basic interference identification

**Specialist:** Sensors Specialist (usually Level 2 general)

---

### CARGO SYSTEMS

**Escalate If:**
- Structural damage to cargo bay
- Hazmat spill or containment breach
- Door mechanism completely failed
- Restraint system hardware failure
- Need load distribution engineering

**You Can Handle:**
- Cargo restraint troubleshooting (KB-045)
- Door operation basics (Top 20 #16)
- Load limit guidance
- Basic hazmat procedure guidance
- Door lubrication and basic maintenance

**Specialist:** Cargo Operations Specialist

---

### HULL & STRUCTURE

**Escalate If:**
- Active hull breach (Level 3 if decompression)
- Structural integrity warnings
- Stress analysis needed
- Repair procedure guidance needed
- Micro-fracture assessment
- Airlock complete failure

**You Can Handle:**
- Basic airlock troubleshooting (Top 20 #13)
- Hull inspection procedure guidance
- Emergency patch procedures (under expert guidance)
- Basic seal checks

**Specialist:** Structural Engineer

---

### DEFENSIVE SYSTEMS / WEAPONS

**Escalate If:**
- In active combat situation (expedite)
- Multiple weapons/defense systems down
- Targeting computer hardware failure
- Shield generator physical damage
- Weapons safety interlock failures
- Fire control system errors

**You Can Handle:**
- Basic shield activation (Top 20 #10)
- Targeting system resets (Top 20 #15)
- Power allocation checks
- Basic weapons system checks
- Simple fire control resets

**Specialist:** Weapons & Defense Specialist

---

### MEDICAL FACILITIES

**Escalate If:**
- Life support equipment failure (ventilators, etc.)
- Multiple systems failing
- Medical emergency requiring equipment
- Biological hazard contamination
- Quarantine system failures

**You Can Handle:**
- Basic equipment troubleshooting (Top 20 #17)
- Power cycle procedures
- Calibration guidance
- Basic diagnostic equipment issues

**Specialist:** Medical Systems Specialist

---

## 📞 HOW TO ESCALATE EFFECTIVELY

### Before Escalating - Gather This Information

**Required Information:**
1. ☐ Ship identification (name, class, location)
2. ☐ Clear problem description
3. ☐ Error codes and warnings
4. ☐ All troubleshooting steps already performed
5. ☐ Current system status
6. ☐ Customer technical level
7. ☐ Urgency level and customer situation
8. ☐ Customer contact information and best callback method

**Document in Ticket:**
- Timeline of events
- Symptoms reported
- Diagnostic results
- What worked / what didn't
- Current state of ship/system
- Customer availability

### Warm Handoff Process

**Best Practice - Stay on Line:**
1. Tell customer: "I'm bringing in our [System] specialist"
2. Brief specialist on situation (customer on hold or listening)
3. Introduce specialist to customer
4. Confirm specialist has all needed information
5. Disconnect or stay available if specialist needs you

**Alternative - Schedule Callback:**
1. Tell customer: "Our [System] specialist will call you back within [timeframe]"
2. Get best contact info and availability
3. Document everything in ticket
4. Page specialist with ticket info
5. Confirm specialist has received escalation

### Escalation Communication Templates

**To Customer:**
```
"Based on our troubleshooting, this issue requires our [System] specialist's
expertise. I'm going to [transfer you now / schedule a callback]. They'll have
all the information from our session, so you won't need to repeat everything."
```

**To Specialist:**
```
"[Ship Name] with [issue]. I've completed [troubleshooting steps]. Current
status: [status]. Customer is [technical level] and [availability].
Urgency: [level] because [reason]."
```

---

## ⚠️ ESCALATION RED FLAGS

### When You MUST Escalate

**You lack knowledge/authority to:**
- Make configuration changes
- Authorize warranty exceptions
- Perform hardware diagnostics
- Access certain systems remotely
- Provide certain parts/services

**Customer explicitly requests:**
- Supervisor or manager
- Specialist or expert
- Second opinion
- Formal complaint process

**Situation is deteriorating:**
- System failure is progressing
- More systems failing over time
- Customer situation becoming dangerous
- Your troubleshooting is making things worse

**Legal/liability concerns:**
- Customer reports injury
- Significant damage has occurred
- Customer threatens legal action
- Compliance or regulatory issues involved

---

## 🎯 SPECIAL ESCALATION SCENARIOS

### VIP / Priority Customers
- Military vessels
- Government ships
- Emergency services
- Priority support contracts

**Process:**
- Flag ticket as priority
- Shorter escalation threshold (10 minutes vs. 15)
- Notify Level 2 supervisor of VIP escalation
- Expedite specialist callback

---

### After-Hours Escalation
**On-Call Specialists Available For:**
- Emergencies only (Level 3)
- Critical system failures (can't wait until morning)
- Stranded vessels

**Standard Issues:**
- Document thoroughly
- Schedule next-business-day callback
- Provide workarounds if possible
- Set clear expectations with customer

---

### Multiple Simultaneous Escalations
**If You Have Multiple Emergencies:**
1. Triage by severity (life safety first)
2. Page emergency response with count
3. Handle highest severity
4. Get backup agents for other calls
5. Document everything

---

## 📊 ESCALATION METRICS & QUALITY

### Good Escalation Indicators
- ✅ Clear documentation of troubleshooting performed
- ✅ All relevant information gathered
- ✅ Appropriate specialist selected
- ✅ Customer expectations set properly
- ✅ Escalated at appropriate time (not too early, not too late)

### Poor Escalation Indicators
- ❌ Escalating without attempting basic troubleshooting
- ❌ Incomplete information provided to specialist
- ❌ Wrong specialist contacted
- ❌ Customer not informed of escalation
- ❌ Escalating issues you should handle

### Your Escalation Rate Should Be
- **20-30% of calls** - Good range for Level 1
- **< 15%** - May be holding calls too long or missing complex issues
- **> 40%** - May be escalating too quickly; review Top 20 and KB articles

---

## 🔄 WHAT TO DO AFTER ESCALATION

### If You Transfer Call
1. ☐ Document final status in ticket
2. ☐ Note specialist name and time of transfer
3. ☐ Follow up in ticket to see resolution (learn from it)
4. ☐ If recurring issue, suggest KB article or documentation update

### If Specialist Will Callback
1. ☐ Document all info in ticket
2. ☐ Confirm customer availability
3. ☐ Set customer expectation for callback timing
4. ☐ Follow up to ensure callback happened
5. ☐ Check resolution for your learning

### Learn from Escalations
- Review how specialist resolved issue
- Ask questions if you don't understand resolution
- Suggest documentation updates if info was lacking
- Build your knowledge for similar future issues

---

## 💡 ESCALATION BEST PRACTICES

### DO:
- ✅ Escalate when in doubt
- ✅ Document thoroughly before escalating
- ✅ Set customer expectations about what happens next
- ✅ Warm handoff when possible
- ✅ Learn from each escalation
- ✅ Escalate based on complexity, not ego

### DON'T:
- ❌ Hold calls beyond 15 minutes trying to avoid escalation
- ❌ Escalate without attempting basic troubleshooting
- ❌ Surprise customer with sudden transfer
- ❌ Dump calls on specialists without proper briefing
- ❌ Take escalation personally (it's about expertise, not performance)
- ❌ Escalate same issues repeatedly without learning

---

## 📈 WHEN NOT TO ESCALATE

**These You Should Definitely Handle:**
- Customer can't find documentation (send them links)
- Simple "how-to" questions
- Issues clearly covered in Top 20
- Basic parameter checks
- Filter replacement questions
- Error codes with clear resolution in documentation
- User error issues (tactful education opportunity)
- Warranty policy questions (you can answer these)

**Gray Areas - Use Judgment:**
- Unusual but not complex issues
- Customer is very technical and guiding you
- Issue is 90% resolved, just need to confirm
- Specialist recently helped with same ship (might handle continuity)

---

## 🔗 QUICK REFERENCE LINKS

**Before Escalating:**
- [Top 20 Common Issues](./top-20-common-issues.md) - Try these first
- [KB Articles](../kb-articles/) - Check for relevant KB article
- [Error Codes](../error-codes/) - Lookup error codes
- [Symptom Guide](./symptom-based-troubleshooting.md) - Identify system

**When Escalating:**
- [Customer Response Templates](./customer-response-templates.md) - Escalation scripts
- [Help Desk Index](./HELP-DESK-INDEX.md) - Main navigation

**Emergency Procedures:**
- [EMERG-001: Hull Breach](../emergency-procedures/emerg-001-hull-breach.md)
- [EMERG-002: Fire](../emergency-procedures/emerg-002-fire.md)
- [EMERG-003: Life Support](../emergency-procedures/emerg-003-life-support.md)
- [EMERG-004: FTL Failure](../emergency-procedures/emerg-004-ftl-failure.md)
- [EMERG-005: Reactor Emergency](../emergency-procedures/emerg-005-reactor-emergency.md)

---

## 📞 SPECIALIST CONTACT DIRECTORY

### Level 2 Specialists
- **Power Systems:** [Contact Method]
- **Navigation/FTL:** [Contact Method]
- **Life Support:** [Contact Method]
- **Communications:** [Contact Method]
- **Sensors:** [Contact Method]
- **Cargo Operations:** [Contact Method]
- **Hull & Structure:** [Contact Method]
- **Weapons & Defense:** [Contact Method]
- **Medical Systems:** [Contact Method]

### Level 3 Emergency
- **Emergency Response Coordinator:** [Emergency Contact]
- **After-Hours On-Call:** [Emergency Contact]

### Management
- **Support Supervisor:** [Contact Method]
- **Support Manager:** [Contact Method]

---

**Document Version:** 1.0 | **Last Updated:** Stardate 2438.11

**Remember:** Escalation is a tool, not a failure. Use it wisely to ensure customers get the right expertise at the right time.
