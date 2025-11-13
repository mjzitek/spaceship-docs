# KB-033: Complete Loss of Communications

**Category:** Communications Systems
**Difficulty:** Intermediate
**Est. Time to Resolve:** 20-60 minutes
**Last Updated:** 2847.09.14

## Issue Description

Customer unable to transmit or receive communications via any method (EM radio, subspace, emergency channels). Total communications blackout affecting all frequencies and protocols.

## Symptoms

- Cannot establish contact with stations or other ships
- No response when transmitting on any frequency
- Unable to receive broadcasts (emergency channels silent)
- Communications panel may show errors or be unresponsive
- May have error codes E-COM-101 through E-COM-115

## Severity Assessment

**CRITICAL if:**
- In distress situation requiring rescue
- In regulated space (traffic control communication required)
- Carrying time-sensitive cargo/passengers
- In hazardous area (asteroid field, combat zone)

**URGENT if:**
- Approaching station (need docking clearance)
- Multi-day journey (need ability to call for help)

**NON-CRITICAL but should fix if:**
- Docked safely
- Short journey with no hazards
- In well-traveled shipping lanes (other vessels nearby)

## Quick Diagnostic Questions

Ask the customer:

1. **"Is the communications panel powered on and showing any displays?"**
   - Dark panel: Power supply issue
   - Displays active: System has power, issue elsewhere
   - Error messages: Note specific codes

2. **"When did communications stop working?"**
   - During FTL jump: FTL interference (wait 30 min after exit)
   - After docking/undocking: Antenna damage possible
   - After electrical event: Power surge or reactor issue
   - Gradual degradation: Component failure
   - Suddenly: Specific event or component failure

3. **"Can you see your antennas from a window or camera?"**
   - Visible damage: Physical antenna damage
   - Missing antenna: Broken off during docking or debris impact
   - Looks normal: Internal failure or configuration issue

4. **"Have you made any recent changes to communications settings?"**
   - Frequency changes: May have misconfigured
   - Firmware update: Update may have failed
   - New equipment: Interference or installation error

5. **"Are any other ship systems malfunctioning?"**
   - Multiple systems down: Ship-wide power or computer issue
   - Only comms affected: Isolated to communications system

## Common Solutions

### Solution A: Power Supply Failure (30% of cases)

**Cause**: Communications system not receiving electrical power.

**Resolution Steps:**

1. **Check Communications Panel Power**
   - Lights on panel: Yes or No?
   - If completely dark: No power reaching panel
   - If lights but no function: Power present but system fault

2. **Check Circuit Breakers**
   - Locate electrical panel (usually in engineering)
   - Find communications system breaker(s)
     - Usually labeled "COMMS" or "COMMUNICATIONS"
     - May be multiple breakers (primary, backup, emergency)
   - Check if tripped (switch in middle position or OFF)

3. **Reset Tripped Breakers**
   - Switch breaker to OFF position
   - Wait 10 seconds
   - Switch to ON position
   - Check if communications panel powers up

4. **If Breaker Immediately Trips Again:**
   - Indicates short circuit in communications system
   - Do NOT repeatedly reset (fire hazard)
   - Isolate fault:
     - Turn OFF main communications panel switch
     - Reset breaker
     - If holds: Fault in panel/equipment
     - If trips: Fault in wiring between breaker and panel
   - Escalate to electrician or repair facility

5. **Check Q-Core Reactor Output**
   - Verify reactor producing adequate power
   - Communications requires 2-40 kW depending on model
   - If reactor output low, communications may be shed to preserve critical systems
   - Refer to KB-001 if reactor issue

**Expected Result:** Communications panel powers up, displays show normal operation, can attempt transmission.

**If Unresolved:** Wiring fault or panel failure, requires professional repair.

---

### Solution B: Antenna Damage (25% of cases)

**Cause**: External antenna arrays damaged or disconnected.

**Resolution Steps:**

1. **Visual Inspection (if possible)**
   - From docking port: Look at visible antennas
   - From windows: Scan hull for antenna arrays
   - Via external cameras: Survey all antenna locations
   - Common damage:
     - Antenna bent or broken
     - Antenna missing (torn off)
     - Burn marks (lightning, weapons fire)
     - Impact damage (collision, debris)

2. **Check Antenna Status on Panel**
   - Access: Comms Panel > System > Antenna Status
   - Shows status of all antenna arrays (typically 4-12)
   - Green: Antenna functional
   - Yellow: Antenna degraded (high VSWR)
   - Red: Antenna failed or disconnected

3. **Identify Pattern**
   - All antennas red: Unlikely all damaged, probably connection issue
   - Single antenna red: Specific damage to that antenna
   - Multiple in same area red: Damage to that hull section

