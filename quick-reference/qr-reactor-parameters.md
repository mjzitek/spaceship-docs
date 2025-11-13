# Quick Reference: Q-Core Reactor Normal Parameters

**Document ID:** QR-PWR-001
**Revision:** 2.1
**Last Updated:** 2847.09.14

## At-A-Glance Parameter Ranges

### Core Temperature
| Mode | Temperature (°C) |
|------|------------------|
| Standby | 600-800 |
| Standard Operation | 1,800-2,400 |
| Maximum Output | 2,400-2,800 |
| **CRITICAL** | **>3,000** |

### Plasma Density
| Status | Density (g/cm³) |
|--------|-----------------|
| Standby | 2.0-2.5 |
| Normal | 3.5-4.2 |
| High | 4.5-5.0 |
| **CRITICAL** | **>5.5** |

### Coolant Pressure
| Status | Pressure (PSI) |
|--------|----------------|
| Minimum Safe | 80 |
| Normal Operating | 120-140 |
| Maximum Safe | 180 |
| **CRITICAL** | **<60 or >200** |

### Magnetic Field Strength
| Status | Field (Tesla) |
|--------|---------------|
| Standby | 4.5 |
| Normal Operation | 6.0-7.5 |
| Maximum | 9.0 |
| **CRITICAL** | **<5.0 during operation** |

### Radiation Level (1m from reactor)
| Status | Dose (mSv/h) |
|--------|--------------|
| Normal | 0.2-0.5 |
| Elevated | 0.6-1.0 |
| Warning | 1.0-2.0 |
| **EVACUATE** | **>2.0** |

## Power Output by Model

### Q-Core Mark III (Civilian)
- **Rated**: 50-150 MW
- **Fuel**: 0.4 kg/day @ 60% power
- **Applications**: Personal craft, shuttles

### Q-Core Mark V (Commercial)
- **Rated**: 200-400 MW
- **Fuel**: 1.2 kg/day @ 60% power
- **Applications**: Freighters, transports

### Q-Core Mark VII (Military)
- **Rated**: 500-800 MW
- **Fuel**: 2.8 kg/day @ 60% power
- **Applications**: Military, heavy industrial

## Operating Modes

### Standby (10% Output)
- **Purpose**: Ready state, quick startup
- **Core Temp**: 600-800°C
- **Field**: 4.5 Tesla
- **Coolant**: 20% flow
- **Startup**: 3-5 minutes to full power

### Standard (60-85% Output)
- **Purpose**: Normal operations
- **Core Temp**: 1,800-2,400°C
- **Field**: 6.0-7.5 Tesla
- **Coolant**: 60% flow
- **Fuel**: Normal consumption rate

### Maximum (95-100% Output)
- **Purpose**: Emergency, combat, FTL charge
- **Core Temp**: 2,400-2,800°C
- **Field**: 7.5-9.0 Tesla
- **Coolant**: 100% flow
- **Duration**: Can sustain continuously if monitored

## Startup Times

### Cold Start (Fully Offline)
- **Duration**: 12-18 minutes
- **Power Required**: 5 kW backup power
- **Procedure**: See PWR-SYS-002

### Hot Start (From Standby)
- **Duration**: 3-5 minutes
- **Power Required**: Reactor self-powered
- **Procedure**: Simplified ramp-up

### Emergency Startup
- **Duration**: 8-10 minutes
- **Risk**: Thermal stress to components
- **Only When**: Life support critical

## Shutdown Times

### Standard Shutdown
- **Duration**: 15-25 minutes
- **Safe**: Controlled cooldown
- **Recommended**: Use whenever possible

### Shutdown to Standby
- **Duration**: 5 minutes
- **Purpose**: Temporary shutdown <48 hours
- **Benefit**: Faster restart

### Emergency SCRAM
- **Duration**: 30-90 seconds
- **Risk**: Component damage from thermal shock
- **Only When**: Imminent danger
- **After**: Requires full inspection before restart

## Critical Warnings

