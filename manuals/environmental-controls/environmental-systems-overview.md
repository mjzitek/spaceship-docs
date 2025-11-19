# Environmental Control Systems Overview

## Overview
Environmental Control and Life Support Systems (ECLSS) maintain a habitable environment for the crew. This includes atmosphere composition, temperature, humidity, pressure, and contaminant removal.

## System Architecture

### Primary Functions
1. **Atmosphere Management**: Oxygen generation, CO₂ removal, pressure control
2. **Thermal Control**: Heating and cooling
3. **Humidity Control**: Water vapor management
4. **Air Quality**: Contaminant removal, filtration
5. **Pressure Control**: Maintaining proper atmospheric pressure

### System Integration
- **Life Support**: Primary atmospheric processing
- **Thermal Management**: Heat distribution and rejection
- **Water Systems**: Humidity control, recycling
- **Power Systems**: Energy supply for all functions
- **Sensors**: Continuous environmental monitoring

## Atmospheric Composition

### Target Parameters

**Standard Earth-Like Atmosphere**:
- **Oxygen (O₂)**: 21% ± 1%
- **Nitrogen (N₂)**: 78% ± 1%
- **Other gases**: 1% (argon, trace gases, water vapor)
- **Carbon Dioxide (CO₂)**: < 0.5% (5,000 ppm maximum)
- **Total Pressure**: 1.0 bar (101.3 kPa) ± 0.05 bar
- **Temperature**: 20-24°C (adjustable by zone)
- **Humidity**: 40-60% relative humidity

### Atmospheric Monitoring

```
ENVIRONMENTAL > ATMOSPHERE STATUS

=== ATMOSPHERIC CONDITIONS ===

Oxygen (O₂): 20.9% [Target: 21% ± 1%] - NORMAL
Nitrogen (N₂): 78.5% [Target: 78% ± 1%] - NORMAL
Carbon Dioxide (CO₂): 0.12% (1,200 ppm) [Max: 0.5%] - NORMAL
Pressure: 1.01 bar [Target: 1.0 ± 0.05] - NORMAL
Temperature: 22°C [Target: 20-24°C] - NORMAL
Humidity: 48% RH [Target: 40-60%] - NORMAL

Contaminants:
  Particulates: 5 μg/m³ [Max: 50 μg/m³] - LOW
  VOCs: 0.2 ppm [Max: 2 ppm] - LOW
  Carbon Monoxide: 0 ppm [Max: 10 ppm] - NONE

Air Quality Index: 98/100 (EXCELLENT)

Last full system test: 2 days ago
Next scheduled test: 5 days
```

## Oxygen Generation

### Primary O₂ Generation - Electrolysis

#### System: Water Electrolysis Unit
- **Location**: Life support bay, Deck 3
- **Capacity**: 5 kg O₂ per day (supports 20 crew)
- **Process**: Split water (H₂O) into oxygen and hydrogen
- **Input**: Purified water from recycling system
- **Outputs**:
  - Oxygen → Atmosphere
  - Hydrogen → Vented or used for fuel cells

#### Operating Principle
```
2H₂O + electrical energy → 2H₂ + O₂

Water is split into hydrogen and oxygen gas using electrical current.
```

**Power Requirements**: 50 kW continuous
**Water Consumption**: 9 kg per day
**Efficiency**: 75%

#### Status Monitoring
```
ENVIRONMENTAL > O2_GENERATION STATUS

Oxygen Generation System:

Status: OPERATIONAL
Mode: AUTO (maintains 21% O₂)
Current output: 210 g/hour (5 kg/day capacity)
Power consumption: 52 kW

Electrolysis cells:
  Cell 1: ACTIVE, 98% efficiency
  Cell 2: ACTIVE, 97% efficiency
  Cell 3: STANDBY
  Cell 4: STANDBY (backup)

Water input: 375 g/hour (from recycling system)
O₂ output: 210 g/hour (to atmosphere)
H₂ output: 165 g/hour (vented to space)

System health: NOMINAL
Next maintenance: 15 days
```

### Backup O₂ Systems

