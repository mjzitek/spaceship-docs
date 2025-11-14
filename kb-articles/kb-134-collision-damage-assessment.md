# KB-134: Collision Damage Assessment and Repair

**Category:** Hull Integrity - Damage Assessment
**Difficulty:** Advanced
**Est. Time to Resolve:** 30 minutes - several days (depending on damage severity)
**Last Updated:** 2847.09.14

## Issue Description

Ship has experienced collision (with another vessel, station, asteroid, debris, or other object). Need to assess damage, determine if safe to continue operations, and plan repairs. May range from minor scrapes to catastrophic damage requiring immediate emergency response.

## Urgency and Safety

**Collision severity classification:**

### Level 1: Minor (Cosmetic)
- Surface scrapes, paint damage
- No structural damage
- No pressure loss
- Ship fully operational
- **Response:** Document, repair at convenience

### Level 2: Moderate (Structural but Non-Critical)
- Dents, bent plating
- Minor structural damage to non-critical areas
- Sensors or antennas damaged
- Pressure holding
- Ship operational with limitations
- **Response:** Assess, temporary repairs, schedule professional repair

### Level 3: Severe (Critical but Stable)
- Major structural damage
- Pressure loss (but sealed/contained)
- Critical systems damaged but backup available
- Ship operational but unsafe for extended operations
- **Response:** Emergency repairs, proceed to nearest port immediately

### Level 4: Catastrophic (Life-Threatening)
- Hull breach, active decompression
- Critical systems failing
- Crew in immediate danger
- Ship may not be salvageable
- **Response:** Emergency procedures, possible evacuation

## Immediate Post-Collision Actions (First 5 Minutes)

### Step 1: Assess Crew Safety (30 seconds)

**Check:**
□ All crew accounted for?
□ Any injuries?
□ Anyone in danger (trapped, exposed to vacuum, etc.)?

**If injuries:**
- Administer first aid
- Call medical emergency if severe (121.6 MHz)

**If crew in danger:**
- Rescue immediately (highest priority)
- Use pressure suits if decompression risk
- Two-person minimum for rescue (safety)

---

### Step 2: Check for Immediate Hazards (1 minute)

**Critical checks:**

□ **Pressure:** Is ship holding pressure?
  - Check pressure gauge: Should be 101 kPa ± 2 kPa
  - If dropping: Hull breach (see Step 3)

□ **Fire:** Any fires started by collision?
  - Sparks, smoke, flames?
  - If yes: See KB-089 (Fire Response)

□ **Reactor:** Is reactor stable?
  - Check reactor panel: All normal?
  - If alarms: May need emergency shutdown

□ **Life Support:** Is O₂ and temperature normal?
  - O₂: 20-21%
  - Temperature: 18-24°C

□ **Propulsion:** Are engines damaged?
  - Can ship maneuver?
  - In stable orbit or drifting toward hazard?

---

### Step 3: Contain Hull Breach (If Present) (2-5 minutes)

**If pressure dropping:**

1. **Locate breach:** Hull integrity panel shows breach location
2. **Seal compartment:** Close bulkheads to isolate breach
3. **Apply emergency sealant:**
   - Part #: SEAL-EMER-A
   - Or deploy auto-seal foam (if equipped)
4. **Monitor pressure:** Should stabilize once sealed

**See:** EMERG-007 (Hull Breach) for complete procedures

**If cannot seal:**
- Evacuate affected compartment
- May need to evacuate ship (escape pods)
- Call for rescue (121.5 MHz)

---

### Step 4: Stabilize Ship Position (2-3 minutes)

**If ship drifting or spinning:**

1. **Check attitude control:** RCS thrusters working?
2. **Stop rotation:** Use RCS to counter spin
3. **Establish safe orbit/position:**
   - Not on collision course with anything
   - Stable relative to station/planet/objects
4. **If propulsion damaged:** May need station tug or rescue

---

### Step 5: Initial Damage Report (5-10 minutes)

**Quick assessment:**

