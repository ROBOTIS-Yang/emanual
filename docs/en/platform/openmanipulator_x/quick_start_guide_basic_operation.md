---
layout: archive
lang: en
ref: openmanipulator_x_quick_start_guide_basic_operation
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/openmanipulator_x/quick_start_guide_basic_operation/
tabs: "ROS"
#tab_title1: Kinetic
tab_title2: Noetic
#tab_title3: Dashing
#tab_title4: Foxy
tab_title5: Humble
tab_title6: Arduino
sidebar:
  title: "OpenMANIPULATOR-X"
  nav: "openmanipulator_x"
product_group: openmanipulator_x
page_number: 5
---

<div style="counter-reset: h1 4"></div>
<div style="counter-reset: h2 1"></div>

{::options parse_block_html="true" /}

<!--[dummy Header 1]>
  <h1 id="quick_start_guide">Quick Start Guide</h1>
  <h2 id="basic_operation_intro">Basic Operation</h2>
  <p class="dummy_content">Showing how to run basic Operation for your OpenMANIPULATOR-X</p>
<![end dummy Header 1]-->

## [Basic Operation](#basic-operation)

Please note that this instruction is written for the **ROBOTIS official OpenMANIPULATOR-X package**. If you are operating a home made OpenMANIPULATOR-X, make sure to configure each DYNAMIXEL as below before operating.

![](/assets/images/platform/openmanipulator_x/OpenManipulator_id_baudrate.png)

**WARNING** The gripper module(ID 15) requires `Current based Position Control Mode`. Please make sure your DYNAMIXEL model supports the required [Operating Mode](https://emanual.robotis.com/docs/en/dxl/x/xm430-w350/#operating-mode11).
{: .notice--danger}

{% capture note_01 %}
`FAQ`
- You can configure your DYNAMIXEL using [DYNAMIXEL Wizard 2.0](/docs/en/software/dynamixel/dynamixel_wizard2/).
- After completing the [Communication Interface](/docs/en/platform/openmanipulator_x/quick_start_guide/#communication-interface) section, use DYNAMIXEL Wizard 2.0 to configure the DYNAMIXEL.
{% endcapture %}
<div class="notice--warning">{{ note_01 | markdownify }}</div>

### [Launch Controller](#launch-controller)

<!-- <section data-id="{{ page.tab_title1 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_kinetic.md %}
</section> -->

<section data-id="{{ page.tab_title2 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_noetic.md %}
</section>

<!-- <section data-id="{{ page.tab_title3 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_dashing.md %}
</section> -->

<!-- <section data-id="{{ page.tab_title4 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_foxy.md %}
</section> -->

<section data-id="{{ page.tab_title5 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_humble.md %}
</section>

<section data-id="{{ page.tab_title6 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/launch_controller_arduino.md %}
</section>

### [Keyboard Teleoperation](#keyboard-teleoperation)

<!-- <section data-id="{{ page.tab_title1 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/keyboard_teleop_kinetic.md %}
</section> -->

<section data-id="{{ page.tab_title2 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/keyboard_teleop_noetic.md %}
</section>

<!-- <section data-id="{{ page.tab_title3 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/keyboard_teleop_dashing.md %}
</section> -->

<!-- <section data-id="{{ page.tab_title4 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/keyboard_teleop_foxy.md %}
</section> -->

<section data-id="{{ page.tab_title5 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/quick_start_guide/keyboard_teleop_humble.md %}
</section>

<section data-id="{{ page.tab_title6 }}" class="tab_contents">
Not supported.
{: .notice--warning}
</section>
