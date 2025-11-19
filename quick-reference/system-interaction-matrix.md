# SYSTEM INTERACTION MATRIX
**Understanding System Dependencies and Cascade Failures**

## PURPOSE
This matrix shows how ship systems interact and depend on each other. When multiple systems fail simultaneously, this guide helps you:
1. Identify the root cause system
2. Predict which other systems will be affected
3. Prioritize troubleshooting and repairs
4. Understand why fixing one system resolves multiple issues

**Key Insight:** Many "multi-system failures" are actually single-system failures causing cascade effects.

---

## 🔌 POWER DEPENDENCY MATRIX

**Rule:** Almost everything needs power. If multiple unrelated systems fail, check power first.

### Systems by Power Dependency

| System | Min Power % | Priority Level | Failure Mode if Power Lost |
|--------|-------------|----------------|---------------------------|
| Life Support | 15% | Critical | Emergency backup (30-60 min) |
| Navigation | 10% | Critical | Dead reckoning only |
| Sensors | 8% | High | Passive only, no active scanning |
| Communications | 5% | High | Reduced range/power |
| Propulsion | 25% | High | Reduced thrust |
| FTL Drive | 35% | High | Cannot charge/jump |
| Shields | 25% | Medium | Cannot activate |
| Weapons | 20% | Medium | Limited functionality |
| Medical Bay | 10% | Medium | Basic functions only |
| Cargo Systems | 5% | Low | Manual operation required |
| Environmental | 12% | Critical | Linked with life support |

### Power Cascade Failure Pattern

```
Reactor Problem → Power Output Reduced
         ↓
    [Priority System Allocation Activates]
         ↓
1. Life Support: MAINTAINED (highest priority)
2. Navigation: MAINTAINED (critical for safety)
3. Sensors: REDUCED (passive only)
4. Communications: REDUCED (emergency only)
5. Propulsion: REDUCED (maneuvering only, no full thrust)
         ↓
6. FTL Drive: OFFLINE (insufficient power)
7. Shields: OFFLINE (insufficient power)
8. Weapons: OFFLINE (insufficient power)
9. Non-essential systems: OFFLINE
```

**Diagnostic Clue:** If multiple systems in categories 6-9 are offline but 1-4 are working, suspect power supply issue.

---

## 🌡️ COOLING SYSTEM DEPENDENCIES

**Rule:** Coolant failures escalate quickly and affect multiple systems.

### Systems Requiring Cooling

| System | Cooling Need | Failure Timeline | Symptoms |
|--------|--------------|------------------|----------|
| Reactor | Critical | Minutes | Temperature rise, auto-throttle |
| FTL Drive | Critical | 10-15 minutes | Cannot charge, overheating warnings |
| Power Distribution | High | 30 minutes | Circuits trip, power fluctuations |
| Computers | High | 20-30 minutes | Slowdowns, crashes, data corruption |
| Sensors | Medium | 1-2 hours | Accuracy degradation, false readings |
| Weapons | Medium | 15-30 minutes | Overheating after firing, reduced rate |
| Shields | Medium | 20-40 minutes | Reduced strength, generator overheating |

### Coolant Cascade Failure Pattern

```
Coolant Leak/Pressure Loss
         ↓
Reactor Overheating (MINUTES)
         ↓
Automatic Reactor Throttle (safety)
         ↓
Reduced Power Output
         ↓
[Follows Power Cascade Pattern Above]
         +
Overheating Warnings Across Multiple Systems
```

**Diagnostic Clue:** Temperature warnings across multiple unrelated systems = cooling problem, not individual system failures.

---

## 🧭 NAVIGATION SYSTEM DEPENDENCIES

### Systems That Depend on Navigation Data

| Dependent System | What It Needs | Impact if Nav Fails |
|------------------|---------------|---------------------|
| FTL Drive | Position, heading, velocity | Cannot calculate safe jumps |
| Autopilot | Position, course | Cannot maintain course |
| Sensors | Position reference | Cannot calculate target positions |
| Weapons | Targeting solution | Cannot compensate for own ship movement |
| Communications | Position for relay routing | Reduced relay efficiency |

### Navigation Failure Cascade

```
Navigation Computer Failure
         ↓
Lost Position Awareness
         ↓
- FTL: Cannot validate jump coordinates → Jump fails
- Autopilot: Cannot maintain course → Manual control only
- Weapons: Cannot calculate targeting solutions → Manual aim only
- Sensors: Cannot provide accurate range/bearing → Relative positions only
```

