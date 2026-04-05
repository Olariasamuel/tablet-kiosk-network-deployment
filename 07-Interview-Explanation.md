# Interview Explanation

## How I Identified the Real Problem

At first, the tablet was connected through guest Wi-Fi and MAC-whitelisted, but it only worked for a few days before failing again. Because of that, I first checked whether the issue was related to the browser, user interaction, or cookie loss.

I deployed Fully Kiosk Browser to lock the device into kiosk mode and tested cookie persistence. After confirming that cookies were not being cleared, I ruled out the browser as the primary cause.

Next, I tested the Ethernet line that had been used by the previous Marriott-provided device. That also worked temporarily, which showed that the tablet itself could function correctly on Ethernet. But when it failed again, I investigated deeper at the network level.

Using a network diagnostic tool on the tablet, I confirmed that the device could still see internal hosts on the Marriott private network. Then I triggered a connectivity check URL and was redirected to a Marriott NAC enforcement page indicating the device had been blocked for non-compliance.

That was the turning point. It showed me the problem was not the app and not simply physical connectivity. The real issue was that the device was being placed on network paths that were not suitable for its use case.

## My Logic
I isolated the problem step by step:
1. Browser behavior
2. Cookie persistence
3. Ethernet functionality
4. Internal network reachability
5. Internet access control behavior

Once I confirmed the tablet only needed internet access, I stopped trying to force it into the Marriott-managed private network. Instead, I moved it to a more appropriate connection path by running a new Ethernet cable from a different switch and coordinating with Blueprint to open the port.

## What I Would Say in an Interview
I started by testing the most likely explanations, such as browser session loss or accidental user interaction. After locking the device in Fully Kiosk and confirming that cookies were still present, I shifted to the network layer. When Ethernet also failed later, I used network diagnostics and a connectivity check URL to confirm the tablet had been blocked by Marriott NAC for non-compliance. At that point, I recognized the device did not need private network access at all, only internet access, so I redesigned the connection path by running a new cable from a different switch and having the port enabled by the provider. That made the kiosk stable.
