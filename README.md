# Ni-Scope-Multirecords-Plugin
## Overview
NI Scope Multi-Records Panel allows you to record multiple waveforms based on the trigger setting in the NI-Scope Configuration file.

![NI Scope Multi-Records Panel](./picture/Panel1.png)

## Tips
Use the NI Scope front panel to adjust the desired settings and export as .niscopeconfig file (Gear >> Export >> Driver Configuration).

![Export scope config](./picture/Export%20Scope%20Config.png)

Then, use the NI Scope Multi-Records Panel to load the configuration file. Set the desired **Number of Records** to repeat the acquisition. Adjust the **Reference Position (%)** and **Crop (%)**,  to overwrite the original settings. 

The **Reference Position** will adjust the proportion of pre-trigger and post-trigger samples in each record. 

The **Crop** will reduce the waveform duration in the ratio against original waveform duration. That means 100% = No waveform cropping. 

## Software Dependencies
- InstrumentStudio Pro (2025 Q4 or higher)
- NI-SCOPE (2025 Q4 or higher)
- LabVIEW (2025 Q4 or higher)