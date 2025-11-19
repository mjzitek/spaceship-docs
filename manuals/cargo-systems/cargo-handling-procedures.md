# Cargo Handling Procedures

## Overview
Safe and efficient cargo handling is critical for vessel operations, crew safety, and cargo integrity. This manual covers all aspects of cargo loading, securing, monitoring, and unloading.

## Pre-Loading Preparations

### Cargo Bay Inspection

#### Daily Inspection Checklist
- [ ] Cargo bay doors operational
- [ ] Pressure seals intact
- [ ] Lighting functional (100%)
- [ ] Atmosphere verified (breathable)
- [ ] Temperature within limits (10-30°C)
- [ ] Securing points inspected
- [ ] Deck clear of debris
- [ ] Fire suppression systems tested
- [ ] Emergency exits unobstructed
- [ ] Loading equipment operational

#### Equipment Check
- [ ] Cargo crane functional
- [ ] Power loaders charged (minimum 80%)
- [ ] Magnetic grapples tested
- [ ] Cargo nets inspected
- [ ] Securing straps tested (load rated)
- [ ] Anti-gravity pallets operational
- [ ] Cargo scanner functional
- [ ] Weight sensors calibrated

### Cargo Documentation Review

#### Required Documents
- **Manifest**: Complete list of cargo items
- **MSDS**: Material Safety Data Sheets for hazmat
- **Certificates**: Required for regulated cargo
- **Insurance**: Proof of cargo insurance
- **Customs**: Clearance for restricted items
- **Special Handling**: Instructions for sensitive cargo

#### Manifest Verification
```
CARGO > MANIFEST LOAD [manifest_id]
Items: 247
Total mass: 1,847,523 kg
Total volume: 3,214 m³
Hazmat items: 3
Special handling: 12
Destination: Alpha Centauri Station
```

## Cargo Classification

### By Handling Requirements

#### Class A - Standard Cargo
- **Description**: Non-hazardous, standard handling
- **Examples**: Consumer goods, packaged food, textiles
- **Special Requirements**: None
- **Loading Priority**: Normal

#### Class B - Fragile Cargo
- **Description**: Damage-sensitive items
- **Examples**: Electronics, glassware, artwork
- **Special Requirements**:
  - Maximum acceleration: 2G
  - Shock-absorbing packaging
  - Climate control
  - Minimal handling
- **Loading Priority**: Load last, unload first

#### Class C - Heavy Cargo
- **Description**: High-mass individual items
- **Examples**: Machinery, vehicles, structural components
- **Special Requirements**:
  - Reinforced securing points
  - Center-of-mass near ship centerline
  - Load distribution analysis
  - Certified rigging
- **Loading Priority**: Load first (low in bay)

#### Class D - Hazardous Materials (HAZMAT)
- **Description**: Dangerous goods
- **Examples**: Chemicals, radioactive materials, explosives, compressed gases
- **Special Requirements**:
  - Isolated storage
  - Special containment
  - Environmental monitoring
  - Emergency equipment nearby
  - Crew certification required
- **Loading Priority**: As per hazmat regulations

#### Class E - Perishable Cargo
- **Description**: Time or environment sensitive
- **Examples**: Food, biological samples, medical supplies
- **Special Requirements**:
  - Temperature control
  - Atmosphere control
  - Time-sensitive delivery
  - Regular monitoring
- **Loading Priority**: Quick loading, immediate departure

#### Class F - Live Cargo
- **Description**: Living organisms
- **Examples**: Livestock, plants, research specimens
- **Special Requirements**:
  - Life support systems
  - Regular care and feeding
  - Veterinary/botanical support
  - Humane conditions
  - Special permits
- **Loading Priority**: Load last, unload first, immediate care

#### Class G - Valuable Cargo
- **Description**: High-value items
- **Examples**: Precious metals, gems, currency, artifacts
- **Special Requirements**:
  - Secure storage (vault)
  - Armed security
  - Insurance verification
  - Chain of custody documentation
  - Restricted access