4. **Test with Working Antennas**
   - Even with some antennas damaged, should be able to communicate
   - Access: Comms Panel > Settings > Antenna Selection
   - Manually select a working (green status) antenna
   - Attempt transmission

5. **If No Antennas Show Green:**
   - Problem is NOT antenna damage
   - Check antenna connections at base:
     - May require EVA or access to exterior hull compartments
     - Verify coax cables connected to antenna feeds
     - Check for corrosion on connectors
     - Measure antenna impedance with VSWR meter (should be <2.0:1)

**Temporary Workaround:**
- If some antennas working, can still communicate
- Reduced range and coverage
- Position ship to use working antennas (e.g., if forward antennas broken, face away from station)
- Proceed to port for antenna replacement

**Antenna Replacement:**
- Part #: ANT-EM-series (varies by frequency band and vessel)
- Requires EVA or yard service
- Professional installation recommended (alignment critical)

**Expected Result:** At least one antenna functional, communications restored (may be degraded).

---

### Solution C: Post-FTL Interference (15% of cases)

**Cause**: Residual quantum field from recent FTL jump interfering with communications.

**Resolution Steps:**

1. **Verify Recent FTL Jump**
   - Check if FTL jump completed within last 60 minutes
   - FTL field takes 20-60 minutes to fully dissipate
   - Affects subspace communications primarily, may affect EM as well

2. **Wait for Field Dissipation**
   - Park in safe location
   - Wait 30-60 minutes after FTL exit
   - Check FTL panel for "Field Residual" indicator
   - When reads 0%, interference cleared

3. **Check for FTL Drive Malfunction**
   - If field not dissipating after 60 minutes:
     - Access FTL panel: System > Field Status
     - QFM should show "Idle" and <400°C
     - Tachyon emitters should show "Standby"
   - If FTL drive still active or hot:
     - May have shutdown issue
     - Refer to NAV-FTL-004 troubleshooting
     - FTL drive leaking field interferes with communications

4. **Test EM Communications First**
   - EM radio less affected by FTL field than subspace
   - Try local radio (VHF/UHF bands)
   - If EM works: Wait for subspace to clear
   - If EM also blocked: Issue not FTL-related

**Expected Result:** After field dissipates, communications restore to normal function.

**Prevention:** This is normal physics, cannot be prevented. Allow 30-60 minutes after FTL exit before expecting full communications capability.

---

### Solution D: Communications Computer Failure (10% of cases)

**Cause**: Computer managing communications protocols and routing has crashed or malfunctioned.

**Resolution Steps:**

1. **Check for System Errors**
   - Communications panel: System > Status
   - Look for error messages like:
     - "System Error"
     - "Processor Fault"
     - "Memory Error"
     - Error codes E-COM-301 through E-COM-350

2. **Reboot Communications System**
   - Soft Reboot (try first):
     - Access: Comms Panel > System > Restart
     - System will shutdown and restart (takes 2-3 minutes)
     - All settings preserved
   - Hard Reboot (if soft fails):
     - Power OFF communications panel
     - Wait 30 seconds
     - Power ON
     - System will boot from scratch (3-5 minutes)
     - May lose custom settings

3. **After Reboot, Test Basic Functions**
   - Panel should show "Ready" or normal status
   - Try transmitting on common frequency (e.g., channel 9, 156.45 MHz)
   - Listen to emergency frequency (121.5 MHz) - should hear traffic or at least static
   - If working: Issue resolved

4. **If Reboot Doesn't Help:**
   - Access: Comms Panel > Diagnostics > System Test
   - Run complete diagnostic (5-10 minutes)
   - Checks: Processor, memory, software, I/O
   - Review test results:
     - All pass: Software issue, try firmware reload
     - Hardware failures: Requires component replacement

5. **Firmware Reload (if software suspected)**
   - **CAUTION**: This erases all settings
   - Backup settings if possible: System > Backup Configuration
   - Download firmware from ORSM support portal
   - Access: System > Update > Manual Firmware Load
   - Follow on-screen instructions
   - After reload, restore settings from backup

**Expected Result:** System reboots successfully, communications restored.

