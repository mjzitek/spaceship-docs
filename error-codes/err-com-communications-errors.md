# Communications System Error Codes (E-COM Series)

**Document ID:** ERR-COM-100
**Revision:** 3.6
**Last Updated:** 2847.09.14
**Manufacturer:** Outer Rim Starship Manufacturing

## Overview

This document provides complete error code reference for Atlas-Series Communications Systems including EM radio, subspace, Q-Link beacon, and related systems.

## Error Code Format

**E-COM-XXX**
- **E**: Error code indicator
- **COM**: Communications system
- **XXX**: Specific error number (001-999)

## Severity Levels

- **CRITICAL** (Red): Complete communications loss, safety hazard
- **WARNING** (Orange): Serious degradation, investigate urgently
- **ADVISORY** (Yellow): Partial failure, schedule maintenance
- **INFO** (Blue): Informational, no immediate action

---

## General Communications Errors (E-COM-100 series)

### E-COM-101: Communications System Offline
**Severity:** CRITICAL
**Cause:** Complete loss of communications capability

**Symptoms:**
- Cannot transmit or receive on any frequency
- Communications panel dark or unresponsive
- No power to system

**Immediate Actions:**
1. Check circuit breakers (communications breaker may be tripped)
2. Verify Q-Core reactor producing power
3. Reset breaker and check if system powers up

