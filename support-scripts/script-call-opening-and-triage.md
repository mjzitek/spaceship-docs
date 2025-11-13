# Support Script: Call Opening and Triage

**Document Type:** Customer Service Script
**Audience:** Technical Support Representatives
**Last Updated:** 2847.09.14

## Purpose

This script guides support representatives through the initial contact with customers, ensuring consistent service quality, proper information gathering, and accurate issue triage to the appropriate support level.

## Call Opening (All Calls)

### Greeting

**Script:**
> "Thank you for contacting Outer Rim Starship Manufacturing Technical Support. My name is [YOUR NAME]. May I have your ship registration number and the name I'm speaking with?"

**Notes:**
- Professional, friendly tone
- Identify yourself clearly
- Get ship registration FIRST (pulls up customer record)

### Verify Customer Information

**Script:**
> "Thank you, [CUSTOMER NAME]. I show your vessel as a [SHIP CLASS/MODEL] registered to [OWNER NAME]. Is that correct?"

**Verify:**
- Ship registration matches customer
- Ship model (determines which systems present)
- Warranty status (active, expired, extended)
- Service history (recent repairs, known issues)

**If mismatch or not found:**
> "I'm not finding that registration in our system. Can you verify the registration number for me? It should be on your bridge console, usually format XX-####."

### Location and Safety Check (Critical for Emergencies)

**Script:**
> "Can you tell me your current location and situation?"

**Document:**
- Location: Docked, in transit, system name, coordinates if available
- Situation: Emergency, routine operations, maintenance
- Crew status: Number aboard, any injuries

**If Emergency Situation:**
> "I understand you're experiencing [SITUATION]. Is anyone injured? Is your crew in immediate danger?"

**Escalate immediately if:**
- Life-threatening situation (hull breach, life support failure, reactor critical)
- Crew injured
- Request for rescue/evacuation

**Emergency Escalation Script:**
> "I'm going to connect you with our emergency response team right now. Stay on the line."
→ Transfer to Emergency Line (121.7 MHz Emergency Support or Emergency Coordinator)

**If NOT life-threatening emergency but serious:**
> "I understand this is urgent. Let me get some quick information so I can help you as quickly as possible."
→ Continue with triage

## Issue Description and Triage

### Open-Ended Question

**Script:**
> "What can I help you with today?"

**Listen for:**
- Symptoms customer is experiencing
- How long issue has been occurring
- What they've already tried (if anything)
- Impact on operations (stranded, delayed, inconvenience only)

**Let customer talk** - don't interrupt initial description. Take notes.

### Clarifying Questions

**After customer describes issue, ask 2-3 clarifying questions:**

**For System Failures:**
> "Is the [SYSTEM] completely non-functional, or is it partially working?"
> "When did you first notice this problem?"
> "Have you seen any error codes or messages?"

**For Performance Issues:**
> "How is this different from normal operation?"
> "Has anything changed recently? New fuel, maintenance, repairs?"
> "Is this happening constantly or intermittently?"

**For Error Codes:**
> "What is the exact error code you're seeing?"
> "Where is this error displayed? On which panel?"
> "Is the error constant or does it come and go?"

### Triage Decision Matrix

Based on information gathered, categorize issue:

#### EMERGENCY (Route to Emergency Support Immediately)
- Life support failure with <6 hours O₂ remaining
- Reactor critical (radiation, imminent failure)
- Hull breach, active decompression
- Fire spreading or uncontrolled
- Medical emergency requiring immediate intervention
- Crew in imminent danger

**Script:**
> "This is an emergency situation. I'm connecting you to our emergency response team immediately. Please stay on the line."

**Action:** Transfer to Emergency Coordinator or Emergency Line

---

#### URGENT (Expedited Support, Resolve This Call)
- Critical system failure BUT crew safe for now (life support degraded but >6 hours, propulsion failed but stable orbit)
- Stranded, unable to reach port
- Collision avoidance systems down in congested space
- Navigation failure approaching hazard
- Time-sensitive cargo at risk

**Script:**
> "I understand this is urgent and needs immediate attention. Let me work through this with you step-by-step to get you back operational."

