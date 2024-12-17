---
layout: archive
lang: en
ref: openmanipulator_x_ros_controller_experiment
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/openmanipulator_x/ros_controller_experiment/
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
page_number: 9
---

<div style="counter-reset: h1 5"></div>
<div style="counter-reset: h2 3"></div>

{::options parse_block_html="true" /}

<!--[dummy Header 1]>
  <h1 id="controller">Controller</h1>
  <h2 id="experimental">Experimental</h2>
  <p class="dummy_content"> Experimental of OpenMANIPULATOR-X; MoveIt, Gravity Compenstaion and etc</p>
<![end dummy Header 1]-->

## [Experimental](#experimental)

{% if page.tab_title5 != "Humble" %}
**WARNING**  
This section introduces other experimental controllers. These controllers may not fully compatible with OpenMANIPULATOR-X.
{: .notice--warning}
{% endif %}

### [MoveIt!](#moveit)

<!-- <section data-id="{{ page.tab_title1 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/moveit_kinetic.md %}
</section> -->

<section data-id="{{ page.tab_title2 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/moveit_noetic.md %}
</section>

<!-- <section data-id="{{ page.tab_title3 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/moveit_dashing.md %}
</section> -->

<!-- <section data-id="{{ page.tab_title4 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/moveit_dashing.md %}
</section> -->

<section data-id="{{ page.tab_title5 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/moveit_humble.md %}
</section>

<section data-id="{{ page.tab_title6 }}" class="tab_contents">
Not supported
{: .notice--warning}
</section>

### [Gravity Compensation](#gravity-compensation)

<!-- <section data-id="{{ page.tab_title1 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/gravity_compensation_kinetic.md %}
</section> -->

<section data-id="{{ page.tab_title2 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/gravity_compensation_noetic.md %}
</section>

<!-- <section data-id="{{ page.tab_title3 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/gravity_compensation_dashing.md %}
</section> -->

<!-- <section data-id="{{ page.tab_title4 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/gravity_compensation_dashing.md %}
</section> -->

<section data-id="{{ page.tab_title5 }}" class="tab_contents">
{% include en/platform/openmanipulator_x/controller/gravity_compensation_dashing.md %}
</section>

<section data-id="{{ page.tab_title6 }}" class="tab_contents">
Not supported
{: .notice--warning}
</section>