- **Loading Priority**: Supervised loading, secure immediately

## Loading Procedures

### Standard Loading Sequence

#### 1. Cargo Reception
```
CARGO > BEGIN_LOADING
Enter manifest ID: [id]
Verify crew ready: YES
Cargo bay pressurized: YES
Loading equipment ready: YES
Begin cargo reception.
```

#### 2. Cargo Inspection
**For Each Item**:
1. Verify against manifest
2. Visual inspection for damage
3. Scan for contraband (if required)
4. Weigh and measure
5. Photograph for records
6. Log reception in system

```
CARGO > INSPECT_ITEM [item_id]
Scanning item...
Type: Class A - Standard
Mass: 450 kg
Volume: 2.1 m³
Condition: Good
Matches manifest: YES
Accept (Y/N): Y
Item logged.
```

#### 3. Cargo Placement

**Placement Priorities**:
1. **Heavy items low**: Lower center of gravity
2. **Dense loading**: Minimize wasted space
3. **Access order**: Last-in-first-out if unloading sequence known
4. **Compatibility**: Separate incompatible materials
5. **Weight distribution**: Balance port/starboard, fore/aft
6. **Emergency access**: Keep aisles clear

**Load Distribution Computer**:
```
CARGO > PLACEMENT_ADVISOR [item_id]
Analyzing current load distribution...
Recommended location: Bay 2, Section C, Row 4
Reason: Balance starboard loading
Alternative: Bay 1, Section A, Row 2
Center of gravity after loading: OPTIMAL
Proceed (Y/N): Y
```

#### 4. Cargo Securing

**Securing Methods**:

**A. Tie-Down Straps**
- Use for: Standard cargo, irregular shapes
- Requirements:
  - Minimum 4 attachment points
  - Rated for 3x cargo mass
  - No sharp edges on cargo
  - Inspect before each use

**B. Cargo Nets**
- Use for: Multiple small items, irregular loads
- Requirements:
  - Mesh size appropriate for cargo
  - Rated for total enclosed mass
  - Secured at minimum 8 points
  - No protruding items

**C. Magnetic Locks**
- Use for: Metallic cargo, palletized loads
- Requirements:
  - Verify magnetic compatibility
  - Minimum 4 lock points
  - Test lock strength before release
  - Backup with straps for critical cargo

**D. Friction Clamps**
- Use for: Palletized cargo, containers
- Requirements:
  - Clean contact surfaces
  - Proper clamp size for load
  - Torque to specification
  - Lock mechanisms engaged

**E. Anti-Gravity Restraints**
- Use for: Extremely heavy or delicate items
- Requirements:
  - AG system calibrated
  - Backup power supply verified
  - Secondary mechanical backup
  - Continuous monitoring

**Securing Verification**:
```
CARGO > SECURE_VERIFY [item_id]
Testing securing integrity...
Method: Tie-down straps (4 points)
Strap tension: NOMINAL
Attachment points: SECURE
Load test: PASS (10G simulated)
Shift detection: ENABLED
Status: SECURED
```

### Special Handling Procedures

#### Hazardous Materials Loading

**Pre-Loading Requirements**:
1. Hazmat-certified crew only
2. Review MSDS thoroughly
3. Verify containment integrity
4. Prepare spill kit
5. Notify all crew of hazmat operation
6. Restrict non-essential personnel

**Loading Procedure**:
1. Isolate hazmat bay section
2. Load hazmat cargo
3. Secure with redundant restraints
4. Install monitoring sensors
5. Verify ventilation operational
6. Seal containment zone
7. Post warning signs
8. Update hazmat log