**Action:**
- You handle this call (do not transfer unless stuck)
- Pull up appropriate KB article or troubleshooting manual
- Walk customer through diagnosis and repair
- Escalate to Level 2 only if beyond your expertise
- Follow up required: Schedule callback or verify resolution

---

#### STANDARD (Normal Support, Resolve This Call or Schedule)
- Non-critical system malfunction (crew safe, ship operational)
- Performance issues (system working but degraded)
- Maintenance questions
- "How do I..." questions
- Error codes that don't indicate immediate danger

**Script:**
> "I can help you with that. Let me pull up some information about [SYSTEM/ISSUE]."

**Action:**
- You handle this call
- Use KB articles and manuals as reference
- Walk through troubleshooting systematically
- If call will take >30 minutes, offer to schedule callback
- Escalate to Level 2 if issue beyond KB articles

---

#### NON-TECHNICAL (Route to Appropriate Department)
- Parts ordering
- Service appointment scheduling
- Warranty claims
- Billing questions
- Registration updates

**Script:**
> "I can help get you connected to the right department for that. Let me transfer you to [DEPARTMENT]."

**Action:** Transfer to appropriate department

**Departments:**
- Parts & Service: Extension 2
- Warranty Claims: Extension 3
- Billing/Accounts: Extension 4
- Registration/Admin: Extension 5

---

## Issue Categories and Initial Questions

### Power Systems (Q-Core Reactor)

**Identify Issue Type:**
- Won't start → KB-001
- Overheating → Q-Core Troubleshooting Manual, Section 4.2
- Low output → KB-015
- Error codes E-PWR-### → Error Code Reference ERR-PWR-100

**Key Questions:**
> "What is the reactor control panel showing? Any error codes?"
> "Is the panel powered on or completely dark?"
> "What is the reactor temperature reading?"
> "Can you hear the coolant pumps running?"

### Navigation Systems (FTL / Sublight)

**Identify Issue Type:**
- FTL jump fails → KB-012
- Sublight engines low thrust → KB-045
- Navigation computer error → NAV-COMP Troubleshooting
- Error codes E-NAV-### → Error Code Reference ERR-NAV-500

**Key Questions:**
> "Is this affecting your FTL drive, sublight engines, or both?"
> "What error code are you seeing, if any?"
> "Are you able to maneuver at all, or completely without propulsion?"
> "When did you last successfully jump/maneuver?"

### Life Support Systems

**Identify Issue Type:**
- Low oxygen → KB-027 (URGENT)
- Water issues → WRMS Troubleshooting Manual
- Temperature problems → KB-018
- Error codes E-LIFE-### → Error Code Reference ERR-LIFE-100

**Key Questions:**
> "What is your current oxygen level?"
> "How many crew members are aboard?"
> "What is the ship's interior temperature?"
> "Is the APU panel showing any errors?"

**If O₂ <18%:** URGENT priority, walk through immediately

### Communications Systems

**Identify Issue Type:**
- Total communications loss → KB-033
- Subspace only failing → Subspace troubleshooting, KB-033 Solution F
- Antenna damage → KB-033 Solution B
- Error codes E-COM-### → Error Code Reference ERR-COM-100

**Key Questions:**
> "Can you transmit or receive on any frequency, or is it complete loss?"
> "Is the communications panel powered on?"
> "Can you see your antennas? Any visible damage?"
> "Did this start after an FTL jump?" (post-FTL interference common)

### Hull Integrity

**Identify Issue Type:**
- Active breach → EMERG-007 (EMERGENCY if decompression)
- Breach sealed, assessing damage → Hull Integrity Manual
- Stress warnings → Hull Integrity Manual, Section 5
- Error codes E-HULL-### → Error Code Reference ERR-HULL-100

**Key Questions:**
> "Are you currently losing pressure?"
> "Has the breach been sealed?"
> "What is your current pressure reading?"
> "Where is the breach located?"

**If active decompression:** EMERGENCY priority

### Security Systems

**Identify Issue Type:**
- Lockdown malfunction → Security Systems Manual, Section 8
- Sensor false alarms → Security Troubleshooting
- Access control issues → Security Systems Manual, Section 6
- Error codes E-SEC-### → Error Code Reference ERR-SEC-100