**Diagnostic Clue:** Multiple systems reporting "cannot calculate" or "solution failed" errors = navigation data problem.

---

## 📡 SENSOR SYSTEM DEPENDENCIES

### Systems That Rely on Sensor Data

| Dependent System | Uses Sensors For | Impact if Sensors Fail |
|------------------|------------------|------------------------|
| Navigation | Position fixing, obstacle detection | Degraded position accuracy |
| Weapons | Target acquisition and tracking | Cannot lock targets |
| Shields | Threat detection for auto-activation | Manual operation only |
| Communications | Antenna pointing | Must manually aim antenna |
| FTL Drive | Space-time anomaly detection | Unsafe jump conditions undetected |
| Collision Avoidance | Obstacle detection | No automatic warnings |

### Sensor Failure Cascade

```
Sensor Array Offline
         ↓
Loss of External Awareness
         ↓
- Weapons: Cannot acquire targets → Manual targeting only
- Navigation: No star fix → Inertial navigation only (drift over time)
- Communications: Cannot auto-track → Manual antenna pointing
- FTL: Cannot detect anomalies → Jump safety compromised
- Collision Warning: OFFLINE → Pilot must maintain visual watch
```

**Diagnostic Clue:** Systems reporting "no target data" or "no external reference" = sensor problem, not targeting/nav problem.

---

## 💨 LIFE SUPPORT SYSTEM INTERACTIONS

### Systems Affecting Life Support

| System | How It Affects Life Support | Critical? |
|--------|----------------------------|-----------|
| Power | Runs atmospheric processors | YES - Emergency backup only |
| Cooling | Cools life support equipment | YES - Equipment fails hot |
| Environmental | Temperature/humidity control | Moderate - Comfort issue |
| Hull Integrity | Maintains pressure | YES - Breach causes rapid failure |
| Sensors | Monitors atmosphere | No - Manual checks possible |

### Life Support Failure Causes

```
PRIMARY FAILURE:
- Atmospheric processor malfunction
- O2 tank depletion
- CO2 scrubber failure

SECONDARY FAILURE (Root Cause Elsewhere):
- Power loss → Processors stop
- Coolant loss → Processors overheat
- Hull breach → Atmosphere vents
- Filter clogged → Reduced efficiency
- Sensor failure → False readings (not actual failure)
```

**Diagnostic Clue:** Life support alarms with power/coolant warnings = not a life support problem, fix root cause.

---

## 🗣️ COMMUNICATIONS SYSTEM INTERACTIONS

### What Communications Depends On

| Dependency | What's Needed | Impact if Missing |
|------------|---------------|-------------------|
| Power | 5-20% depending on range | Reduced range, no comms |
| Sensors | Antenna pointing | Must manually aim |
| Navigation | Position for relay routing | Less efficient routing |
| Computer | Protocol processing | Basic only, no encryption |
| Antenna Hardware | Physical antenna | Cannot transmit/receive |

### Communications Failure Diagnosis

```
"Comms Don't Work" →

Is there power? NO → Power system problem
         ↓ YES
Is antenna physically damaged? YES → Hardware problem
         ↓ NO
Can antenna track target? NO → Sensor or antenna motor problem
         ↓ YES
Is encryption working? NO → Computer or crypto module problem
         ↓ YES
Is signal in range? NO → Not a failure, physics limit
         ↓ YES
         ↓
Actual communications system problem
```

**Diagnostic Clue:** Most "comms failures" are actually power, antenna, or sensor issues, not comms electronics.

---

## 🚀 PROPULSION SYSTEM DEPENDENCIES

### Systems That Affect Propulsion

| System | Impact on Propulsion | Severity |
|--------|---------------------|----------|
| Power | Thrust available | Critical |
| Fuel System | Duration of thrust | Critical |
| Computer | Engine control | High |
| Cooling | Engine operating temp | High |
| Sensors | Velocity feedback | Medium |
| Navigation | Autopilot course maintenance | Medium |

### Propulsion Performance Matrix

| Scenario | Available Thrust | Cause |
|----------|-----------------|-------|
| Normal ops | 100% | All systems nominal |
| Low power | 40-60% | Power system issue |
| Fuel low | Varies | Fuel depletion (not malfunction) |
| Overheating | 30-50% | Cooling system issue |
| Computer fault | Manual only | Computer or control issue |
| Thruster damage | Asymmetric | Physical damage |

**Diagnostic Clue:** Symmetric thrust reduction across all engines = power or fuel issue. Asymmetric = thruster hardware.

---

## 🛡️ DEFENSIVE SYSTEMS INTERACTIONS

