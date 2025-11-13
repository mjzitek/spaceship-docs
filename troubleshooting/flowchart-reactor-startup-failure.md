# Troubleshooting Flowchart: Q-Core Reactor Startup Failure

**Document ID:** FLOW-PWR-001
**Revision:** 2.3
**Last Updated:** 2847.09.14
**Use Case:** Reactor won't start, ignition fails, or plasma won't form

## How to Use This Flowchart

1. Start at the top
2. Answer each question YES or NO
3. Follow the arrows to next step
4. Continue until you reach a SOLUTION box
5. Implement the solution
6. If solution doesn't work, return to flowchart and try alternate path

---

## START: Reactor Startup Attempted But Failed

```
┌─────────────────────────────────────────────────────────┐
│   REACTOR STARTUP ATTEMPTED - IGNITION FAILED           │
│                                                          │
│   Error codes may include:                              │
│   E-PWR-101, E-PWR-102, E-PWR-103, E-PWR-104, E-PWR-105 │
└──────────────────────┬──────────────────────────────────┘
                       │
                       ▼
              ┌────────────────┐
              │  Is control    │
              │  panel powered │
              │  and showing   │
              │  displays?     │
              └────┬───────┬───┘
                   │       │
                YES│       │NO
                   │       │
                   │       ▼
                   │  ┌─────────────────────────┐
                   │  │ CHECK POWER SUPPLY      │
                   │  │                         │
                   │  │ 1. Check main breaker   │
                   │  │ 2. Verify Q-Core backup │
                   │  │    power (5 kW needed)  │
                   │  │ 3. Check control board  │
                   │  │    fuses                │
                   │  │ 4. Reset breaker        │
                   │  │                         │
                   │  │ SOLUTION A: Power Issue │
                   │  │ See PWR-SYS-002         │
                   │  └─────────────────────────┘
                   │
                   ▼
              ┌────────────────┐
              │  What error    │
              │  code is       │
              │  displayed?    │
              └────┬───────────┘
                   │
        ┌──────────┼──────────┬─────────────┐
        │          │          │             │
    E-PWR-101  E-PWR-102  E-PWR-103    Other/None
        │          │          │             │
        ▼          ▼          ▼             ▼
   ┌────────┐ ┌────────┐ ┌────────┐   ┌─────────┐
   │ FUEL   │ │MAGNETIC│ │COOLANT │   │CONTINUE │
   │ SYSTEM │ │ SYSTEM │ │ SYSTEM │   │ BELOW   │
   │ PATH   │ │  PATH  │ │  PATH  │   │         │
   └────┬───┘ └────┬───┘ └────┬───┘   └────┬────┘
        │          │          │             │
        │          │          │             │
```

---

## Path 1: FUEL SYSTEM (E-PWR-101)

```
┌─────────────────────────────────────┐
│  E-PWR-101: FUEL SYSTEM FAULT       │
└──────────────┬──────────────────────┘
               │
               ▼
        ┌──────────────┐
        │ Check fuel   │
        │ canister     │
        │ pressure     │
        │ gauge        │
        └──┬───────────┘
           │
    ┌──────┴──────┐
    │             │
  <100 PSI    150-200 PSI
    │             │
    ▼             ▼
┌─────────────┐  ┌──────────────┐
│ SOLUTION B: │  │ Pressure OK  │
│             │  │ Check fuel   │
│ Replace     │  │ valve        │
│ depleted    │  └──┬───────────┘
│ fuel        │     │
│ canister    │     ▼
│             │  ┌──────────────┐
│ Part #:     │  │ Is fuel valve│
│ FUL-DT-3MM  │  │ fully open?  │
│             │  └──┬───────────┘
│ Procedure:  │     │
│ 1. Close    │  ┌──┴────┐
│    main     │  │       │
│    valve    │ YES     NO
│ 2. Depres-  │  │       │
│    surize   │  │       ▼
│ 3. Replace  │  │  ┌──────────┐
│ 4. Open     │  │  │SOLUTION C│
│    valve    │  │  │          │
│ 5. Verify   │  │  │Open fuel │
│    pressure │  │  │valve to  │
│             │  │  │full open │
└─────────────┘  │  │position  │
                 │  └──────────┘
                 │
                 ▼
         ┌───────────────┐
         │ Check fuel    │
         │ injectors     │
         │               │
         │ Run injector  │
         │ test:         │
         │ System >      │
         │ Fuel >        │
         │ Injector Test │
         └───┬───────────┘
             │
      ┌──────┴─────┐
      │            │
   PASS         FAIL
      │            │
      ▼            ▼
┌──────────┐  ┌────────────┐
│ Fuel OK  │  │ SOLUTION D │
│ Check    │  │            │
│ other    │  │ Clean or   │
│ systems  │  │ replace    │
└──────────┘  │ clogged    │
              │ injectors  │
              │            │
              │ Part #:    │
              │ INJ-ASM-Q  │
              │ series     │
              │            │
              │ See        │
              │ PWR-SYS-003│
              └────────────┘
```

