---
layout: page
title: Flatener
description: ML approach for flattening the beam
img: assets/img/Flattener.png
importance: 1
category: work-related,
related_publications: true
---

We developed a beam-flattening approach based on a two-stage scattering concept: a pre-scatterer followed by a conical scatterer to broaden and homogenize the transverse dose distribution. The downstream beam shaping is tuned using two orbit correctors and three quadrupoles, which together dominate the controllable degrees of freedom of the system.

To systematize the tuning and reduce operator overhead, we train a machine-learning surrogate model of the beam-shaping response. The model takes as input the quadrupole settings (currents) and a compact description of the measured beam profile. Beam “flatness” is quantified via kurtosis computed over an 8D feature representation of the profile (capturing higher-order shape information beyond simple RMS metrics). Once trained, the surrogate is inverted: we specify the desired flat profile (target kurtosis/features), and the inverse model returns the corresponding corrector and quadrupole currents required to achieve it. This enables closed-loop, data-driven beam flattening with minimal manual iteration.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        CLEAR layout for making the beam flatter
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Actuall devices used
</div>

This work is ongoing and is currently being validated through iterative experimental campaigns. We are refining the feature set and model inversion strategy, expanding the training dataset to improve generalization across operating conditions, and assessing robustness to measurement noise and day-to-day machine drifts. The objective is to converge toward a reliable, operator-ready workflow for repeatable beam flattening with minimal tuning time.

