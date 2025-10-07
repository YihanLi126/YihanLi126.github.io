---
layout: page
title: Iterative MPPI Car Racing
description: Undergraduate Thesis
img: assets/img/project_img/mppi_racing_cover.JPG
importance: 3
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/inhand_background.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

While dexterous manipulation in humans is highly adaptive, which enables tasks despite injuries or impairments, how would robotic hands adapt to scenarios in which they experience an “injury” including full amputations, power losses to certain actuators, and combinations thereof? My research at Robot System Lab aims on building an injury-adaptive in-hand manipulation policy for Allegro hand in the repose task with multimodal perception, in which the robot is asked to reposition the cube on its palm to a different position.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/pipeline.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Pipeline for our injury-adaptive policy.
</div>

We train a teacher-student policy for this task, as shown in Figure 1. The teacher policy is trained with privileged perception, including ground-truth object state and injury state that are unavailable to the student., and a student policy can be distilled using only real-world-available perception information through behavior cloning. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_img/implement_detail.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: Details for teacher policy implementation.
</div>

My work mainly focuses on the teacher policy during RSF. Specifically, 3 types of injuries are implemented for the training setup in IsaacLab, as shown in Figure 2: joint torque loss, joint lock and joint encoder offset, while the injured joints and robot are randomly picked in the environment. The results show that with injury information the teacher policy out performs the base policy without information but becomes harder to get converged. The future works would focus on teacher policy optimization and Sim2Real gap filling.


<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <video class="img-fluid rounded z-depth-1" src="/assets/video/random_joint_torque_loss_base_policy.mp4" autoplay muted loop playsinline controls></video>
    <div class="caption">Base policy rollout with random joint torque loss</div>
  </div>
  <div class="col-sm mt-3 mt-md-0">
    <video class="img-fluid rounded z-depth-1" src="/assets/video/random_joint_torque_loss_injury_policy.mp4" autoplay muted loop playsinline controls></video>
    <div class="caption">Injury-aware policy rollout with random joint torque loss</div>
  </div>
</div>
