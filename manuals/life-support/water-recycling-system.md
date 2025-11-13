# Water Recycling and Management System

**Document ID:** LIFE-WAT-001
**Revision:** 3.6
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Purpose

This document describes the Water Recycling and Management System (WRMS) that processes, purifies, and distributes water for drinking, hygiene, and life support systems aboard ORSM vessels.

## System Description

The WRMS is a closed-loop system that recovers water from all sources (wastewater, humidity condensation, crew exhalation), purifies it to potable standards, and redistributes it for various uses. Properly maintained systems can achieve 95-98% water recovery rates.

### Operating Principle

The WRMS operates through six processes:

1. **Collection**: Gathering wastewater from all sources
2. **Pre-Filtration**: Removing solid waste and large particles
3. **Biological Treatment**: Breaking down organic contaminants
4. **Multi-Stage Filtration**: Removing dissolved contaminants and pathogens
5. **Purification**: Final sterilization and mineralization
6. **Distribution**: Delivering water to various systems

### Key Components

- **Wastewater Collection Tank**: Holding tank for used water (200-2,000L capacity)
- **Pre-Filter Assembly**: Screens and sediment filters
- **Biological Reactor**: Aerobic bacteria culture breaking down organics
- **Reverse Osmosis Unit**: Membrane filtration removing dissolved solids
- **UV Sterilizer**: Ultraviolet light kills remaining pathogens
- **Activated Carbon Filter**: Removes odors and trace chemicals
- **Mineralization Unit**: Adds essential minerals for drinking water
- **Potable Water Tank**: Clean water storage (200-2,000L capacity)
- **Distribution Pumps**: Delivers water to taps, showers, and systems
- **Water Quality Sensors**: Continuous monitoring of purity

## WRMS Models

### WRMS-Compact (Small Vessels)
- **Capacity**: 1-4 crew members
- **Daily Processing**: 20-80 liters
- **Storage**: 200L wastewater + 200L potable
- **Recovery Rate**: 92-95%
- **Power Consumption**: 1.5-3 kW
- **Typical Vessels**: Shuttles, scouts, personal craft

### WRMS-Standard (Medium Vessels)
- **Capacity**: 5-20 crew members
- **Daily Processing**: 100-400 liters
- **Storage**: 500L wastewater + 500L potable
- **Recovery Rate**: 95-97%
- **Power Consumption**: 5-10 kW
- **Typical Vessels**: Freighters, transports, patrol craft

### WRMS-Industrial (Large Vessels)
- **Capacity**: 25-100 crew members
- **Daily Processing**: 500-2,000 liters
- **Storage**: 2,000L wastewater + 2,000L potable
- **Recovery Rate**: 96-98%
- **Power Consumption**: 15-35 kW
- **Typical Vessels**: Large freighters, military vessels, passenger ships

## Water Budget

### Per-Person Daily Consumption (typical)

- **Drinking**: 2-3 liters
- **Food Preparation**: 1-2 liters
- **Hygiene** (washing hands, face): 3-5 liters
- **Shower**: 8-12 liters (water-saving shower heads)
- **Toilet**: 1-2 liters (low-flow systems)
- **Laundry**: 3-5 liters (weekly average)
- **Total**: 18-24 liters per person per day

### Water Loss

Despite recycling, some water is lost:

- **Oxygen Generation**: Electrolysis consumes ~1.1 kg water per 1.0 kg O₂
- **Metabolic Loss**: 0.3 kg per person per day (exhaled, not recoverable)
- **System Inefficiency**: 2-5% of processed water
- **Total Loss**: 2-4 liters per person per day

**Water resupply needed every 30-90 days** depending on crew size and storage capacity.

## Normal Operating Parameters

| Parameter | Minimum | Optimal Range | Maximum | Critical |
|-----------|---------|---------------|---------|----------|
| Potable Tank Level | 30% | 60-90% | 100% | <20% |
| Wastewater Tank Level | 0% | 20-50% | 80% | >90% |
| Processing Rate | 50% rated | 80-100% rated | 110% rated | <40% |
| Water Purity (TDS) | N/A | 50-150 ppm | 300 ppm | >500 ppm |
| Bacterial Count | N/A | 0 CFU/100ml | 0 CFU/100ml | >0 CFU/100ml |
| pH Level | 6.0 | 6.5-8.5 | 9.0 | <6.0 or >9.5 |
| Chlorine Residual | 0 ppm | 0.2-0.5 ppm | 1.0 ppm | >2.0 ppm |
| UV Sterilizer Output | 80% | 95-100% | 100% | <70% |

