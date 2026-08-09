---
layout: default
title: Predictor
nav: predictor
permalink: /predictor/
container: page
---

<p class="eyebrow">Interactive Interview Predictor</p>

## Predict how many interviews you will get!

Curious how your stats stack up? This tool takes four inputs — CBSE, class rank, externships, and research — and returns a **predicted interview conversion rate** based on a [simple model](https://omfsdata.com/analysis/) (see Section 6) that was trained on the [SDN dataset](https://omfsdata.com/assets/omfs_all.csv). Drag the sliders to enter your stats and watch it update.

First, what “interview conversion” actually means: it’s the share of programs you apply to that send you an interview invite — **invites ÷ applications.** For example, if you apply to 30 programs and 15 invite you, that’s a 50% conversion rate. It is **NOT** your chance of matching, and it’s **NOT** how many interviews you’ll get in total (that depends on how many places you apply).

<iframe src="{{ 'https://omfsdata.com/assets/predictor.html' | relative_url }}" width="100%" height="320"
        frameborder="0" title="Interview-conversion estimator"></iframe>

### More details and disclaimers
* **This tool predicts interviews, not matching.** It cannot tell you your odds of matching — the data that was used to train the model contains only people who matched, so the model has never seen a non-matcher. A low estimate here is not a verdict on your candidacy, and a high one is not a guarantee.
* **The tool is built entirely from success stories.** The model was fit to 73 applicants who matched and chose to post their stats on SDN. That makes it a description of what conversion looked like **among matchers**, so it is heavily biased. 
* **The model gets more uncertain at the low end of CBSE scores/rank.** Because matchers cluster toward the stronger end of the applicant pool, the model has little data on low scores — so for a CBSE much below the mid-60s it’s extrapolating, and probably reading optimistically. Treat estimates down there as a loose ceiling, not a floor.
* **The real uncertainty of model estimates is wide.** Two applicants with identical stats can land far apart. The range shown is illustrative — read the output as “somewhere in this neighborhood,” never a precise figure.
