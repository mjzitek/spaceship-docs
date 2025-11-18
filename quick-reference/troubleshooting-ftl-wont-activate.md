# Troubleshooting Flowchart: FTL Drive Won't Activate

**Document ID:** TROUBLESHOOT-FTL-001
**Category:** Quick Reference / Troubleshooting
**System:** Navigation - FTL Drive
**Last Updated:** 2847.09.14

## Overview

This flowchart guides you through systematic troubleshooting when the FTL drive fails to activate. Follow the decision tree from top to bottom, performing tests and checks at each node.

**Estimated Time**: 5-30 minutes depending on issue

**Required Tools**:
- Diagnostic tablet
- Multimeter (for power checks)
- Basic hand tools

**Safety**: FTL drive operates at high voltages and temperatures. Use caution.

---

## START: FTL Drive Won't Activate

**Symptom**: FTL charge sequence fails to initiate or aborts during charge

```
┌─────────────────────────────────────┐
│   FTL DRIVE WON'T ACTIVATE          │
│   Press FTL Charge Button           │
│   What happens?                     │
└─────────────────────────────────────┘
            │
            ├──────────────────────────────────────────────┐
            │                                              │
    ┌───────▼────────┐                          ┌─────────▼─────────┐
    │ No response,   │                          │ Error message     │
    │ nothing happens│                          │ or warning shown  │
    └────────┬───────┘                          └─────────┬─────────┘
             │                                             │
             └──────────────┬──────────────────────────────┘
                            │
                      [Go to Section 1]
```

---

## Section 1: Identify the Symptom

### Question 1A: What exactly happens when you press FTL charge?

```
┌─────────────────────────────────────────────────────────────┐
│  A: Nothing happens, no response                            │
│     └──> Go to BRANCH A: Power/Computer Issues             │
│                                                             │
│  B: Error message appears immediately                       │
│     └──> Go to BRANCH B: Safety Interlock                  │
│                                                             │
│  C: Charge starts but aborts after a few seconds/minutes    │
│     └──> Go to BRANCH C: Charge Sequence Failure           │
│                                                             │
│  D: Charge completes but "Initiate Jump" button won't work │
│     └──> Go to BRANCH D: Jump Initiation Failure           │
└─────────────────────────────────────────────────────────────┘
```

---

## BRANCH A: Power/Computer Issues (No Response)

**Symptom**: FTL charge button does nothing, no error displayed

### Check 1: FTL System Power

```
┌────────────────────────────────────────┐
│ Check FTL power indicator              │
│ (usually on FTL control panel)         │
│                                        │
│ Is power indicator lit?                │
└────────────────────────────────────────┘
         │
         ├─────── NO ──────┐
         │                 │
         YES               ▼
         │         ┌──────────────────────────┐
         │         │ Check circuit breakers:  │
         │         │ 1. Main panel            │
         │         │ 2. Look for "FTL DRIVE"  │
         │         │    or "NAVIGATION"       │
         │         │                          │
         │         │ Is breaker tripped?      │
         │         └───────┬──────────────────┘
         │                 │
         │                 ├─── YES ──┐
         │                 │          │
         │                 NO         ▼
         │                 │    ┌──────────────────┐
         │                 │    │ Reset breaker    │
         │                 │    │ Test FTL again   │
         │                 │    │                  │
         │                 │    │ Works? → SOLVED  │
         │                 │    │ Trips again? →   │
         │                 │    │ Electrical fault │
         │                 │    │ (Call support)   │
         │                 │    └──────────────────┘
         │                 │
         │                 ▼
         │         ┌──────────────────────────┐
         │         │ Check power cable        │
         │         │ connections to FTL drive │
         │         │                          │
         │         │ Connections secure?      │
         │         └───────┬──────────────────┘
         │                 │
         │                 ├─── NO ──┐
         │                 │         │
         │                 YES       ▼
         │                 │    ┌──────────────┐
         │                 │    │ Reconnect    │
         │                 │    │ Test → OK?   │
         │                 │    └──────────────┘
         │                 │
         │                 ▼
         │         ┌──────────────────────────┐
         │         │ Power supply failure     │
         │         │ Requires repair          │
         │         │ → ERR-NAV-510            │
         │         └──────────────────────────┘
         │
         ▼
┌────────────────────────────────────────┐
│ Check FTL Computer Status              │
│                                        │
│ Is navigation computer responsive?    │
│ (Can you access nav menus?)           │
└────────────────────────────────────────┘
         │
         ├─────── NO ──────┐
         │                 │
         YES               ▼
         │         ┌──────────────────────────┐
         │         │ Restart navigation       │
         │         │ computer:                │
         │         │ 1. Nav menu → System     │
         │         │ 2. Restart Computer      │
         │         │ 3. Wait 60 seconds       │
         │         │ 4. Test FTL again        │
         │         │                          │
         │         │ Works? → SOLVED          │
         │         │ Still dead? →            │
         │         │ Computer failure         │
         │         │ → ERR-NAV-520            │
         │         └──────────────────────────┘
         │
         ▼
┌────────────────────────────────────────┐
│ FTL control panel has power,           │
│ computer responds, but charge          │
│ still won't initiate                   │
│                                        │
│ → Check BRANCH B: Safety Interlock    │
└────────────────────────────────────────┘
```

