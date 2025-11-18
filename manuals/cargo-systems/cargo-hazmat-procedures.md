# Hazardous Materials Cargo Procedures

## Overview
Hazardous materials (HAZMAT) require special handling, storage, and emergency procedures to protect crew, vessel, and cargo.

## HAZMAT Classification

### Class 1 - Explosives

#### Division 1.1 - Mass Explosion Hazard
- **Examples**: TNT, dynamite, military ordnance
- **Hazard**: Entire cargo can explode simultaneously
- **Quantity Limits**: Maximum 100 kg per voyage
- **Storage**: Isolated magazine, minimum 50m from other cargo
- **Special Requirements**:
  - Bonded and grounded at all times
  - No static-generating materials nearby
  - Temperature controlled (15-20°C)
  - Armed security if quantity > 10 kg

#### Division 1.2 - Projection Hazard
- **Examples**: Rockets, flares, ammunition
- **Hazard**: Fragments projected but not mass explosion
- **Quantity Limits**: Maximum 500 kg per voyage
- **Storage**: Separate magazine, minimum 25m from other cargo

#### Division 1.3 - Fire Hazard
- **Examples**: Propellants, rocket fuels
- **Hazard**: Fire without explosion
- **Quantity Limits**: Maximum 1,000 kg per voyage
- **Storage**: Fire-resistant compartment

#### Division 1.4 - Minor Blast Hazard
- **Examples**: Fireworks, small arms ammunition
- **Hazard**: Minor explosion hazard
- **Quantity Limits**: Maximum 2,000 kg per voyage
- **Storage**: Standard secure storage

#### Handling Procedures
```
CARGO > HAZMAT_CLASS1 LOAD [item_id]
WARNING: Explosive material
Division: 1.1
Mass: 45 kg
Destination magazine: Bay 5, Isolated section

Pre-load checks:
[ ] Magazine cleared of incompatibles: YES
[ ] Grounding straps connected: YES
[ ] No static sources present: YES
[ ] Temperature verified (15-20°C): YES
[ ] Security notified: YES
[ ] Fire suppression ready: YES

Authorization required: CAPTAIN + CARGO_OFFICER
Authorize (code): **********
Loading authorized. Proceed with caution.
```

### Class 2 - Gases

#### Division 2.1 - Flammable Gases
- **Examples**: Hydrogen, methane, propane, acetylene
- **Hazard**: Fire, explosion, asphyxiation
- **Storage**: Pressure-rated compartment, away from ignition sources
- **Monitoring**: Continuous gas detection

#### Division 2.2 - Non-Flammable, Non-Toxic Gases
- **Examples**: Nitrogen, carbon dioxide, argon, helium
- **Hazard**: Asphyxiation by displacement of oxygen
- **Storage**: Well-ventilated area
- **Monitoring**: Oxygen level sensors

#### Division 2.3 - Toxic Gases
- **Examples**: Chlorine, ammonia, hydrogen sulfide
- **Hazard**: Toxicity, corrosivity
- **Storage**: Isolated compartment with independent ventilation
- **Monitoring**: Gas-specific detectors, continuous monitoring
- **PPE**: Breathing apparatus available immediately outside storage

#### Handling Procedures
```
CARGO > HAZMAT_CLASS2 LOAD [item_id]
Gas type: Hydrogen (Division 2.1)
Container: High-pressure cylinder
Pressure: 200 bar
Volume: 50 liters
Temperature: 20°C

Pre-load checks:
[ ] Cylinder integrity: PASS
[ ] Pressure relief valve: TESTED
[ ] Ventilation system: OPERATIONAL
[ ] Gas detector: CALIBRATED
[ ] No ignition sources: VERIFIED
[ ] Fire suppression: READY

Loading to: Bay 3, Gas storage section
Securing method: Cylinder rack with chains
Monitoring: Continuous H₂ detection
Alert threshold: 100 ppm (0.25% LEL)
```

### Class 3 - Flammable Liquids

