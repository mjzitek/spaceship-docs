# Model-3 Sublight Impeller System

**Document ID:** NAV-SUB-001
**Revision:** 3.4
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Purpose

This document describes the Model-3 Sublight Impeller system used for non-FTL propulsion in ORSM vessels. Sublight engines provide thrust for normal-space maneuvering, orbital operations, and sub-luminal transit.

## System Description

The Model-3 Sublight Impeller is a plasma-based propulsion system that generates thrust by accelerating ionized particles to extreme velocities and expelling them through vectored exhaust nozzles. The system provides efficient, controllable thrust for all standard flight operations.

### Operating Principle

1. **Plasma Generation**: Q-Core reactor power ionizes deuterium fuel
2. **Magnetic Acceleration**: Electromagnets accelerate plasma to 0.05c (5% light speed)
3. **Exhaust Vectoring**: Gimbaled nozzles direct thrust for precise maneuvering
4. **Reaction Mass**: Expelled plasma provides thrust via Newton's third law

### Key Components

- **Plasma Chamber**: Ionization chamber where fuel becomes plasma
- **Acceleration Coils**: 24 electromagnetic coils per engine
- **Thrust Nozzle**: Reinforced ceramic-alloy exhaust port with 360° vectoring
- **Fuel Injector Assembly**: Delivers deuterium fuel to plasma chamber
- **Cooling Manifold**: Liquid coolant system prevents thermal damage
- **Thrust Controller**: Computer-controlled throttle and vector management
- **Inertial Dampener Interface**: Protects crew from acceleration forces

## Engine Configurations

### Single-Engine (Light Craft)
- **Vessels**: Small scouts, personal shuttles, escape pods
- **Total Thrust**: 50-150 kN
- **Max Acceleration**: 0.5-1.5 G
- **Fuel Consumption**: 0.8 kg/hour at full thrust

### Dual-Engine (Standard Configuration)
- **Vessels**: Transports, freighters, medium patrol craft
- **Total Thrust**: 300-800 kN
- **Max Acceleration**: 2-4 G
- **Fuel Consumption**: 3.2 kg/hour at full thrust

### Quad-Engine (Heavy/Military)
- **Vessels**: Large freighters, military cruisers, industrial ships
- **Total Thrust**: 1,500-3,000 kN
- **Max Acceleration**: 5-8 G
- **Fuel Consumption**: 12 kg/hour at full thrust

### Maneuvering Thrusters

All vessels equipped with 12-24 small thrusters for fine control:
- **Thrust per Thruster**: 5-20 kN
- **Purpose**: Docking, attitude adjustment, low-speed maneuvering
- **Fuel Type**: Compressed nitrogen (separate from main engine fuel)

## Operating Modes

### Standby
- Engines warm, ready for immediate activation
- Plasma chamber at 200°C (maintenance temperature)
- Power consumption: 1 MW per engine
- Startup time from standby: 5 seconds

### Standard Thrust (40-70%)
- Normal flight operations
- Plasma chamber temperature: 600-900°C
- Fuel efficiency: Optimal
- Typical use: Orbital transfers, routine transit

### Maximum Thrust (70-100%)
- Emergency acceleration
- Plasma chamber temperature: 1,000-1,400°C
- Fuel efficiency: Reduced (30% less efficient than standard)
- Typical use: Combat maneuvers, emergency evasion
- **Maximum Duration**: 30 minutes continuous before cooldown required

### Emergency Overburn (100-120%)
- Critical situations only
- Plasma chamber temperature: 1,500-1,800°C
- Fuel efficiency: Very poor (50% less efficient)
- **WARNING**: Risk of engine damage
- **Maximum Duration**: 5 minutes
- Requires immediate cooldown and inspection afterward

## Normal Operating Parameters

| Parameter | Standby | Standard | Maximum | Overburn | Critical |
|-----------|---------|----------|---------|----------|----------|
| Plasma Chamber Temp | 200°C | 600-900°C | 1,000-1,400°C | 1,500-1,800°C | >1,900°C |
| Acceleration Coil Current | 10 A | 80-120 A | 150-180 A | 190-220 A | >230 A |
| Exhaust Velocity | 0 | 0.03c | 0.05c | 0.06c | N/A |
| Fuel Pressure | 50 PSI | 120-150 PSI | 180-200 PSI | 220-250 PSI | >270 PSI |
| Coolant Flow Rate | 5 L/min | 25-40 L/min | 60-80 L/min | 100 L/min | Insufficient |
| Thrust Output | 0% | 40-70% | 70-100% | 100-120% | N/A |