---

## BRANCH B: Safety Interlock (Error Message Displayed)

**Symptom**: Error message appears when trying to charge FTL

### Check 2: Read the Error Message

```
┌─────────────────────────────────────────────────────────────┐
│ What error is displayed?                                    │
└─────────────────────────────────────────────────────────────┘
         │
         ├─ "INSUFFICIENT POWER" → Go to B1
         ├─ "MASS SHADOW DETECTED" → Go to B2
         ├─ "TACHYON EMITTER FAULT" → Go to B3
         ├─ "COOLDOWN TIMER ACTIVE" → Go to B4
         ├─ "HULL BREACH DETECTED" → Go to B5
         ├─ "NAVIGATION LOCK FAILED" → Go to B6
         └─ Other error → Note error code, consult ERR-NAV document
```

### B1: Insufficient Power

```
┌─────────────────────────────────────────┐
│ ERROR: "INSUFFICIENT POWER"             │
│                                         │
│ FTL drive requires minimum power from   │
│ Q-Core reactor                          │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check Q-Core reactor output             │
│ - Main panel → Power Systems            │
│ - Check Q-Core output percentage        │
│                                         │
│ Q-Core output?                          │
└─────────────────────────────────────────┘
         │
         ├─── <80% ───┐
         │            │
         ≥80%         ▼
         │     ┌──────────────────────────────┐
         │     │ Q-Core output too low        │
         │     │                              │
         │     │ ACTIONS:                     │
         │     │ 1. Reduce power to           │
         │     │    non-essential systems     │
         │     │ 2. Increase Q-Core output:   │
         │     │    - Main panel → Q-Core     │
         │     │    - Increase to 80%+        │
         │     │ 3. Check for power drain:    │
         │     │    - Heavy cargo systems?    │
         │     │    - Damaged systems?        │
         │     │                              │
         │     │ If cannot reach 80% →        │
         │     │ Q-Core problem (see KB-001)  │
         │     └──────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Q-Core output sufficient but FTL still  │
│ reports insufficient power              │
│                                         │
│ Possible power coupling fault           │
│ → ERR-NAV-515                           │
│ → Requires technician                  │
└─────────────────────────────────────────┘
```

### B2: Mass Shadow Detected

```
┌─────────────────────────────────────────┐
│ ERROR: "MASS SHADOW DETECTED"           │
│                                         │
│ FTL cannot activate too close to        │
│ large masses (planets, stars)           │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check current position:                 │
│ - Navigation → Position                 │
│ - Display nearby celestial objects      │
│                                         │
│ Are you within minimum distance?        │
└─────────────────────────────────────────┘
         │
         ├─── YES (too close) ───┐
         │                       │
         NO (far enough)          ▼
         │              ┌────────────────────────┐
         │              │ Move farther from mass:│
         │              │                        │
         │              │ Minimum distances:     │
         │              │ - Star: 2 AU           │
         │              │ - Planet: 100,000 km   │
         │              │ - Station: 1,000 km    │
         │              │                        │
         │              │ Use sublight engines   │
         │              │ to move to safe zone   │
         │              │                        │
         │              │ → SOLVED               │
         │              └────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ If mass shadow detected but you're      │
│ in open space far from objects:         │
│                                         │
│ 1. Check graviton detector working:     │
│    - Sensors → Graviton Status          │
│ 2. Detector may be malfunctioning       │
│    (false detection)                    │
│ 3. Or uncharted mass nearby             │
│                                         │
│ ACTIONS:                                │
│ - Run graviton detector diagnostic      │
│ - Visual scan for objects               │
│ - Check star charts for unknowns        │
│                                         │
│ If detector faulty → ERR-SENS-420       │
│ If real unknown mass → Report to nav    │
└─────────────────────────────────────────┘
```