#### Categories
- **Flash point < -18°C**: Extremely flammable (gasoline, ether)
- **Flash point -18 to 23°C**: Flammable (diesel, kerosene)
- **Flash point 23 to 60°C**: Combustible (fuel oil, certain chemicals)

#### Storage Requirements
- Fire-resistant compartment
- No ignition sources
- Spill containment
- Bonded and grounded
- Ventilation system
- Foam fire suppression

#### Handling Procedures
```
CARGO > HAZMAT_CLASS3 LOAD [item_id]
Liquid: Ethanol (95%)
Flash point: 13°C
Container: 200L drum, UN-rated
Quantity: 800L (4 drums)

Pre-load checks:
[ ] Container integrity: INSPECTED
[ ] Spill containment ready: YES
[ ] Bonding cable connected: YES
[ ] Ventilation active: YES
[ ] Foam suppression charged: YES
[ ] No ignition sources (10m radius): VERIFIED
[ ] Incompatibles removed: YES

Loading to: Bay 2, Flammable liquid storage
Securing: Drum rack with restraints
Spill kit location: Bay 2, Station 1
```

### Class 4 - Flammable Solids

#### Division 4.1 - Flammable Solids
- **Examples**: Matches, sulfur, metal powders
- **Hazard**: Ignition by friction, heat, or moisture
- **Storage**: Cool, dry location

#### Division 4.2 - Spontaneously Combustible
- **Examples**: White phosphorus, oily rags, certain chemicals
- **Hazard**: Self-ignition in air
- **Storage**: Air-tight containers, temperature controlled

#### Division 4.3 - Dangerous When Wet
- **Examples**: Sodium, calcium carbide, lithium
- **Hazard**: Release flammable gases when wet
- **Storage**: Absolutely dry location, sealed containers

### Class 5 - Oxidizers and Organic Peroxides

#### Division 5.1 - Oxidizers
- **Examples**: Nitrates, chlorates, perchlorates, hydrogen peroxide
- **Hazard**: Intensify fires, react with organics
- **Storage**: Isolated from flammables, organics, and reducing agents
- **Special**: No contamination with organics (oils, grease)

#### Division 5.2 - Organic Peroxides
- **Examples**: Benzoyl peroxide, methyl ethyl ketone peroxide
- **Hazard**: Explosive decomposition, fire
- **Storage**: Temperature controlled (typically < 25°C)
- **Monitoring**: Continuous temperature

### Class 6 - Toxic and Infectious Substances

#### Division 6.1 - Toxic Substances
- **Examples**: Pesticides, cyanides, heavy metal compounds
- **Hazard**: Poisoning by inhalation, ingestion, or skin contact
- **Storage**: Isolated, secure, well-ventilated
- **PPE**: Protective equipment staged outside storage

#### Division 6.2 - Infectious Substances
- **Examples**: Medical samples, cultures, diagnostic specimens
- **Hazard**: Disease transmission
- **Storage**: Biohazard-rated containers, temperature controlled
- **Special**: Triple containment required

### Class 7 - Radioactive Materials

#### Categories by Activity Level
- **Low**: < 1 TBq (industrial sources)
- **Medium**: 1-1000 TBq (medical isotopes)
- **High**: > 1000 TBq (fuel elements)

#### Storage Requirements
- Shielded compartment
- Radiation monitoring (continuous)
- Distance from crew areas
- Secured and locked
- Dosimetry records

#### Handling Procedures
```
CARGO > HAZMAT_CLASS7 LOAD [item_id]
Material: Cobalt-60 source
Activity: 5 TBq
Half-life: 5.27 years
Radiation type: Gamma
Container: Lead-shielded Type B package

Pre-load checks:
[ ] Radiation survey: COMPLETE
[ ] Container integrity: CERTIFIED
[ ] Shielding verified: PASS
[ ] Monitors calibrated: YES
[ ] Personnel dosimeters: ISSUED
[ ] Exclusion zone established: YES
[ ] Emergency equipment ready: YES

Loading to: Bay 4, Shielded compartment
Exposure rate at 1m: 0.05 mSv/hr (acceptable)
Maximum handling time: 30 minutes
Personnel: 2 (radiation safety certified)
Monitoring: Continuous area monitors + personal dosimeters
```