## Safety Systems

### Automatic Safeguards

- **Thermal Limiter**: Reduces thrust if plasma chamber exceeds 1,800°C
- **Fuel Flow Governor**: Prevents over-fueling that could cause explosion
- **Acceleration Limiter**: Restricts acceleration to safe crew tolerance (override available)
- **Coolant Loss Detector**: Emergency shutdown if coolant pressure drops critically
- **Nozzle Integrity Monitor**: Shuts down engine if exhaust nozzle damaged

### Manual Controls

- Emergency engine shutdown (all engines, instant cut-off)
- Manual thrust override (bypass computer control)
- Individual engine disable (for multi-engine configurations)
- Inertial dampener adjustment (crew comfort vs performance)

## Fuel System

### Primary Fuel: Deuterium

- **Form**: Liquid deuterium (heavy hydrogen isotope)
- **Storage**: Cryogenic tanks at -250°C
- **Typical Capacity**: 500-5,000 kg depending on vessel size
- **Refueling**: Available at most stations and ports

### Maneuvering Thruster Fuel: Compressed Nitrogen

- **Form**: Pressurized nitrogen gas
- **Storage**: High-pressure tanks at 3,000 PSI
- **Typical Capacity**: 50-200 kg
- **Refueling**: Standard atmospheric gas, easily obtained

### Fuel Consumption Rates

**Main Engines (per engine at standard thrust):**
- Single-engine configuration: 0.8 kg/hour
- Dual-engine configuration: 1.6 kg/hour per engine
- Quad-engine configuration: 3.0 kg/hour per engine

**Maneuvering Thrusters:**
- Approximately 0.1 kg/hour per thruster when active

### Range Calculations

Maximum flight time = (Fuel capacity) / (Consumption rate × Number of engines)

**Example**: Dual-engine freighter
- Fuel capacity: 2,000 kg
- Consumption: 1.6 kg/hour per engine at standard thrust
- Flight time: 2,000 / (1.6 × 2) = 625 hours (~26 days)

**Note**: Range depends on acceleration, ship mass, and thrust level. Above calculation assumes continuous standard thrust operation.

## Acceleration and Performance

### Calculating Acceleration

Acceleration (G) = (Total Thrust) / (Ship Mass × 9.81 m/s²)

**Example**: 5,000-ton freighter with dual-engine configuration (800 kN total)
- Thrust: 800,000 N
- Mass: 5,000,000 kg
- Acceleration: 800,000 / (5,000,000 × 9.81) = 0.016 G

### Inertial Dampeners

Inertial dampeners reduce felt acceleration:
- Standard dampening: 80% reduction (4 G feels like 0.8 G)
- High dampening: 95% reduction (4 G feels like 0.2 G, but uses more power)
- Combat mode: 50% reduction (allows higher performance)
- Dampeners require 5-15 MW power depending on acceleration

**WARNING**: Inertial dampener failure during high-G maneuvers can cause serious crew injury.

## Pre-Flight Checklist

Before activating sublight engines:

- [ ] Deuterium fuel tanks at least 20% full
- [ ] Coolant system operational and filled
- [ ] Exhaust path clear of obstacles (for docked vessels)
- [ ] Inertial dampeners online
- [ ] Engine diagnostics passed (run pre-flight test sequence)
- [ ] Thrust vectoring test completed (nozzles move freely)
- [ ] Q-Core reactor producing adequate power
- [ ] Crew and cargo secured for acceleration

## Startup Procedure (from Cold)

**Duration**: Approximately 3-5 minutes

1. **Enable Engine Power**
   - Activate engine control panel
   - Verify power feed from Q-Core reactor
   - Check all status indicators

2. **Initialize Coolant System**
   - Start coolant pumps
   - Verify coolant flow to all engines
   - Confirm coolant temperature below 60°C

3. **Warm Plasma Chambers**
   - Activate chamber pre-heaters
   - Ramp chamber temperature to 200°C
   - Wait for thermal stabilization (2-3 minutes)

4. **Energize Acceleration Coils**
   - Bring coils online sequentially
   - Verify magnetic field generation
   - Check coil current: Should reach 10 A (standby level)

5. **Pressurize Fuel System**
   - Open deuterium tank valves
   - Prime fuel injectors
   - Verify fuel pressure at 50 PSI (standby level)

6. **Run Diagnostic Test**
   - Execute engine self-test sequence
   - Verify all systems show green
   - Test thrust vectoring (nozzles should move through full range)

7. **Engage Standby Mode**
   - Engines now ready for thrust commands
   - Can go from standby to full thrust in 5 seconds

