# Security Systems Overview

**System:** Integrated Ship Security System (ISSS)
**Manufacturer:** Outer Rim Starship Manufacturing (ORSM)
**Variants:** Basic, Standard, Enhanced, Military-Grade
**Document Version:** 3.2
**Last Updated:** 2847.09.14

## Purpose

The Integrated Ship Security System (ISSS) protects vessels and crew from unauthorized access, intrusion, theft, and hostile boarding. Features include access control, intrusion detection, video surveillance, and emergency lockdown capabilities.

## System Variants by Ship Class

### ISSS-Basic (Scout and small personal vessels)
- External door locks (mechanical and electronic)
- Bridge lockout code
- Basic intrusion alarm
- 2-4 interior cameras
- **Cost**: Included standard on all vessels

### ISSS-Standard (Freighters, civilian transports)
- ISSS-Basic features plus:
- Compartment-by-compartment access control
- 8-12 interior cameras with recording (72 hours storage)
- External cameras (4 views: fore, aft, port, starboard)
- Authorized personnel database (crew manifest integration)
- Tamper alarms on critical systems (reactor, life support, cargo)
- Emergency lockdown mode
- **Cost**: 12,000 credits (typical freighter installation)

### ISSS-Enhanced (High-value cargo, passenger ships)
- ISSS-Standard features plus:
- Biometric access control (fingerprint or retinal)
- 20-32 interior cameras (comprehensive coverage)
- Motion sensors in cargo bays and critical areas
- Pressure pad sensors on airlocks and doors
- Armed/disarmed modes (like building security)
- Cargo vault reinforced locks
- Silent alarm to authorities
- Remote monitoring capability
- **Cost**: 45,000 credits

### ISSS-Military (Military, high-security government)
- ISSS-Enhanced features plus:
- Facial recognition system
- Hardened electronics (EMP resistant)
- Automated defensive systems (non-lethal: gas, foam, shock)
- Hull breach detection integrated with security
- Self-destruct capability (requires dual authorization)
- Encrypted communications with command
- Anti-tampering self-destruct on sensitive equipment
- **Cost**: 150,000+ credits (restricted sale, requires authorization)

## Core Components

### 1. Access Control System

**Purpose**: Controls who can enter ship and specific compartments.

**Components:**
- **Door Lock Controllers**: Electronic locks on all hatches and doors
  - Part #: LOCK-ELEC-A (standard), LOCK-BIO-A (biometric)
  - Override: Emergency manual release (inside) or master keycode
- **Access Card/Fob System**: Crew members carry RFID cards
  - Part #: CARD-RFID-A
  - Programmable: Grant/revoke access per person per door
- **Biometric Scanners** (Enhanced/Military):
  - Fingerprint: Part #: SCAN-FING-A
  - Retinal: Part #: SCAN-RET-A
  - Cannot be stolen or duplicated like keycards

**Access Levels** (typical configuration):
- **Level 1 - Public**: Airlock, common areas (granted to all)
- **Level 2 - Crew**: Quarters, galley, recreation (granted to crew)
- **Level 3 - Operations**: Bridge, engineering (granted to qualified crew)
- **Level 4 - Command**: Captain's quarters, secure storage (captain/officers only)
- **Level 5 - Critical**: Reactor core, armory (captain only or dual authorization)

**Programming Access:**
- Access: Security Panel > Access Control > User Management
- Add/remove users
- Assign access levels per user
- View access logs (who entered where and when)

### 2. Intrusion Detection System

**Purpose**: Detect unauthorized entry or tampering.

**Sensors:**
- **Door/Hatch Sensors**: Magnetic switches detect opening
  - Part #: SENS-MAG-A
  - Installed on all exterior hatches and critical interior doors
  - Triggers alarm if opened without authorization
- **Motion Sensors**: Passive infrared (PIR) detects movement
  - Part #: SENS-PIR-A
  - Cover cargo bays, engineering, other critical spaces
  - Armed when ship unoccupied or in lockdown mode
- **Pressure Pad Sensors**: Detect footsteps
  - Part #: SENS-PRES-A
  - Under floor plates in critical areas
  - Cannot be seen, difficult to bypass
- **Glass Break Sensors**: Detect viewport/window breakage
  - Part #: SENS-GLASS-A
  - Acoustic sensor detects sound of breaking
  - Rare on spaceships (few windows), more common on shuttles

