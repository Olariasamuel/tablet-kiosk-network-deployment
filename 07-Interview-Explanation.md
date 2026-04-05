# Interview Explanation

## How I Identified It Was a Network Issue

The problem continued even after I changed multiple device-level and application-level settings.

I tested:
- Fully Kiosk Browser configuration
- Android battery and background activity settings
- MAC address whitelisting
- Ethernet connectivity

If the issue had been caused only by the application, I would have expected the behavior to improve after adjusting the kiosk browser and Android system settings.

However, the problem persisted across all of those changes.

That told me the root cause was probably outside the tablet itself.

The biggest clue was that the device was operating on a guest Wi-Fi network with a captive portal. Those networks are designed for temporary guest sessions, not for persistent kiosk devices that must stay authenticated for long periods.

Even after whitelisting the MAC address, the device still experienced instability, which suggested that the network design itself was the limitation.

## My Troubleshooting Logic

I approached the issue by isolating variables:

1. Device settings
2. Application behavior
3. Network authentication method
4. Alternate connection method (Ethernet)

Because the issue remained after changes in steps 1 through 4, I concluded that the problem was network-level rather than app-level.

## What I Would Say in an Interview

I identified it as a network issue because the problem persisted even after I changed the app configuration, Android background settings, and connection method. I also tested MAC whitelisting, which removed part of the captive portal friction but did not fully stabilize the device. That told me the issue was not just the tablet or the browser. Since the device was running on a guest network with a captive portal, I concluded that the root cause was the network design, which was not intended for a persistent kiosk device.