## Normal Operation

### Thrust Control

**Throttle Input**: 0-100% thrust via control interface
- Helm console for piloted craft
- Autopilot for automated navigation
- Manual override controls on engine compartment panel

**Thrust Response Time**:
- 0 to 50% thrust: 2 seconds
- 50% to 100% thrust: 3 seconds
- 100% to 0% thrust: 1 second (emergency cut-off)

### Vector Control

Thrust vectoring allows directional control:
- Nozzles gimbal up to ±20° from centerline
- Response time: 1 second for full deflection
- Provides pitch, yaw, and roll control
- Computer-controlled for stability

**For multi-engine configurations**: Differential thrust used in combination with vectoring for enhanced maneuverability.

### Maneuvering Thrusters

Fine control for docking and attitude adjustment:
- Controlled independently from main engines
- Can operate while main engines active or inactive
- Provide 6-axis control (translation and rotation)
- Typical use: Station approach, debris avoidance, orientation adjustment

## Shutdown Procedure

**Standard Shutdown (planned):**

1. Reduce thrust to zero
2. Allow plasma chamber to cool to 400°C (5 minutes)
3. Depressurize fuel system
4. De-energize acceleration coils
5. Maintain coolant circulation for 10 minutes
6. Shut down coolant pumps
7. Switch engine power off

**Emergency Shutdown:**

1. Press emergency cut-off button
2. Fuel injection stops immediately
3. Thrust ceases within 1 second
4. Coolant continues circulating (prevent thermal damage)
5. Requires inspection before restart

## Integration with Ship Systems

Sublight engines interface with:

- **Q-Core Reactor**: Power source for plasma generation and magnetic acceleration
- **Navigation Computer**: Provides thrust commands based on flight plan
- **Inertial Dampeners**: Compensate for acceleration forces
- **FTL Drive**: Engines must be idle during FTL transit
- **Fuel Management System**: Monitors deuterium consumption and reserves
- **Attitude Control**: Coordinates with maneuvering thrusters
- **Collision Avoidance**: Provides automatic evasive thrust

## Maintenance Requirements

**See NAV-SUB-002 for complete maintenance procedures.**

**Critical Intervals:**
- Daily: Visual inspection, parameter logging
- Weekly: Coolant check, nozzle inspection
- Monthly: Acceleration coil calibration, fuel injector cleaning
- Quarterly: Plasma chamber inspection, thrust vectoring system service
- Annually: Complete engine overhaul, component replacement

## Common Issues

### Engine Won't Start
- Insufficient power from Q-Core
- Coolant system not operational
- Fuel pressure low or zero
- Acceleration coil failure

### Reduced Thrust
- Clogged fuel injectors
- Degraded acceleration coils
- Partially blocked exhaust nozzle
- Fuel contamination

### Overheating
- Coolant leak or pump failure
- Excessive thrust duration at maximum/overburn
- Blocked cooling manifold
- Plasma chamber damage

### Vibration or Noise
- Misaligned thrust nozzle
- Damaged acceleration coil
- Loose mounting bolts
- Fuel flow irregularity

**See NAV-SUB-003 for detailed troubleshooting procedures.**

## Warning Signs

Immediately investigate if:

- Plasma chamber temperature exceeds 1,600°C
- Unusual vibrations or grinding sounds
- Visible exhaust discoloration (should be blue-white, not yellow/orange)
- Thrust output significantly lower than throttle setting
- Coolant pressure dropping
- Error codes E-NAV-100 through E-NAV-199 (sublight propulsion errors)

## Performance Optimization

### Fuel Efficiency Tips

- Operate at 50-60% thrust when possible (optimal efficiency range)
- Use maneuvering thrusters for small adjustments (more efficient than main engines)
- Plan acceleration/deceleration to minimize fuel use
- Avoid repeated maximum thrust cycles

### Maximum Performance

For situations requiring best acceleration:
- Disable non-essential systems to maximize power to engines
- Set inertial dampeners to combat mode (50% reduction)
- Use emergency overburn only when absolutely necessary
- Monitor engine temperature carefully

## Related Documents

- NAV-SUB-002: Sublight Engine Maintenance Guide
- NAV-SUB-003: Sublight Engine Troubleshooting
- NAV-FTL-001: FTL Drive System Overview
- FUEL-001: Fuel Management and Safety
- ERR-NAV-100: Sublight Propulsion Error Codes

---

**EFFICIENCY NOTE**: Proper engine maintenance can improve fuel efficiency by 15-20%. Keep acceleration coils calibrated and fuel injectors clean for optimal performance.