**Alarm Modes:**
- **Disarmed**: Sensors inactive, crew moving freely (normal operation)
- **Armed-Stay**: Perimeter armed (exterior hatches), interior disarmed (crew aboard)
- **Armed-Away**: All sensors armed (ship unoccupied)
- **Lockdown**: All compartments locked, all sensors armed (emergency)

**Alarm Response:**
- Audio/visual alert on bridge and security panel
- Log entry (time, location, sensor triggered)
- Optional: Transmit to station security or remote monitoring
- Optional: Automated response (lock compartments, activate cameras, etc.)

### 3. Video Surveillance System

**Purpose**: Visual monitoring and recording of ship interior/exterior.

**Cameras:**
- **Interior Cameras**:
  - Part #: CAM-INT-1080P (Standard), CAM-INT-4K (Enhanced)
  - Coverage: Corridors, airlocks, cargo bays, engineering, bridge
  - NOT in: Crew quarters, bathrooms (privacy laws)
  - Resolution: 1080p (Standard) to 4K (Enhanced)
  - Night vision: Infrared illuminators for low-light areas
- **Exterior Cameras**:
  - Part #: CAM-EXT-HULL
  - Coverage: Fore, aft, port, starboard, dorsal, ventral (full sphere coverage)
  - Ruggedized for space environment
  - Used for security and docking assistance

**Recording:**
- **Storage**: Solid-state recorder, 72 hours rolling buffer (Standard) to 30 days (Enhanced)
  - Part #: REC-SEC-72H or REC-SEC-30D
- **Retention**: Automatically overwrites oldest footage when full
- **Export**: Can copy specific time ranges to external storage (incident investigation)

**Monitoring:**
- **Live View**: Security Panel displays all camera feeds
  - Grid view (all cameras small) or focus view (one camera large)
  - Cycle through cameras automatically or manual selection
- **Playback**: Review recorded footage
  - Access: Security Panel > Surveillance > Playback
  - Search by time or camera
  - Export clips for evidence

### 4. Emergency Lockdown System

**Purpose**: Secure ship against intrusion or contain internal threat.

**Lockdown Activation:**
- Manual: Security Panel > Emergency > Lockdown
- Automatic: Some systems trigger lockdown (hull breach, unauthorized reactor access, etc.)
- Remote: Captain can activate from personal communicator

**Lockdown Effects:**
- All exterior hatches LOCK (cannot be opened without override code)
- All interior compartment doors LOCK
- Crew current location when lockdown activates: Trapped until lockdown lifted
- Critical systems remain accessible to authorized personnel via override codes
- All security sensors ARM
- All cameras activate recording
- Optional: Alarm transmits to station authorities

**Lockdown Override:**
- Master Override Code: Captain-only code unlocks all doors (emergency evacuation)
- Compartment Override: Authorized crew can unlock specific door from interior panel
- Manual Override: Every door has manual release (inside only) for safety

**Use Cases:**
- **Hostile Boarding**: Lock exterior hatches to prevent/delay entry
- **Mutiny/Hostile Crew Member**: Lock down specific compartments to contain threat
- **Hazmat Incident**: Lock down affected area to prevent spread
- **Station/Port Security Requirement**: Some high-security ports require lockdown when docked (prevent smuggling)

### 5. Critical System Tamper Alarms

**Purpose**: Detect unauthorized access to critical ship systems.