**Resolution:**
- If breaker trips repeatedly: Short circuit in system, escalate
- If power present but system dead: Control board failure
- Replace communications computer if necessary (Part #: COM-CPU-A series)

**Related:** KB-033, COMM-SYS-001

---

### E-COM-105: Multiple Antenna Failures
**Severity:** CRITICAL
**Cause:** Several or all antenna arrays non-functional

**Symptoms:**
- Antenna status showing multiple red indicators
- Cannot transmit even on working channels
- May indicate power issue or major damage

**Resolution:**
- If all antennas red: Power distribution issue or central failure
- If some antennas red: Physical damage to those specific arrays
- Check antenna power supply
- Inspect antennas for physical damage
- Replace damaged antennas (Part #: ANT-EM-series)

**Related:** KB-033

---

### E-COM-110: Communication Range Severely Reduced
**Severity:** WARNING
**Cause:** System transmitting but at much lower power than rated

**Symptoms:**
- Can communicate only with very close stations/ships
- Signal strength meter shows weak output
- May indicate power loss or antenna degradation

**Resolution:**
- Check transmit power setting (should be 100-1000W for EM)
- Verify Q-Core providing adequate power to comms system
- Check antenna VSWR (should be <2.0:1)
- Clean or replace degraded antennas

**Related:** COMM-SYS-001

---

## EM Radio Errors (E-COM-150 series)

### E-COM-151: EM Transmission Failure
**Severity:** WARNING
**Cause:** Cannot transmit on EM radio frequencies

**Symptoms:**
- Can receive but not transmit
- No error when pressing transmit, but no signal sent
- Subspace may work (EM-specific issue)

**Resolution:**
- Check EM transmitter section of transceiver
- Verify PTT (push-to-talk) circuit functioning
- Check microphone connection
- Replace EM transceiver board if failed

**Related:** COMM-SYS-001

---

### E-COM-155: EM Reception Failure
**Severity:** WARNING
**Cause:** Cannot receive EM radio signals

**Symptoms:**
- Can transmit but not receive
- Static or silence on all EM channels
- Subspace reception may work

**Resolution:**
- Check EM receiver section
- Verify antenna connections
- Check for receiver desensitization (overload from strong signal)
- Replace receiver board if failed

**Related:** COMM-SYS-001

---

### E-COM-160: Antenna VSWR High
**Severity:** ADVISORY
**Cause:** Antenna impedance mismatch reducing efficiency

**Symptoms:**
- VSWR (Voltage Standing Wave Ratio) >2.0:1
- Reduced transmit efficiency
- May damage transmitter if severe (>3.0:1)

**Resolution:**
- Check antenna connections (corrosion, loose)
- Inspect antenna for damage
- Measure VSWR with proper meter
- Clean antenna insulators
- Replace antenna if VSWR cannot be improved

**Related:** COMM-SYS-001

---

## Subspace Errors (E-COM-200 series)

### E-COM-201: Subspace Transmission Failure
**Severity:** WARNING
**Cause:** Cannot transmit via subspace (EM may work)

**Symptoms:**
- EM radio works
- Subspace shows error or no output
- Cannot reach distant stations requiring subspace

**Possible Causes:**
- Subspace emitter crystal exhausted
- Insufficient power (subspace requires 10-25 kW)
- FTL interference (if recent jump)
- Subspace transmitter failure

**Resolution:**
- Check subspace crystal status (should show >10% lifespan)
- Replace crystal if exhausted (Part #: SUB-CRYS-A series)
- Verify 10-25 kW power available
- Wait 30 min if recent FTL jump (field dissipates)
- Check subspace transmitter diagnostics

**Related:** KB-033, COMM-SYS-001

---

### E-COM-205: Subspace Emitter Crystal Depleted
**Severity:** WARNING
**Cause:** Subspace crystal exhausted, no output

**Symptoms:**
- Crystal status shows 0% or "DEPLETED"
- Subspace transmission impossible
- EM radio still functional

**Resolution:**
- Replace subspace emitter crystal
- Crystals are consumable (3-6 month lifespan)
- After replacement, calibration auto-runs (5 minutes)
- Test subspace transmission

**Related:** KB-033, COMM-SYS-001

---

### E-COM-210: Subspace Dead Zone Detected
**Severity:** INFO
**Cause:** Location has subspace interference preventing transmission

**What This Means:**
- Certain areas of space have subspace turbulence
- Near black holes, neutron stars, certain nebulae
- Not a system failure - environmental condition

**Resolution:**
- Move to different location (outside dead zone)
- Use EM radio for local communications
- Use relay stations if available
- Wait until clear of interference zone

**Related:** NAV-FTL-001, COMM-SYS-001

---

### E-COM-215: FTL Drive Interference
**Severity:** INFO (temporary condition)
**Cause:** Recent FTL jump, residual quantum field interfering

**Symptoms:**
- Subspace not working after FTL exit
- EM may be partially affected
- Temporary condition (20-60 minutes)

**Resolution:**
- Wait 30-60 minutes for FTL field to dissipate
- Check FTL drive status (should show "Field Residual" decreasing)
- EM communications should work (use while waiting)
- If field not dissipating after 60 min: FTL drive may have issue

**Related:** KB-033, NAV-FTL-004

---

## Emergency Beacon Errors (E-COM-250 series)

### E-COM-251: Q-Link Status Unknown
**Severity:** WARNING
**Cause:** Cannot verify Q-Link emergency beacon status

**What This Means:**
- Q-Link is quantum-entangled emergency beacon
- Should show "ARMED" status always
- If status unknown: May not function in emergency

**Resolution:**
- Check Q-Link module connection
- Test Q-Link status circuit (NOT THE BEACON - test mode only)
- Replace Q-Link module if failed (Part #: QLINK-MOD-A)
- **NOTE**: Q-Link is single-use, costs 50,000 credits to replace

**Related:** COMM-SYS-001, EMERG-011

---

### E-COM-255: Q-Link Activated
**Severity:** INFO (but indicates emergency occurred)
**Cause:** Q-Link emergency beacon was triggered

**What This Means:**
- Someone pressed Q-Link emergency activation
- Quantum-entangled signal sent to emergency services
- Rescue will be dispatched to last known position
- Q-Link is now depleted (single-use)

**Resolution:**
- If deliberate activation: Await rescue
- If accidental: Contact emergency services immediately on standard channels
  - Explain false alarm
  - Provide ship ID and position
  - Expect fine (5,000-25,000 credits for false activation)
- Q-Link module must be replaced at authorized station
- Module is destroyed upon activation (cannot be reused)

**Related:** COMM-SYS-001

---

### E-COM-260: Emergency Beacon Malfunction
**Severity:** WARNING
**Cause:** Standard EM emergency beacon not functioning

**Symptoms:**
- Cannot activate emergency beacon
- Beacon test fails
- In emergency, would not auto-broadcast distress

**Resolution:**
- Check beacon power supply
- Test beacon antenna (separate from main comms antennas)
- Replace beacon transmitter if failed (Part #: BCN-EMERG-EM)
- Required by regulation - must repair immediately

**Related:** EMERG-011

---

## Protocol and Software Errors (E-COM-300 series)

### E-COM-301: Communications Computer Fault
**Severity:** CRITICAL
**Cause:** Computer managing protocols/routing has failed

**Symptoms:**
- System powered but not responding
- Cannot establish connections
- Protocol errors
- May show "SYSTEM ERROR" on panel

**Resolution:**
- Reboot communications system
  - Soft reboot: Comms Panel > System > Restart (2-3 min)
  - Hard reboot: Power OFF, wait 30 sec, power ON (3-5 min)
- Run system diagnostic after reboot
- Update firmware if software fault
- Replace communications computer if hardware failure

**Related:** KB-033, COMM-SYS-001

---

### E-COM-305: Protocol Negotiation Failed
**Severity:** ADVISORY
**Cause:** Cannot establish compatible protocol with other station/ship

**Symptoms:**
- Can hear other party
- Cannot establish data connection
- May get "PROTOCOL MISMATCH" message

**Resolution:**
- Verify both using ICP (Interstellar Communications Protocol)
- Check if other party using proprietary/military protocol
- Request they switch to ICP (universal standard)
- Update communications firmware (may add protocol support)

**Related:** COMM-SYS-001

---

### E-COM-310: Encryption Failure
**Severity:** ADVISORY
**Cause:** Encryption system not working

**Symptoms:**
- Cannot send encrypted messages
- May receive unencrypted only
- Encryption module fault

**Resolution:**
- Check encryption module installed (Part #: ENC-Q1024)
- Verify encryption keys loaded
- Update encryption firmware
- Replace encryption module if failed
- Can still communicate without encryption (less secure)

**Related:** COMM-SYS-001

---

## Recorder and Logging Errors (E-COM-350 series)

### E-COM-351: Communications Recorder Failure
**Severity:** ADVISORY
**Cause:** System not recording transmissions as required

**What This Means:**
- Legally required to record emergency and official communications
- Recording failure = regulatory violation
- May need recording for incident investigation

**Resolution:**
- Check recorder storage (may be full)
- Archive old recordings to free space
- Check recorder module power/connections
- Replace recorder if failed (Part #: REC-COM-A)
- Repair promptly - required for regulatory compliance

**Related:** COMM-SYS-001

---

### E-COM-355: Recorder Storage Full
**Severity:** INFO
**Cause:** Recording storage at capacity

**Resolution:**
- Archive recordings to backup media
- Delete non-critical recordings (if legally permissible)
- Some recordings must be retained 7 years (regulatory requirement)
- Expand storage if frequently full (install additional memory)

**Related:** COMM-SYS-001

---

## Hardware Errors (E-COM-400 series)

### E-COM-401: Transceiver Overheating
**Severity:** WARNING
**Cause:** Communications transceiver running too hot

**Symptoms:**
- Transceiver temperature >80°C
- May automatically reduce power to protect hardware
- Reduced transmission range

**Resolution:**
- Check cooling system (fan, heat sink)
- Reduce transmit duty cycle (transmit less, receive more)
- Check for blockage of cooling vents
- Replace cooling fan if failed
- Allow system to cool before resuming high-power ops

**Related:** COMM-SYS-001

---

### E-COM-405: Antenna Physical Damage Detected
**Severity:** WARNING
**Cause:** Antenna damaged (bent, broken, or missing)

**Symptoms:**
- Visual damage to antenna
- Very high VSWR (>3.0:1)
- Little or no transmission/reception
- May have been damaged during docking, debris impact

**Resolution:**
- External inspection of antenna
- Repair if bent (may be able to straighten)
- Replace if broken (Part #: ANT-EM-series)
- Check antenna mounting (may be loose)
- May require EVA or yard service for external antennas

**Related:** COMM-SYS-001, KB-033

---

### E-COM-410: Signal Processor Failure
**Severity:** CRITICAL
**Cause:** DSP (digital signal processor) failed

**Symptoms:**
- Garbled audio
- Cannot decode signals
- May hear transmission but unintelligible

**Resolution:**
- Reboot communications system (may be software glitch)
- Run diagnostic on signal processor
- Update DSP firmware
- Replace signal processor board if hardware fault (Part #: DSP-COM-A)

**Related:** Contact ORSM Support

---

## Interference and Environmental Errors (E-COM-450 series)

### E-COM-451: Strong Interference Detected
**Severity:** ADVISORY
**Cause:** High noise levels on frequencies

**Symptoms:**
- Static, buzzing, or garbled signals
- Cannot hear other party clearly
- May be natural (stellar phenomena) or artificial (jamming)

**Resolution:**
- Change frequencies (try different band)
- Switch to subspace if EM affected
- Increase transmit power
- Use directional antenna (focuses beam, reduces interference)
- Move to location with less interference
- If intentional jamming: Report to authorities

**Related:** COMM-SYS-001

---

### E-COM-455: Electromagnetic Interference from Ship Systems
**Severity:** ADVISORY
**Cause:** Other ship equipment interfering with communications

**Common Sources:**
- Reactor (if poorly shielded)
- FTL drive (during charge or operation)
- Sublight engines (plasma interference)
- Power distribution (arcing, poor grounding)

**Resolution:**
- Identify interference source (turn systems off one at a time)
- Improve shielding on interfering system
- Reroute cables away from communications equipment
- Add filters to power supply
- May require professional EMI troubleshooting

**Related:** COMM-SYS-001

---

## Station/Traffic Control Errors (E-COM-500 series)

### E-COM-501: Cannot Contact Traffic Control
**Severity:** WARNING (CRITICAL in regulated space)
**Cause:** Unable to establish communication with station/port

**Symptoms:**
- Transmitting on traffic control frequency
- No response from station
- May indicate wrong frequency or station issue

**Resolution:**
- Verify correct frequency (station broadcasts on beacon)
- Check if station is staffed (some remote stations automated)
- Try alternate frequencies (hailing, emergency)
- Use ship-to-ship to relay message
- If critical (need docking clearance): Use standard approach procedures and visual signals

**Related:** COMM-SYS-001

---

### E-COM-505: Traffic Control Transmission Garbled
**Severity:** ADVISORY
**Cause:** Receiving station but cannot understand

**Possible Causes:**
- Weak signal (too far or low power)
- Interference
- Station equipment malfunction
- Protocol incompatibility

**Resolution:**
- Request station increase power
- Move closer to station
- Switch frequencies
- Use text/data mode instead of voice
- Request relay through other ship

**Related:** COMM-SYS-001

---

## Error Code Quick Reference

| Code | System | Severity | Description |
|------|--------|----------|-------------|
| E-COM-101 | General | CRITICAL | System offline |
| E-COM-105 | Antennas | CRITICAL | Multiple antenna failures |
| E-COM-110 | General | WARNING | Range reduced |
| E-COM-151 | EM | WARNING | Cannot transmit |
| E-COM-155 | EM | WARNING | Cannot receive |
| E-COM-160 | Antenna | ADVISORY | High VSWR |
| E-COM-201 | Subspace | WARNING | Subspace TX failure |
| E-COM-205 | Subspace | WARNING | Crystal depleted |
| E-COM-210 | Subspace | INFO | Dead zone |
| E-COM-215 | Subspace | INFO | FTL interference |
| E-COM-251 | Q-Link | WARNING | Status unknown |
| E-COM-255 | Q-Link | INFO | Q-Link activated |
| E-COM-260 | Beacon | WARNING | Beacon malfunction |
| E-COM-301 | Computer | CRITICAL | Computer fault |
| E-COM-305 | Protocol | ADVISORY | Protocol failed |
| E-COM-310 | Encryption | ADVISORY | Encryption failed |
| E-COM-351 | Recorder | ADVISORY | Recorder failed |
| E-COM-355 | Recorder | INFO | Storage full |
| E-COM-401 | Hardware | WARNING | Overheating |
| E-COM-405 | Antenna | WARNING | Physical damage |
| E-COM-410 | Hardware | CRITICAL | Processor failed |
| E-COM-451 | Environment | ADVISORY | Interference |
| E-COM-455 | EMI | ADVISORY | Ship interference |
| E-COM-501 | Station | WARNING | No station contact |
| E-COM-505 | Station | ADVISORY | Garbled transmission |

## Related Documents

- COMM-SYS-001: Communications System Overview
- COMM-SYS-003: Communications Troubleshooting
- KB-033: Complete Loss of Communications
- EMERG-011: Loss of Communications Emergency
- NAV-FTL-001: FTL Drive Overview (interference)

---

**Document maintained by ORSM Technical Publications. Communications errors should be resolved promptly - ability to call for help is critical for safety.**