### Class 8 - Corrosive Materials

#### Categories
- **Acids**: Sulfuric, hydrochloric, nitric
- **Bases**: Sodium hydroxide, potassium hydroxide
- **Others**: Certain salts, batteries

#### Storage Requirements
- Corrosion-resistant compartment
- Acids separated from bases
- Spill containment
- Neutralization materials available
- Ventilation system

### Class 9 - Miscellaneous Dangerous Goods

#### Examples
- Magnetized materials
- Dry ice
- Lithium batteries
- Marine pollutants
- Environmentally hazardous substances

## Segregation Requirements

### Incompatibility Matrix

```
         | 1.1 | 1.4 | 2.1 | 2.2 | 2.3 | 3  | 4.1 | 4.2 | 4.3 | 5.1 | 5.2 | 6.1 | 6.2 | 7  | 8  |
---------|-----|-----|-----|-----|-----|----| ----|-----|-----|-----|-----|-----|-----|----|----|
Class1.1 |  X  |  X  |  X  |  2m |  X  | X  |  X  |  X  |  X  |  X  |  X  | 10m | 5m  | 5m | X  |
Class1.4 |  X  |  2m |  X  |  *  |  X  | X  |  X  |  X  |  X  |  X  |  X  | 2m  | 2m  | 2m | X  |
Class2.1 |  X  |  X  |  2m |  *  |  X  | 5m |  X  |  X  |  X  |  X  |  X  | 2m  | *   | 2m | 2m |
Class2.2 |  2m |  *  |  *  |  *  |  X  | *  |  *  |  *  |  *  |  *  |  *  | *   | *   | *  | *  |
Class2.3 |  X  |  X  |  X  |  X  |  5m | X  |  X  |  X  |  X  |  X  |  X  | 5m  | X   | 5m | X  |
Class 3  |  X  |  X  |  5m |  *  |  X  | 2m |  5m |  X  |  X  |  X  |  X  | 2m  | *   | 2m | 5m |
Class4.1 |  X  |  X  |  X  |  *  |  X  | 5m |  2m |  X  |  X  |  X  |  X  | 2m  | *   | 2m | 2m |
Class4.2 |  X  |  X  |  X  |  *  |  X  | X  |  X  |  X  |  X  |  X  |  X  | 2m  | *   | 2m | X  |
Class4.3 |  X  |  X  |  X  |  *  |  X  | X  |  X  |  X  |  X  |  X  |  X  | 2m  | *   | 2m | X  |
Class5.1 |  X  |  X  |  X  |  *  |  X  | X  |  X  |  X  |  X  |  5m |  X  | 2m  | *   | 2m | 5m |
Class5.2 |  X  |  X  |  X  |  *  |  X  | X  |  X  |  X  |  X  |  X  |  X  | 2m  | *   | 2m | X  |
Class6.1 | 10m |  2m |  2m |  *  |  5m | 2m |  2m |  2m |  2m |  2m |  2m | 2m  | 5m  | 2m | 2m |
Class6.2 |  5m |  2m |  *  |  *  |  X  | *  |  *  |  *  |  *  |  *  |  *  | 5m  | 2m  | 2m | *  |
Class 7  |  5m |  2m |  2m |  *  |  5m | 2m |  2m |  2m |  2m |  2m |  2m | 2m  | 2m  | *  | 2m |
Class 8  |  X  |  X  |  2m |  *  |  X  | 5m |  2m |  X  |  X  |  5m |  X  | 2m  | *   | 2m | 5m |

Legend:
X = Must be separated (different compartments)
* = No restriction
#m = Minimum separation distance in meters
```

## Monitoring Requirements

### Continuous Monitoring