### IMMEDIATE SCRAM Required If:
- Core temperature >3,000°C
- Coolant pressure <60 PSI
- Magnetic field <4.5 Tesla during operation
- Radiation >2.0 mSv/h external
- Plasma containment instability
- Coolant loss detected
- Multiple coil failures

### Investigate Promptly If:
- Core temperature >2,800°C sustained
- Coolant pressure <80 PSI or >180 PSI
- Magnetic field variance ±0.5 Tesla
- Radiation >1.0 mSv/h external
- Single coil failure
- Power output <60% capacity unexpectedly

## Fuel Requirements

### Fuel Type
- **Specification**: D-T pellets (deuterium-tritium)
- **Size**: 3mm diameter
- **Storage**: Cryogenic at -250°C
- **Canister Pressure**: 150-200 PSI

### Consumption Rates (Standard Operation)
- **Mark III**: 0.4 kg/day
- **Mark V**: 1.2 kg/day
- **Mark VII**: 2.8 kg/day

### Canister Replacement
- **When**: Pressure <100 PSI
- **Part Number**: FUL-DT-3MM series
- **Procedure**: See PWR-SYS-002

## Coolant Requirements

### Coolant Type
- **Specification**: Sodium-Potassium Grade-A
- **Part Number**: COL-NAK-100
- **DO NOT SUBSTITUTE**: Other fluids will damage system

### Level Requirements
- **Minimum for Operation**: 85%
- **Optimal**: 92-98%
- **Refill When**: Below 90%

### Replacement Schedule
- **Frequency**: Annually
- **Reason**: Contamination degrades cooling
- **Disposal**: Hazardous material, proper handling required

## Maintenance Intervals

### Daily
- Visual inspection
- Parameter logging
- Radiation scan

### Weekly
- Coolant level check
- Filter inspection
- Radiation survey (detailed)

### Monthly
- Magnetic field calibration
- Injector cleaning
- Full diagnostic

### Quarterly
- Containment vessel inspection
- Coolant flush/replacement
- Component replacement per schedule

### Annually
- Complete system overhaul
- Certification inspection
- Firmware updates

## Common Error Codes

### Startup Errors
- **E-PWR-101**: Fuel system fault
- **E-PWR-102**: Magnetic containment fault
- **E-PWR-103**: Coolant system fault

### Operating Errors
- **E-PWR-201**: Insufficient power output
- **E-PWR-220**: Temperature critical
- **E-PWR-250**: Plasma instability
- **E-PWR-260**: Coolant loss

### Maintenance
- **E-PWR-400**: Routine maintenance due
- **E-PWR-405**: Component lifespan warning

## Emergency Contacts

### ORSM Support Line
- **Standard Support**: 24/7 technical assistance
- **Emergency Hotline**: Critical failures
- **Service Portal**: parts.outerrimstarship.com

### When to Call Emergency Support
- SCRAM event occurred
- Radiation levels dangerous
- Coolant loss or leak
- Containment failure
- Multiple critical errors
- Safety concerns

## Quick Diagnostic Questions

**If Reactor Won't Start:**
1. Fuel canister pressure? (Need 150+ PSI)
2. Coolant level? (Need 85%+)
3. Magnetic coils powered? (All 12 must be green)

**If Low Power Output:**
1. Core temperature? (Should be 1,800-2,400°C)
2. Plasma density? (Should be 3.5-4.2 g/cm³)
3. Injectors clean? (Clean monthly)

**If Overheating:**
1. Coolant flowing? (Verify pumps running)
2. Coolant level? (Must be adequate)
3. Power output? (Reduce if at maximum)

---

**KEEP THIS REFERENCE ACCESSIBLE AT REACTOR CONTROL STATION**

**For complete procedures, see:**
- PWR-SYS-001: Q-Core Reactor Overview
- PWR-SYS-002: Startup and Shutdown
- PWR-SYS-003: Maintenance Guide
- PWR-SYS-004: Troubleshooting Manual
