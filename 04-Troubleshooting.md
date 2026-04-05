# Troubleshooting

## Step 1: Guest Wi-Fi Deployment
- Connected the tablet to the hotel guest Wi-Fi
- Coordinated MAC address whitelisting so the device could bypass normal guest access friction
- The device worked temporarily, but disconnected again after a few days

---

## Step 2: Browser / User Behavior Investigation
- Considered whether the browser was losing session state
- Considered whether employees were accidentally moving the tablet out of the intended workflow
- Deployed Fully Kiosk Browser to lock the tablet into kiosk mode

---

## Step 3: Cookie Persistence Validation
- Tested whether browser cookies were being cleared
- Confirmed that cookies persisted in Fully Kiosk Browser
- This made a browser-level explanation less likely

---

## Step 4: Shift to Network Hypothesis
- Since kiosk mode and cookie persistence did not solve the issue, focus shifted from the application layer to the network layer

---

## Step 5: Ethernet Test Using Existing Marriott Line
- Connected the tablet using the Ethernet line previously used by the earlier Marriott-provided device
- The tablet gained internet access and worked for several days
- After approximately six days, the device stopped working again

---

## Step 6: Validate Network State on Tablet
- Installed a network diagnostic tool on the tablet
- Performed a LAN scan while connected to the Marriott private network
- Confirmed visibility of internal lobby devices and local network presence
- Successfully tested internet behavior from the device during troubleshooting

---

## Step 7: Detect NAC Enforcement
- Used the URL `connectivitycheck.gstatic.com` to trigger network behavior
- The device was redirected to a Marriott page indicating NAC enforcement due to non-compliance
- This confirmed that the problem was not simply app failure or cable failure, but network access control blocking the device

---

## Step 8: Redesign the Connection Path
- Determined that the tablet did not need access to Marriott private network resources
- Identified a different switch used for wireless access infrastructure
- Ran a new Ethernet cable from that switch to the tablet location
- Coordinated with Blueprint to enable the switch port

---

## Final Result
- The tablet received stable internet access
- The kiosk became reliable
- The solution avoided unnecessary dependency on the Marriott-managed private network
