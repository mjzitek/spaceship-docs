# Sensor Calibration Procedures

## Overview
Proper sensor calibration is critical for accurate detection, navigation, and threat assessment. This manual covers calibration procedures for all sensor types on board.

## Calibration Schedule

### Daily Calibration
- Navigation sensors
- Proximity sensors
- Docking sensors

### Weekly Calibration
- Long-range scanners
- Communication array
- Thermal sensors

### Monthly Calibration
- Deep space scanners
- Gravimetric sensors
- Subspace detection array

### Quarterly Calibration
- All sensor systems (comprehensive)
- Backup sensor arrays
- Emergency detection systems

## Equipment Required

### Standard Calibration Kit
- Calibration signal generator
- Reference radiation source (shielded)
- Optical alignment laser
- Electromagnetic field generator
- Test target (various ranges)
- Calibration software suite
- Precision measurement tools

### Safety Equipment
- Radiation badge
- Protective eyewear
- Grounding strap
- Insulated tools

## Navigation Sensor Calibration

### Star Tracker Calibration

#### Prerequisites
- Clear view of known star field
- Stable ship orientation
- Navigation computer online
- Current stellar database loaded

#### Procedure
1. **Initialization**
   - Access navigation console
   - Select "Calibration Mode"
   - Enter authorization code
   - Disable autopilot

2. **Star Field Acquisition**
   - Orient ship to calibration zone (Sector 7-Alpha recommended)
   - Allow sensors to acquire minimum 20 reference stars
   - Verify star identification against database
   - Check for any unidentified objects

3. **Alignment Verification**
   - Compare sensor data with known positions
   - Calculate angular deviation
   - Acceptable tolerance: ± 0.001 degrees
   - Record baseline measurements

4. **Adjustment Process**
   - Access alignment controls
   - Make incremental adjustments (0.0001° steps)
   - Verify improvement after each adjustment
   - Continue until within tolerance
   - Lock alignment settings

5. **Verification**
   - Reacquire star field
   - Verify accuracy with secondary targets
   - Test at various ship orientations
   - Document final calibration state

### Inertial Measurement Unit (IMU) Calibration

#### Zero-Motion Calibration
1. Ensure ship is stationary (relative to local frame)
2. Disable all thrusters
3. Initiate IMU calibration sequence
4. Allow 10-minute settling period
5. Collect baseline data (30-minute duration)
6. Calculate and apply correction factors
7. Verify zero-bias within specifications (< 0.001°/hour drift)

#### Motion Calibration
1. Execute pre-programmed maneuver sequence
2. Compare IMU data with star tracker reference
3. Calculate error coefficients
4. Apply calibration matrix
5. Verify accuracy with test maneuvers

## Long-Range Scanner Calibration

### Passive Sensor Calibration

#### Electromagnetic Spectrum Analysis
1. **Background Noise Measurement**
   - Select quiet space region
   - Record baseline across all frequencies
   - Duration: 60 minutes minimum
   - Identify and filter known sources
   - Establish noise floor

2. **Sensitivity Adjustment**
   - Use calibrated reference source
   - Test each frequency band independently:
     - Radio (1 MHz - 300 GHz)
     - Microwave (300 MHz - 300 GHz)
     - Infrared (300 GHz - 430 THz)
     - Visible (430 THz - 770 THz)
     - Ultraviolet (770 THz - 30 PHz)
     - X-ray (30 PHz - 30 EHz)
     - Gamma ray (> 30 EHz)
   - Verify detection threshold
   - Adjust gain if necessary

3. **Resolution Verification**
   - Test angular resolution (should be ≤ 0.1°)
   - Test spectral resolution
   - Test temporal resolution
   - Verify against specifications

### Active Sensor Calibration

#### LIDAR/RADAR Calibration
1. **Transmitter Calibration**
   - Verify output power (should be within ± 2% of rated)
   - Check pulse width and shape
   - Verify frequency stability
   - Test modulation accuracy

2. **Receiver Calibration**
   - Check sensitivity with known returns
   - Verify time-of-flight accuracy
   - Test dynamic range
   - Validate signal processing algorithms

3. **Range Accuracy Test**
   - Use test target at known distance
   - Test at multiple ranges:
     - Close: 100m - 1km
     - Medium: 1km - 100km
     - Long: 100km - 10,000km
     - Extreme: > 10,000km
   - Acceptable error: ± 0.1% of range
   - Adjust timing circuits if needed

## Proximity Sensor Calibration

### Docking Sensor Array

#### Alignment Check
1. Use precision alignment fixture
2. Verify sensor axes orthogonal to hull
3. Check coverage pattern (should overlap 10%)
4. Verify minimum range (0.1m)
5. Verify maximum range (100m)
6. Test accuracy at critical ranges (1m, 5m, 10m, 25m, 50m)

#### Multi-Sensor Fusion Test
1. Position test object in known location
2. Verify all sensors detect object
3. Check position calculation accuracy (± 5cm required)
4. Test at various approach velocities
5. Verify collision prediction algorithm

### Collision Avoidance System

#### Detection Threshold Calibration
1. Test with various object sizes:
   - Small: 10cm - 1m (debris)
   - Medium: 1m - 10m (satellites, cargo)
   - Large: 10m - 100m (other vessels)
   - Massive: > 100m (stations, asteroids)
2. Verify detection at maximum safe range
3. Test tracking accuracy
4. Verify alert timing (must alert before collision unavoidable)