### Shield System Dependencies

| Depends On | Why | Impact if Lost |
|------------|-----|----------------|
| Power (25%+) | Generator operation | Shields offline |
| Cooling | Generator heat dissipation | Overheating, reduced capacity |
| Computer | Field calculations | Manual mode, reduced efficiency |
| Sensors | Threat detection | Manual activation only |
| Emitters | Field projection | Cannot form shield bubble |

### Weapons System Dependencies

| Depends On | Why | Impact if Lost |
|------------|-----|----------------|
| Power (20%+) | Weapon operation | Weapons offline |
| Cooling | Heat dissipation | Overheating, reduced fire rate |
| Sensors | Target acquisition | Manual targeting only |
| Navigation | Motion compensation | Reduced accuracy |
| Computer | Fire control | Manual aim only |

**Diagnostic Clue:** Both shields and weapons failing together = power or cooling issue, not defensive system issue.

---

## 🏗️ STRUCTURAL INTEGRITY & OTHER SYSTEMS

### How Hull Damage Affects Other Systems

| Hull Damage Location | Systems Affected | Impact |
|---------------------|------------------|---------|
| Hull breach (any) | Life Support | Atmosphere loss |
| Engine section | Propulsion, Power | Physical damage to systems |
| Sensor array area | Sensors | Physical damage, blind spots |
| Communications array | Communications | Antenna damage |
| Cargo bay | Cargo systems, Hull pressure | Bay exposure, pressure loss |

### Environmental Control Dependencies

| Depends On | Impact if Lost |
|------------|----------------|
| Power | No HVAC, temperature drift |
| Life Support | Linked atmospheric processing |
| Cooling | Heat removal for HVAC |
| Sensors | No temperature monitoring |

---

## 🔄 COMMON CASCADE FAILURE PATTERNS

### Pattern 1: Power Cascade
```
Root Cause: Reactor Throttle or Power Distribution Failure
         ↓
Lower Priority Systems Lose Power (by design)
         ↓
Symptoms:
- FTL won't charge
- Shields won't activate
- Weapons offline
- Non-essential systems dark

Diagnosis: Check reactor output and power distribution
Fix: Resolve power issue, all systems return
```

---

### Pattern 2: Coolant Cascade
```
Root Cause: Coolant Leak or Pump Failure
         ↓
Multiple Systems Overheat
         ↓
Symptoms:
- Temperature warnings across systems
- Reactor auto-throttle (reduces power)
- Computer slowdowns/crashes
- FTL overheating
- Performance degradation across board

Diagnosis: Check coolant pressure/temperature
Fix: Resolve coolant issue, allow systems to cool, then restore
```

---

### Pattern 3: Computer Cascade
```
Root Cause: Primary Computer Failure or Power to Computers
         ↓
Automated Systems Lose Control
         ↓
Symptoms:
- Autopilot disengaged
- Automatic processes stopped
- Fire control manual only
- Shield optimization lost
- Sensor processing degraded

Diagnosis: Check computer status and power to computer core
Fix: Restart or restore computers, systems regain automation
```

---

### Pattern 4: Sensor Cascade
```
Root Cause: Sensor Array Offline
         ↓
Systems Lose External Data
         ↓
Symptoms:
- Weapons can't lock targets
- Navigation can't fix position
- Collision warnings offline
- Communications can't auto-point antenna
- FTL can't verify jump safety

Diagnosis: Check sensor system status
Fix: Restore sensors, dependent systems regain functionality
```

---

### Pattern 5: Battle Damage Cascade
```
Root Cause: Physical Impact/Damage
         ↓
Multiple Systems Damaged in Same Area
         ↓
Symptoms:
- System failures localized to ship section
- Structural warnings
- Possible atmosphere loss
- Affected systems completely offline (not degraded)

Diagnosis: Check for hull damage, impact reports
Fix: Requires physical repair, cannot resolve remotely
```

---

## 🎯 TROUBLESHOOTING MULTI-SYSTEM FAILURES

### Step 1: Identify the Pattern
Ask: "Are the failing systems related by:
- Power dependency?
- Physical location?
- Data dependency (sensors, nav)?
- Cooling requirements?
- Computer control?"

### Step 2: Check Common Dependencies
**In this order:**
1. **Reactor/Power** - Affects almost everything
2. **Coolant** - Causes overheating cascade
3. **Computer** - Affects automation
4. **Sensors** - Affects data-dependent systems
5. **Physical damage** - Affects location-based systems