**Key Questions:**
> "What security system component is affected?"
> "Are you locked out of a compartment or is it a sensor issue?"
> "Is this a safety concern (can't access critical systems)?"

**If locked out of critical systems (reactor, bridge):** URGENT priority

### Cargo Systems

**Identify Issue Type:**
- Cargo bay door won't open/close → Cargo Systems Manual
- Hazmat incident → EMERG-008, may need hazmat response
- Fire in cargo bay → EMERG-006 (URGENT/EMERGENCY)
- Environmental control in bay → Related to HVAC, KB-018

**Key Questions:**
> "Is this a door mechanism issue or an environmental issue?"
> "What type of cargo is affected?"
> "Any hazardous materials involved?"

**If hazmat or fire:** URGENT/EMERGENCY priority

## Customer Information to Gather (Document in Call Log)

**Always Document:**
1. Ship registration number
2. Customer name and role (captain, engineer, owner)
3. Ship model/class
4. Current location
5. Issue description (symptoms, duration, error codes)
6. Impact (crew safety, operational, economic)
7. What customer has tried already (if anything)
8. Resolution steps taken
9. Outcome (resolved, escalated, callback scheduled)
10. Parts ordered or recommended (if any)

**Call Log Template:**
```
Date/Time: [AUTO]
Ship Reg: ___________
Customer: ___________
Model: ___________
Location: ___________
Issue: ___________
Priority: EMERG / URGENT / STANDARD / NON-TECH
Resolution: ___________
Parts: ___________
Follow-up: ___________
Rep: [YOUR ID]
```

## Escalation Guidelines

### When to Escalate to Level 2 (Senior Technician)

- Issue not covered in KB articles or manuals
- Customer followed KB troubleshooting but still not resolved
- Requires specialized knowledge (advanced diagnostics, rare issue)
- Customer requests supervisor/senior tech
- Issue requires authorization (warranty exception, part substitution)

**Escalation Script:**
> "I want to make sure you get the best help for this issue. Let me connect you with one of our senior technicians who specializes in [SYSTEM]. Please hold for a moment."