---

## Path 2: MAGNETIC CONTAINMENT (E-PWR-102)

```
┌─────────────────────────────────────┐
│  E-PWR-102: MAGNETIC FAILURE        │
└──────────────┬──────────────────────┘
               │
               ▼
        ┌──────────────┐
        │ Check coil   │
        │ power supply │
        │ voltage      │
        └──┬───────────┘
           │
    ┌──────┴─────┐
    │            │
 <380 VDC    380-420 VDC
    │            │
    ▼            ▼
┌──────────┐  ┌────────────┐
│SOLUTION E│  │ Voltage OK │
│          │  │ Test coils │
│Check:    │  └──┬─────────┘
│1. Breaker│     │
│   tripped│     ▼
│2. Power  │  ┌────────────┐
│   feed   │  │ Run coil   │
│3. Reset  │  │ diagnostic:│
│   breaker│  │ System >   │
│          │  │ Magnetic > │
│If trips  │  │ Coil Test  │
│again:    │  └──┬─────────┘
│Wiring    │     │
│fault     │  ┌──┴──────┐
│Escalate  │  │         │
└──────────┘ ALL      ANY
             PASS    FAIL
              │        │
              ▼        ▼
        ┌─────────┐ ┌────────────┐
        │ Coils   │ │ SOLUTION F │
        │ working │ │            │
        │ Check   │ │ Replace    │
        │ field   │ │ failed     │
        │ strength│ │ coil(s)    │
        └─────────┘ │            │
                    │ Part #:    │
                    │ MAG-COIL-Q │
                    │ series     │
                    │            │
                    │ After      │
                    │ replacement│
                    │ recalibrate│
                    │ magnetic   │
                    │ field      │
                    └────────────┘
```

---

## Path 3: COOLANT SYSTEM (E-PWR-103)

```
┌─────────────────────────────────────┐
│  E-PWR-103: COOLANT NOT READY       │
└──────────────┬──────────────────────┘
               │
               ▼
        ┌──────────────┐
        │ Check coolant│
        │ level        │
        │ indicator    │
        └──┬───────────┘
           │
    ┌──────┴─────┐
    │            │
  <85%        ≥85%
    │            │
    ▼            ▼
┌──────────┐  ┌────────────┐
│SOLUTION G│  │ Level OK   │
│          │  │ Check pumps│
│Top off   │  └──┬─────────┘
│coolant:  │     │
│          │     ▼
│Part #:   │  ┌────────────┐
│COL-NAK-  │  │ Are coolant│
│100       │  │ pumps      │
│          │  │ running?   │
│Fill to   │  └──┬─────────┘
│92-98%    │     │
│          │  ┌──┴────┐
│Check for │  │       │
│leaks!    │ YES     NO
└──────────┘  │       │
              │       ▼
              │  ┌──────────┐
              │  │SOLUTION H│
              │  │          │
              │  │Start     │
              │  │coolant   │
              │  │pumps:    │
              │  │          │
              │  │1. Check  │
              │  │   pump   │
              │  │   power  │
              │  │2. Reset  │
              │  │   pump   │
              │  │   control│
              │  │3. Manual │
              │  │   start  │
              │  │          │
              │  │If won't  │
              │  │start:    │
              │  │Pump may  │
              │  │be failed │
              │  └──────────┘
              │
              ▼
         ┌──────────┐
         │ Check    │
         │ coolant  │
         │ flow rate│
         └──┬───────┘
            │
     ┌──────┴────┐
     │           │
   NORMAL      LOW
     │           │
     ▼           ▼
┌─────────┐  ┌──────────┐
│ Coolant │  │SOLUTION I│
│ system  │  │          │
│ OK      │  │Check for:│
│         │  │1. Blocked│
│ Retry   │  │   lines  │
│ startup │  │2. Closed │
└─────────┘  │   valves │
             │3. Air in │
             │   system │
             │4. Pump   │
             │   wear   │
             │          │
             │Purge air,│
             │open      │
             │valves,   │
             │clear     │
             │blockages │
             └──────────┘
```

---

## Path 4: OTHER/NO ERROR CODE