□ **Hull integrity:** Breaches? Pressure stable?
□ **Critical systems:** Reactor, life support, propulsion status?
□ **Crew status:** Injuries, safe?
□ **Ship operability:** Can ship operate? Limitations?

**Communicate status:**
- If near station: Report to traffic control
- If in distress: Mayday call (121.5 MHz)
- If stable: Assess further (continue to detailed assessment)

---

## Detailed Damage Assessment (15-60 minutes)

**Once immediate hazards addressed and crew safe:**

### External Damage Survey

**Methods:**
1. **External cameras:** View damage from multiple angles
2. **EVA (if safe):** Direct visual inspection
3. **Station assistance:** Ask station to photograph damage

**Document with photos/video** (needed for insurance, repairs)

**Inspect for:**

**Hull Plating:**
- Scrapes (surface only)
- Dents (deformed but intact)
- Cracks (may propagate)
- Holes/punctures (breach risk)
- Torn or peeled plating (severe)

**Structure:**
- Bent frames or ribs
- Misalignment (doors not closing, etc.)
- Stress damage away from impact point (shock traveled through structure)

**External Equipment:**
- Antennas (bent, broken, missing)
- Sensors (damaged, misaligned)
- Docking collar (damaged, may prevent docking)
- Engines/thrusters (nozzles damaged, mounts bent)
- Heat exchanger radiators (dented, punctured)

**Rate each damage location:**
- **Green:** Cosmetic only (no function impact)
- **Yellow:** Damaged but functional (monitor, repair soon)
- **Red:** Non-functional or unsafe (repair before operating)

---

### Internal Damage Survey

**Inspect interior areas near impact:**

**Structural:**
- Bulkheads: Deformed? Leaking? Seals compromised?
- Deck/ceiling: Buckled? Cracks?
- Supports: Bent? Cracked welds?

**Systems:**
- Wiring/piping: Severed? Crushed? Leaking?
- Equipment: Computers, panels, machinery damaged?
- Cargo: Shifted? Damaged? Hazmat concerns?

**Mark damaged areas:**
- Yellow caution tape or chalk
- Keep crew away from unstable structures
- Post warnings ("STRUCTURAL DAMAGE - STAY CLEAR")

---

### System Functionality Tests

**Test each major system:**

**Propulsion:**
□ Sublight engines: Throttle test (25%, 50%, 75%)
  - Normal thrust?
  - Unusual vibration or sounds?
  - Exhaust plume symmetrical?

□ RCS thrusters: Test each axis (X, Y, Z, pitch, yaw, roll)
  - All responding?
  - Adequate authority?

**Reactor:**
□ Power output stable?
□ All parameters normal?
□ No radiation leaks?

**Life Support:**
□ APU producing O₂?
□ WRMS producing water?
□ Temperature control working?

**Navigation:**
□ Sensors functional?
□ Computer operational?
□ FTL drive (if applicable): Status?

**Communications:**
□ Can transmit/receive?
□ Antennas damaged?

**Hull Integrity:**
□ Pressure holding?
□ Bulkheads sealing properly?
□ Stress sensors: Elevated readings?

**Create functionality matrix:**

| System | Status | Limitations | Repair Priority |
|--------|--------|-------------|-----------------|
| Propulsion | Yellow | 80% thrust max | Medium |
| Reactor | Green | Normal | N/A |
| Life Support | Green | Normal | N/A |
| Navigation | Red | Sensors failed | High |
| Communications | Yellow | Limited range | Medium |
| Hull | Yellow | Stress elevated | High |

---

### Stress Analysis

**Hull stress from collision may cause delayed failure:**

**Check stress sensors:**
- Review hull stress display
- Normal: <80% design limit
- Caution: 80-95% design limit
- Critical: >95% design limit

**If elevated stress:**
1. **Identify high-stress areas:** Where on ship?
2. **Assess cause:** Impact point or stress concentration?
3. **Monitor over time:** Is stress increasing (propagating damage)?
4. **Restrict operations:** Avoid maneuvers that increase stress
   - Gentle acceleration only
   - Avoid high-G turns
   - Pressurize/depressurize slowly