**TDS = Total Dissolved Solids
**CFU = Colony Forming Units (bacterial contamination)

## Water Sources and Collection

### Wastewater Sources

**Greywater** (90% of wastewater):
- Sink drains
- Shower drains
- Laundry discharge
- Food preparation waste

**Blackwater** (10% of wastewater):
- Toilet waste
- Requires additional treatment

**Atmospheric** (bonus water):
- Condensation from humidity control (APU system)
- Collected automatically and routed to wastewater system
- Can provide 1-3 liters per person per day

### Collection Process

1. All drains route to wastewater collection tank
2. Tank has agitator preventing solids from settling
3. Level sensors monitor tank capacity
4. When tank reaches 50% full, processing cycle initiates automatically
5. Emergency manual processing can be triggered if needed

## Water Processing Cycle

**Total Cycle Time**: 6-12 hours depending on load and system model

### Stage 1: Pre-Filtration (30 minutes)

1. Wastewater pumped from collection tank
2. Passes through coarse screen (removes objects >5mm)
3. Sediment filter catches particles >100 microns
4. Pre-filtered water enters biological reactor

### Stage 2: Biological Treatment (4-8 hours)

1. Aerobic bacteria culture breaks down organic matter
   - Bacteria consume proteins, fats, carbohydrates
   - Converts complex organics to simple compounds
   - Oxygen continuously bubbled through reactor

2. Residence time: 4-8 hours depending on contamination level
3. Bacteria culture maintained at 30-35°C (optimal activity)
4. Periodic bacteria culture refresh required (monthly)

### Stage 3: Mechanical Filtration (1-2 hours)

1. **Multimedia Filter**
   - Layers of sand, gravel, activated carbon
   - Removes particles >10 microns
   - Removes some dissolved organics

2. **Reverse Osmosis (RO) Membrane**
   - High-pressure pump forces water through semi-permeable membrane
   - Membrane pore size: 0.0001 microns
   - Removes:
     - 95-99% of dissolved salts
     - 99% of organic molecules
     - All bacteria and viruses
   - Concentrate (waste) stream sent back to collection tank for reprocessing

### Stage 4: Sterilization (15 minutes)

1. **UV Sterilization**
   - Water exposed to high-intensity UV-C light (254 nm wavelength)
   - UV destroys DNA of any remaining microorganisms
   - Minimum exposure: 30 mJ/cm²
   - No chemicals added, no residual taste

2. **Activated Carbon Polishing**
   - Final pass through carbon filter
   - Removes any remaining odors or trace organics
   - Improves taste

### Stage 5: Mineralization and Storage (15 minutes)

1. **Mineral Addition**
   - RO removes all minerals, making water "too pure"
   - Mineralization unit adds back essential minerals:
     - Calcium: 30-50 ppm
     - Magnesium: 10-20 ppm
     - Potassium: 5-10 ppm
   - Improves taste and provides health benefits

2. **Final pH Adjustment**
   - Target: 7.0-7.5 (neutral to slightly alkaline)
   - Uses food-grade sodium bicarbonate if needed

3. **Transfer to Potable Tank**
   - Purified water pumped to clean water storage
   - Final quality check by sensors before acceptance
   - If water fails quality check, diverted back for reprocessing

## Daily Monitoring

Crew should check WRMS status daily:

1. **Tank Levels**
   - Potable water tank: Should be 60-90% full
   - Wastewater tank: Should be below 80%
   - If imbalance, may indicate leak or processing issue

2. **Water Quality Indicators**
   - Control panel displays TDS, pH, bacterial count
   - All should be in green (optimal) range
   - Yellow or red indicators require investigation

3. **System Status**
   - Check for error codes or warnings
   - Verify processing cycles running on schedule
   - Listen for unusual pump or motor sounds

4. **Visual Inspection**
   - Look for water leaks around tanks, pipes, fittings
   - Check UV sterilizer lamp (should see purple glow when active)
   - Inspect filter housings for signs of pressure leaks

## Weekly Maintenance

