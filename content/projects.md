---
title: "Projects"
draft: false
---

## FKeras: A Fault Tolerant Library for Understanding NN Resilience
[Workshop][6]

Many scientific applications require neural networks (NNs) to operate correctly in safety-critical or high radiation environments, including automated driving, space, and high energy physics. 
For example, physicists at the Large Hadron Collider want to deploy an autoencoder to filter their experimental data at a high data rate (~40TB/s) in a high radiation environment. 
Thus, the autoencoder hardware must be both efficient and robust.

However, efficiency and robustness are often in conflict with each other.
To address these opposing demands, we must understand the fault tolerance inherent in NNs.
To identify where and why this inherent redundancy exists in a NN, we present [FKeras](https://github.com/KastnerRG/fkeras), an open-source tool that measures the fault tolerance of NNs at the bit level, using various metrics such as the gradient and the Hessian. 
Once we identify which parts of the NN are insensitive to radiation faults, we need not protect them, reducing the resources spent on robust hardware.

## Tailor: Altering Skip Connections for Resource-Efficient Inference
[SLOHA'21][3], [FPGA'23][5], [TRETS][7]

Deep neural networks employ skip connections---identity functions that combine the outputs of different layers---to improve training convergence; however, these skip connections are costly to implement in hardware because they consume valuable resources. 
For certain classification tasks though, a network's skip connections are needed for the network to learn but not necessary for inference after convergence. 
We introduce *Tailor*, a fine-tuning/retraining method that alters skip connections in a fully-trained network to reduce their hardware cost.

## Maximizing Channel Capacity in Time-to-Digital Converters
[FCCM'21][2], [FPGA'23][4]

Side-channel leakage poses a major security threat in multi-tenant environments. 
In FPGA systems, one tenant can instantiate a voltage fluctuation sensor that measures minute changes in the power distribution network and infer information about co-tenant computation and data. 
In this project, we present the *Tunable Dual-Polarity Time-to-Digital Converter*---a voltage fluctuation sensor with three dynamically tunable parameters: the sample duration, sample clock phase, and sample clock frequency. 
The sensor captures both rising and falling transition polarities which provides additional identifiable information about the target computation.

## Evaluating Achievable Latency and Cost: SSD Latency Predictors
[AccML'20][1]

Cutting tail latencies at the millisecond level in internet services to achieve good response times in data-parallel applications is possible by integrating MittOS, an OS/data center interface. 
Typically, MittOS analyzes white-box information of the internals of devices such as SSD's and decides if a given server can "fast reject" a service request. 
But commercial SSD's have a black-box design, so MittOS researchers have developed machine learning models to determine if requests to commercial SSD's can be rejected or not. 
When run on CPUs, however, these models cannot predict in the time it takes an SSD to fully process a request, defeating MittOS's fast-rejecting abilities. 
We demonstrate that ASICs such as the Efficient Inference Engine (EIE) accelerate the prediction times of these MittOS models well within the time it takes an SSD to complete a request at minimal cost, cutting SSD tail latencies. 
EIE achieves 2.01 us inference latency while incurring minimal area costs (20.4 mm^2) and power costs (0.29 W). 
We show that integrating machine learning into the critical path of operating systems becomes cost-efficient and within reason.

[0]: /projects
[1]: /papers/accml_2020.pdf
[2]: https://ieeexplore.ieee.org/abstract/document/9444070 
[3]: https://arxiv.org/abs/2102.01351
[4]: https://dl.acm.org/doi/10.1145/3543622.3573193
[5]: https://dl.acm.org/doi/10.1145/3543622.3573172 
[6]: /papers/radit2023.pdf
[7]: https://dl.acm.org/doi/pdf/10.1145/3624990 