**Critical stress (>95%):**
- Structure at risk of failure
- May need to depressurize affected compartment (reduces stress)
- Reinforce with temporary bracing (beams, straps)
- Seek professional assessment ASAP

---

## Operability Decision Matrix

**Based on assessment, determine if safe to operate:**

### Scenario A: Minor Damage - Continue Operations

**Criteria:**
- All critical systems functional
- Pressure stable
- No crew injuries
- Stress levels normal (<80%)
- Damage cosmetic or non-critical

**Actions:**
- Document damage (photos, log entry)
- File insurance claim
- Schedule repairs at convenience
- Continue mission

**Example:** Scraped paint from debris impact, antenna bent but functional

---

### Scenario B: Moderate Damage - Proceed to Port with Caution

**Criteria:**
- Critical systems functional (may be degraded)
- Pressure stable
- Crew safe
- Stress elevated but <95%
- Ship can reach port safely with limitations

**Actions:**
- Temporary repairs (reinforce weak areas, restore partial function to systems)
- Restrict operations (speed limit, gentle maneuvers)
- Proceed to nearest port
- Notify port of damage (may need special docking assistance)
- Professional repair at port

**Example:** Dented hull plating, sensor damaged, 80% thrust available

---

### Scenario C: Severe Damage - Emergency Response

**Criteria:**
- Critical systems damaged or at risk
- Pressure marginal (holding but leaks present)
- Crew safe but ship unsafe for extended operations
- Stress critical (>95%) in areas

**Actions:**
- Emergency repairs (stabilize immediate threats)
- Distress call (may need assistance)
- Proceed to nearest safe haven (station, planet)
- May need tug assistance
- Possible crew evacuation if situation worsens

**Example:** Major hull breach sealed but stress critical, propulsion at 50%, backup life support active

---

### Scenario D: Catastrophic Damage - Evacuate

**Criteria:**
- Hull breach cannot be sealed
- Critical systems failed (multiple)
- Crew in immediate danger
- Ship may break up or become uninhabitable

**Actions:**
- Emergency procedures (SCRAM reactor if needed)
- Evacuate to escape pods
- Mayday call (121.5 MHz)
- Abandon ship
- Await rescue

**Example:** Multiple breaches, uncontrolled decompression, reactor containment at risk

---

## Temporary Repairs

**If continuing operations with damage:**

### Temporary Hull Repairs