**Protected Systems:**
- Q-Core Reactor: Access panel sensor (Part #: SENS-TAMP-A)
- Life Support (APU): Cover removal sensor
- Cargo Bay: Door open sensor (when armed)
- Navigation Computer: Case intrusion sensor
- Communications: Tampering with transmitter (frequency changes, power modifications)

**Tamper Response:**
- Immediate alarm (cannot be silenced without code)
- Log entry with timestamp
- Optional: Photo capture from nearest camera
- Optional: Lock out system (prevent operation until reset by authorized person)

**Purpose of Tamper Alarms:**
- Prevent sabotage
- Detect theft of equipment or cargo
- Regulatory compliance (some cargoes require tamper monitoring)
- Insurance requirement (lower premiums with tamper detection)

## User Interfaces

### Security Panel (Main Control)

**Location**: Bridge, and/or captain's quarters

**Access**: Requires security code or biometric authentication

**Functions:**
- Arm/disarm intrusion sensors
- View live camera feeds
- Review recorded footage
- Manage user access levels
- View access logs (who entered where/when)
- Activate emergency lockdown
- Silence alarms
- Run system diagnostics

**Display Example:**
```
SHIP SECURITY STATUS
Status: Armed-Stay (Perimeter) | Crew: 4 aboard

INTRUSION SENSORS
Exterior Hatches: ARMED ✓
Cargo Bay: DISARMED
Engineering: DISARMED
Bridge: DISARMED

CAMERAS (12)
All cameras: Recording
Storage: 45/72 hours used

ACCESS CONTROL
Recent Activity:
14:35 - Crew Member "J. Smith" - Bridge access granted
14:22 - Crew Member "A. Jones" - Cargo Bay access granted
13:58 - Crew Member "M. Chen" - Engineering access granted

ALERTS: None
```

### Door Panel (Individual Compartment Access)

**Location**: Beside each secured door

**Types:**
- **Basic**: Keypad (enter code)
- **Standard**: Card reader (swipe/tap RFID card)
- **Enhanced**: Biometric scanner (fingerprint or retinal)

**Indicators:**
- Green: Access granted, door unlocked
- Red: Access denied
- Amber: System armed, do not enter (triggers alarm)
- Flashing Red: Lockdown active, door locked

### Remote Monitoring (Optional, Enhanced/Military)

**Capability**: Monitor ship security from remote location

**Use Cases:**
- Owner monitors ship while away
- Fleet management monitors all vessels
- Authorities monitor high-risk cargo shipments

**Access Methods:**
- Subspace link (real-time, expensive)
- Store-and-forward logs (delayed, cheaper)

**Security Concerns:**
- Remote access must be secured (encrypted, authenticated)
- Potential hacking vulnerability if not properly configured
- Many crews disable remote monitoring (privacy concerns)

## Integration with Other Ship Systems

### Hull Integrity System
- Security system receives breach alerts
- Can trigger automatic lockdown if exterior hull breached
- Compartment isolation coordinates with security doors

### Life Support (APU)
- Security can lock out life support controls
- Prevents unauthorized adjustment (oxygen deprivation as weapon)
- Tamper alarm if APU accessed without authorization

### Q-Core Reactor
- Security can lock out reactor controls
- Prevents unauthorized shutdown or SCRAM
- Tamper alarm on reactor access panel

### Communications
- Security system can transmit alarms to station authorities
- Optional: Automatic distress call if intrusion detected
- Integration with crew personal communicators

### Navigation
- Lockdown can disable propulsion (prevent ship theft)
- Integration with emergency beacon (activate on intrusion)

## Power Requirements

- **ISSS-Basic**: 100-200 W
- **ISSS-Standard**: 300-600 W
- **ISSS-Enhanced**: 800-1,200 W
- **ISSS-Military**: 1,500-2,500 W

**Battery Backup**: All systems include 4-12 hour battery backup in case of power failure. Security should remain operational even if reactor fails.

## Common Security Threats and Countermeasures

### Threat: Piracy / Hostile Boarding

**Countermeasures:**
- Arm perimeter sensors when in risky space
- Activate lockdown at first sign of approach
- Reinforce exterior hatches (aftermarket armor available)
- Interior cameras help identify intruder locations
- Some ships: Non-lethal defensive systems (gas, foam)

**Limitations:**
- Determined pirates can breach hull (cutting torch, explosives)
- Lockdown buys time, not permanent solution
- Best defense: Avoid pirate-heavy regions, travel in convoys

### Threat: Theft (Cargo, Equipment, Ship Itself)

**Countermeasures:**
- Always arm system when ship unoccupied
- Use cargo vault for high-value items
- Tamper alarms on expensive equipment
- Immobilize ship (lockout navigation) when docked
- Insurance-approved security reduces premiums

### Threat: Sabotage

**Countermeasures:**
- Tamper alarms on critical systems
- Access control: Limit who can access reactor, life support, etc.
- Cameras monitor critical areas
- Review access logs for unusual activity

**Note**: Insider threat (crew member) difficult to prevent with standard security. Enhanced background checks and crew vetting more effective.

### Threat: Regulatory Inspection / Search

**Not a threat, but security consideration:**
- Authorities can request access at ports
- Must be able to provide access logs and camera footage
- Failure to cooperate may result in detention or fines
- Some security features (encryption, anti-tamper self-destruct) may be illegal in certain jurisdictions

### Threat: Hacking / Cyber Intrusion

**Countermeasures:**
- Security system on isolated network (not connected to ship's main computer)
- Encrypted communications
- Regular firmware updates (patch vulnerabilities)
- Strong passwords/codes (not factory defaults)

**Vulnerabilities:**
- Older systems may have unpatched security holes
- Remote monitoring creates potential attack vector
- Physical access to security panel can allow reset (need to protect panel location)

## Maintenance Requirements

### Daily (If crew aboard)
- Visual check: Are cameras functioning? Doors locking?
- Review access logs for unusual activity

### Weekly
- Test all door locks (lock/unlock cycle)
- Verify all cameras displaying and recording
- Check battery backup status (should show 100% if charging)

### Monthly
- Test intrusion sensors (trigger each sensor, verify alarm)
- Review and export important footage (before overwritten)
- Update access cards/codes (remove departed crew, add new crew)

### Quarterly
- Full system diagnostic
- Clean camera lenses
- Check door panel keypads/readers for wear
- Update firmware (if updates available)

### Annually
- Professional inspection (if Enhanced or Military system)
- Replace worn components (locks, sensors)
- Battery backup load test and replacement if degraded

## Troubleshooting Quick Reference

**False Alarms:**
- Motion sensors too sensitive: Adjust sensitivity settings
- Door sensors misaligned: Realign sensor with magnet
- Environmental: Temperature changes, vibration triggering sensors

**Door Won't Unlock:**
- Check access level: Does user have authorization?
- Check lockdown status: May be locked due to emergency
- Battery in lock depleted: Replace battery (Part #: BATT-LOCK-9V)
- Lock mechanism jammed: Manual override, then repair

**Camera Not Working:**
- Check power to camera
- Check cable connection
- Camera may have failed: Replace (Part #: CAM-INT-1080P)

**System Won't Arm:**
- Check for open doors/hatches: Must all be closed to arm
- Check for sensor faults: Faulty sensor prevents arming
- Check battery backup: Low battery may prevent arming

See KB-102 (Security System Troubleshooting) for detailed solutions.

## Legal and Privacy Considerations

### Privacy Laws (Common in core systems)
- Cannot record in crew quarters or bathrooms
- Must notify crew that surveillance is active
- Footage retention limits (typically 30-90 days max)
- Crew may have right to review footage of themselves

### Outer Rim (Less regulated)
- Few privacy restrictions
- Ship owner has wide latitude
- Still recommended to respect crew privacy (morale, retention)

### Evidence Use
- Security footage admissible in legal proceedings
- Must preserve footage if incident occurs (don't overwrite)
- Tamper-evident storage (chain of custody for court)

### Insurance Requirements
- Many insurers require minimum security level (usually ISSS-Standard)
- Must maintain and test system (evidence of maintenance)
- Failure to activate security may void coverage for theft

## Upgrade Paths

**Basic → Standard**: 10,000 credits (adds cameras, access control)
**Standard → Enhanced**: 35,000 credits (adds biometrics, more cameras)
**Enhanced → Military**: 125,000+ credits (requires authorization, substantial electronics upgrade)

Upgrades typically require 2-5 days yard work (wiring, sensor installation, configuration).

## Related Documentation

- KB-102: Security System Troubleshooting
- KB-156: Lost or Stolen Access Cards
- ERR-SEC-100: Security System Error Codes
- PROC-SEC-001: Emergency Lockdown Procedures
- PROC-SEC-002: Granting Temporary Access (Passengers, Inspectors)

## Support

**ORSM Security System Support:**
- Emergency: Subspace channel 447.2 (24/7)
- Non-emergency: Submit ticket at ORSM support portal
- Firmware updates: ORSM support portal, Security Systems section

---

**Installation Note**: All ORSM vessels include ISSS-Basic as standard equipment. Upgrades to Standard, Enhanced, or Military available at time of purchase or retrofitted at any authorized service center. Contact ORSM sales for pricing and installation scheduling.
