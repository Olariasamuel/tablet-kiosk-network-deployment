# Troubleshooting

## Step 1: Network Verification
- Confirmed tablet receives IP address
- Verified internet connectivity
- Checked signal strength

---

## Step 2: Captive Portal Behavior
- Used http://neverssl.com to trigger captive portal
- Confirmed network requires periodic authentication

---

## Step 3: MAC Address Whitelisting
- Provided tablet MAC address to Blueprint
- Device bypassed captive portal login screen
- Issue persisted → not root cause

---

## Step 4: Session & Cookies Testing
- Used https://httpbin.org/cookies
- Verified session inconsistency over time

---

## Step 5: Android System Checks
- Disabled battery optimization
- Disabled “Pause app activity if unused”
- Allowed unrestricted background activity

---

## Step 6: Kiosk Configuration
- Configured Fully Kiosk Browser:
  - Single app mode
  - Auto-start URL
  - Persistent session settings

---

## Step 7: Ethernet Testing
- Connected tablet via Ethernet adapter
- Observed connection but still affected by network policies

---

## Step 8: Vendor Coordination
- Contacted Blueprint and Marriott Service Desk
- Identified possible network-level restrictions
- Issue escalated to network team

---

## Key Finding
Problem persisted across:
- Different configurations
- App settings
- Connection methods

→ Indicates network-level limitation, not app issue