**Small punctures (<5cm):**
1. Clean area around hole
2. Apply emergency sealant (Part #: SEAL-EMER-A)
   - Covers hole, cures in 5 minutes
   - Holds pressure temporarily (days to weeks)
3. Monitor for leaks
4. Professional repair at port (weld patch)

**Large holes (5-50cm):**
1. Cut patch from sheet metal or hull plate
2. Position over hole (interior or exterior)
3. Bolt or weld patch in place
4. Seal edges with sealant
5. Test pressure
6. **Caution:** Temporary only, not structural

**Very large damage (>50cm):**
- May not be repairable at sea
- Depressurize compartment (if possible to isolate)
- Seal bulkheads
- Do not enter damaged compartment
- Professional repair required

**See:** EMERG-007 for complete breach repair procedures

---

### Temporary Antenna Repair

**Bent antenna:**
1. If accessible, carefully straighten (don't force, may break)
2. Test VSWR (should be <3:1)
3. If functional: Usable temporarily
4. Replace at port

**Broken antenna:**
- Cannot repair temporarily
- Use remaining antennas
- Restrict communications to working bands
- Replace at port

**See:** KB-056 (Antenna Damage and Replacement)

---

### Temporary Structural Bracing

**If hull stress elevated:**

1. **Identify stressed area:** Where is stress >85%?
2. **Install temporary bracing:**
   - Use cargo straps, chains, or beams
   - Brace stressed section (prevents bending)
   - Secure firmly to strong points
3. **Test:** Monitor stress sensors (should decrease slightly)
4. **Operate gently:** Avoid loads that stress braced area

**Professional structural repair needed at port**

---

## Insurance Claims

**Documentation required for insurance:**

### 1. Incident Report

**Include:**
- Date, time, location of collision
- Description of what happened
  - What did ship collide with? (asteroid, debris, other ship, station?)
  - Speed and angle of impact
  - Any warning? Avoidable?
- Who was at fault (if applicable)?
- Witnesses (crew, other ships, station)

---

### 2. Damage Documentation

**Photos/video:**
- All damaged areas (exterior and interior)
- Multiple angles per damaged area
- Close-ups of specific damage (cracks, dents, etc.)
- Context shots (where on ship)

**Written description:**
- Location of each damaged area
- Type of damage (scrape, dent, puncture, crack, etc.)
- Severity (cosmetic, functional, critical)
- Systems affected

---

### 3. Repair Estimates

**Get quotes from repair facilities:**
- List of repairs needed
- Parts and labor costs
- Estimated time
- Multiple quotes (insurance may require 2-3 estimates)

---

### 4. Ship's Log Entry

**Official record in ship's log:**
- Collision event (time, location, cause)
- Damage assessment
- Crew actions (emergency response, temporary repairs)
- Operability decision and rationale

---

### 5. Third-Party Reports (if applicable)

**If collision involved other parties:**
- Station incident report (if at station)
- Other ship's account (if ship-to-ship collision)
- Traffic control communications log
- Witness statements

---

### Insurance Claim Process

1. **Notify insurance within 24 hours** (most policies require prompt notification)
   - Insurance company contact info in policy documents
   - Provide brief description, estimate of damage

2. **Submit documentation** (within 7 days typically)
   - All items listed above
   - Insurance claim form (obtain from insurance company)

3. **Insurance assessment:**
   - Adjuster may inspect damage (in person or via photos)
   - Adjuster determines coverage and payout
   - May take 1-4 weeks

4. **Repair authorization:**
   - Insurance approves repair facility and costs
   - Some policies allow owner choice of facility, some require approved shops
   - Begin repairs once authorized

5. **Payment:**
   - Insurance pays facility directly OR reimburses owner (depends on policy)
   - Deductible: Owner pays deductible (typically 1,000-10,000 credits)

---

## Professional Repair Planning

**Once at repair facility:**

### 1. Comprehensive Inspection

**Professional inspectors assess:**
- Structural integrity (ultrasonic testing, x-ray, etc.)
- Hidden damage (internal structure, wiring, piping)
- Secondary damage (shock transmitted through structure)
- Complete repair list (may find more damage than initially apparent)

---

### 2. Repair Scope

**Repairs may include:**

**Structural:**
- Hull plate replacement (cut out damaged section, weld in new plate)
- Frame/rib straightening or replacement
- Welding cracks
- Bulkhead repair

**Systems:**
- Replace damaged sensors, antennas
- Repair or replace wiring, piping
- Realign equipment (if shock-mounted equipment shifted)
- Test all systems (comprehensive post-repair testing)

**Cosmetic:**
- Paint/finish (protects against corrosion)
- Decals/markings (replace if damaged)

---

### 3. Repair Time Estimates

**Minor repairs:**
- 1-3 days
- Cost: 5,000-15,000 credits

**Moderate repairs:**
- 5-14 days
- Cost: 20,000-80,000 credits

**Major repairs:**
- 3-8 weeks
- Cost: 100,000-500,000+ credits

**Catastrophic (near total loss):**
- May not be economical to repair
- Insurance may declare "total loss"
- Payout: Ship replacement value (per policy)

---

### 4. Repair Certification

**After repairs complete:**
- Repair facility provides certification (work performed meets standards)
- Regulatory inspection (if required by jurisdiction)
- Insurance inspection (confirm repairs completed satisfactorily)
- Update ship's documentation (repair history)

---

## Prevention: Collision Avoidance

**Best repair is prevention:**

### 1. Maintain Sensor Systems

- Proximity sensors functional (see KB-067)
- Regular cleaning and calibration
- Replace failed sensors promptly

### 2. Situational Awareness

- Monitor traffic in congested areas
- Use Traffic Control guidance
- Visual lookout (don't rely solely on sensors)
- Slow down in high-traffic, debris fields, unknown areas

### 3. Safe Approach Speeds

- Station approach: <10 m/s at 1 km, <1 m/s at 100m
- Asteroid fields: <50 m/s (allows reaction time)
- Debris fields: <20 m/s or avoid entirely

### 4. Communications

- Monitor Traffic Control frequency
- Announce intentions ("This is [SHIP], departing Port 5, heading 090")
- Listen for warnings ("Debris field reported at coordinates...")

### 5. Navigation Planning

- Plot course to avoid known hazards
- Use established traffic lanes (where available)
- Update star charts (NOTAMs - Notice to Airmen/Spacemen)

### 6. Equipment Maintenance

- Propulsion responsive (can maneuver to avoid collision)
- RCS thrusters functional (fine control for docking)
- Brakes/reverse thrust adequate (can stop quickly if needed)

### 7. Crew Training

- Collision avoidance procedures
- Emergency maneuvers
- Regular drills (quarterly)

---

## Legal and Liability

**Collision liability:**

### At-Fault Determination

**Who is responsible?**

**Ship-to-ship collision:**
- Right-of-way rules (similar to maritime law)
- Overtaking vessel yields to overtaken vessel
- Port side yields to starboard side (in crossing situation)
- Vessel with less maneuverability has right-of-way (large/damaged ship vs. small/maneuverable)
- May be shared fault (both contributed)

**Ship-to-station collision:**
- Usually ship at fault (station stationary)
- Unless station moved unexpectedly or gave bad guidance

**Ship-to-asteroid/debris:**
- Ship's responsibility to navigate safely
- Not at fault if debris suddenly appeared (e.g., explosion created debris field)

**If at fault:**
- Your insurance covers your damage
- You may be liable for other party's damage
- Possible fines or license suspension (if negligence)

**If other party at fault:**
- Their insurance covers your damage
- May need to pursue claim against other party
- Legal action if not covered or dispute

---

## Psychological Impact

**Collision is traumatic:**

**Crew reactions:**
- Shock, fear, anxiety (normal immediately after)
- Relief (once safe)
- Guilt (if crew feels responsible)
- Anger (at self, other party, situation)

**Support:**
- Debrief after incident (discuss what happened, feelings)
- Acknowledge fear is normal
- Focus on positive (crew responded well, safe outcome)
- Professional counseling if needed (trauma, PTSD)

**Captain's role:**
- Project calm and confidence
- Acknowledge crew's good work
- Don't assign blame immediately (investigate first)
- Support crew emotionally

**Learning:**
- Review incident objectively
- Identify lessons learned
- Improve procedures/training
- Move forward (don't dwell, but do learn)

---

## Related Articles

- EMERG-007: Hull Breach and Decompression
- KB-067: Proximity Sensors Malfunction
- KB-056: Antenna Damage and Replacement
- KB-102: Docking Procedure Without Sensors
- Hull Integrity Manual
- Insurance Policy Documentation

---

**Support Note:** Collision calls range from minor (scratched paint, customer wants to know if it's a problem) to catastrophic (hull breach, crew in danger). Triage quickly: "Is crew safe? Is ship holding pressure? Can ship maneuver?" If answers are yes/yes/yes, it's damage assessment and repair planning (not emergency). If any no, prioritize emergency response. Most collision damage is moderate (dents, damaged sensors) - ship operational but needs professional repair. Guide customer through safe temporary measures and documentation for insurance.

**Safety Reminder:** After collision, ship may have hidden damage (cracks, stress, damaged systems not immediately obvious). Recommend professional inspection even if ship seems OK. Stress cracks can propagate and cause delayed failure (hours to days later). Better to get full assessment than to have catastrophic failure en route.

**Insurance Reminder:** Document thoroughly. Take more photos than you think necessary. Insurance claims can be denied for insufficient documentation. "If it's not documented, it didn't happen" is insurance motto. Help customer understand documentation requirements (save claim hassles later).