**If Unresolved:** Hardware failure, communications computer may need replacement (Part #: COM-CPU-A series). Escalate to professional service.

---

### Solution E: Incorrect Frequency or Settings (10% of cases)

**Cause**: User accidentally misconfigured communications system.

**Resolution Steps:**

1. **Verify Frequency Settings**
   - Check what frequency customer trying to use
   - Common frequencies (should work at most locations):
     - Emergency: 121.5 MHz (always monitored)
     - Ship hailing: 156.45 MHz (Channel 9)
     - Traffic control: Varies, usually 400-470 MHz (station broadcasts)

2. **Check Transmission Power**
   - Access: Comms Panel > Settings > Power
   - EM transmission: Should be 100-1000 W for local comms
   - If set to minimum (10 W): May not reach anyone
   - Increase to maximum and retry

3. **Verify Protocol Settings**
   - Access: Comms Panel > Settings > Protocol
   - Should be: ICP (Interstellar Communications Protocol)
   - If set to proprietary or military protocol: Incompatible with civilian communications
   - Reset to ICP (standard)

4. **Check for Accidental Encryption**
   - Access: Comms Panel > Settings > Encryption
   - If encryption enabled: Others cannot decode transmission
   - May appear as no response (they hear garbled signal)
   - Disable encryption for general communications

5. **Reset to Factory Defaults** (nuclear option)
   - Access: Comms Panel > System > Factory Reset
   - **WARNING**: Erases ALL custom settings
   - Restores known-good configuration
   - After reset:
     - Confirm station license/ID re-entered
     - Set call sign
     - Retry communications

**Expected Result:** With correct settings, communications established.

**Customer Education:** Explain what settings were wrong and how to avoid in future.

---

### Solution F: Subspace Emitter Crystal Exhausted (Subspace Only)

**Cause**: If EM radio works but subspace does not, emitter crystal may be depleted.

**Resolution Steps:**

1. **Test EM vs Subspace Separately**
   - Try EM radio (short range, local): Working?
   - Try subspace (long range, FTL): Working?
   - If EM works but subspace doesn't: Subspace-specific issue

2. **Check Subspace Emitter Status**
   - Access: Comms Panel > Subspace > Emitter Status
   - Crystal lifespan: Should show percentage (0-100%)
   - If <10%: Crystal exhausted, replacement needed
   - If 0% or "Depleted": Definitely exhausted

3. **Replace Subspace Crystal**
   - Part #: SUB-CRYS-A series (model-specific)
   - Location: Subspace emitter housing (usually ventral hull mounting)
   - **May require depressurization of compartment or EVA**
   - Procedure:
     - Power OFF subspace system
     - Access emitter housing
     - Remove old crystal (handle carefully, may be hot)
     - Install new crystal (ensure proper alignment)
     - Close housing (check seal integrity)
     - Power ON subspace system
   - Calibration auto-runs on first power-up with new crystal

4. **Test Subspace Communication**
   - Wait for calibration to complete (5 minutes)
   - Attempt subspace transmission
   - Should work normally

**Expected Result:** Subspace communications restored. EM radio continues working normally.

**Maintenance:** Subspace crystals consumable, require replacement every 3-6 months depending on usage. Keep spare aboard.

---

## Emergency Workarounds

**If Cannot Restore Communications:**

### Option 1: Emergency Beacon
- Deploy emergency beacon (EM radio, auto-broadcast distress)
- Alerts nearby vessels and stations
- Transmits position, ship ID, emergency nature
- One-way only (cannot hear responses but they hear you)

### Option 2: Q-Link Emergency Beacon
- **LAST RESORT - SINGLE USE**
- Quantum-entangled distress signal
- Instantly alerts emergency coordination center
- They will dispatch rescue
- Q-Link destroyed upon use, requires expensive replacement
- Use ONLY in life-threatening emergency

### Option 3: Visual Signals
- If near station or other ships:
  - Flash running lights in SOS pattern (... --- ...)
  - Deploy signal flares (if equipped)
  - Use ship's exterior lights to signal

### Option 4: Physical Courier
- If in system with other ships:
  - Flag down vessel using course changes
  - Request they relay message to station
  - Proceed to station manually (dead reckoning navigation)

## Escalation Criteria

Escalate to emergency support if:

- In distress and unable to call for help
- Customer tried all solutions without success
- Physical damage to multiple systems
- Electrical fire or power system failure
- Navigation also affected (combined failures)

## Prevention Tips

- **Monthly antenna inspection**: Check for damage, corrosion
- **Weekly system test**: Verify communications on all bands
- **Keep spares**: Subspace crystals, antenna elements, fuses
- **Protect antennas**: Be careful during docking
- **Regular firmware updates**: Prevent software bugs
- **Log settings**: Document custom configurations for easy restore
- **Test after FTL**: Verify communications cleared before needing it

## Related Articles

- KB-056: Antenna Damage and Replacement
- KB-071: Subspace System Troubleshooting
- KB-084: Emergency Beacon Operation
- KB-093: Post-FTL System Recovery

## Related Manuals

- COMM-SYS-001: Communications System Overview
- COMM-SYS-003: Communications Troubleshooting
- EMERG-011: Loss of Communications Emergency
- ERR-COM-100: Communications Error Codes

---

**Support Note**: Always ask about recent FTL jump first - 15% of "total comms failure" calls are just waiting for field dissipation. Save diagnostic time by asking this upfront. If they jumped in last hour, tell them to wait and call back if still not working in 30 minutes.