### B3: Tachyon Emitter Fault

```
┌─────────────────────────────────────────┐
│ ERROR: "TACHYON EMITTER FAULT"          │
│                                         │
│ One or more tachyon emitters not        │
│ functioning (all 16 required)           │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check emitter status:                   │
│ - Navigation → FTL Systems → Emitters   │
│ - Display shows which emitters failed   │
│                                         │
│ How many emitters show fault?           │
└─────────────────────────────────────────┘
         │
         ├─── 1-2 emitters ───┐
         │                    │
         └─── 3+ emitters ────┤
                              │
                              ▼
              ┌───────────────────────────────┐
              │ Check each faulty emitter:    │
              │                               │
              │ 1. Visual inspect (if EVA     │
              │    possible) - physical damage│
              │ 2. Check power connections    │
              │ 3. Run emitter self-test:     │
              │    - FTL menu → Test Emitters │
              │                               │
              │ Result?                       │
              └───────┬───────────────────────┘
                      │
                      ├─── Pass test ───┐
                      │                 │
                      └─── Fail test ───┤
                                        │
                                        ▼
                        ┌───────────────────────────┐
                        │ Emitter hardware failure  │
                        │                           │
                        │ ACTIONS:                  │
                        │ - 1-2 emitters: May have  │
                        │   spares onboard          │
                        │ - Replace failed emitters │
                        │   (Part #: TAC-EMIT-H2)   │
                        │ - Requires EVA and tools  │
                        │                           │
                        │ If no spares or 3+failed: │
                        │ - Cannot use FTL          │
                        │ - Proceed sublight        │
                        │ - Repair at next port     │
                        │                           │
                        │ → ERR-NAV-530             │
                        └───────────────────────────┘
```

### B4: Cooldown Timer Active

```
┌─────────────────────────────────────────┐
│ ERROR: "COOLDOWN TIMER ACTIVE"          │
│                                         │
│ FTL drive requires rest between jumps   │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check cooldown timer:                   │
│ - FTL panel shows time remaining        │
│                                         │
│ Minimum cooldown by model:              │
│ - Horizon-1: 8 hours                    │
│ - Horizon-2: 6 hours                    │
│ - Horizon-3: 4 hours                    │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ SOLUTION: Wait for cooldown to complete │
│                                         │
│ Cannot be overridden (safety feature)   │
│                                         │
│ Forcing consecutive jumps risks:        │
│ - QFM thermal damage                    │
│ - Catastrophic drive failure            │
│                                         │
│ → WAIT for timer, no workaround         │
│                                         │
│ If emergency requires immediate jump:   │
│ - Understand risk (may destroy drive)   │
│ - Contact ORSM engineering for          │
│   emergency override code (logged)      │
│ - NOT RECOMMENDED                       │
└─────────────────────────────────────────┘
```

### B5: Hull Breach Detected

```
┌─────────────────────────────────────────┐
│ ERROR: "HULL BREACH DETECTED"           │
│                                         │
│ FTL travel with hull breach extremely   │
│ dangerous (safety interlock prevents)   │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check hull integrity:                   │
│ - Hull Systems → Integrity Status       │
│ - Review breach indicators              │
│                                         │
│ Is there an actual breach?              │
└─────────────────────────────────────────┘
         │
         ├─── YES (real breach) ───┐
         │                         │
         NO (false alarm)           ▼
         │              ┌────────────────────────┐
         │              │ CRITICAL:              │
         │              │ - Repair breach before │
         │              │   FTL (see EMERG-010)  │
         │              │ - Temporary patches OK │
         │              │ - Must pass hull       │
         │              │   integrity test       │
         │              │                        │
         │              │ After repair:          │
         │              │ - Run hull diagnostic  │
         │              │ - Verify seal          │
         │              │ - FTL should enable    │
         │              │                        │
         │              │ Cannot override this   │
         │              │ safety (too dangerous) │
         │              └────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ False breach alarm:                     │
│                                         │
│ ACTIONS:                                │
│ 1. Check HIMS sensors:                  │
│    - May be sensor malfunction          │
│    - Run HIMS diagnostic                │
│ 2. Check for pressure loss:             │
│    - Actual breach shows pressure drop  │
│    - Stable pressure = likely false     │
│ 3. Reset HIMS:                          │
│    - Hull Systems → Reset HIMS          │
│    - Re-run integrity check             │
│                                         │
│ If still shows breach but none exists:  │
│ - Sensor fault → ERR-HULL-410           │
│ - May require manual override (risky)   │
│ - Contact support for guidance          │
└─────────────────────────────────────────┘
```

