# Problem

## Description
A Samsung Galaxy Tab A8 was deployed as a Paycom kiosk time clock device, but the connection was unstable across multiple network methods.

The device initially worked on guest Wi-Fi after MAC address whitelisting, but it lost connectivity again after a few days. A second attempt using an existing Ethernet connection from a previous Marriott-provided device also worked temporarily before failing.

---

## Symptoms
- Paycom kiosk stopped working after several days
- Device required repeated recovery actions
- Guest Wi-Fi path was not stable for long-term kiosk use
- Ethernet connection later lost internet access
- Device remained physically connected but could not reach the internet

---

## Business Impact
- Employees could not reliably use the tablet to clock in/out
- Manual intervention was required repeatedly
- The kiosk could not be trusted as a stable production device

---

## Initial Hypotheses
Possible causes included:
- Browser session or cookie loss
- Employees accidentally exiting or changing the app
- Captive portal or guest network instability
- Network-level enforcement blocking the device