```
CARGO > HAZMAT_LOAD [item_id]
WARNING: Hazardous material loading
Classification: Corrosive liquid, Class 8
Personnel protective equipment required: YES
Containment zone: Bay 3, Isolated section
Environmental monitoring: ACTIVE
Spill kit location: Bay 3, Station 2
Emergency procedure: HAZMAT-CORROSIVE-01
Confirm ready (YES/NO): YES
```

**Segregation Requirements**:
- Explosives: Isolated, temperature controlled
- Flammables: Away from ignition sources
- Oxidizers: Separated from fuels
- Corrosives: Separate containment
- Toxics: Sealed, monitored atmosphere
- Radioactives: Shielded, monitored

#### Cryogenic Cargo Loading

**Requirements**:
- Insulated cargo bay section
- Cryogenic-rated handling equipment
- Protective equipment for crew
- Continuous temperature monitoring
- Pressure relief systems verified

**Procedure**:
1. Pre-cool cargo bay section
2. Verify cryogenic container integrity
3. Monitor for leaks continuously
4. Load quickly to minimize heat transfer
5. Secure with thermally-rated restraints
6. Install multiple temperature sensors
7. Configure automatic alarms
8. Establish monitoring schedule

```
CARGO > CRYO_LOAD [item_id]
Container type: Liquid nitrogen (LN2)
Temperature: -196°C
Pressure: 1.2 bar
Hold time: 14 days
Target bay temp: -150°C
Current bay temp: -145°C
Bay pre-cool: COMPLETE
Load authorized: YES
```

#### Oversized Cargo Loading

**Definition**: Cargo exceeding standard bay dimensions
- Length > 20m
- Width > 10m
- Height > 8m

**Special Procedures**:
1. Calculate clearances precisely
2. Remove bay equipment if needed
3. Use external mounting points if necessary
4. Verify door clearance during loading
5. May require multiple crew members
6. May require external loading (EVA)
7. Verify doesn't obstruct critical systems

## In-Transit Cargo Management

### Monitoring Systems

#### Automated Monitoring
```
CARGO > MONITOR STATUS
Total cargo: 247 items
Secured items: 247
Shifted items: 0
Environmental: NOMINAL
- Temperature: 22°C
- Pressure: 1.01 bar
- Humidity: 45%
Hazmat status: NOMINAL
- No leaks detected
- All sensors operational
Special cargo:
- Cryo bay: -148°C (NORMAL)
- Secure vault: LOCKED
- Live cargo: Fed 2 hours ago
Last inspection: 4 hours ago
Next inspection: 4 hours
```

#### Sensor Types
- **Shift Detectors**: Detect cargo movement
- **Mass Sensors**: Monitor weight distribution
- **Temperature Probes**: Track thermal conditions
- **Gas Detectors**: Identify leaks or contamination
- **Radiation Monitors**: Track radioactive cargo
- **Video Surveillance**: Visual monitoring
- **Pressure Sensors**: Detect atmosphere changes

### Regular Inspections

#### Daily Inspection
- Visual walkthrough of all cargo bays
- Check securing points
- Verify environmental systems
- Review sensor data
- Check hazmat status
- Inspect special cargo
- Document findings

**Inspection Route**:
```
CARGO > INSPECTION START
Route loaded: Daily inspection route
Bays: 1, 2, 3, 4
Items to inspect: 247
Estimated time: 45 minutes
Begin inspection: YES

Bay 1: NORMAL
Bay 2: NORMAL
Bay 3 (Hazmat): NORMAL - All sensors green
Bay 4: WARNING - Item 127 shift detected
Investigating item 127...
```

#### Shift Response Procedure
When cargo shifts:

1. **Immediate Assessment**
   - Identify shifted item
   - Assess risk level
   - Check for damage
   - Verify adjacent cargo secure

2. **Re-securing**
   - Don safety equipment
   - Approach cautiously
   - Inspect securing points
   - Re-secure item
   - Add additional restraints if needed
   - Document incident

3. **Investigation**
   - Determine cause of shift
   - Check if others at risk
   - Correct deficiency
   - Update procedures if needed