### B6: Navigation Lock Failed

```
┌─────────────────────────────────────────┐
│ ERROR: "NAVIGATION LOCK FAILED"         │
│                                         │
│ Navigation computer cannot calculate    │
│ valid jump vector                       │
└─────────────────────────────────────────┘
         │
         ▼
┌─────────────────────────────────────────┐
│ Check navigation input:                 │
│                                         │
│ 1. Is destination entered correctly?    │
│    - Navigation → Destination           │
│    - Verify coordinates                 │
│                                         │
│ 2. Is destination within jump range?    │
│    - Check distance vs. rated range     │
│    - Horizon-1: 20 LY max               │
│    - Horizon-2: 50 LY max               │
│    - Horizon-3: 100 LY max              │
│                                         │
│ 3. Is jump path clear?                  │
│    - No mass shadows in path            │
│    - Not through planet/star            │
└─────────────────────────────────────────┘
         │
         ├─ Destination problem ─┐
         │                       │
         └─ All inputs correct ──┤
                                 │
                                 ▼
                 ┌───────────────────────────┐
                 │ Fix destination input:    │
                 │                           │
                 │ - Re-enter coordinates    │
                 │ - Choose closer waypoint  │
                 │ - Plot alternate route    │
                 │   avoiding obstacles      │
                 │                           │
                 │ → SOLVED                  │
                 └───────────────────────────┘
                                 │
                                 ▼
                 ┌───────────────────────────┐
                 │ Navigation computer fault:│
                 │                           │
                 │ 1. Restart nav computer   │
                 │ 2. Update star charts     │
                 │    (may be outdated)      │
                 │ 3. Run nav calibration    │
                 │                           │
                 │ Still failing?            │
                 │ - Computer malfunction    │
                 │ - Manual vector input may │
                 │   be possible (advanced)  │
                 │                           │
                 │ → ERR-NAV-540             │
                 └───────────────────────────┘
```

---

## BRANCH C: Charge Sequence Failure (Aborts During Charge)

**Symptom**: FTL charge begins but aborts before completion

### Check 3: When Does Charge Abort?

```
┌─────────────────────────────────────────────────────────────┐
│ At what point does charge sequence abort?                   │
└─────────────────────────────────────────────────────────────┘
         │
         ├─ Immediately (0-10 seconds) → Likely safety check failure
         ├─ Mid-charge (10-60%) → Likely power or temperature issue
         └─ Near complete (60-99%) → Likely field stability issue
         │
         ▼
┌─────────────────────────────────────────┐
│ Check FTL status display during charge: │
│ - Note which parameter causes abort     │
│ - Tachyon field intensity               │
│ - QFM core temperature                  │
│ - Power draw                            │
│ - Field stability                       │
└─────────────────────────────────────────┘
         │
         ├─ Tachyon field won't build → C1
         ├─ QFM overheating → C2
         ├─ Power fluctuations → C3
         └─ Field instability → C4
```

### C1: Tachyon Field Won't Build

```
Problem: Field intensity not reaching required level

CHECK:
1. All 16 emitters functioning? (see B3)
2. Power sufficient to emitters?
3. Emitter alignment correct?

ACTIONS:
- Test each emitter individually
- Check emitter power distribution
- Run emitter alignment calibration
- If emitters OK but field weak: QFM fault

→ ERR-NAV-550 (emitter issue)
→ ERR-NAV-560 (QFM issue)
```

### C2: QFM Overheating