#### Compressed O₂ Tanks
- **Capacity**: 500 kg total (100 days for 5 crew at minimal activity)
- **Pressure**: 200 bar
- **Number**: 10 tanks @ 50 kg each
- **Location**: Distributed storage
- **Use**: Emergency backup, EVA supply, medical use

#### Chemical O₂ Generators
- **Type**: Sodium chlorate candles
- **Capacity**: 50 kg O₂ (10 canisters)
- **Duration**: 10 days for 5 crew (emergency only)
- **Activation**: Manual, one-time use
- **Storage**: Emergency locker

## Carbon Dioxide Removal

### Primary CO₂ Removal - Scrubbers

#### System: Regenerative CO₂ Scrubber
- **Technology**: Amine-based absorption
- **Location**: Life support bay, Deck 3
- **Capacity**: Remove CO₂ from entire ship atmosphere
- **Cycle**: Absorb CO₂, then regenerate scrubber by heating

#### Operating Cycle

**Absorption Phase** (4 hours):
- Air circulated through scrubber beds
- CO₂ absorbed by amine solution
- Clean air returned to ship
- Monitor CO₂ levels continuously

**Regeneration Phase** (2 hours):
- Heat scrubber to release CO₂
- CO₂ vented to space or stored
- Scrubber cooled and ready for reuse
- Switch to backup scrubber during regeneration

#### Status Monitoring
```
ENVIRONMENTAL > CO2_REMOVAL STATUS

CO₂ Removal System:

Status: OPERATIONAL
Mode: AUTOMATIC

Scrubber A: ABSORBING (2.5 hours into cycle)
  CO₂ removed this cycle: 8.2 kg
  Capacity remaining: 65%
  Switch to regeneration in: 1.5 hours

Scrubber B: STANDBY (regenerated, ready)
  Last regeneration: 3 hours ago
  Ready for use: YES

Ship CO₂ level: 0.12% (1,200 ppm)
Target: < 0.5% (5,000 ppm)
Status: WELL BELOW LIMIT

CO₂ generation rate: 2.5 kg/hour (14 crew members)
CO₂ removal rate: 2.6 kg/hour (adequate)

System health: NOMINAL
Next maintenance: 8 days
```

### Backup CO₂ Removal

#### Lithium Hydroxide (LiOH) Canisters
- **Capacity**: 50 canisters (emergency supply)
- **Each canister**: Absorbs 2.5 kg CO₂
- **Duration**: ~10 days for full crew (emergency)
- **Type**: One-time use, not regenerable
- **Use**: Emergency only, backup system

## Temperature Control

### Heating and Cooling Systems

#### Heat Management Zones

**Zone 1 - Habitation Areas**
- **Target**: 20-24°C (adjustable)
- **Includes**: Crew quarters, common areas, bridge
- **Individual Control**: Each cabin adjustable ± 2°C

**Zone 2 - Work Areas**
- **Target**: 18-22°C
- **Includes**: Cargo bays, workshops, engineering
- **Cooling Priority**: Higher (equipment generates heat)

**Zone 3 - Critical Systems**
- **Target**: 15-20°C
- **Includes**: Computer core, reactor control, power systems
- **Priority**: HIGHEST (must maintain for safety)

**Zone 4 - Storage Areas**
- **Target**: 10-25°C (less critical)
- **Includes**: General storage, non-critical areas
- **Priority**: LOW (adjust as needed for power savings)

#### Temperature Control
```
ENVIRONMENTAL > TEMPERATURE CONTROL

=== TEMPERATURE BY ZONE ===

Zone 1 (Habitation):
  Current: 22°C
  Target: 20-24°C
  Status: NORMAL
  Crew comfort: OPTIMAL

Zone 2 (Work Areas):
  Current: 20°C
  Target: 18-22°C
  Status: NORMAL
  Equipment operating temp: SAFE

Zone 3 (Critical Systems):
  Current: 18°C
  Target: 15-20°C
  Status: NORMAL
  Priority: HIGHEST

Zone 4 (Storage):
  Current: 16°C
  Target: 10-25°C
  Status: NORMAL
  Priority: LOW

=== SYSTEM STATUS ===

Heat Generation: 450 kW (total ship)
  Reactor: 200 kW waste heat
  Equipment: 150 kW
  Crew/life support: 50 kW
  Solar absorption: 50 kW

Heat Rejection: 455 kW (adequate)
  Radiators: 400 kW
  Active cooling: 55 kW

Thermal Balance: +5 kW (slight cooling trend)
Status: NOMINAL
```