### Step 3: Look for the Root System
The root cause system usually shows:
- Direct error codes (not secondary failures)
- Failed first (customer may not have noticed)
- Most severe symptoms
- Abnormal parameters (not just "offline" status)

### Step 4: Fix Root Cause First
- Don't troubleshoot secondary failures
- Fix the root system
- Wait for dependent systems to recover/reset
- Only troubleshoot persistently failing systems after root cause fixed

---

## 📊 QUICK DIAGNOSTIC MATRIX

### If Multiple Systems Are Offline...

| Failing Systems | Check First | Likely Cause |
|----------------|-------------|--------------|
| FTL, Shields, Weapons | Power output | Power supply issue |
| Targeting, Nav, Collision Warning | Sensors | Sensor array offline |
| All systems in one section | Hull integrity | Physical damage |
| Systems with temp warnings | Coolant | Cooling system failure |
| Automated functions | Computer | Computer system failure |
| Everything | Reactor | Total power loss |

---

## 💡 DIAGNOSTIC TIPS

### Signs of Root Cause vs. Secondary Failure

**Root Cause Indicators:**
- ⚠️ Has specific error code
- ⚠️ Abnormal parameters (temp, pressure, voltage)
- ⚠️ Failed first chronologically
- ⚠️ Physical damage or leak visible
- ⚠️ Critical alarm (not just "offline" status)

**Secondary Failure Indicators:**
- ℹ️ Generic "offline" or "no data" status
- ℹ️ Normal parameters (just not operating)
- ℹ️ Failed after other system
- ℹ️ Advisory warning (not critical)
- ℹ️ Multiple unrelated systems failing identically

### Questions That Reveal Root Cause

1. "Which system showed problems first?"
2. "Are there any temperature or pressure warnings?"
3. "What were you doing when this started?"
4. "Did anything unusual happen before the failures?" (impact, loud noise, etc.)
5. "Are any alarms more urgent than others?"
6. "Is there anything physically different?" (leaks, damage, smoke, etc.)

---

## 🔗 RELATED DOCUMENTATION

When you've identified the root cause system:
- [Power Issues](../manuals/power/power-system-troubleshooting.md)
- [Coolant Problems](../manuals/power/coolant-system-maintenance.md)
- [Sensor Failures](../manuals/sensors/sensor-array-overview.md)
- [Navigation Problems](../manuals/navigation/navigation-troubleshooting.md)
- [Computer Issues](../manuals/) - Various computer-related manuals
- [Hull Damage](../manuals/hull-integrity/hull-integrity-overview.md)

General Resources:
- [Top 20 Common Issues](./top-20-common-issues.md)
- [Escalation Guide](./escalation-triage-guide.md)
- [Help Desk Index](./HELP-DESK-INDEX.md)

---

## 📋 SYSTEM DEPENDENCY QUICK REFERENCE

### Critical Dependencies (These affect EVERYTHING)
1. **Power** - 95% of systems need it
2. **Cooling** - Affects power generation and high-power systems
3. **Computer** - Affects automation across all systems

### Important Dependencies (These affect MANY things)
4. **Sensors** - Affects navigation, targeting, collision avoidance
5. **Navigation** - Affects FTL, autopilot, weapons
6. **Life Support** - Affects crew (who operate all systems)

### Limited Dependencies (These affect FEW things)
7. **Communications** - Mostly standalone
8. **Weapons** - Mostly standalone (needs power, sensors for automation)
9. **Cargo** - Mostly standalone
10. **Medical** - Mostly standalone

---

## 🎓 TRAINING SCENARIO

**Customer reports:**
"My FTL drive won't charge, shields won't activate, and weapons are offline. But life support and navigation are working fine."

**Your Analysis:**
1. Multiple unrelated systems failing
2. But critical systems (life support, nav) working
3. Check power output → Likely reduced power
4. Failed systems are all high power consumers (35%, 25%, 20%)
5. Working systems are low power (15%, 10%)

**Diagnostic Questions:**
- "What's your reactor output showing?"
- "Are you seeing any power warnings?"
- "What percentage power allocation are you seeing?"

**Expected Finding:**
Reactor is running but output reduced (maybe 30%), or power distribution priority has kicked in due to high load.

**Resolution:**
Fix reactor issue or reduce power load, high-power systems will come back online.

**Lesson:**
Don't troubleshoot FTL, shields, and weapons separately - they're secondary failures.

---

**Document Version:** 1.0 | **Last Updated:** Stardate 2438.11

**Remember:** When multiple systems fail, resist the urge to troubleshoot each one. Find the root cause, fix that, and watch the cascade resolve itself.
