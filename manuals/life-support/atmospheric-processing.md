# Atmospheric Processing Unit (APU) System

**Document ID:** LIFE-ATM-001
**Revision:** 4.1
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Purpose

This document describes the Atmospheric Processing Unit (APU) system responsible for maintaining breathable air, regulating atmospheric pressure, and removing contaminants in ORSM vessels.

## System Description

The APU is a closed-loop life support system that continuously processes cabin atmosphere to maintain safe, breathable conditions for crew and passengers. The system recycles air, removes CO₂ and toxins, generates oxygen, and regulates pressure and humidity.

### Operating Principle

The APU operates through five continuous processes:

1. **Air Circulation**: Fans draw cabin air through processing system
2. **Filtration**: HEPA filters remove particulates and biological contaminants
3. **CO₂ Scrubbing**: Chemical absorption removes carbon dioxide
4. **O₂ Generation**: Electrolysis splits water into oxygen and hydrogen
5. **Climate Control**: Temperature and humidity regulation

### Key Components

- **Circulation Fans**: 4-12 fans (depending on vessel size) moving air through system
- **HEPA Filter Banks**: Three-stage filtration removing 99.97% of particles
- **CO₂ Scrubber Assembly**: Chemical beds absorbing carbon dioxide
- **Electrolysis Unit**: Water-splitting apparatus generating oxygen
- **Humidity Controller**: Condensation and evaporation system
- **Atmospheric Sensors**: 20+ sensors monitoring air quality throughout vessel
- **Pressure Regulator**: Maintains cabin pressure at safe levels
- **Emergency Air Tanks**: Backup oxygen supply (6-24 hour capacity)

## APU Models

### APU-Compact (Small Vessels)
- **Capacity**: 1-4 crew members
- **Air Volume**: 100-300 cubic meters
- **O₂ Generation**: 0.5-1.2 kg/day
- **Power Consumption**: 2-4 kW
- **Typical Vessels**: Shuttles, scouts, escape pods

### APU-Standard (Medium Vessels)
- **Capacity**: 5-20 crew members
- **Air Volume**: 500-2,000 cubic meters
- **O₂ Generation**: 2-6 kg/day
- **Power Consumption**: 8-15 kW
- **Typical Vessels**: Freighters, transports, patrol craft

### APU-Industrial (Large Vessels)
- **Capacity**: 25-100 crew members
- **Air Volume**: 3,000-10,000 cubic meters
- **Air Volume**: 3,000-10,000 cubic meters
- **O₂ Generation**: 8-30 kg/day
- **Power Consumption**: 25-60 kW
- **Typical Vessels**: Large freighters, military vessels, passenger ships

## Normal Operating Parameters

| Parameter | Minimum | Optimal Range | Maximum | Critical |
|-----------|---------|---------------|---------|----------|
| Cabin Pressure | 85 kPa | 95-105 kPa | 110 kPa | 115 kPa |
| Oxygen Level | 18% | 19.5-21% | 23% | 25% |
| CO₂ Level | <0.1% | <0.04% | 0.5% | 1.0% |
| Temperature | 10°C | 18-24°C | 30°C | 35°C |
| Humidity | 20% | 40-60% | 75% | 85% |
| Particulate Count | 0 | <100/m³ | 500/m³ | 1000/m³ |
| Air Changes/Hour | 4 | 6-10 | 15 | N/A |

## Safety Systems

### Automatic Safeguards

- **Oxygen Depletion Alert**: Alarm when O₂ drops below 19%
- **CO₂ Accumulation Warning**: Alert when CO₂ exceeds 0.4%
- **Pressure Loss Detection**: Monitors for hull breach or leak
- **Filter Clog Indicator**: Alerts when airflow restricted
- **Toxin Detector**: Sensors identify harmful gases (CO, methane, ammonia)
- **Automatic Scrubber Regeneration**: Chemical bed refresh cycle
- **Emergency Air Release**: Deploys backup oxygen if system fails

### Manual Controls

- Emergency air tank activation
- Individual compartment isolation (seal sections with contaminated air)
- Manual pressure equalization
- Atmosphere venting (extreme emergencies only)
- Backup fan activation

## Consumables and Supplies

### Replaceable Components