### Heat Rejection - Radiators

#### Radiator Panels
- **Location**: External hull, port and starboard
- **Area**: 100 m² per side (200 m² total)
- **Type**: Deployable panels with heat pipes
- **Coolant**: Ammonia loop
- **Capacity**: 500 kW heat rejection (maximum)
- **Operating Temperature**: -50°C to +50°C

#### Radiator Control
```
ENVIRONMENTAL > RADIATOR STATUS

Deployable Radiator Panels:

Port Side Radiator:
  Status: DEPLOYED
  Panel Area: 100 m²
  Heat Rejection: 225 kW
  Coolant Temp: 10°C (inlet), -5°C (outlet)
  Flow Rate: 150 L/min
  Panel Orientation: Optimal (away from sun)
  Micrometeorite Hits: 3 (no damage)

Starboard Side Radiator:
  Status: DEPLOYED
  Panel Area: 100 m²
  Heat Rejection: 225 kW
  Coolant Temp: 10°C (inlet), -5°C (outlet)
  Flow Rate: 150 L/min
  Panel Orientation: Optimal (away from sun)
  Micrometeorite Hits: 5 (no damage)

Total Heat Rejection: 450 kW
Capacity Available: 50 kW (10% margin)

Coolant System:
  Coolant: Ammonia (NH₃)
  Pressure: 2.5 bar
  Leak Detection: NEGATIVE
  Pump Status: NOMINAL

Recommendations:
  - Normal operation
  - Adequate cooling capacity
  - Monitor solar radiation levels
```

#### Coolant Loop
1. **Cold Side**: Picks up heat from ship systems
2. **Pump**: Circulates coolant
3. **Radiator**: Rejects heat to space
4. **Return**: Cool coolant returns to ship

### Emergency Cooling

**If radiators damaged or insufficient**:
1. **Reduce Heat Generation**:
   - Non-essential systems offline
   - Reduce crew activity
   - Minimize reactor output (if safe)

2. **Vent Coolant** (emergency only):
   - Spray water into space
   - Water evaporates, carrying heat
   - Limited by water supply

3. **Heat Sinks** (temporary):
   - Ice storage can absorb heat temporarily
   - Limited duration (hours)

## Humidity Control

### Target Humidity
- **Range**: 40-60% relative humidity
- **Optimal**: 45-50% for crew comfort and equipment

### Humidity Management

**Too High (> 60%)**:
- Condensation risk
- Mold/mildew growth
- Equipment corrosion
- **Solution**: Activate dehumidifiers

**Too Low (< 40%)**:
- Dry skin, irritation
- Static electricity
- Respiratory discomfort
- **Solution**: Inject water vapor into atmosphere

```
ENVIRONMENTAL > HUMIDITY CONTROL

Current Humidity: 48% RH
Target: 40-60% RH
Status: OPTIMAL

Dehumidifiers:
  Unit 1: STANDBY (on demand)
  Unit 2: STANDBY (on demand)
  Water collected (24h): 12 liters

Humidifiers:
  Unit 1: OFFLINE (not needed)
  Unit 2: OFFLINE (not needed)

Water Recovery:
  - Dehumidifier water → Recycling system
  - Humidity contributes to water balance

Condensation Risk: LOW
Mold/Mildew Risk: LOW

Recommendations: Current levels optimal, no action needed
```

## Air Circulation and Filtration

### Air Circulation System

**Circulation Rate**: Complete air exchange every 2 hours

