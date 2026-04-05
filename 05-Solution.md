# Solution

## Root Cause
The issue was not caused by cookie deletion or kiosk browser misconfiguration.

The tablet was being affected by network design and enforcement decisions across two different paths:
- Guest Wi-Fi was not reliable enough for a persistent kiosk device
- Marriott private network access was later blocked by NAC due to non-compliance

---

## Final Solution
Instead of continuing to force the device into a managed network path it did not need, the connection strategy was changed.

Actions taken:
- Located an alternative switch used for wireless access infrastructure
- Ran a new Ethernet cable to the tablet location
- Worked with Blueprint to enable the required switch port
- Moved the tablet onto a stable internet-only connection path

---

## Why This Worked
The Paycom kiosk only required internet access.

It did not require privileged access to Marriott internal resources, so keeping it on a tightly controlled private network introduced unnecessary risk and instability.

By moving the device to a simpler and more appropriate network path, the kiosk became stable and production-ready.

---

## Outcome
- Stable internet connectivity
- Reliable Paycom kiosk operation
- Reduced recurring troubleshooting effort
- Better fit between device purpose and network design
