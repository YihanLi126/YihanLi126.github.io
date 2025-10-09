---
layout: page
title: Iterative MPPI Car Racing
description: Undergraduate Thesis
img: assets/img/project_img/mppi_racing_cover.JPG
importance: 3
category: work
---

This project focuses on solving the multimodal problem in sampling-based MPC([MPPI](https://sites.gatech.edu/acds/mppi/), Model Predictive Path Integral Control) in car-racing scenarios. 

We can treat MPPI as a single-step diffusion process. Compared to the basic MPPI version which samples only 1 iteration in every step, applying iterative MPPI which updates the mean value according to the sampling result in last iteration would help avoid local minimum and improve sampling efficiency. However, when there are multiple feasible minimum values, iterative MPPI would suffer from the zig-zag between multimodal solutions in complex environment.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_right.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Right overtake behavior.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_right_traj.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_right_plot1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_right_plot2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: Right overtake rollout data.
</div>

As shown in Figure 1 and Figure 3, the ego vehicle could overtake the obstacles either from the right or left side. Figure 3 shows that the vehicle could get stuck when the intention of overtaking keeps jumping between the left and right.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_left.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3: Left overtake behavior.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_left_traj.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_left_plot1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/iter_overtake_left_plot2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 4: Left overtake rollout data.
</div>

In this project, We propose an iterative MPPI framework with regrouping–resampling that unifies scenario generation,
planning, and control, enabling the algorithm to automatically work out the overtaking tendency of static obstacles in car racing scenarios and bridging the planning process with trajectory generation, and solve the multimodal problem through maintaining a separate mean value and covariance matrix for each intention and pick the optimal solution with minimum efforts, as shown in Figure 5.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/mppi_regroup.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 5: Demonstration of iterative MPPI with regroup policy.
</div>


<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <div class="embed-responsive embed-responsive-4by3">
      <iframe
        class="embed-responsive-item"
        src="/assets/pdf/mppi_racing_report.pdf#view=FitH"
        title="Iterative MPPI Car Racing PDF">
      </iframe>
    </div>
    <div class="caption mt-2">
      Full report.
    </div>
  </div>
</div>