**Time Required**: 30-45 minutes

### Task 1: Water Quality Testing

1. **Sample Potable Water**
   - Draw sample from tap or tank test port
   - Use test strips or portable analyzer

2. **Measure Parameters**
   - TDS (should be 50-150 ppm)
   - pH (should be 6.5-8.5)
   - Chlorine residual (should be 0.2-0.5 ppm if chlorination used)

3. **Bacterial Test** (recommended monthly minimum)
   - Use sterile sample bottle
   - Incubate test culture 24-48 hours
   - Count colonies (should be zero)

### Task 2: Filter Inspection

1. Check pre-filter differential pressure
   - Gauge shows pressure drop across filter
   - Normal: <5 PSI
   - If >10 PSI: Filter clogged, replacement needed

2. Inspect sediment filter
   - Remove filter cartridge
   - Visually check for heavy loading
   - Replace if >50% of surface area clogged

3. Check activated carbon filter
   - Note color and odor of processed water
   - If taste/odor issues, carbon may be exhausted

### Task 3: System Performance Check

1. Monitor processing cycle time
   - Should complete in expected time (6-12 hours)
   - If taking longer, may indicate filter clogging or pump wear

2. Check RO membrane permeate flow
   - Normal flow: varies by model, see specifications
   - If flow reduced by >30%, membrane cleaning or replacement needed

3. Verify UV sterilizer operation
   - Lamp should be glowing when water passing through
   - Check UV intensity meter (should be >80% of rated output)

## Monthly Maintenance

**Time Required**: 2-4 hours

### Task 1: Filter Replacement