#### Circulation Fans
- **Number**: 20 fans (distributed throughout ship)
- **Capacity**: 1,000 m³/hour each
- **Power**: 500W per fan
- **Redundancy**: Can lose 25% of fans and maintain adequate circulation

#### Air Distribution
- Main ducts carry air to all compartments
- Return ducts bring air back to ECLSS
- Balanced flow (input = output for each compartment)
- Adjustable vents in each compartment

### Air Filtration

#### Particulate Filters (HEPA)
- **Efficiency**: 99.97% of particles > 0.3 μm
- **Location**: All air intakes
- **Replacement**: Every 90 days or when clogged
- **Purpose**: Remove dust, debris, biological particles

#### Activated Carbon Filters
- **Purpose**: Remove odors, volatile organic compounds (VOCs)
- **Location**: Secondary filtration stage
- **Replacement**: Every 180 days
- **Effectiveness**: Absorbs chemical contaminants

#### Chemical/Biological Filters
- **Type**: CBRN (Chemical, Biological, Radiological, Nuclear)
- **Location**: Emergency filtration system
- **Purpose**: Extreme contamination scenarios
- **Activation**: Manual, emergency use only

```
ENVIRONMENTAL > FILTRATION STATUS

Air Filtration System:

HEPA Filters:
  Location: Main air intake
  Status: OPERATIONAL
  Pressure Drop: 45 Pa (Normal: < 100 Pa)
  Efficiency: 99.97%
  Age: 62 days (Replace at 90 days)
  Recommendation: NORMAL OPERATION

Activated Carbon Filters:
  Location: Secondary filtration
  Status: OPERATIONAL
  Saturation: 45%
  Age: 125 days (Replace at 180 days)
  Recommendation: NORMAL OPERATION

CBRN Filters:
  Status: SEALED (emergency use only)
  Condition: GOOD (tested annually)
  Last Test: 45 days ago

Particulate Level: 5 μg/m³ (Excellent)
VOC Level: 0.2 ppm (Low)
Odor Control: EFFECTIVE

Filter replacement schedule:
  - HEPA: 28 days
  - Carbon: 55 days
```

## Pressure Control

### Pressure Regulation

**Target Pressure**: 1.0 bar (101.3 kPa)
**Tolerance**: ± 0.05 bar

#### Pressure Monitoring
```
ENVIRONMENTAL > PRESSURE STATUS

Atmospheric Pressure: 1.01 bar (101.3 kPa)
Target: 1.0 ± 0.05 bar
Status: NORMAL

Pressure by Compartment:
  Bridge: 1.01 bar - NORMAL
  Habitation: 1.01 bar - NORMAL
  Engineering: 1.01 bar - NORMAL
  Cargo Bay: 1.01 bar - NORMAL
  Medical: 1.02 bar - NORMAL (positive pressure)

Pressure Control:
  Inlet valves: AUTO
  Exhaust valves: AUTO
  Emergency vents: CLOSED

Leak Rate: < 0.1% per day (ACCEPTABLE)
  Normal: 0.05% per day from micro-leaks
  Action required if: > 0.5% per day

Last pressure test: 3 days ago (PASSED)
Next pressure test: 4 days
```

### Pressure Emergencies

#### Rapid Decompression
**If pressure drops rapidly**:
1. **Automatic Response**:
   - Seal all pressure doors automatically
   - Isolate affected compartment
   - Alert all crew
   - Emergency O₂ masks deploy

2. **Crew Actions**:
   - Don emergency breathing equipment
   - Proceed to safe compartment
   - Account for all personnel
   - Report to bridge

3. **Damage Control**:
   - Locate breach
   - Seal compartment
   - Patch breach if possible
   - Restore pressure gradually

#### Slow Leak
**If pressure slowly decreasing**:
1. Increase O₂ generation to compensate
2. Locate leak (ultrasonic detector, visual)
3. Repair leak
4. Restore normal pressure

## Emergency Environmental Systems

### Emergency Breathing Masks

**Location**: Throughout ship (every compartment)
**Type**: Demand-flow oxygen masks
**Supply**: 15 minutes per mask
**Use**: Immediate response to contamination or decompression