#### Required Sensors
- **Gas detectors**: For gaseous hazmat and volatiles
- **Temperature probes**: For temperature-sensitive materials
- **Pressure sensors**: For compressed gases
- **Radiation monitors**: For radioactive materials
- **Humidity sensors**: For moisture-sensitive materials
- **Motion detectors**: For security

#### Alert Thresholds
```
CARGO > HAZMAT_MONITORING STATUS

Bay 3 - Flammable gas storage:
- H₂ concentration: 0 ppm (Alarm: 100 ppm)
- O₂ level: 20.9% (Alarm: < 19.5% or > 23%)
- Temperature: 22°C (Alarm: > 30°C)
- Pressure: 1.01 bar (Normal)

Bay 4 - Radioactive storage:
- Gamma radiation: 0.02 mSv/hr (Alarm: > 0.1 mSv/hr)
- Temperature: 21°C (Normal)
- Security: LOCKED (Alarm on unauthorized access)

Bay 2 - Flammable liquid storage:
- Vapor concentration: 0% LEL (Alarm: > 10% LEL)
- Temperature: 20°C (Alarm: > 35°C)
- Spill detection: DRY (Alarm on liquid detected)

All systems: NOMINAL
Last calibration: 36 hours ago
Next calibration: 12 hours
```

## Emergency Response

### Hazmat Spill Response

#### Immediate Actions
1. **Alert**
   - Activate hazmat alarm
   - Notify all crew
   - Alert hazmat team

2. **Contain**
   - Seal affected compartment
   - Activate ventilation (if appropriate)
   - Stop source if safe

3. **Protect**
   - Don appropriate PPE
   - Establish safe perimeter
   - Account for all personnel

4. **Mitigate**
   - Deploy spill kit
   - Neutralize/absorb spill
   - Prevent spread
   - Document incident

#### Spill Kit Contents
- Absorbent pads and pillows
- Neutralizing agents
- Containment dikes
- Non-sparking tools
- PPE (gloves, suits, respirators)
- Waste bags (hazmat rated)
- Spill response guide

### Fire Involving Hazmat

#### Special Considerations
- **Class 1 (Explosives)**: Evacuate, jettison if possible
- **Class 2.1 (Flammable gas)**: Do not extinguish unless leak can be stopped
- **Class 3 (Flammable liquid)**: Use foam, not water
- **Class 4.2 (Spontaneous combustible)**: Smother, exclude oxygen
- **Class 4.3 (Water reactive)**: Do NOT use water, use dry powder
- **Class 5 (Oxidizer)**: Copious water to cool, remove fuel
- **Class 7 (Radioactive)**: Extinguish fire, contain runoff, minimize exposure

### Hazmat Exposure

#### Inhalation
1. Remove victim from exposure
2. Move to fresh air
3. Administer oxygen if available
4. Monitor breathing
5. Get medical attention immediately
6. Consult MSDS for specific treatment

#### Skin Contact
1. Remove contaminated clothing
2. Flush with copious water (15+ minutes)
3. For acids: Can neutralize with weak base solution
4. For bases: Can neutralize with weak acid solution
5. Get medical attention
6. Consult MSDS

#### Eye Contact
1. Flush immediately with water (15+ minutes)
2. Remove contact lenses if present
3. Continue flushing
4. Get medical attention urgently
5. Consult MSDS

#### Ingestion
1. Do NOT induce vomiting unless directed
2. Rinse mouth with water
3. Give water to drink (if conscious)
4. Get medical attention immediately
5. Bring MSDS to medical personnel

## Documentation Requirements

### Material Safety Data Sheet (MSDS/SDS)
Required for ALL hazmat cargo:
- Chemical identification
- Hazard identification
- Composition/ingredients
- First aid measures
- Fire-fighting measures
- Accidental release measures
- Handling and storage
- Exposure controls/PPE
- Physical and chemical properties
- Stability and reactivity
- Toxicological information
- Ecological information
- Disposal considerations
- Transport information
- Regulatory information

