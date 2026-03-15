# NI Scope Multirecords Plugin

## Overview

NI Scope Multi-Records Panel allows you to record multiple waveforms based on the trigger setting in the NI-Scope Configuration file.
Only support single instrument session (allow multiple channels, but all must be within one single instrument).

![NI Scope Multi-Records Panel](./picture/Panel1.png)

## How To Use

### Basic Configuration

First, use the normal NI Scope front panel to adjust the desired scope settings and export as .niscopeconfig file (Gear >> Export >> Driver Configuration).

![Export scope config](./picture/Export%20Scope%20Config.png)

Then, use the NI Scope Multi-Records Panel to load the configuration file. Set the desired **Number of Records** to repeat the acquisition. Adjust the **Trigger Position** and **Record Length**,  to overwrite the original settings.

### Change Configuration of **Trigger Position** and **Record Length**

When **Delay Mode** On, the **Trigger Position** will be in seconds to configure the Trigger Delay. When **Delay Mode** Off, the **Trigger Position** will be in percentage to confiugre the Reference Position - proportion of pre-trigger samples vs post-trigger samples.

The unit of **Record Length** can be either percentage or seconds. When **Length Unit** is Percentage, 100% is the original record length. When **Length Unit** is seconds, you can set to any positive value for exact length in time, or set to zero or less to use the original record length.

### Export Records or Stream Records to File

A quick way to export records shown on the graph is by right clicking it >> Export feature of LabVIEW graph to export records into other formats:
![Export records](./picture/Export%20Records%20to%20Files.png)

However, the graph on the panel will only display the latest 10 records of all channels. To ensure all the records are saved, specify the **Stream To File Path** to a new or existing TDMS file.

Following shows an example of the TDMS group and channel names after save records into file:
![TMDS Structure](./picture/TdmsExportStructure.png)

## Software Dependencies

- InstrumentStudio Pro (2025 Q4 or higher)
- NI-SCOPE (2025 Q4 or higher)
- LabVIEW (2025 Q3 or higher)
- [JSONtext by JDP Science](https://www.vipm.io/package/jdp_science_jsontext/) - a VI Package from JKI VIPM

