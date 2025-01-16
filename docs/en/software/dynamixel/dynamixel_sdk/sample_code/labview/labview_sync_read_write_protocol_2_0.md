---
layout: archive
lang: en
ref: labview_sync_read_write_protocol_2_0
read_time: true
share: true
author_profile: false
permalink: /docs/en/software/dynamixel/dynamixel_sdk/sample_code/labview_sync_read_write_protocol_2_0/
sidebar:
  title: DYNAMIXEL SDK
  nav: "dynamixel_sdk"
---

<style>body {counter-reset: h1 5 !important;}</style>
<div style="counter-reset: h2 22"></div>
<div style="counter-reset: h3 2"></div>

<!--[dummy Header 1]>
  <h1 id="sample-code"><a href="#sample-code">Sample Code</a></h1>
  <h2 id="labview-protocol-20"><a href="#labview-protocol-20">LabVIEW Protocol 2.0</a></h2>
<![end dummy Header 1]-->

### [LabVIEW Sync Read Write Protocol 2.0](#labview-sync-read-write-protocol-20)

- Description

  This example writes goal positions to two DYNAMIXEL's and repeats to read present positions simultaneously until DYNAMIXEL stop moving. The funtions that are related with the Syncread and Syncwrite handle the number of items which are near each other in the Dynamixel control table on multiple DYNAMIXEL's, such as the goal position and the goal velocity.

- Available Dynamixel

  All series using protocol 2.0

- Control Panel

  ![](/assets/images/sw/sdk/dynamixel_sdk/library_setup/labview/windows/sample_code/sync_read_write2/sync_read_write2.png)

- Block Diagram

  ![](/assets/images/sw/sdk/dynamixel_sdk/library_setup/labview/windows/sample_code/sync_read_write2/block_diagram.png)
