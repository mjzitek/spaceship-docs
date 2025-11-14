# Sensor Systems Overview

**System:** Integrated Sensor Suite (ISS)
**Manufacturer:** Outer Rim Starship Manufacturing (ORSM)
**Variants:** Basic, Standard, Enhanced, Scientific
**Document Version:** 2.8
**Last Updated:** 2847.09.14

## Purpose

Ship sensor systems provide situational awareness of the vessel's surroundings and internal status. Sensors detect other ships, obstacles, hazards, and monitor ship health. Critical for safe navigation, collision avoidance, threat detection, and system monitoring.

## Sensor Categories

### 1. External Sensors (Detect External Environment)

**Purpose:** Detect objects, hazards, and conditions outside the ship

**Types:**
- Proximity sensors (collision avoidance, docking)
- Long-range sensors (detect ships/objects at distance)
- Navigational sensors (position, velocity, attitude)
- Threat sensors (weapons fire, hostile targeting)
- Scientific sensors (stellar phenomena, resource detection)

### 2. Internal Sensors (Monitor Ship Systems)

**Purpose:** Monitor ship health, system status, crew safety

**Types:**
- Hull integrity sensors (stress, breach detection)
- System monitoring (temperature, pressure, power, flow)
- Atmospheric sensors (O₂, CO₂, toxins, temperature)
- Radiation sensors (reactor monitoring, space hazards)
- Security sensors (intrusion, access, surveillance)

### 3. Communications/Electronic Sensors

**Purpose:** Detect and analyze electromagnetic signals

**Types:**
- Communications receivers (intercept signals, detect traffic)
- Radar/LIDAR (active sensing, uses emitted signals)
- Passive EM detection (detect emissions from other ships)
- Electronic warfare (jamming detection, countermeasures)

---

## External Sensor Systems

### Proximity Sensors (Collision Avoidance)

**Function:** Detect nearby objects to prevent collisions

**Technologies:**

**RADAR (Radio Detection and Ranging):**
- **Range:** 0.1 - 50 km (depending on target size)
- **Accuracy:** ±50 meters
- **Update Rate:** 1-5 Hz
- **Advantages:** Works through dust, debris fields; reliable
- **Disadvantages:** Lower resolution than LIDAR; can be jammed
- **Part #:** SENS-PROX-RAD

**LIDAR (Light Detection and Ranging):**
- **Range:** 0.01 - 20 km
- **Accuracy:** ±1 meter (very precise)
- **Update Rate:** 10-50 Hz
- **Advantages:** High precision; excellent for docking
- **Disadvantages:** Blocked by particulates (dust, fog); shorter range
- **Part #:** SENS-PROX-LID

**Gravitic Sensors** (military/high-end only):
- **Range:** 0.1 - 5 km
- **Accuracy:** ±10 meters
- **Update Rate:** 1 Hz
- **Advantages:** Cannot be jammed; detects mass directly; works through obstacles
- **Disadvantages:** Very expensive (10x cost of RADAR); short range; high power consumption
- **Part #:** SENS-PROX-GRAV (restricted sale)

**Typical Configuration:**
- **Small vessel (scout):** 6 sensors (fore, aft, port, starboard, dorsal, ventral)
- **Medium vessel (freighter):** 12 sensors (redundant coverage, better resolution)
- **Large vessel (station ship):** 24+ sensors (complete sphere coverage, high redundancy)

**Coverage Pattern:**
- Sensors overlap (redundancy)
- If one sensor fails, others compensate
- Blind spots minimized by strategic placement

**See:** KB-067 (Proximity Sensors Malfunction) for troubleshooting

---

### Long-Range Sensors

**Function:** Detect objects at distances beyond proximity sensor range

**Technologies:**

