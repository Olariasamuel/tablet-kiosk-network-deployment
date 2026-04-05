# Solution

## Short-Term Fix
- MAC address whitelisting
- Optimized kiosk browser configuration
- Disabled Android restrictions affecting sessions

---

## Limitations
- Issue not fully resolved
- Session resets still occurred intermittently

---

## Root Cause
Captive portal networks are not designed for persistent authenticated devices.

They periodically reset sessions, invalidating authentication tokens.

---

## Proposed Long-Term Solution
- Move device to private VLAN
- Assign static IP address
- Remove dependency on captive portal
- Use wired Ethernet connection if possible

---

## Expected Result
- Stable persistent connection
- No login interruptions
- Enterprise-level reliability
