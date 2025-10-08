---
layout: page
title: Iterative MPPI Car Racing
description: Undergraduate Thesis
img: assets/img/project_img/mppi_racing_cover.JPG
importance: 3
category: work
---

This project focus on the 

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
    Figure 2: Right overtake data.
</div>

We train a teacher-student policy for this task, as shown in Figure 1. The teacher policy is trained with privileged perception, including ground-truth object state and injury state that are unavailable to the student., and a student policy can be distilled using only real-world-available perception information through behavior cloning. 

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
    Figure 4: Left overtake data.
</div>

My work mainly focuses on the teacher policy during RSF. Specifically, 3 types of injuries are implemented for the training setup in IsaacLab, as shown in Figure 2: joint torque loss, joint lock and joint encoder offset, while the injured joints and robot are randomly picked in the environment. The results show that with injury information the teacher policy out performs the base policy without information but becomes harder to get converged. The future works would focus on teacher policy optimization and Sim2Real gap filling.


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
      Figure 5: Full report (interactive PDF).
    </div>
  </div>
</div>