## Gravimetric Sensor Calibration

### Procedure
1. **Baseline Establishment**
   - Position in known gravity field (near planet/star if possible)
   - Record readings for 24 hours
   - Calculate average and standard deviation
   - Establish noise characteristics

2. **Sensitivity Test**
   - Detect known mass at various distances
   - Verify inverse-square relationship
   - Check minimum detectable mass
   - Verify maximum range

3. **Gradient Measurement**
   - Test in varying gravity gradients
   - Verify accuracy of gradient calculation
   - Important for detecting cloaked vessels

## Subspace Sensor Calibration

### FTL Signature Detection
1. **Calibration Source**
   - Requires nearby FTL activity or
   - Use FTL signature generator (if available)
   - Known subspace distortion source

2. **Sensitivity Adjustment**
   - Establish subspace baseline
   - Adjust for local variations
   - Verify detection range
   - Test directional accuracy

3. **Classification Verification**
   - Test with known ship signatures
   - Verify signature database accuracy
   - Check false-positive rate (should be < 1%)

## Thermal Sensor Calibration

### Infrared Array Calibration
1. **Temperature Reference**
   - Use blackbody calibration source
   - Test at multiple temperatures:
     - Cryogenic: 20K - 100K
     - Cold: 100K - 200K
     - Cool: 200K - 273K
     - Warm: 273K - 400K
     - Hot: 400K - 1000K
     - Very Hot: > 1000K
   - Verify linearity across range

2. **Spatial Resolution**
   - Use multi-temperature target
   - Verify pixel-to-pixel uniformity
   - Check for dead pixels
   - Verify minimum resolvable temperature difference (< 0.1K)

3. **Background Subtraction**
   - Record cold-space background
   - Apply correction factors
   - Verify improved signal-to-noise ratio

## Communication Array Calibration

### Signal Reception
1. **Sensitivity Test**
   - Use calibrated signal generator
   - Test across all communication bands
   - Verify minimum detectable signal
   - Should meet: -140 dBm for standard comms

2. **Directional Accuracy**
   - Use multiple known beacons
   - Verify direction-finding accuracy (± 1° required)
   - Test at various signal strengths

### Signal Transmission
1. **Power Output Verification**
   - Measure output power on all bands
   - Verify within rated specifications
   - Check for harmonic distortion
   - Ensure regulatory compliance

2. **Modulation Accuracy**
   - Test all modulation schemes
   - Verify bit error rate (< 10⁻⁹ required)
   - Check encoding/decoding accuracy

## Automated Calibration Routines

### Auto-Calibration System
Many sensors include automated calibration routines. To initiate:

```
SENSOR > CALIBRATE AUTO <sensor_id>
```

#### Advantages
- Faster than manual calibration
- Consistent results
- Can run during non-critical periods
- Logs automatically maintained

#### Limitations
- May not detect all issues
- Requires manual verification quarterly
- Cannot handle major failures
- Limited to standard scenarios

### Scheduled Auto-Calibration
Configure in sensor management system:
1. Access sensor configuration interface
2. Navigate to Auto-Calibration settings
3. Set schedule for each sensor type
4. Configure alert thresholds
5. Enable automatic logging
6. Set notification preferences

## Troubleshooting Calibration Issues

### Calibration Won't Converge
**Symptoms**: Calibration process cannot achieve acceptable tolerance
**Possible Causes**:
- Hardware degradation
- Environmental interference
- Incorrect reference source
- Software error

**Solutions**:
1. Verify reference source accuracy
2. Check for interference sources
3. Update calibration software
4. Inspect hardware for damage
5. Replace sensor if necessary

### Calibration Drifts Quickly
**Symptoms**: Recently calibrated sensor out of spec within hours/days
**Possible Causes**:
- Temperature instability
- Mechanical vibration
- Power supply issues
- Component aging

**Solutions**:
1. Check environmental controls
2. Verify mounting stability
3. Test power supply quality
4. Inspect for failing components
5. Consider component replacement

### Inconsistent Readings
**Symptoms**: Sensor readings vary significantly between calibrations
**Possible Causes**:
- Intermittent hardware fault
- Software bug
- External interference
- Improper calibration procedure

**Solutions**:
1. Review calibration procedure adherence
2. Test in shielded environment
3. Update sensor firmware
4. Run extended diagnostics
5. Monitor over longer period

## Calibration Records

### Required Documentation
- Date and time of calibration
- Technician performing calibration
- Sensor identification
- Calibration method used
- Reference standards used
- Pre-calibration readings
- Post-calibration readings
- Any adjustments made
- Verification test results
- Next calibration due date

### Record Retention
- Electronic logs: 10 years
- Critical systems: Permanent
- Backup to secure storage monthly
- Include in vessel certification documentation

## Required Certifications
- Sensor Systems Technician (Level 2 minimum)
- Calibration Specialist certification
- Radiation Safety (for certain sensors)
- Electrical Safety qualification

## Related Documentation
- See: `sensor-array-overview.md` for system architecture
- See: `sensor-advanced-operations.md` for operational procedures
- See: `kb-089-sensor-ghost-contacts.md` for troubleshooting

## Revision History
- v2.3 - Added subspace sensor calibration procedures
- v2.1 - Updated gravimetric sensor specifications
- v2.0 - Comprehensive rewrite for Mark VI sensor suite
