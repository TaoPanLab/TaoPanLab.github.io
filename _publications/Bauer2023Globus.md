---
layout: publication
publication: true
key: Bauer2023Globus
---

## Abstract
We present a unique function-as-a-service (FaaS) dataset capturing the use of the Globus Compute (previously funcX) platform. Globus Compute implements a federated model via which users may deploy endpoints on arbitrary remote computers, from the edge to high performance computing (HPC) cluster, and they may then invoke Python functions on those endpoints via a reliable cloud-hosted service. The dataset covers 31 weeks and includes 2,121,472 task submissions from 252 users executed on 580 remote computing endpoints. It includes \num{277386} registered functions. We describe the dataset and various observations, some that are similar to other FaaS datasets, for example, that 74\% of tasks run for less than 1 second, and some that are unique to Globus Compute, for example, that endpoints are used in different ways and that the majority of functions are related to scientific computing and machine learning. To the best of our knowledge, this dataset represents the first federated FaaS dataset that includes user workloads, distributed computing endpoints, and analysis of registered function bodies. We expect the dataset to be useful for researching FaaS architectures, workload modeling, container warming, and other distributed computing architectures. 

## Data Set
We released the data set at [Zenodo](https://doi.org/10.5281/zenodo.10044780). The dataset was gathered from the Globus Compute platform starting from November 28th, 2022, 00:00:00 UTC (inclusive) until July 3rd, 2023, 00:00:00 UTC (exclusive) and comprises information about
(i) the function invocations, (ii) the functions, and (iii) the endpoints. The UTC timestamps in the function invocation dataset are recorded in nanoseconds allowing fine-grained insights. 