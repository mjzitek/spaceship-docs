# KB-156: Communications System Complete Failure
**Category:** Communications | **Severity:** High | **Avg Resolution Time:** 20 minutes

## ISSUE SUMMARY
Customer reports complete inability to send or receive communications. All frequencies affected, not just specific bands.

**Common Symptoms:**
- Cannot transmit or receive on any frequency
- "COM-501: Communications System Offline" error
- No response from communications panel
- Antenna system unresponsive

**Related Issues:**
- For partial communications issues, see [Top 20 #4: Communications Interference](../quick-reference/top-20-common-issues.md#4-communications-interferencestaticit)
- For encryption-specific issues, see [Top 20 #18: Encryption Failure](../quick-reference/top-20-common-issues.md#18-encryption-key-exchange-failure)

---

## QUICK DIAGNOSTIC QUESTIONS

Ask these questions FIRST to triage severity and root cause:

### Safety Assessment
1. **Are you in a hazardous situation requiring emergency communications?**
   - If YES → Escalate to emergency response, provide alternative contact methods
   - If NO → Proceed with troubleshooting

### Scope Questions
2. **Can you transmit, receive, both, or neither?**
   - Neither → Complete system failure (this article)
   - One direction only → Partial failure (different diagnosis)
   - Both but poor quality → Interference issue, not system failure

3. **When did this start?**
   - After maintenance/update → Configuration or installation issue
   - After impact/combat → Physical damage likely
   - Gradually → Component degradation
   - Suddenly with no event → System or power failure

4. **Have you checked other systems?**
   - Multiple systems down → Power or computer issue (see [System Interaction Matrix](../quick-reference/system-interaction-matrix.md))
   - Only comms affected → Communications-specific issue

---

## DIAGNOSTIC FLOWCHART

```
Communications Completely Offline
         ↓
Is power indicator lit on comms panel?
         ↓ NO                    ↓ YES
[Go to Section A:           [Go to Section B:
 Power Issues]               System Issues]
         ↓                        ↓
Power restored?              System responsive?
         ↓ NO                    ↓ NO
[Escalate: Power]          [Go to Section C:
                            Hardware Issues]
                                  ↓
                            Visible damage?
                            ↓ YES        ↓ NO
                      [Escalate:      [Go to Section D:
                       Hardware]       Software Issues]
```

---

## SECTION A: POWER ISSUES

### Symptoms
- Comms panel completely dark
- No lights or indicators
- System doesn't respond to any inputs

### Step 1: Check Power Allocation
**Customer Action:**
```
1. Go to main power distribution panel
2. Check "Communications" power allocation
3. Report: What percentage is allocated? Is it showing as "Offline" or "No Power"?
```

**Expected Result:**
- Should be 5-20% depending on transmission needs
- Minimum 5% required for basic operation

**If power allocation is 0% or "Offline":**
```
Diagnosis: Power distribution issue
→ Check if comms circuit breaker tripped
→ Check for comms system in power priority settings
→ May need to disable non-essential systems to free up power
→ See [Power Distribution Manual](../manuals/power/power-distribution-networks.md)
```

**If power allocated but panel still dark:**
```
Diagnosis: Power delivery issue (cabling or panel)
→ Proceed to Step 2
```

---

### Step 2: Check Circuit Breaker
**Customer Action:**
```
1. Locate communications circuit breaker
   - Usually in main electrical panel near bridge
   - Labeled "COMMS" or "Communications Array"
2. Check breaker status
3. If tripped, attempt reset
```

**If breaker trips immediately when reset:**
```
Diagnosis: Short circuit in communications system
→ DO NOT keep resetting (fire hazard)
→ Escalate to electrical specialist
→ Recommend backup communications methods
```

**If breaker stays set but still no power to comms:**
```
Diagnosis: Wiring issue between breaker and comms equipment
→ Check for visible damage to wiring
→ Escalate if wiring issue confirmed
```

---

### Step 3: Try Backup/Emergency Communications
**Customer Action:**
```
Most ships have backup comms capability:
1. Check for "Emergency Comms" panel (usually near airlock)
2. Try portable/handheld communication units
3. Check lifeboat/escape pod communication systems
```

**If backup comms work:**
```
Diagnosis: Primary system failure, but ship has communications capability
→ Continue troubleshooting to restore primary
→ Customer can use backup in meantime
```

---

## SECTION B: SYSTEM ISSUES (Power Present)

### Symptoms
- Comms panel has power (lights on)
- System unresponsive or error messages
- Panel controls don't work

### Step 1: Restart Communications Computer
**Customer Action:**
```
1. Communications Panel → System → Restart Comms Computer
   (OR)
2. Hold power button on comms panel for 10 seconds until shutdown
3. Wait 30 seconds
4. Power back on
5. Wait for system initialization (usually 60-90 seconds)
6. Check if communications functional
```

**Expected Result:**
- System should boot up and run self-diagnostics
- Should hear/see initialization sequence
- Display should show status screens

**If system boots normally:**
```
Diagnosis: Software glitch or crashed computer
→ Test communications functionality
→ If working, issue resolved
→ Document what customer was doing when it crashed (for trending)
```

**If system won't boot or boots to error:**
```
→ Note exact error message
→ Proceed to Step 2
```

---

### Step 2: Check Communications Computer Status
**Customer Action:**
```
1. Main Computer Panel → System Status → Communications
2. Report status of:
   - Comms Computer: Online/Offline/Error?
   - Comms Processor: % Utilization
   - Memory Status: Available
   - Error Log: Any critical errors?
```

**If comms computer shows "Offline":**
```
Diagnosis: Computer hardware failure or connection
→ Check physical connection between computer and comms equipment
→ Try "Reset Comms Computer" from main computer panel
→ If persists, escalate for computer hardware issue
```

**If showing errors:**
```
→ Note error codes
→ Check [Error Codes: Communications](../error-codes/error-codes-communications.md)
→ Resolve based on error code guidance
```

---

### Step 3: Check Antenna System
**Customer Action:**
```
1. Comms Panel → Antenna Status
2. Check:
   - Antenna Position: Should show current orientation
   - Motor Status: Should show "Operational"
   - Tracking Mode: Auto/Manual
3. Try commanding antenna to move:
   - Manual Control → Rotate antenna
   - Does it respond?
```

**If antenna won't move or shows errors:**
```
Diagnosis: Antenna system failure
→ Proceed to Section C: Hardware Issues (antenna-specific)
```

**If antenna moves but still no comms:**
```
Diagnosis: Antenna functional, issue with transmitter/receiver
→ Proceed to Step 4
```

---

### Step 4: Run Communications Self-Diagnostic
**Customer Action:**
```
1. Comms Panel → Diagnostics → Full System Test
2. Test will take 3-5 minutes
3. Report results:
   - Overall status: Pass/Fail
   - Which components failed?
   - Any specific error codes?
```

**Interpret Results:**
- **Transmitter Failed:** Cannot send signals
- **Receiver Failed:** Cannot receive signals
- **Frequency Synthesizer Failed:** Cannot change frequencies
- **Antenna Interface Failed:** Cannot control antenna
- **Encryption Module Failed:** Can't do secure comms (basic comms may work)

**Based on diagnostic results:**
```
→ Note failed components
→ If multiple component failures → Likely power or computer issue
→ If single component failure → Hardware replacement may be needed
→ Proceed to Section C: Hardware Issues
```

---

## SECTION C: HARDWARE ISSUES

### Symptoms
- Diagnostics show hardware component failure
- Physical damage visible to antenna or equipment
- System powers on but specific hardware non-functional

### Step 1: Visual Inspection
**Customer Action (if safe):**
```
1. Visually inspect:
   - External antenna (from window/camera if available)
   - Communications equipment bay (if accessible)
   - Cable connections to communications equipment

2. Look for:
   - Broken/bent antenna
   - Disconnected cables
   - Burn marks or melted components
   - Loose connections
   - Impact damage
```

**If visible damage found:**
```
Diagnosis: Physical damage requires repair
→ Document damage (photos if possible)
→ Escalate to hardware repair
→ Provide workaround options (backup comms, alternate antenna if available)
```

**If no visible damage:**
```
→ Proceed to Step 2
```

---

### Step 2: Check Cable Connections
**Customer Action (if accessible):**
```
1. Locate communications equipment bay
2. Check all cable connections:
   - Power cable: Firmly connected?
   - Data cables: Secured and not damaged?
   - Antenna cable: Connected at both ends?
3. If any loose, reconnect firmly
4. Retry communications
```

**If reconnecting cables resolves issue:**
```
Diagnosis: Loose connection from vibration or maintenance
→ Issue resolved
→ Recommend securing cables properly
→ May indicate excessive vibration (investigate if recurring)
```

---

### Step 3: Test with Alternate Antenna (if available)
**Customer Action (if ship has multiple antennas):**
```
1. Comms Panel → Antenna Select
2. Switch to alternate antenna (if equipped)
3. Test communications
```

**If alternate antenna works:**
```
Diagnosis: Primary antenna hardware failure
→ Continue operations on backup antenna
→ Schedule repair for primary antenna
→ Note: Backup may have different capabilities (range, directionality)
```

**If no alternate antennas work:**
```
Diagnosis: Likely communications computer or transmitter issue, not antenna
→ Escalate to communications specialist
```

---

### Step 4: Check for Interference from Own Ship
**Customer Action:**
```
1. Temporarily shut down high-power systems:
   - Weapons (if safe to do so)
   - FTL drive
   - Active sensors
2. Try communications
3. Power systems back up one at a time
4. Identify if any cause interference
```

**If communications work with systems off:**
```
Diagnosis: Electromagnetic interference from own ship systems
→ Shield or filter issue
→ Systems may be operating outside normal parameters
→ Escalate to systems integration specialist
```

---

## SECTION D: SOFTWARE/CONFIGURATION ISSUES

### Symptoms
- Hardware diagnostics pass
- Power present and stable
- System boots but doesn't communicate properly

### Step 1: Check Configuration Settings
**Customer Action:**
```
1. Comms Panel → Settings → System Configuration
2. Verify:
   - Ship ID/Call Sign: Correct?
   - Frequency Range: Correct for your region?
   - Protocol Settings: Match intended contacts?
   - Power Level: Set to appropriate level (not 0%)?
3. Check if "TEST MODE" or "MAINTENANCE MODE" is enabled
```

**If settings incorrect:**
```
→ Note what's wrong
→ Correct settings to proper values
→ Test communications
→ If resolved, determine how settings changed (recent update? User error?)
```

---

### Step 2: Reset to Factory Defaults
**Customer Action:**
```
⚠️ WARNING: This will erase all saved frequencies, contacts, and settings
1. Backup current settings if possible:
   - Comms Panel → Settings → Export Configuration
2. Reset to defaults:
   - Comms Panel → System → Factory Reset
   - Confirm reset
3. System will reboot (2-3 minutes)
4. Enter basic configuration:
   - Ship call sign
   - Home port frequency
5. Test basic communications
```

**If communications work after reset:**
```
Diagnosis: Configuration corruption or incorrect settings
→ Issue resolved
→ Customer will need to reconfigure preferences
→ Restore backup if available
→ If happens repeatedly, may indicate failing memory/storage
```

---

### Step 3: Update Communications System Firmware
**Customer Action (if update available):**
```
1. Main Computer → System Updates → Communications
2. Check for available firmware updates
3. If updates available:
   - Note current version number
   - Install updates
   - System will reboot
   - Test after update completes
```

**If update resolves issue:**
```
Diagnosis: Known bug in previous firmware version
→ Issue resolved
→ Document firmware versions for records
```

**If update fails or doesn't help:**
```
→ Escalate to communications software specialist
```

---

## ESCALATION CRITERIA

**Escalate to Level 2 Communications Specialist if:**
- [ ] Power present but hardware diagnostics show multiple component failures
- [ ] Physical antenna damage requiring repair
- [ ] Software/firmware issues unresolved by restart or reset
- [ ] Interference issues that cannot be isolated
- [ ] Issue not resolved after 20 minutes of troubleshooting
- [ ] Customer in hazardous situation requiring communications

**Escalate to Emergency Response if:**
- [ ] Ship in immediate danger and needs emergency communications
- [ ] Rescue coordination required
- [ ] Medical emergency requiring communications for assistance

**Escalate to Power Systems if:**
- [ ] Multiple systems offline (not just communications)
- [ ] Power distribution issue identified
- [ ] Circuit breaker repeatedly tripping

---

## WORKAROUNDS & ALTERNATIVES

### Temporary Communication Methods

#### 1. Backup/Emergency Communications
```
- Most ships have emergency comms panels (near airlocks)
- Limited range but functional for distress calls
- Usually on standard emergency frequencies
```

#### 2. Handheld/Portable Units
```
- If ship has portable comm units, can use temporarily
- Limited range (line of sight, typically < 100 km)
- Useful for ship-to-ship or ship-to-station when close
```

#### 3. Optical Communications
```
- If visual contact with another ship/station:
- Use signal lights (many ships have Morse code capability)
- Limited but effective in emergencies
```

#### 4. Message Buoy (if equipped)
```
- Deploy communications relay buoy
- Buoy broadcasts pre-programmed message
- Others can respond via buoy
- Limited functionality but better than nothing
```

#### 5. Route Through Nearby Ship
```
- If another ship nearby with working comms:
- Use backup comms to reach them
- Ask them to relay messages
- Temporary solution until repairs complete
```

---

## PREVENTION & MAINTENANCE

### Regular Maintenance Reduces Comms Failures

**Recommended Schedule:**
1. **Weekly:** Visual inspection of external antenna
2. **Monthly:** Clean antenna contacts and cable connections
3. **Quarterly:** Run full communications diagnostics
4. **Annually:** Firmware updates and configuration backup

### Warning Signs of Impending Failure
- Intermittent reception (comes and goes)
- Increasing static or noise floor
- Reduced transmission range
- Antenna slow to respond to commands
- Frequent software crashes

**If these signs appear:** Schedule preventive maintenance before complete failure.

---

## RELATED DOCUMENTATION

**Troubleshooting Guides:**
- [Top 20 #4: Communications Interference](../quick-reference/top-20-common-issues.md#4-communications-interferencestaticit)
- [Top 20 #18: Encryption Key Failure](../quick-reference/top-20-common-issues.md#18-encryption-key-exchange-failure)
- [Error Codes: Communications](../error-codes/error-codes-communications.md)

**Technical Manuals:**
- [Communications Protocols](../manuals/communications/communications-protocols.md)
- [Signal Processing](../manuals/communications/signal-processing.md)
- [Encryption Systems](../manuals/communications/encryption-systems.md)

**System Dependencies:**
- [System Interaction Matrix](../quick-reference/system-interaction-matrix.md)
- [Power Distribution Manual](../manuals/power/power-distribution-networks.md)

**Help Desk Resources:**
- [Help Desk Index](../quick-reference/HELP-DESK-INDEX.md)
- [Escalation Guide](../quick-reference/escalation-triage-guide.md)
- [First Responder Checklist](../quick-reference/first-responder-checklist.md)

---

## DOCUMENT INFORMATION

**KB Article:** KB-156
**Version:** 1.0
**Last Updated:** Stardate 2438.11
**Author:** Technical Documentation Team
**Applies To:** All ship classes with standard communications systems

**Revision History:**
| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Stardate 2438.11 | Initial publication |

---

**Success Rate:** Following this procedure resolves approximately 70% of complete communications failures at Level 1 support.

**Average Resolution Time:** 20 minutes

**Common Root Causes:**
1. Power distribution issues (30%)
2. Software crash/corruption (25%)
3. Physical antenna damage (20%)
4. Hardware component failure (15%)
5. Configuration errors (10%)