**Pre-Filters** (Part #: FLT-WRMS-PRE)
- Replace coarse screen if damaged
- Replace sediment filter (every 1-2 months)
- Note: Replacement frequency depends on water quality and usage

**Activated Carbon Filter** (Part #: FLT-WRMS-AC)
- Replace every 2-3 months
- More frequently if taste/odor issues
- Used carbon can be recycled at most stations

### Task 2: RO Membrane Maintenance

1. **Check Membrane Performance**
   - Measure TDS of permeate (purified) water
   - Measure TDS of concentrate (waste) water
   - Calculate rejection rate: (1 - Permeate TDS / Feed TDS) × 100%
   - Should be >95%

2. **Clean Membrane if Needed**
   - If rejection rate <90%, cleaning recommended
   - Use manufacturer-approved cleaning solution
   - Follow chemical cleaning procedure (see LIFE-WAT-002)

3. **Replace Membrane if Degraded**
   - If cleaning doesn't restore performance
   - Or if membrane in use for >24 months
   - Part #: MEM-RO-series (model specific)

### Task 3: Biological Reactor Service

1. **Check Bacteria Culture Health**
   - Culture should appear cloudy/milky (indicates active bacteria)
   - No foul odors (indicates culture die-off or contamination)
   - Microscopic check (if equipment available) shows motile bacteria

2. **Refresh Bacteria Culture**
   - Drain 50% of reactor volume
   - Add fresh bacteria culture supplement (Part #: BIO-CULT-WRM)
   - Allow 24 hours for culture to reestablish

3. **Clean Reactor**
   - Remove accumulated sludge from bottom
   - Scrub reactor walls if biofilm buildup observed
   - Check air bubbler function (continuous aeration required)

### Task 4: UV Sterilizer Service

1. **Clean UV Lamp Sleeve**
   - Mineral deposits on quartz sleeve reduce UV transmission
   - Remove sleeve and clean with vinegar solution
   - Rinse thoroughly and reinstall

2. **Check UV Lamp Output**
   - Use UV intensity meter
   - Lamp output should be >80% of rated intensity
   - UV lamps degrade over time even if still glowing

3. **Replace UV Lamp if Needed**
   - Lifespan: 8,000-10,000 hours (about 12 months continuous use)
   - Replace if output <70% or per manufacturer schedule
   - Part #: UV-LAMP-254 (various wattages)

## Troubleshooting

### Low Potable Water Supply

**Symptoms**: Potable tank level dropping, not refilling after processing cycle

**Possible Causes**:
- Leak in potable water system
- Processing system malfunction
- Excessive consumption
- Water quality failures causing reprocessing

**Diagnostics**:
1. Check for visible leaks in pipes, tanks, fittings
2. Monitor consumption rate vs crew size
3. Review water quality sensor logs
4. Check if processing cycles completing successfully

### Poor Water Taste/Odor

**Symptoms**: Water has unpleasant taste or smell despite passing purity tests

**Possible Causes**:
- Exhausted activated carbon filter
- Biological contamination (non-pathogenic but taste-causing)
- Mineralization imbalance
- Chlorine residual too high

**Diagnostics**:
1. Replace activated carbon filter
2. Check UV sterilizer operation
3. Test mineralization unit output
4. Adjust chlorine dosing if used

### Bacterial Contamination

**Symptoms**: Bacterial test shows colony growth, water quality alarm

**CRITICAL**: Do not consume water if bacterial contamination confirmed

**Actions**:
1. Post "DO NOT DRINK" warnings at all water outlets
2. Switch to emergency water ration if available
3. Shock treat system:
   - Add chlorine to achieve 50 ppm throughout system
   - Circulate for 4 hours
   - Flush system completely
   - Retest before allowing consumption

4. Investigate contamination source:
   - UV sterilizer failure most common cause
   - Crack in potable tank
   - Backflow from contaminated source

### High TDS (Total Dissolved Solids)

**Symptoms**: TDS >300 ppm, water tastes salty or mineral

**Possible Causes**:
- RO membrane failure or degradation
- RO pump pressure insufficient
- Membrane fouled

**Actions**:
1. Check RO pump pressure (should be 200-400 PSI depending on model)
2. Clean RO membrane
3. If cleaning ineffective, replace membrane
4. Verify mineralization unit not over-dosing

### Wastewater Tank Overfilling

**Symptoms**: Wastewater tank approaching 100%, processing can't keep up

**Possible Causes**:
- Processing system malfunction (pumps, filters, etc.)
- Excessive water usage
- RO rejection rate too high (too much concentrate being recycled)

**Actions**:
1. Implement water conservation measures
2. Run processing cycles more frequently (manual initiation)
3. Check for failed components (pumps, filters)
4. May need to emergency dump excess wastewater (only if absolutely necessary, requires approval)

**See LIFE-WAT-003 for complete troubleshooting guide.**

## Water Conservation

During emergencies or low water situations:

### Priority 1: Drinking and Food Prep
- Minimum 3 liters per person per day
- Cannot be reduced further without health risk

### Priority 2: Critical Hygiene
- Hand washing, face cleaning
- Reduce to 2 liters per person per day
- Use waterless hand sanitizer when possible

### Priority 3: Reduced Showering
- Limit to 30-second rinse every 2-3 days
- Use dry shampoo and cleansing wipes
- 2-3 liters per person per week

### Priority 4: Minimal Laundry
- Wear clothes multiple days
- Spot clean only
- Use waterless fabric refreshers

**Severe Rationing**: Can reduce to 5-8 liters per person per day for short periods

## Emergency Procedures

### Complete WRMS Failure

**IMMEDIATE ACTIONS:**

1. Check potable water tank level
   - Calculate days of water remaining: (Tank liters) / (Crew × 3L/day)

2. Implement strict rationing immediately
3. Attempt system restart:
   - Check power supply
   - Reset WRMS controller
   - Manually initiate processing cycle

4. If restart fails:
   - Diagnose and repair if possible
   - Send distress signal if water will run out before help available
   - Prepare for emergency docking or rescue

### Contamination Event

If potable water contaminated with chemicals, fuel, or unknown substance:

1. **STOP all water consumption immediately**
2. Isolate potable tank (close all outlet valves)
3. Switch to emergency water ration
4. Identify contaminant source
5. Drain and decontaminate entire potable system:
   - Requires complete system flush
   - May need to discard all potable water
   - 24-48 hours before water safe to drink

6. Contact ORSM support for decontamination procedures

**See EMERG-009 for complete water system emergency procedures.**

## Related Documents

- LIFE-WAT-002: WRMS Maintenance Schedule
- LIFE-WAT-003: WRMS Troubleshooting Guide
- LIFE-ATM-001: Atmospheric Processing Unit
- EMERG-009: Water System Emergency Procedures
- ERR-LIFE-200: Water System Error Codes

---

**SURVIVAL REMINDER**: Water is your most critical consumable. Never defer water system maintenance. Always maintain emergency water ration as backup.