### Environmental Control

#### Temperature Management

**Standard Cargo**:
- Range: 15-25°C
- Tolerance: ±5°C
- Alert if outside range

**Climate-Controlled Cargo**:
- Per manifest requirements
- Typical ranges:
  - Frozen: -20°C to -10°C
  - Refrigerated: 2°C to 8°C
  - Warm: 30°C to 40°C
  - Cryogenic: -196°C to -150°C

**Control Commands**:
```
CARGO > BAY_TEMP SET [bay] [temp]
CARGO > BAY_TEMP 2 SET 5
Target temperature: 5°C
Current temperature: 22°C
Cooling system: ACTIVATING
Estimated time to target: 2 hours
Monitor closely: YES
```

#### Atmosphere Control

**Standard Atmosphere**:
- 78% N₂, 21% O₂, 1% other
- Pressure: 1.0 bar
- Humidity: 30-60%

**Special Atmospheres**:
- **Inert (N₂)**: For reactive cargo
- **Low O₂**: For fire-sensitive cargo
- **Controlled humidity**: For moisture-sensitive cargo
- **Vacuum**: For space-exposed cargo

### Live Cargo Care

#### Requirements
- Daily feeding and watering
- Health monitoring
- Waste management
- Social needs (for intelligent species)
- Environmental enrichment
- Veterinary care available

#### Daily Care Log
```
CARGO > LIVE_CARGO STATUS
Cargo: 4 Terran cattle, 12 Centauri plants

Cattle status:
- Fed: 6 hours ago (scheduled)
- Water: Fresh, levels good
- Health: All animals normal
- Temperature: 20°C (optimal)
- Humidity: 55% (optimal)
- Waste management: Cleaned 8 hours ago
- Next care: 18 hours

Plant status:
- Watered: 3 hours ago
- Light cycle: Day (6 hours remaining)
- Growth: Normal
- Temperature: 24°C (optimal)
- Humidity: 70% (optimal)
- Next care: 21 hours
```

## Unloading Procedures

### Pre-Unloading Preparations

#### Checklist
- [ ] Verify destination/recipient
- [ ] Review customs requirements
- [ ] Prepare documentation
- [ ] Verify unloading equipment available
- [ ] Check weather/environmental conditions
- [ ] Notify crew of unloading schedule
- [ ] Clear deck space
- [ ] Stage cargo in unloading sequence

#### Unloading Sequence Planning
```
CARGO > UNLOAD_SEQUENCE PLAN
Destination: Alpha Centauri Station
Items to unload: 127 items
Remaining items: 120 items
Planning optimal sequence...

Sequence recommended:
1. Bay 4, Section A (20 items) - Door access
2. Bay 3, Section B (15 items) - Priority delivery
3. Bay 2, Section C (45 items) - Standard cargo
4. Bay 1, Section A (47 items) - Last in, first out

Estimated unload time: 6 hours
Crew required: 4
Equipment needed: 2 power loaders, 1 crane
Accept plan (Y/N): Y
```

### Unloading Process

#### 1. Cargo Preparation
- Release securing mechanisms
- Verify cargo intact
- Update cargo database
- Prepare paperwork
- Stage near bay doors

#### 2. Cargo Transfer
- Verify recipient present
- Inspect cargo together
- Photograph condition
- Have recipient sign receipt
- Transfer custody
- Update manifest

#### 3. Post-Unloading
- Inspect bay for damage
- Check for left-behind items
- Update weight distribution
- Clean bay if necessary
- Prepare for next cargo

### Documentation

#### Required Records
- **Unloading Log**: Date, time, items, recipient
- **Condition Report**: Any damage noted
- **Recipient Signature**: Proof of delivery
- **Photos**: Visual documentation
- **Updated Manifest**: Remaining cargo

## Emergency Procedures

### Cargo Fire

