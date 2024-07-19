---
layout: post
date: 2024-07-18 15:59:00-0500
inline: true
---

Our research paper, "An Empirical Investigation of Container Building Strategies and Warm Times to Reduce Cold Starts in Scientific Computing Serverless Functions", has been accepted for presentation at the 20th IEEE International Conference on e-Science ([eScience](https://www.escience-conference.org/2024/)). Serverless computing abstracts infrastructure, letting developers focus on code. Yet, "cold start" latency, the cost to deploy environments, can hinder scientific computing with its sporadic demands. Our study tackles this by pre-installing Python packages in container images. Analyzing data from Globus Compute and Binder, we evaluate four container strategies. Pre-installed packages reduce cold start time but need more storage, while dynamic installs save space but add delays. Our simulator shows moderate warm times can cut cold starts without heavy overhead.