# Q-Core Reactor Maintenance and Inspection Guide

**Document ID:** PWR-SYS-003
**Revision:** 4.0
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Maintenance Philosophy

Regular maintenance of Q-Core Reactor systems is essential for safe operation, fuel efficiency, and component longevity. Deferred maintenance can result in decreased performance, increased radiation exposure, and catastrophic failure.

**ORSM Recommendation:** Never exceed prescribed maintenance intervals. When operating in harsh environments (high radiation zones, extreme temperatures, combat conditions), reduce intervals by 25%.

## Required Tools and Materials

### Standard Maintenance Kit (Part #: MNT-QCR-STD)

- Magnetic field tester (calibrated within last 6 months)
- Thermal imaging scanner
- Coolant pressure gauge (0-250 PSI range)
- Radiation detector (calibrated, 0-10 mSv/h range)
- Plasma injector cleaning rods (3mm diameter, titanium)
- Containment seal inspection kit
- Diagnostic tablet with Q-Core firmware v8.2 or higher

### Consumables

- Replacement coolant (Sodium-Potassium Grade-A, Part #: COL-NAK-100)
- Magnetic coil lubricant (Cryogenic Synthetic, Part #: LUB-CRY-50)
- Radiation shielding patches (Lead-polymer composite, Part #: SHD-RAD-25)
- Replacement fuel injector nozzles (Part #: INJ-NOZ-Q3, Q5, or Q7)
- Containment vessel gaskets (Part #: GSK-CNT-series)

## Daily Inspections (Reactor Operating)

**Time Required:** 10-15 minutes
**Performed By:** Ship's engineer or certified operator

### Visual Inspection

1. **Control Panel Check**
   - Verify all status lights show green (normal operation)
   - Confirm no warning indicators active
   - Check display readouts for parameter drift

2. **External Visual Scan**
   - Inspect reactor housing for cracks, discoloration, or deformation
   - Check all access panels secured
   - Look for signs of coolant leakage (wet spots, staining)
   - Verify cooling vent airflow (use smoke test if available)

3. **Radiation Scan**
   - Measure radiation at 1 meter from reactor housing
   - Normal reading: 0.2-0.5 mSv/h
   - If reading exceeds 1.0 mSv/h, check shielding integrity
   - Record reading in maintenance log

### Parameter Logging

Record the following in daily log (required for warranty):

| Parameter | Reading | Status |
|-----------|---------|--------|
| Core Temperature | ______°C | Normal / Elevated / Critical |
| Plasma Density | ______ g/cm³ | Normal / High / Low |
| Coolant Pressure | ______ PSI | Normal / High / Low |
| Magnetic Field Strength | ______ Tesla | Stable / Fluctuating |
| Power Output | ______% | Normal / Reduced |
| Fuel Consumption Rate | ______ kg/day | Normal / High / Low |

## Weekly Maintenance (Reactor Can Remain Operating)

**Time Required:** 45-60 minutes
**Performed By:** Ship's engineer with Q-Core certification

### Task 1: Coolant System Inspection

1. **Check Coolant Reservoir Level**
   - Minimum acceptable: 85%
   - Optimal range: 92-98%
   - Top off with Grade-A sodium-potassium coolant if below 90%

2. **Inspect Coolant Lines**
   - Check all visible piping for corrosion or wear
   - Feel for unusual heat along coolant runs
   - Listen for gurgling or knocking sounds (indicates air in system)
   - Tighten any loose fittings

3. **Test Coolant Pressure**
   - Normal operating pressure: 120-140 PSI
   - If below 100 PSI, check for leaks or pump degradation
   - If above 160 PSI, check for blockages or valve malfunction

4. **Sample Coolant Quality**
   - Extract 10ml sample from test port
   - Check color (should be silver-gray, not brown or black)
   - Test pH (acceptable range: 7.5-8.5)
   - If contaminated, schedule coolant flush

### Task 2: Radiation Shielding Verification

1. **Comprehensive Radiation Survey**
   - Measure radiation at 8 points around reactor housing
   - Map measurements on shielding diagram
   - Identify any hot spots (areas above 0.8 mSv/h)

2. **Shield Panel Inspection**
   - Remove inspection covers on shielding panels
   - Check lead-polymer layers for cracks or separation
   - Look for discoloration indicating radiation damage
   - Replace damaged sections with shielding patches

3. **Seal Integrity Test**
   - Verify all shielding panel seals intact
   - Check gasket compression
   - Replace any hardened or cracked gaskets

### Task 3: Magnetic Containment Diagnostics

1. **Field Strength Test**
   - Use calibrated field tester at designated test points
   - Compare readings to baseline (should be within ±0.2 Tesla)
   - If variance exceeds tolerance, schedule coil recalibration

2. **Coil Temperature Check**
   - Use thermal scanner on each superconducting coil
   - Normal temperature: 60-80°C
   - If any coil exceeds 100°C, reduce reactor load and investigate

## Monthly Maintenance (Reduce Reactor to Standby Mode)

**Time Required:** 3-4 hours
**Performed By:** Certified Q-Core technician

### Task 1: Magnetic Field Calibration

1. **Reduce Reactor to Standby**
   - Follow standby procedure in PWR-SYS-002
   - Magnetic field will be at 4.5 Tesla

2. **Run Auto-Calibration Sequence**
   - Connect diagnostic tablet to reactor control interface
   - Navigate to: Diagnostics > Magnetic Systems > Calibration
   - Select "Full Field Calibration"
   - Process takes approximately 45 minutes
   - System will cycle field strength 0-9 Tesla multiple times

3. **Verify Calibration Results**
   - Review calibration report on diagnostic tablet
   - Field uniformity should be ≥ 98%
   - Field stability should be ≤ 0.05 Tesla variance
   - If calibration fails, individual coils may need replacement

### Task 2: Plasma Injector Cleaning

**CRITICAL:** Clogged injectors reduce fuel efficiency and can cause plasma instability.

1. **Shutdown Fuel System**
   - Close main fuel valve
   - Depressurize fuel lines
   - Verify zero fuel flow

2. **Remove Injector Assembly**
   - Unscrew injector access panel (6 bolts, 10mm hex)
   - Carefully extract injector array (contains 12 individual nozzles)
   - Place in clean work area

3. **Clean Injector Nozzles**
   - Use 3mm titanium cleaning rod for each nozzle
   - Gently push through to remove carbon buildup
   - Inspect nozzle opening with magnification (should be perfectly circular)
   - Replace any damaged or deformed nozzles (Part #: INJ-NOZ-Q series)

4. **Reinstall and Test**
   - Insert cleaned injector assembly
   - Torque mounting bolts to 15 Nm
   - Repressurize fuel system
   - Check for fuel leaks
   - Test fire injectors at standby mode (should see smooth plasma stream)

### Task 3: Full System Diagnostic

1. **Connect Diagnostic Tablet**
   - Use certified ORSM diagnostic tablet
   - Connect to reactor maintenance port
   - Launch Q-Core Diagnostic Suite v8.2+

2. **Run Diagnostic Battery**
   - Select "Complete System Analysis"
   - Tests include:
     - Power output stability test
     - Thermal regulation test
     - Magnetic containment stress test
     - Coolant flow dynamics
     - Radiation containment verification
     - Emergency shutdown system test
   - Duration: 60-90 minutes

3. **Review and Log Results**
   - Check for any failed tests or warnings
   - Save diagnostic report to ship's maintenance database
   - Address any identified issues before returning to normal operation

## Quarterly Maintenance (Reactor Shutdown Required)

**Time Required:** Full work shift (8-10 hours)
**Performed By:** Certified technician team (minimum 2 persons)

### Task 1: Containment Vessel Internal Inspection

**DANGER:** Only perform when reactor fully shut down and core temperature below 100°C.

1. **Full Reactor Shutdown**
   - Follow complete shutdown procedure (PWR-SYS-002)
   - Wait minimum 4 hours after shutdown
   - Verify core temperature below 100°C

2. **Open Containment Vessel**
   - Engage reactor lockout/tagout procedures
   - Don full radiation suits (even when shut down)
   - Remove containment vessel access hatch (20 bolts, 15mm hex)
   - Allow vessel to equalize with ambient pressure (30 minutes)

3. **Internal Visual Inspection**
   - Use high-intensity portable lights
   - Inspect fusion chamber walls for:
     - Stress cracks or fractures
     - Erosion or pitting
     - Discoloration indicating hot spots
     - Carbon or fuel residue buildup
   - Photograph any anomalies

4. **Measure Vessel Wear**
   - Use ultrasonic thickness gauge
   - Measure vessel wall at 16 designated points
   - Compare to baseline measurements
   - If wall thickness reduced by >15%, vessel replacement recommended

5. **Clean Internal Surfaces**
   - Remove loose debris with vacuum system
   - Wipe surfaces with approved cleaning solvent
   - Do not use abrasive materials on fusion chamber

6. **Reassemble Containment**
   - Install new containment gasket (Part #: GSK-CNT-series)
   - Replace access hatch
   - Torque bolts to 45 Nm in star pattern
   - Perform pressure leak test (pressurize to 50 PSI, hold 10 minutes)

### Task 2: Coolant System Flush and Replacement

1. **Drain Old Coolant**
   - Connect coolant recovery tank
   - Open drain valves and pump coolant into recovery tank
   - Dispose of old coolant per environmental regulations
   - Used coolant is classified as hazardous material

2. **Flush System**
   - Fill system with flushing solution (Part #: FLS-NAK-CLN)
   - Run coolant pumps for 20 minutes
   - Drain flushing solution
   - Inspect drained fluid for metal particles or sludge

3. **Refill with Fresh Coolant**
   - Use only Grade-A sodium-potassium coolant
   - Fill to 95% capacity
   - Purge air from system (open bleed valves at high points)
   - Verify no leaks

4. **Pressure Test**
   - Pressurize system to 150 PSI
   - Hold pressure for 30 minutes
   - Check all fittings, seals, and welds
   - Address any leaks before restart

### Task 3: Component Replacement Schedule

Replace the following components quarterly (regardless of condition):

| Component | Part Number | Quantity | Notes |
|-----------|-------------|----------|-------|
| Containment Vessel Gasket | GSK-CNT-Q3/5/7 | 1 | Model-specific |
| Fuel Injector O-rings | ORG-INJ-12 | 12 | One per nozzle |
| Coolant Filters | FLT-COL-50 | 2 | Primary and secondary |
| Radiation Monitor Sensors | SNR-RAD-Q | 4 | External hull sensors |
| Control Panel Fuses | FUS-QCR-20A | 6 | Main power circuit |

## Annual Maintenance (Extended Shutdown, Yard Service Recommended)

**Time Required:** 3-5 days
**Performed By:** ORSM certified service facility or master technician

Annual maintenance includes all quarterly tasks plus:

- Superconducting magnet coil replacement or refurbishment
- Thermoelectric converter efficiency testing and refurbishment
- Complete electrical system inspection and rewiring as needed
- Firmware update to latest Q-Core operating system
- Structural integrity scan of reactor mounting
- Replacement of all hoses, tubes, and flexible connections
- Recertification of emergency shutdown system
- Official ORSM inspection and warranty validation

**See Service Bulletin:** SVC-QCR-ANNUAL for complete annual service checklist.

## Maintenance Logs and Record Keeping

### Required Documentation

Maintain the following logs for warranty compliance:

1. **Daily Log**: Parameter readings and visual inspection notes
2. **Weekly Log**: Coolant checks, radiation surveys
3. **Monthly Log**: Calibration results, diagnostic reports
4. **Quarterly Log**: Internal inspection reports, component replacements
5. **Annual Log**: Full service records, certification documents

### Digital Logging

ORSM diagnostic tablets automatically upload maintenance records to:
- Ship's local database
- ORSM Service Cloud (if network available)
- Backup storage on diagnostic tablet

**Retain all records for minimum 10 years** per interstellar maritime law.

## Signs Requiring Immediate Maintenance

Stop normal operations and perform maintenance if:

- Radiation levels exceed 1.5 mSv/h at 1 meter from reactor
- Coolant pressure drops below 80 PSI or rises above 180 PSI
- Core temperature fluctuates more than ±200°C during stable operation
- Unusual sounds (grinding, squealing, banging) from reactor compartment
- Visible coolant leaks or steam
- Power output drops below 50% capacity without load reduction
- Magnetic field strength variance exceeds ±0.5 Tesla
- Any error code in E-PWR-200 through E-PWR-299 range (critical errors)

## Common Maintenance Mistakes

**DO NOT:**

- Use non-approved coolant or substitute fluids
- Exceed torque specifications on bolts
- Perform internal inspection while reactor is warm
- Skip calibration procedures
- Mix old and new coolant
- Reuse single-use gaskets or seals
- Work on reactor without proper radiation protection
- Ignore small leaks ("they'll seal themselves")

## Parts Ordering

Order replacement parts through:
- **ORSM Parts Portal**: parts.outerrimstarship.com
- **Emergency Parts Hotline**: For critical failures
- **Authorized Dealers**: See dealer locator at ORSM website

**Lead Times:**
- Standard parts: 3-7 days (station delivery)
- Specialized components: 2-4 weeks
- Custom orders: 6-12 weeks

**Always specify:**
- Q-Core model (Mark III, V, or VII)
- Ship serial number
- Part number
- Quantity needed

## Related Documents

- PWR-SYS-001: Q-Core Reactor System Overview
- PWR-SYS-002: Q-Core Startup and Shutdown Procedures
- PWR-SYS-004: Q-Core Troubleshooting Manual
- ERR-PWR-100: Power System Error Codes
- SVC-QCR-ANNUAL: Annual Service Bulletin

---

**WARRANTY WARNING**: Failure to perform scheduled maintenance voids Q-Core reactor warranty. Keep all maintenance logs as proof of compliance.