**Before Transferring:**
- Brief Level 2 tech on issue, what's been tried
- Transfer customer with warm handoff (don't just transfer blind)

### When to Escalate to Emergency Coordinator

- Life-threatening situation
- Rescue required
- Multiple critical system failures
- Crew injury requiring medical evacuation
- Situation beyond technical support scope

**Escalation Script:**
> "I'm connecting you with our emergency coordinator immediately. Stay on the line."

## Difficult Customer Situations

### Customer is Panicking

**Remain calm, speak slowly and clearly:**
> "[CUSTOMER NAME], I understand this is stressful. I'm here to help you. Let's work through this together step by step. First, are you and your crew safe right now?"

**Focus on immediate safety, then problem-solving.**

### Customer is Angry/Frustrated

**Acknowledge, empathize, but stay professional:**
> "I understand you're frustrated, and I want to help resolve this as quickly as possible. Let me see what we can do."

**Do NOT:**
- Get defensive
- Argue with customer
- Make promises you can't keep ("I'll get you a free part")

**Do:**
- Listen
- Apologize for situation (not necessarily admitting fault)
- Focus on solution

### Customer Lacks Technical Knowledge

**Use simple language, avoid jargon:**
> "The Q-Core reactor is the power plant that runs your ship. I'm going to walk you through checking it step by step."

**Be patient, explain each step:**
> "You're looking for a panel labeled Q-CORE or REACTOR. It's usually in the engineering section. Can you locate that?"

**Visual guidance:**
> "The panel should have several displays. What do you see on the top-left display?"

### Customer is Highly Technical (Engineer, Former Military, etc.)

**Match their level, use technical terms:**
> "Understood. Check your magnetic containment field strength. Should be 2.5-3.2 Tesla. If it's below 2.0, you're likely having field degradation causing plasma instability."

**Don't waste their time with basics:**
> "I assume you've already checked circuit breakers and power supply?"

**Respect their expertise:**
> "Since you're experienced with this system, let's jump to the advanced diagnostics."

### Language Barriers

**Use simple, clear words:**
- Short sentences
- Avoid idioms or slang
- Speak slowly
- Repeat important information

**Confirm understanding:**
> "Can you repeat back to me what I asked you to check?"

**Use visual references:**
> "Look at your reactor panel. Do you see a red light or a green light?"

**If needed:**
> "I'm going to connect you with a translator to make sure we communicate clearly."

Transfer to translation services if available and customer agrees.

## Call Closing

### Issue Resolved

**Script:**
> "Great, it sounds like we've got [SYSTEM] working again. Just to confirm, [summarize resolution]. Is everything working normally now?"

**Verify customer satisfaction:**
> "Is there anything else I can help you with today?"

**Closing:**
> "Thank you for contacting ORSM Technical Support. Safe travels, [CUSTOMER NAME]."

### Issue Not Resolved, Callback Scheduled

**Script:**
> "This issue is going to take some additional time to diagnose and repair. I'd like to schedule a callback with you in [TIMEFRAME] to continue working on this. What's a good time for you?"

**Or, if customer needs to perform repairs first:**
> "Once you've [completed the repair step], give us a call back at [SUPPORT NUMBER] and we'll continue from there. Reference call ticket [TICKET NUMBER]."

**Provide ticket number:**
> "Your ticket number is [####]. Keep this for your records."

### Escalated to Level 2

**Script:**
> "I'm transferring you to [SENIOR TECH NAME] who specializes in [SYSTEM]. They'll be able to help you with this. One moment please."

**Brief Level 2:**
- Customer name, ship reg
- Issue description
- What's been tried
- Current status

**Warm transfer** (stay on line until Level 2 picks up and you brief them)

### Emergency Escalation

**Script:**
> "I'm connecting you with our emergency response coordinator immediately. Stay on the line and they'll assist you. [If decompression or immediate threat] Find a safe location and stay there."

**Emergency transfer:**
- Immediate transfer (do not delay)
- Brief emergency coordinator on separate line if possible
- Stay on line until confirmed transfer

## After Call Actions

**Document in system:**
1. Update call log with resolution
2. If issue unresolved, create ticket with details
3. If escalated, note who took over
4. If parts ordered, enter order
5. If follow-up needed, schedule callback reminder

**Personal notes:**
- Was this a new issue not in KB? Report to documentation team
- Did KB article have errors? Report for correction
- Especially difficult call? Debrief with supervisor if needed

## Quality Standards

**Target Metrics:**
- **First Call Resolution:** 70%+ (resolve on first call)
- **Average Handle Time:** 15-25 minutes (standard issues)
- **Customer Satisfaction:** 4.5/5.0 or higher
- **Escalation Rate:** <20% (escalate when needed, but try to resolve first)

**Call Quality Checklist:**
□ Professional greeting
□ Verified customer information
□ Gathered all relevant details
□ Used appropriate KB articles/manuals
□ Walked customer through systematically
□ Confirmed resolution or next steps
□ Professional closing
□ Documented call thoroughly

## Resources Available to You

**During Call:**
- Knowledge Base (KB articles) - Quick solutions to common issues
- Technical Manuals - Detailed system information
- Error Code Reference - Interpret all error codes
- Call Log System - Customer history, ship info
- Level 2 Escalation - Senior technicians for complex issues
- Emergency Coordinator - Life-threatening situations

**Between Calls:**
- Training materials - Continuous learning
- Peer support - Ask experienced reps
- Supervisor - Questions, difficult situations
- Documentation team - Report KB errors or gaps

## Remember

**You are the customer's lifeline.**
- Your knowledge and calm guidance may save lives
- Be thorough but efficient
- Don't be afraid to escalate when needed
- Document everything
- Continuous improvement: Learn from each call

**Customer Service Philosophy:**
> "Every ship, every crew, every call matters. We bring them home safely."

---

**New Representative Onboarding:**
- Shadow experienced reps for 40 hours
- Practice with simulated calls
- Review all KB articles
- Familiarize with technical manuals
- Start with non-emergency calls under supervision
- Graduate to independent calls after supervisor signoff

**Ongoing Training:**
- Monthly: New systems or procedures
- Quarterly: Refresher on emergency protocols
- Annually: Full certification renewal