**HEPA Filters** (Part #: FLT-HEPA-APU)
- Lifespan: 6 months typical use
- Replacement: Monthly inspection, replace when airflow drops 30%
- Quantity: 6-18 filters depending on APU model

**CO₂ Scrubber Cartridges** (Part #: SCR-CO2-series)
- Lifespan: 30-45 days of operation
- Replacement: When saturation indicator shows red
- Quantity: 2 active + 2 spare minimum

**Electrolysis Electrodes** (Part #: ELC-OXY-PLT)
- Lifespan: 12-18 months
- Replacement: When oxygen generation efficiency drops below 85%
- Quantity: 1 set per electrolysis unit

### Consumables

**Water for Electrolysis**
- Consumption: 1.1 kg water per 1.0 kg oxygen produced
- Source: Ship's water recycling system
- Quality: Purified, deionized water required

**Scrubber Regeneration Chemical** (Part #: RGN-SCR-100)
- Purpose: Refreshes CO₂ scrubber beds
- Usage: 0.5 kg per regeneration cycle
- Frequency: Every 15 days typical

**Emergency Oxygen** (compressed)
- Storage: High-pressure tanks (3,000 PSI)
- Capacity: 6-24 hours breathable air depending on vessel/crew
- Replacement: After use or every 2 years

## Daily Monitoring

Crew should check APU status daily:

1. **Review Atmospheric Sensor Readings**
   - O₂ level (should be 19.5-21%)
   - CO₂ level (should be <0.04%)
   - Cabin pressure (95-105 kPa)
   - Temperature and humidity

2. **Check Status Indicators**
   - Green: All systems normal
   - Yellow: Warning condition, investigate
   - Red: Critical condition, immediate action required

3. **Inspect HEPA Filters**
   - Visual check through inspection windows
   - Note if filters appear dirty or clogged
   - Check airflow indicator (should be in green range)

4. **Verify Fan Operation**
   - Listen for unusual sounds
   - Check vibration (should be minimal)
   - Confirm all fans running (check tachometer readings)

5. **Log Readings**
   - Record parameters in daily log
   - Required for warranty and regulatory compliance
   - Helps identify trends before they become problems

## Weekly Maintenance

**Time Required**: 30-45 minutes

### Task 1: Filter Inspection and Replacement

1. Check filter airflow indicators
   - Green: Filters clean, adequate airflow
   - Yellow: Filters partially clogged, monitor closely
   - Red: Filters clogged, replacement required

2. Remove and inspect pre-filters
   - Located at air intake points
   - Can be washed and reused 3-4 times
   - Replace if damaged or heavily soiled

3. Check HEPA filter banks
   - Visually inspect through access panels
   - Measure differential pressure across filters
   - If pressure drop >150 Pa, replacement recommended

### Task 2: CO₂ Scrubber Check

1. Check scrubber saturation indicators
   - Fresh cartridge: Blue indicator
   - Partially saturated: Purple indicator
   - Saturated (replace): Red indicator

2. Verify scrubber airflow
   - Should hear air passing through chemical beds
   - Check inlet and outlet temperatures (outlet should be slightly warmer)

3. Monitor CO₂ levels
   - Should remain <0.04% with functional scrubbers
   - Rising CO₂ indicates saturation or malfunction

### Task 3: Electrolysis Unit Performance

1. Check oxygen generation rate
   - Compare actual O₂ production to expected rate
   - Should match consumption by crew (approx 0.84 kg/person/day)

2. Inspect water supply
   - Verify adequate purified water available
   - Check water quality (conductivity should be <10 μS/cm)
   - Inspect water feed lines for leaks

3. Monitor electrolysis cell current
   - Should be steady at rated value
   - Fluctuating current indicates electrode degradation

## Monthly Maintenance

**Time Required**: 2-3 hours

### Task 1: Comprehensive Filter Service

1. Replace all HEPA filters if:
   - In use for 6 months
   - Airflow indicator showing yellow/red
   - Particulate count elevated despite filtration

2. Clean or replace pre-filters
3. Clean fan blades and housings
4. Check fan motor bearings (should spin freely, no grinding)

### Task 2: CO₂ Scrubber Regeneration or Replacement

1. If using regenerable scrubbers:
   - Remove cartridges from service
   - Heat to 200°C for 4 hours (drives off absorbed CO₂)
   - Add regeneration chemical per manufacturer instructions
   - Cool and reinstall
   - Test with CO₂ challenge

2. If using disposable scrubbers:
   - Replace saturated cartridges
   - Dispose of used cartridges per environmental regulations
   - Install fresh cartridges
   - Verify proper seating and airflow

### Task 3: Sensor Calibration

1. Calibrate atmospheric sensors:
   - O₂ sensor: Use calibration gas (20.9% O₂)
   - CO₂ sensor: Use zero air and span gas
   - Pressure sensor: Compare to reference barometer
   - Humidity sensor: Use salt solution calibration

2. Replace any sensors showing drift >2% from standard

3. Document calibration in maintenance log

### Task 4: System Diagnostic Test

1. Connect diagnostic tablet to APU control panel
2. Run "Complete System Test":
   - Fan performance test
   - Filter airflow test
   - Scrubber efficiency test
   - Electrolysis output test
   - Sensor accuracy verification
   - Emergency backup test

3. Review results and address any failures

## Emergency Procedures

### Low Oxygen Emergency (O₂ < 18%)

**IMMEDIATE ACTIONS:**

1. Sound alarm and alert all crew
2. Activate emergency oxygen tanks
   - Located in strategic positions throughout vessel
   - Press "EMERGENCY O₂" button on APU panel

3. Reduce crew activity (minimize oxygen consumption)
4. Check for obvious problems:
   - Electrolysis unit running?
   - Hull breach venting air to space?
   - Fire consuming oxygen?

5. Increase electrolysis rate to maximum
6. If O₂ continues dropping, prepare for evacuation

**See EMERG-008 for complete low oxygen procedures.**

### High CO₂ Emergency (CO₂ > 0.5%)

**IMMEDIATE ACTIONS:**

1. Alert crew (symptoms: headache, dizziness, rapid breathing)
2. Check CO₂ scrubbers:
   - Verify airflow through scrubbers
   - Check saturation indicators
   - Replace if saturated

3. Increase air circulation (run fans at maximum)
4. Reduce crew activity (minimize CO₂ production)
5. If multiple crew, consider isolating personnel to separate compartments

### Pressure Loss (Cabin Pressure Dropping)

**IMMEDIATE ACTIONS:**

1. Sound decompression alarm
2. Identify location of leak:
   - Check hull breach detectors
   - Listen for hissing sounds
   - Feel for air current
   - Use smoke test if available

3. Seal leak if possible:
   - Emergency hull patches
   - Close bulkhead doors to isolate section
   - Use emergency sealant foam

4. Activate emergency air to maintain pressure
5. If unable to stop leak, evacuate affected compartment and seal

**See EMERG-007 for complete decompression procedures.**

### Toxic Contamination

**IMMEDIATE ACTIONS:**

1. If toxin sensors alarm or crew shows symptoms:
   - Identify contaminant (check sensor readings)
   - Locate source (fire, chemical spill, equipment malfunction)

2. Activate emergency respirators
3. Increase air filtration and circulation
4. Isolate contaminated compartment if possible
5. Vent contaminated air to space if safe to do so (only if sufficient emergency O₂ available)

### Complete APU Failure

**IMMEDIATE ACTIONS:**

1. Activate all emergency air tanks
2. Calculate available air time:
   - Tank capacity / (crew count × 0.84 kg/person/day)
   - Provides hours to days depending on tanks and crew

3. Attempt manual APU restart:
   - Check power supply
   - Reset APU controller
   - Engage backup systems

4. If restart fails:
   - Ration emergency air
   - Reduce crew activity to minimum
   - Send distress signal
   - Prepare for emergency docking or rescue

## Troubleshooting

### O₂ Levels Dropping

**Possible Causes:**
- Electrolysis unit malfunction
- Water supply exhausted
- Hull leak
- Crew count exceeds rated capacity

**Diagnostics:**
1. Check electrolysis unit output (should produce 0.84 kg per person per day)
2. Verify water supply and purity
3. Scan for hull breaches
4. Confirm crew count within APU capacity rating

### CO₂ Levels Rising

**Possible Causes:**
- Scrubber saturation
- Inadequate air circulation
- Scrubber bypass due to fan failure
- Crew count exceeds capacity

**Diagnostics:**
1. Check scrubber saturation indicators
2. Verify all fans operating
3. Measure airflow through scrubbers
4. Confirm crew count within rated capacity

### Pressure Fluctuations

**Possible Causes:**
- Minor hull leak
- Pressure regulator malfunction
- Airlock cycling
- Thermal expansion/contraction

**Diagnostics:**
1. Monitor pressure trend over time
2. Check for correlation with temperature changes
3. Inspect airlocks for seal integrity
4. Test pressure regulator function

### High Humidity

**Possible Causes:**
- Humidity controller malfunction
- Excessive moisture from crew
- Coolant leak contaminating air
- Condensation system failure

**Diagnostics:**
1. Check humidity controller operation
2. Inspect condensation collector (should be draining)
3. Look for water leaks or spills
4. Verify crew activities (cooking, bathing produce moisture)

**See LIFE-ATM-003 for complete troubleshooting guide.**

## Related Documents

- LIFE-ATM-002: APU Maintenance Schedule
- LIFE-ATM-003: APU Troubleshooting Guide
- LIFE-WAT-001: Water Recycling System
- EMERG-007: Decompression Emergency Procedures
- EMERG-008: Low Oxygen Emergency Procedures
- ERR-LIFE-100: Life Support Error Codes

---

**CRITICAL REMINDER**: Atmospheric system is critical for crew survival. Never defer maintenance. Always maintain adequate supply of filters, scrubber cartridges, and emergency air.