```
┌─────────────────────────────────────┐
│  NO ERROR CODE OR OTHER ERROR       │
└──────────────┬──────────────────────┘
               │
               ▼
        ┌──────────────┐
        │ Does plasma  │
        │ form briefly │
        │ then die?    │
        └──┬───────────┘
           │
    ┌──────┴─────┐
    │            │
   YES          NO
    │            │
    ▼            ▼
┌──────────┐  ┌────────────┐
│SOLUTION J│  │ Check if   │
│          │  │ all pre-   │
│Magnetic  │  │ startup    │
│field too │  │ conditions │
│weak to   │  │ met:       │
│contain   │  └──┬─────────┘
│plasma    │     │
│          │     ▼
│Increase  │  ┌────────────┐
│field     │  │ □ Coolant  │
│strength  │  │   ≥85%     │
│or        │  │ □ Backup   │
│recalibrate│  │   power    │
│          │  │   ≥5kW     │
│See:      │  │ □ Fuel     │
│PWR-SYS-003│  │   150+PSI  │
└──────────┘  │ □ All      │
              │   panels   │
              │   closed   │
              │ □ No       │
              │   safety   │
              │   lockouts │
              └──┬─────────┘
                 │
          ┌──────┴────┐
          │           │
       ALL MET    MISSING
          │           │
          ▼           ▼
     ┌─────────┐  ┌──────────┐
     │SOLUTION K│  │ SOLUTION │
     │          │  │          │
     │Control   │  │ Meet all │
     │system    │  │ missing  │
     │reset:    │  │ prereqs  │
     │          │  │          │
     │1. Breaker│  │ Then     │
     │   OFF    │  │ retry    │
     │2. Wait   │  │ startup  │
     │   30 sec │  └──────────┘
     │3. Breaker│
     │   ON     │
     │4. Wait   │
     │   60 sec │
     │5. Retry  │
     │          │
     │See:      │
     │KB-001    │
     └──────────┘
```

---

## Path 5: SCRAM LOCKOUT

```
┌─────────────────────────────────────┐
│  Reactor shows "SCRAM LOCKOUT"      │
│  or recent emergency shutdown       │
└──────────────┬──────────────────────┘
               │
               ▼
        ┌──────────────┐
        │ Was reactor  │
        │ SCRAM'd      │
        │ recently?    │
        └──┬───────────┘
           │
          YES
           │
           ▼
     ┌────────────────────────────┐
     │ SOLUTION L                 │
     │                            │
     │ POST-SCRAM INSPECTION      │
     │ REQUIRED                   │
     │                            │
     │ Reactor CANNOT restart     │
     │ after SCRAM until:         │
     │                            │
     │ 1. Complete inspection     │
     │    by qualified technician │
     │ 2. Verify no damage        │
     │ 3. Document findings       │
     │ 4. Manual lockout reset    │
     │    (requires tech auth)    │
     │                            │
     │ SCRAM causes thermal       │
     │ stress - components may    │
     │ be damaged                 │
     │                            │
     │ DO NOT BYPASS lockout      │
     │                            │
     │ See: EMERG-005             │
     └────────────────────────────┘
```

---

## Quick Decision Tree Summary

```
START
  │
  ├─ Panel dark? → CHECK POWER (Solution A)
  │
  ├─ E-PWR-101? → CHECK FUEL
  │   ├─ Low pressure? → REPLACE CANISTER (Solution B)
  │   ├─ Valve closed? → OPEN VALVE (Solution C)
  │   └─ Injectors fail? → CLEAN INJECTORS (Solution D)
  │
  ├─ E-PWR-102? → CHECK MAGNETIC
  │   ├─ Low voltage? → CHECK BREAKER (Solution E)
  │   └─ Coil failed? → REPLACE COIL (Solution F)
  │
  ├─ E-PWR-103? → CHECK COOLANT
  │   ├─ Low level? → TOP OFF COOLANT (Solution G)
  │   ├─ Pump not running? → START PUMP (Solution H)
  │   └─ Low flow? → CLEAR BLOCKAGE (Solution I)
  │
  ├─ Plasma dies? → WEAK FIELD (Solution J)
  │
  ├─ No error? → CHECK PREREQS/RESET (Solution K)
  │
  └─ SCRAM lockout? → TECH INSPECTION (Solution L)
```

---

## Solution Quick Reference

| Solution | Issue | Fix | Time | Parts Needed |
|----------|-------|-----|------|--------------|
| A | No power | Check breaker | 5 min | None |
| B | Depleted fuel | Replace canister | 15 min | FUL-DT-3MM |
| C | Closed valve | Open fuel valve | 2 min | None |
| D | Clogged injectors | Clean injectors | 2 hrs | INJ-ASM-Q (if damaged) |
| E | No coil power | Reset breaker | 5 min | None |
| F | Failed coil | Replace coil | 8 hrs | MAG-COIL-Q |
| G | Low coolant | Top off coolant | 15 min | COL-NAK-100 |
| H | Pump stopped | Start pump | 10 min | PMP-COL-Q (if failed) |
| I | Blocked coolant | Clear blockage | 1 hr | None |
| J | Weak field | Recalibrate | 1 hr | None |
| K | System glitch | Reset control | 5 min | None |
| L | SCRAM lockout | Tech inspection | Varies | Varies |

---

## Related Documents

- PWR-SYS-001: Q-Core Reactor Overview
- PWR-SYS-002: Startup and Shutdown Procedures
- PWR-SYS-003: Maintenance Guide
- PWR-SYS-004: Troubleshooting Manual (detailed)
- KB-001: Reactor Won't Start (quick guide)
- EMERG-005: Reactor Emergency Procedures
- ERR-PWR-100: Power System Error Codes

---

**NOTE**: This flowchart covers common startup failures. For complex issues, intermittent problems, or cases where flowchart doesn't resolve issue, consult PWR-SYS-004 Troubleshooting Manual or contact ORSM support.