```
Problem: Quantum Field Manipulator temperature exceeds safe limit

CHECK QFM TEMPERATURE:
- Normal charge: 800-1,200°C
- Maximum safe: 1,600°C
- Critical: 1,800°C (abort)

CAUSES:
1. Insufficient cooldown from last jump
   → Wait longer between jumps
2. Cooling system malfunction
   → Check coolant levels and pumps
3. QFM degradation (age/wear)
   → May need replacement

ACTIONS:
1. Allow longer cooldown (add 2+ hours)
2. Check cooling system:
   - Coolant level full?
   - Pumps operating?
   - Radiators clear?
3. Reduce ambient temperature if possible
4. If persists: QFM service needed

→ ERR-NAV-570 (cooling fault)
→ ERR-NAV-571 (QFM degraded)
```

### C3: Power Fluctuations

```
Problem: Power draw unstable, causing charge abort

CHECK:
1. Q-Core output stable?
   - Should maintain steady power during charge
2. Power coupling connections?
3. Other systems drawing power spikes?

ACTIONS:
1. Monitor Q-Core output during charge attempt
   - If drops below 80%: Q-Core problem
   - If fluctuating: Possible coupling or distribution fault
2. Disable non-essential systems during charge
3. Check power coupling connections (see power systems manual)

→ ERR-PWR-XXX (Q-Core issues, see power error codes)
→ ERR-NAV-515 (power coupling fault)
```

### C4: Field Stability Issues

```
Problem: Quantum field unstable, preventing safe jump initiation

CHECK FIELD STABILITY:
- Normal: 95-99%
- Minimum safe: 85%
- Abort threshold: <85%

CAUSES:
1. Graviton compensator overload
2. Nearby gravitational disturbance
3. Field manipulator malfunction
4. Cargo interference (exotic materials)

ACTIONS:
1. Check graviton compensators:
   - Status and load percentage
   - Should be <90% load
   - Calibrate if needed
2. Check for nearby mass disturbances:
   - Move farther from large objects
3. Check cargo:
   - Exotic materials can interfere
   - See cargo restrictions (NAV-FTL-001)
4. Run field stability diagnostic

→ ERR-NAV-580 (graviton compensator)
→ ERR-NAV-585 (field generator)
```

---

## BRANCH D: Jump Initiation Failure (Charge Complete But Won't Jump)

**Symptom**: Charge reaches 100% but "Initiate Jump" fails

```
Charge complete, all systems green, but jump won't initiate

RARE SITUATION - Usually indicates:

1. Final safety check failure
   - Last-second mass shadow detection
   - Navigation lock lost
   - Hull integrity sensor trigger

2. Software glitch
   - Restart navigation computer
   - May need to abort and re-charge

3. Manual safety engaged
   - Check for manual FTL lockout
   - May require command authorization

ACTIONS:
1. Check all safety interlocks again (review Branch B)
2. Restart navigation computer
3. Abort charge, wait 5 minutes, try full sequence again
4. Check for manual FTL disable switch (if equipped)

If all checks pass but still won't jump:
→ ERR-NAV-590 (jump initiation fault)
→ Requires specialist diagnosis
```

---

## Quick Reference Summary

### Most Common Issues (80% of FTL Won't Activate)

1. **Insufficient Power** (30%)
   - Q-Core output <80%
   - Fix: Reduce load, increase reactor output

2. **Too Close to Mass** (25%)
   - Within mass shadow of planet/star
   - Fix: Move to safe distance

3. **Cooldown Timer** (15%)
   - Jumped too recently
   - Fix: Wait for cooldown to complete

4. **Emitter Failure** (10%)
   - One or more emitters damaged
   - Fix: Replace failed emitters

5. **Navigation Lock Failed** (10%)
   - Bad coordinates or path
   - Fix: Re-enter destination correctly

### Immediate First Checks (Do These First)

```
☐ Q-Core output ≥80%?
☐ Distance from nearest planet/star sufficient?
☐ Cooldown timer expired?
☐ All 16 tachyon emitters green?
☐ Hull integrity good (no breaches)?
☐ Destination coordinates valid?
```

If all above are OK, proceed to detailed troubleshooting branches.

---

## Related Documents

- **NAV-FTL-001**: FTL Drive System Overview
- **NAV-FTL-002**: FTL Jump Procedures
- **ERR-NAV**: Navigation Error Codes
- **KB-012**: FTL Jump Fails (detailed KB article)
- **EMERG-006**: FTL Emergency Procedures

---

**Support Tip**: When customer calls with "FTL won't work," first question should be "What exactly happens when you try to charge the FTL drive?" This guides you to the correct branch of this flowchart immediately.