**Optical Telescopes:**
- **Range:** 1,000 km - several AU (depends on target brightness)
- **Accuracy:** Arc-seconds (angular), distance varies
- **Advantages:** Passive (doesn't emit, cannot be detected); high resolution for visible objects
- **Disadvantages:** Requires line-of-sight; target must emit or reflect light
- **Part #:** SENS-OPT-TELE-200MM (200mm aperture)

**Infrared (Thermal) Sensors:**
- **Range:** 100 - 100,000 km (depends on target heat signature)
- **Accuracy:** ±1,000 km at max range
- **Advantages:** Detects heat (ship engines, reactors always emit heat); passive
- **Disadvantages:** Less effective in hot environments (near stars)
- **Part #:** SENS-IR-ARRAY

**Subspace Sensors:**
- **Range:** 1 - 5 light-years
- **Accuracy:** ±0.1 LY
- **Advantages:** Detects subspace distortions (FTL drives, quantum events); very long range
- **Disadvantages:** Cannot pinpoint small objects; detects only FTL-capable ships or major gravitational sources
- **Part #:** SENS-SUB-A (basic), SENS-SUB-ARRAY-E (enhanced)

**Gravitic Sensors (long-range):**
- **Range:** 10,000 - 1,000,000 km
- **Accuracy:** ±10,000 km
- **Advantages:** Detects mass (planets, large ships, asteroids); passive; works through obstacles
- **Disadvantages:** Expensive; cannot detect small objects (<1000 tons)
- **Part #:** SENS-GRAV-LR (restricted)

**Typical Configuration:**
- **Basic:** Optical telescope, infrared array
- **Standard:** Optical, infrared, subspace sensor (basic)
- **Enhanced:** Multiple optical arrays, high-res infrared, enhanced subspace, gravitic sensors

**Use Cases:**
- **Navigation:** Identify destination star system from long range
- **Threat Detection:** Detect approaching ships (intent unknown)
- **Scientific:** Study stellar phenomena, planets, anomalies
- **Resource:** Detect asteroid composition (for mining)

---

### Navigational Sensors

**Function:** Determine ship's position, velocity, attitude in space

**Technologies:**

**Inertial Measurement Unit (IMU):**
- **Function:** Measures acceleration and rotation (dead reckoning)
- **Accuracy:** ±0.1 m/s² (acceleration), ±0.01°/s (rotation)
- **Advantages:** Internal (no external reference needed); high update rate (100 Hz)
- **Disadvantages:** Drift over time (errors accumulate); must periodically recalibrate
- **Part #:** NAV-IMU-A

**Star Tracker:**
- **Function:** Identifies stars, calculates position from star patterns
- **Accuracy:** ±1 arc-second (very precise attitude)
- **Advantages:** Absolute position reference (no drift); passive
- **Disadvantages:** Requires clear view of stars; slower update rate (1 Hz)
- **Part #:** NAV-STAR-TRACK

**Quantum Positioning System (QPS):**
- **Function:** Uses quantum-entangled beacons for position triangulation
- **Accuracy:** ±10 meters anywhere in settled space
- **Range:** Up to 100 LY from beacon network
- **Advantages:** Very accurate; real-time
- **Disadvantages:** Only works within beacon network coverage (core/mid-rim systems); expensive subscription
- **Part #:** NAV-QPS-RX (receiver)

**Doppler Velocity Sensor:**
- **Function:** Measures velocity relative to nearby objects or stars
- **Accuracy:** ±0.01 m/s
- **Advantages:** Direct velocity measurement (no calculation from position)
- **Disadvantages:** Requires reference object
- **Part #:** SENS-DOPPLER-A

**Typical Navigation Approach:**
- **Primary:** Star tracker + IMU (complementary: star tracker corrects IMU drift, IMU provides high rate between star tracker updates)
- **Secondary:** QPS (if in network coverage)
- **Tertiary:** Manual celestial navigation (backup if all sensors fail)

**Accuracy:**
- **Position:** ±100 km (in settled space with QPS)
- **Position:** ±10,000 km (deep space, star tracker only)
- **Velocity:** ±0.1 m/s
- **Attitude:** ±0.01° (critical for FTL jump alignment)

---

### Threat Detection Sensors (Military/Security)

**Function:** Detect hostile actions (weapons fire, targeting, jamming)

**Note:** These sensors typically found only on military vessels or high-security civilian ships with special permits

**Technologies:**

**Missile Approach Warning System (MAWS):**
- **Function:** Detects approaching missiles via IR signature or active radar
- **Range:** 10 - 500 km (depends on missile type)
- **Warning Time:** 5-60 seconds (depends on missile speed)
- **Part #:** SENS-MAWS (restricted)

**Laser Warning Receiver:**
- **Function:** Detects if ship is being targeted by laser (rangefinding or weapon)
- **Accuracy:** Direction to laser source ±1°
- **Warning:** Instant (speed of light)
- **Part #:** SENS-LWR (restricted)

**Radar Warning Receiver (RWR):**
- **Function:** Detects if ship is being scanned by radar (targeting or tracking)
- **Range:** Can detect radar from 2x the radar's detection range
- **Provides:** Direction, frequency, type of radar (search vs. tracking vs. fire control)
- **Part #:** SENS-RWR (restricted)

**Electronic Support Measures (ESM):**
- **Function:** Intercepts and analyzes enemy communications and sensor emissions
- **Capabilities:** Signal intelligence, communication intercept, threat identification
- **Part #:** SENS-ESM-SUITE (restricted, military only)

**Not available for civilian vessels without special permit** (military, law enforcement, licensed security contractors)

---

### Scientific Sensors (Research/Exploration Vessels)

**Function:** Detailed analysis of stellar phenomena, planets, anomalies

**Specialized sensors for science vessels:**

**Spectrometer:**
- **Function:** Analyzes light spectrum (determines composition of stars, planets, atmospheres)
- **Range:** Any visible or IR source
- **Accuracy:** Identifies elements/compounds with 99% accuracy
- **Part #:** SENS-SPEC-UV-IR

**Magnetometer:**
- **Function:** Measures magnetic fields (planetary, stellar, ship's)
- **Range:** 0 - 1 AU
- **Sensitivity:** 0.1 nanoTesla
- **Part #:** SENS-MAG-ARRAY

**Particle Detector:**
- **Function:** Detects and identifies particles (cosmic rays, solar wind, exotic particles)
- **Sensitivity:** Individual particle detection
- **Part #:** SENS-PART-ARRAY

**Gravitational Wave Detector:**
- **Function:** Detects ripples in spacetime (black hole mergers, neutron star collisions, quantum events)
- **Range:** Galactic (detects major events across galaxy)
- **Sensitivity:** 10⁻²¹ strain (incredibly sensitive)
- **Part #:** SENS-GRAV-WAVE (very expensive, few ships have this)

**Subspace Anomaly Detector:**
- **Function:** Detects unusual quantum field phenomena (wormholes, subspace rifts, exotic physics)
- **Range:** 0.1 - 1 LY
- **Part #:** SENS-SUB-ANOM

**Typical Science Vessel Configuration:**
- All basic sensors (proximity, long-range, nav)
- Plus: Spectrometer, magnetometer, particle detector, subspace anomaly detector
- Optional: Gravitational wave detector (if budget allows)

---

## Internal Sensor Systems

### Hull Integrity Sensors

**Function:** Monitor structural health, detect damage or stress

**Technologies:**

**Stress Sensors (Strain Gauges):**
- **Quantity:** 200 - 2,000 sensors (depends on ship size)
- **Location:** Critical stress points (hull joints, load-bearing structures)
- **Measurement:** Strain (deformation under load)
- **Alerts:** Yellow warning >80% design limit, red warning >95%
- **Part #:** SENS-STRESS-A

**Breach Detection Sensors:**
- **Function:** Detect hull punctures (pressure loss, acoustic signature of breach)
- **Types:**
  - Pressure sensors (detect local pressure drop)
  - Acoustic sensors (hear "hiss" of escaping air)
  - Thermal sensors (detect temperature change from exposure to space)
- **Response Time:** <1 second
- **Part #:** SENS-BREACH-A

**Accelerometers:**
- **Function:** Detect impacts, collisions, explosions
- **Sensitivity:** 0.01 g
- **Location:** Distributed throughout hull
- **Part #:** SENS-ACCEL-A

**Integration:**
- Sensors feed Hull Integrity Panel on bridge
- Display: 3D ship model color-coded (green=normal, yellow=stress, red=critical/breach)
- Automatic response: Seal bulkheads near breach, alert crew

**See:** Hull Integrity Manual, ERR-HULL error codes

---

### System Monitoring Sensors

**Function:** Monitor critical ship systems (reactor, engines, life support)

**Types:**

**Temperature Sensors:**
- **Locations:** Reactor plasma chamber, engine nozzles, coolant loops, crew compartments, electronics bays
- **Quantity:** 50-500 sensors (depending on ship size)
- **Types:**
  - Thermocouples (high temperature, 0-2000°C)
  - RTDs (medium temperature, -50 to 400°C)
  - Thermistors (low temperature, -20 to 150°C)
- **Part #:** SENS-TEMP-TC, SENS-TEMP-RTD, SENS-TEMP-THERM

**Pressure Sensors:**
- **Locations:** Reactor coolant, fuel lines, hydraulics, cabin pressure, water systems
- **Quantity:** 30-200 sensors
- **Range:** Vacuum to 50 MPa (varies by application)
- **Part #:** SENS-PRES-0-50MPA (specify range)

**Flow Sensors:**
- **Locations:** Coolant loops, fuel lines, water recycling
- **Measurement:** Liters/minute or kg/second
- **Technology:** Turbine, magnetic, ultrasonic (depends on fluid)
- **Part #:** SENS-FLOW-MAG (magnetic)

**Level Sensors:**
- **Locations:** Fuel tanks, water tanks, coolant reservoirs
- **Technology:** Float, capacitive, ultrasonic
- **Accuracy:** ±2%
- **Part #:** SENS-LEVEL-ULTRA (ultrasonic)

**Vibration Sensors:**
- **Locations:** Rotating machinery (pumps, turbines, fans, engines)
- **Purpose:** Detect bearing wear, imbalance, mechanical issues
- **Alert:** Excessive vibration indicates impending failure
- **Part #:** SENS-VIB-A

**Current/Voltage Sensors:**
- **Locations:** Electrical distribution (monitors power consumption, detects shorts)
- **Measurement:** 0-1000 A, 0-10,000 VDC typical
- **Part #:** SENS-CURR-1000A, SENS-VOLT-10KV

**Integration:**
- Sensors feed system-specific panels (reactor panel, engine panel, life support panel)
- Alerts when readings outside normal range
- Data logged for trend analysis (predict failures before they occur)

---

### Atmospheric Sensors

**Function:** Monitor air quality in crew compartments

**Types:**

**Oxygen (O₂) Sensor:**
- **Range:** 0-100%
- **Normal:** 20-21%
- **Alerts:** <18% (hypoxia warning), >23% (fire hazard)
- **Technology:** Electrochemical or paramagnetic
- **Lifespan:** 18-24 months
- **Part #:** SENS-O2-A

**Carbon Dioxide (CO₂) Sensor:**
- **Range:** 0-10%
- **Normal:** <0.5%
- **Alerts:** >1% (discomfort), >5% (dangerous)
- **Technology:** Infrared (NDIR)
- **Lifespan:** 5-10 years
- **Part #:** SENS-CO2-A

**Carbon Monoxide (CO) Sensor:**
- **Range:** 0-1000 ppm
- **Normal:** 0 ppm
- **Alerts:** >50 ppm (warning), >200 ppm (danger)
- **Technology:** Electrochemical
- **Lifespan:** 24-36 months
- **Part #:** SENS-CO-A

**Volatile Organic Compounds (VOC) Sensor:**
- **Function:** Detects chemical vapors (fuel leaks, solvent spills, fire smoke)
- **Range:** 0-10,000 ppm equivalent
- **Normal:** <500 ppm
- **Technology:** Metal oxide or photoionization detector (PID)
- **Part #:** SENS-VOC-A

**Particulate Sensor:**
- **Function:** Measures dust, smoke, particles in air
- **Range:** 0-1000 µg/m³
- **Normal:** <50 µg/m³
- **Alerts:** >100 µg/m³ (check filters), >500 µg/m³ (fire/contamination)
- **Part #:** SENS-PART-AIR

**Temperature/Humidity Sensor:**
- **Range:** -20 to +60°C, 0-100% RH
- **Normal:** 18-24°C, 30-60% RH
- **Technology:** Capacitive humidity, RTD temperature
- **Part #:** SENS-TEMP-HUM

**Typical Configuration:**
- 1 sensor set per compartment (bridge, engineering, quarters, cargo bays)
- Critical areas (bridge, engineering): Redundant sensors
- Feeds Life Support panel and general alarm system

**See:** KB-027 (Low Oxygen), KB-018 (Temperature Control)

---

### Radiation Sensors

**Function:** Detect ionizing radiation (from reactor, space environment, nuclear hazards)

**Types:**

**Gamma Radiation Detector:**
- **Sensitivity:** 0.01 - 10,000 mSv/hr
- **Technology:** Geiger-Müller tube or scintillation detector
- **Locations:** Reactor compartment, exterior hull (space radiation), cargo bay (if carrying radioactive material)
- **Part #:** SENS-RAD-GM

**Neutron Detector:**
- **Function:** Detects neutron radiation (reactor leaks, nuclear weapons)
- **Sensitivity:** 0-100,000 neutrons/cm²/s
- **Location:** Reactor compartment (leak detection)
- **Part #:** SENS-RAD-NEUT

**Dosimeter Badges** (personal):
- **Function:** Crew wears badges to measure cumulative radiation exposure
- **Type:** Thermoluminescent dosimeter (TLD) or film badge
- **Checked:** Monthly (or after radiation incident)
- **Part #:** RAD-BADGE (see Parts Catalog)

**Integration:**
- Feeds reactor panel and safety alarm system
- Automatic alerts:
  - >2 mSv/hr: Caution (limit exposure time)
  - >10 mSv/hr: Warning (evacuate non-essential personnel)
  - >100 mSv/hr: Danger (evacuate immediately, potential reactor failure)
- Logs exposure for crew health records

**See:** Q-Core Reactor Manual (Radiation Safety), EMERG-005 (Reactor Critical Failures)

---

### Security Sensors

**Function:** Detect intrusion, monitor access, surveillance

**See:** Security Systems Overview Manual for complete details

**Types (brief summary):**
- Motion sensors (PIR): Detect movement in secured areas
- Door/hatch sensors: Detect opening without authorization
- Pressure pads: Detect footsteps in restricted zones
- Cameras: Visual surveillance (interior and exterior)
- Glass break sensors: Detect window/viewport breakage
- Tamper sensors: Detect unauthorized access to critical equipment

**Integration:**
- Feeds security panel
- Can trigger lockdown, alarms, recording
- Access logs for investigation

---

## Sensor Integration and Display

### Sensor Fusion

**Concept:** Combining data from multiple sensors for better situational awareness

**Example:**
- RADAR detects object at 20 km, bearing 045°
- Optical telescope confirms visual contact, identifies as ship
- Infrared sensor measures heat signature (ship's engines running hot)
- Subspace sensor detects FTL drive signature (ship has FTL capability)
- **Result:** Computer integrates data → Display shows "Ship, 20 km, bearing 045°, FTL-capable, engines active"

**Benefits:**
- More complete picture than any single sensor
- Cross-verification (if sensors disagree, investigate why)
- Redundancy (if one sensor fails, others compensate)

### Display Systems

**Bridge Sensor Display:**
- **Main Screen:** Tactical overview (3D space around ship, all detected objects)
- **Color Coding:**
  - Green: Friendly or identified non-threat
  - Yellow: Unknown or caution
  - Red: Hostile or threat
  - Blue: Waypoint, destination, or neutral
- **Zoom:** Can zoom from close proximity (10 km) to long range (1000 km+)
- **Filters:** Can show/hide object types (ships, stations, planets, asteroids, debris)

**System Status Panels:**
- Each major system (reactor, engines, life support) has dedicated panel
- Shows readings from all sensors monitoring that system
- Color-coded: Green (normal), yellow (caution), red (critical)
- Trend graphs (temperature over time, etc.)

**Alarm Integration:**
- Sensor readings outside normal range trigger alarms
- Audio alarm + visual indicator (flashing light on bridge)
- Alarm panel shows which sensor(s) triggered, current reading, threshold

---

## Sensor Maintenance

### Routine Maintenance (Preventive)

**Daily (if crew aboard):**
- Visual check of displays (all sensor readings normal?)
- Test alarms (press test button, verify audio/visual)

**Weekly:**
- Clean optical sensors (lenses on telescopes, cameras, LIDAR)
- Verify proximity sensors detecting test object at known range
- Check sensor power consumption (high current may indicate failing sensor)

**Monthly:**
- Calibrate critical sensors (O₂, CO₂, radiation)
- Inspect sensor wiring and connectors (corrosion, damage)
- Test backup sensors (redundant sensors should match primary)
- Review sensor logs (unusual readings?)

**Quarterly:**
- Full sensor diagnostic (automated test of all sensors)
- Replace sensors near end of lifespan (O₂ sensors, dosimeter badges)
- Update sensor firmware (if updates available)

**Annually:**
- Professional inspection of critical sensors (hull integrity, radiation)
- Recalibrate all sensors with precision references
- Replace aging sensors per manufacturer recommendations

### Troubleshooting

**Common Issues:**

**Sensor Reading Erratic:**
- Check wiring (loose connector, damaged wire)
- Check power supply (voltage stable?)
- Check for interference (nearby equipment causing noise)
- Replace sensor if faulty

**Sensor Reading Stuck (Not Changing):**
- Sensor failed or disconnected
- Check connector firmly seated
- Verify sensor has power
- Replace sensor

**False Alarms:**
- Sensor too sensitive (adjust sensitivity setting)
- Sensor contaminated (clean sensor)
- Sensor miscalibrated (recalibrate)
- Environmental (rapid temperature change, vibration can trigger sensors)

**See:** KB-067 (Proximity Sensors), KB-056 (Sensor-related issues), system-specific troubleshooting manuals

---

## Sensor Specifications by Ship Class

### Scout / Small Personal Vessel

**External:**
- Proximity: 6 sensors (RADAR or LIDAR)
- Long-range: Optical telescope, basic IR
- Navigation: IMU + star tracker

**Internal:**
- Hull: 50 stress sensors, 20 breach sensors
- System: 30 temperature, 20 pressure
- Atmospheric: 1 set per compartment (2-3 compartments)

### Freighter / Medium Vessel

**External:**
- Proximity: 12 sensors (mix RADAR/LIDAR)
- Long-range: Optical telescope, IR array, basic subspace sensor
- Navigation: IMU + star tracker + QPS receiver

**Internal:**
- Hull: 200 stress sensors, 50 breach sensors
- System: 100 temperature, 60 pressure, 30 flow
- Atmospheric: 1 set per compartment (5-8 compartments)
- Security: Basic security sensors (motion, door sensors)

### Large Vessel / Industrial / Passenger

**External:**
- Proximity: 24+ sensors (RADAR + LIDAR redundant)
- Long-range: Multiple optical arrays, high-res IR, enhanced subspace, gravitic (optional)
- Navigation: Dual IMU + dual star tracker + QPS

**Internal:**
- Hull: 500-2000 stress sensors, 100+ breach sensors
- System: 300+ temperature, 150+ pressure, 80+ flow, 50+ vibration
- Atmospheric: 2 sets per compartment (10-20 compartments), redundant
- Security: Comprehensive security sensor suite
- Radiation: Multiple detectors in reactor area and crew spaces

### Scientific / Exploration Vessel

**All standard sensors plus:**
- Spectrometer (UV/IR/visible)
- Magnetometer array
- Particle detector
- Subspace anomaly detector
- Gravitational wave detector (if funded)

---

## Sensor Power Requirements

**By Type:**
- Proximity sensors: 5-20 W each
- Long-range optical: 10-50 W
- IR sensors: 15-30 W
- Subspace sensors: 50-200 W
- Internal sensors (each): 0.1-5 W

**Total Power:**
- Scout: 500-1,000 W
- Freighter: 1,500-3,000 W
- Large vessel: 5,000-10,000 W

**Battery Backup:**
- Critical sensors (proximity, hull breach, atmospheric, radiation) have 4-12 hour battery backup
- If main power fails, these sensors remain functional

---

## Related Documentation

- KB-067: Proximity Sensors Malfunction
- Hull Integrity Manual: Stress and Breach Sensors
- Security Systems Manual: Security Sensor Details
- Life Support Manual: Atmospheric Sensor Integration
- Navigation Manual: Navigational Sensor Usage

---

**Sensor Philosophy:** More sensors provide better awareness and safety. Redundancy prevents single-point-of-failure. However, more sensors mean more complexity, more maintenance, and higher cost. Choose sensor suite appropriate to ship's mission: basic for routine cargo, comprehensive for exploration or passenger service.

**Support Note:** Most sensor issues are connectivity (loose wire, corroded connector) or calibration. Very few sensors fail completely. When troubleshooting, always check power and wiring before assuming sensor failed and replacing.
