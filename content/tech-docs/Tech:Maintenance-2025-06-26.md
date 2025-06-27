---
title: Tech:Maintenance/2025-06-26
---

## Maintenance Report – June 26, 2025 

**Window:** June 26, 2025 – 19:00 to 21:00 UTC

**Affected Systems:** cloud15, cloud20

**Providers:** FiberState LLC (upstream DC), WikiTide Foundation Technology Team

### Summary 

This maintenance addressed hardware and configuration issues on two compute nodes: *cloud15* and *cloud20*.

FiberState replaced the fans in both servers after it was determined that they were originally fitted with incorrect standard-performance models. These fans were swapped for high-performance versions suitable for the thermal demands of our workloads.

Additionally, our Technology Team restored BIOS settings on *cloud15* following a CMOS battery replacement performed during the June 23 maintenance. The BIOS had reset to factory defaults, and some critical settings (power profile, turbo boost) had not been reapplied at that time.

### Purpose 

* Replace incorrect fan models in *cloud15* and *cloud20* (FiberState)
* Restore BIOS settings on *cloud15* after CMOS reset during June 23 maintenance (WikiTide Foundation)

### Background 

During the June 23 maintenance, the CMOS battery in *cloud15* was replaced after failure. However, BIOS settings reverted to defaults and were not fully restored. This left the node in "Minimal Power" mode with turbo boost disabled, leading to degraded performance.

Separately, it was discovered that both *cloud15* and *cloud20* were using fans that did not meet our necessary requirements. These were physically replaced by FiberState with the correct high-performance models during the June 26 window.

### Work Performed 

**By FiberState (hardware):**
* Replaced standard fans in *cloud15* and *cloud20* with high-performance fan units

**By WikiTide Foundation Technology Team (configuration):**
* On *cloud15*:
   * Restored BIOS power profile to *Maximum Performance*
   * Re-enabled CPU Turbo Boost
   * Verified settings post-reboot

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Maintenance/2025-06-26)**