```
ENVIRONMENTAL > EMERGENCY_EQUIPMENT

Emergency Environmental Equipment:

Emergency Breathing Masks:
  Total: 48 masks
  Locations: 12 stations
  Status: READY
  Last inspection: 5 days ago
  Oxygen supply: FULL

Pressure Suits:
  Total: 6 suits
  Location: Emergency locker 1, 2
  Status: READY
  Last inspection: 7 days ago

Portable O₂ Bottles:
  Total: 20 bottles
  Capacity: 2 hours each
  Status: FULL
  Pressure: 200 bar

Emergency Atmosphere:
  Compressed O₂: 500 kg (100 days emergency)
  LiOH Canisters: 50 units (10 days emergency)
  Status: ADEQUATE

Recommendations: All emergency equipment ready and adequate
```

### Atmospheric Contamination Response

**If toxic gas or contamination detected**:

1. **Alert**: Immediate ship-wide alarm
2. **Isolation**: Seal affected compartment(s)
3. **Protection**: Don breathing equipment
4. **Ventilation**: Activate emergency ventilation
   - Purge contaminated air to space
   - Supply fresh air from tanks
5. **Filtration**: Activate CBRN filters
6. **Source Control**: Identify and eliminate source
7. **Monitoring**: Continuous atmosphere testing
8. **All-Clear**: When contamination below safe levels

## System Maintenance

### Daily Checks
```
ENVIRONMENTAL > DAILY_CHECKS

Environmental Systems Daily Checklist:

[1/8] Atmospheric Composition
  [ ] O₂ level: 20.9% (NORMAL)
  [ ] CO₂ level: 0.12% (NORMAL)
  [ ] Pressure: 1.01 bar (NORMAL)
  [ ] Contaminants: NONE

[2/8] Temperature
  [ ] All zones within target: YES
  [ ] Radiators deployed: YES
  [ ] Cooling adequate: YES

[3/8] Humidity
  [ ] Relative humidity: 48% (NORMAL)
  [ ] No condensation: VERIFIED

[4/8] O₂ Generation
  [ ] Electrolysis units: OPERATIONAL
  [ ] Output adequate: YES
  [ ] Water supply: ADEQUATE

[5/8] CO₂ Removal
  [ ] Scrubbers operational: YES
  [ ] CO₂ levels controlled: YES

[6/8] Air Circulation
  [ ] All fans operational: 20/20
  [ ] Air flow adequate: YES

[7/8] Filtration
  [ ] HEPA filters: CLEAN
  [ ] Carbon filters: EFFECTIVE

[8/8] Emergency Equipment
  [ ] Emergency masks: READY
  [ ] O₂ tanks: FULL

Daily check: COMPLETE
All environmental systems: NOMINAL
```

### Weekly Maintenance
- Test emergency breathing masks
- Calibrate atmospheric sensors
- Inspect filters (visual)
- Check for leaks (ultrasonic)
- Test pressure relief valves
- Review consumption trends

### Monthly Maintenance
- Replace HEPA filters (or as needed)
- Clean air circulation fans
- Inspect ductwork
- Test emergency ventilation
- Calibrate pressure sensors
- Full system functional test

### Quarterly Maintenance
- Replace activated carbon filters
- Service electrolysis cells
- Regenerate/replace scrubber material
- Inspect radiator panels
- Test all emergency systems
- Complete pressure test (all compartments)

## Required Certifications
- Life Support Systems Operator (Level 2 minimum)
- Atmospheric Control Specialist
- Emergency Response certification
- Environmental Systems Technician (for maintenance)

## Related Documentation
- See: `life-support/atmospheric-processing.md` for detailed processes
- See: `life-support/water-recycling-system.md` for water systems
- See: `emerg-010-hull-breach-decompression.md` for emergencies
- See: `power-systems/q-core-reactor-overview.md` for power requirements

## Revision History
- v3.8 - Enhanced contamination response procedures
- v3.5 - Updated O₂ generation specifications
- v3.2 - Added zone temperature control
- v3.0 - Complete rewrite for new ECLSS system
