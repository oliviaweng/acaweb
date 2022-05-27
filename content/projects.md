---
title: "Projects"
draft: false
---

## Tailor: Altering Skip Connections for Resource-Efficient Inference
Deep neural networks employ skip connections---identity functions that combine the outputs of different layers---to improve training convergence; however, these skip connections are costly to implement in hardware because they consume valuable resources. 
We argue that, for certain classification tasks, a network's skip connections are needed for the network to learn but not necessary for inference after convergence. We thus introduce *Tailor*, a retraining method that alters skip connections in a fully-trained network to mitigate their hardware cost.

## Maximizing Channel Capacity in Time-to-Digital Converters
Side-channel leakage poses a major security threat in multi-tenant environments. In FPGA systems, one tenant can instantiate a voltage fluctuation sensor that measures minute changes in the power distribution network and infer information about co-tenant computation and data. In this project, we present the *Tunable Dual-Polarity Time-to-Digital Converter*---a voltage fluctuation sensor with three dynamically tunable parameters: the sample duration, sample clock phase, and sample clock frequency. The sensor captures both rising and falling transition polarities which provides additional identifiable information about the target computation.

## Evaluating Achievable Latency and Cost: SSD Latency Predictors
[Workshop paper][1]

Cutting tail latencies at the millisecond level in internet services to achieve good response times in data-parallel applications is possible by integrating MittOS, an OS/data center interface. Typically, MittOS analyzes white-box information of the internals of devices such as SSD's and decides if a given server can "fast reject" a service request. But commercial SSD's have a black-box design, so MittOS researchers have developed machine learning models to determine if requests to commercial SSD's can be rejected or not. When run on CPUs, however, these models cannot predict in the time it takes an SSD to fully process a request, defeating MittOS's fast-rejecting abilities. We demonstrate that ASICs such as the Efficient Inference Engine (EIE) accelerate the prediction times of these MittOS models well within the time it takes an SSD to complete a request at minimal cost, cutting SSD tail latencies. EIE achieves 2.01 us inference latency while incurring minimal area costs (20.4 mm^2) and power costs (0.29 W). We show that integrating machine learning into the critical path of operating systems becomes cost-efficient and within reason.

[1]: /accml_2020.pdf
[2]: https://arxiv.org/abs/1912.13179