#### Immediate Actions
1. Activate fire suppression
2. Seal affected bay
3. Evacuate personnel
4. Alert all crew
5. Prepare to jettison if needed

```
CARGO > EMERGENCY FIRE [bay]
FIRE DETECTED - BAY 2
Activating suppression system...
Sealing bay doors...
Cutting atmosphere...
Evacuate bay immediately!
Fire team respond!
```

#### Follow-Up
- Assess damage
- Verify fire extinguished
- Inspect adjacent cargo
- Document incident
- Investigate cause

### Hazmat Leak

#### Immediate Actions
1. Activate containment protocols
2. Don protective equipment
3. Evacuate affected area
4. Activate ventilation
5. Deploy spill kit
6. Follow MSDS procedures

```
CARGO > EMERGENCY HAZMAT_LEAK [bay]
HAZMAT LEAK DETECTED - BAY 3
Material: Corrosive liquid (sulfuric acid)
Activating containment...
Sealing section...
Activating emergency ventilation...
Spill kit location: Bay 3, Station 2
MSDS: Display on all terminals
Alert: HAZMAT TEAM RESPOND
```

### Cargo Shift (Severe)

#### Immediate Actions
1. Reduce ship acceleration to minimum
2. Alert all crew
3. Assess situation visually
4. Determine risk to ship
5. Re-secure if safe
6. Jettison if necessary

```
CARGO > EMERGENCY SHIFT_SEVERE
SEVERE CARGO SHIFT DETECTED
Item: 145 (Heavy machinery - 50,000 kg)
Location: Bay 1, Section C
Center of gravity: CRITICAL SHIFT
Ship stability: COMPROMISED
Recommend: Reduce acceleration immediately
Alert captain: URGENT
```

### Cargo Jettison

#### When Required
- Fire cannot be controlled
- Hazmat leak threatens ship
- Cargo threatens ship stability
- Cargo threatens crew safety

#### Procedure
**Requires Captain's Authorization**

```
CARGO > EMERGENCY JETTISON [item_id]
WARNING: This will jettison cargo into space
Item: [description]
Mass: [mass]
Value: [value]
Reason: [emergency type]

Captain authorization required.
Enter authorization code: ********
Confirm jettison (YES/NO): YES

Opening exterior bay door...
Releasing restraints...
Cargo jettisoned.
Bay door closing...
Verify bay integrity...
Logging jettison event...
Notify insurance: REQUIRED
```

## Cargo Security

### Access Control
- Cargo bays require authorization
- Valuable cargo requires additional clearance
- All access logged
- Video surveillance active
- Motion detectors operational

### Theft Prevention
- Regular inventory checks
- Seal high-value items
- Restrict access
- Monitor for tampering
- Chain of custody documentation

### Contraband Scanning
- Scan all cargo during loading
- Random scans during transit
- Scan before unloading
- Report suspicious items to authorities

```
CARGO > SCAN_CONTRABAND [item_id]
Scanning item 127...
X-ray scan: Complete
Density analysis: Complete
Chemical sniffer: Complete
Radiation check: Complete
Neural net analysis: Complete
Contraband detected: NO
Item cleared.
```

## Required Certifications
- Cargo Handler (Level 2 minimum)
- Hazmat Handling (for hazmat cargo)
- Forklift/Power Loader operation
- Crane operation (for heavy cargo)
- First Aid/Emergency Response

## Related Documentation
- See: `cargo-management-overview.md` for system basics
- See: `cargo-hazmat-procedures.md` for detailed hazmat handling
- See: `emerg-011-cargo-hazmat-emergency.md` for hazmat emergencies
- See: `kb-045-cargo-shifted-during-transit.md` for troubleshooting

## Revision History
- v3.2 - Added live cargo care procedures
- v3.0 - Updated hazmat classifications
- v2.5 - Added anti-gravity restraint procedures
- v2.0 - Comprehensive rewrite for new cargo systems