### Hazmat Manifest
```
CARGO > HAZMAT_MANIFEST DISPLAY

Hazmat Manifest - Voyage #1247
Departure: Earth Station Alpha
Destination: Mars Colony Beta
Date: 2157-06-15

Item 1:
- UN Number: UN1230
- Proper Shipping Name: Methanol
- Class: 3 (Flammable liquid), 6.1 (Toxic)
- Packing Group: II
- Quantity: 200 L
- Location: Bay 2, Section D
- Emergency Contact: +1-800-HAZMAT-1

Item 2:
- UN Number: UN1005
- Proper Shipping Name: Ammonia, anhydrous
- Class: 2.3 (Toxic gas), 8 (Corrosive)
- Packing Group: N/A
- Quantity: 50 kg
- Location: Bay 3, Isolated section
- Emergency Contact: +1-800-HAZMAT-1

Item 3:
- UN Number: UN2915
- Proper Shipping Name: Radioactive material, Type B package
- Class: 7 (Radioactive)
- Packing Group: N/A
- Activity: 5 TBq
- Location: Bay 4, Shielded compartment
- Emergency Contact: +1-800-RAD-SAFE

Total hazmat items: 3
Crew briefed: YES
Emergency equipment verified: YES
```

## Required Equipment

### Personal Protective Equipment (PPE)

**Level A - Maximum Protection**
- Fully encapsulating suit
- Self-contained breathing apparatus (SCBA)
- Chemical-resistant gloves (double layer)
- Chemical-resistant boots
- Use for: Unknown hazards, highly toxic gases

**Level B - Respiratory Protection**
- Chemical splash suit
- SCBA
- Chemical-resistant gloves
- Chemical-resistant boots
- Use for: Known hazard, high concentration

**Level C - Respiratory Protection**
- Chemical splash suit
- Air-purifying respirator (APR)
- Chemical-resistant gloves
- Chemical-resistant boots
- Use for: Known hazard, low concentration, adequate oxygen

**Level D - Minimal Protection**
- Coveralls
- Safety glasses
- Gloves
- Boots
- Use for: No significant hazard

### Emergency Equipment Locations

```
CARGO > HAZMAT_EQUIPMENT LOCATE

PPE Lockers:
- Level A suits (2): Bay 3, Station 1
- Level B suits (4): Bays 2, 3, 4
- Level C suits (6): All cargo bays
- SCBAs (6): Emergency stations 1, 2, 3
- APRs (12): All cargo bays

Spill Kits:
- Universal (4): Each cargo bay
- Acid (2): Bays 2 and 4
- Base (2): Bays 2 and 4
- Mercury (1): Medical bay

Decontamination:
- Emergency shower: Each cargo bay entrance
- Eye wash station: Each cargo bay entrance
- Decon station: Airlock 2

Monitoring Equipment:
- Multi-gas detector (4): Emergency stations
- Radiation meter (2): Bay 4, Medical
- pH paper: All spill kits
```

## Training Requirements

### Mandatory Training
- Hazmat Awareness (all crew)
- Hazmat Operations (cargo crew)
- Hazmat Technician (hazmat specialists)
- Hazmat Specialist (hazmat officers)

### Refresher Training
- Annual recertification required
- Incident-based training after any hazmat event
- Updates when regulations change

### Practical Exercises
- Quarterly spill drills
- Annual full-scale hazmat emergency drill
- PPE donning/doffing practice (monthly)

## Required Certifications
- Hazmat Cargo Handler certification
- Hazmat Emergency Response certification
- Radiation Safety (for radioactive cargo)
- SCBA operation qualification

## Related Documentation
- See: `cargo-handling-procedures.md` for general cargo procedures
- See: `cargo-management-overview.md` for system overview
- See: `emerg-011-cargo-hazmat-emergency.md` for emergencies
- See: Material Safety Data Sheets (MSDS) for each hazmat item

## Revision History
- v4.1 - Updated segregation requirements
- v4.0 - New UN hazmat classification system
- v3.5 - Added radiation monitoring procedures
- v3.0 - Comprehensive rewrite for new regulations
