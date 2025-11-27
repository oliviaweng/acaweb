---
title: "Projects"
draft: false
---

## PrioriFI: Efficient Fault Injection for Edge Neural Networks
[ASPLOS'26 (To appear)][0]
As neural networks (NNs) are increasingly used to provide edge intelligence, there is a growing need to make the edge devices that run them robust to faults. 
Edge devices must mitigate the resulting hardware failures to function correctly.
In addition, edge NNs have strict constraints on power, energy, latency, throughput, memory size, and computational resources.
Edge NNs require fundamental changes in model architecture, e.g., quantization and fewer, smaller layers.
PrioriFI is an efficient fault injection (FI) algorithm that evaluates edge NN robustness by ranking NN bits based on their fault sensitivity.
PrioriFI uses the Hessian for the initial weight ranking (provided by our previous work [FKeras][9]).
Then, during an FI campaign, PrioriFI uses the information gained from each FI to focus the campaign on the bits likely to be the next most sensitive.
With PrioriFI, designers can quickly evaluate different NN architectures and co-design fault-tolerant edge NNs.


## AmigoLUT: Scaling Up LUT-based Neural Networks with Ensemble Learning
[FPGA'25][11]

Applications including high-energy physics and cybersecurity require extremely high throughput and low latency neural network inference on FPGAs. 
Lookup Table (LUT)-based NNs like [LogicNets](https://github.com/Xilinx/logicnets) address these constraints by mapping neural networks directly to LUTs, achieving inference latency on the order of nanoseconds.
However, it is difficult to implement larger, more performant LUT-based NNs because LUT resource usage increases exponentially with respect to the number of LUT inputs.
Our work *AmigoLUT* creates ensembles of smaller LUT-based NNs such that they scale up linearly with respect to the number of models to achieve higher accuracy within the resource constraints of an FPGA.

## FKeras: A Sensitivity Analysis Tool for Edge Neural Networks
[JATS'24][9]

Many scientific applications require neural networks (NNs) to operate correctly in safety-critical or high radiation environments, including automated driving, space, and high energy physics. 
For example, physicists at the Large Hadron Collider want to deploy an autoencoder to filter their experimental data at a high data rate (~40TB/s) in a high radiation environment. 
Thus, the autoencoder hardware must be both efficient and robust.

However, efficiency and robustness are often in conflict with each other.
To address these opposing demands, we must understand the fault tolerance inherent in NNs.
To identify where and why this inherent redundancy exists in a NN, we present [FKeras](https://github.com/KastnerRG/fkeras), a fault tolerance library for Keras, which is an open-source tool that measures the fault tolerance of NNs at the bit level, using various metrics such as the gradient and the Hessian. 
Once we identify which parts of the NN are insensitive to radiation faults, we need not protect them, reducing the resources spent on robust hardware.

## Tailor: Altering Skip Connections for Resource-Efficient Inference
[SLOHA'21][3], [FPGA'23][5], [TRETS'24][7]

Deep neural networks employ skip connections---identity functions that combine the outputs of different layers---to improve training convergence; however, these skip connections are costly to implement in hardware because they consume valuable resources. 
For certain classification tasks though, a network's skip connections are needed for the network to learn but not necessary for inference after convergence. 
We introduce *Tailor*, a fine-tuning/retraining method that alters skip connections in a fully-trained network to reduce their hardware cost.

## Pentimento: Data Remanence in Cloud FPGAs
[ASPLOS'24][8]

Remote attackers can recover "FPGA pentimento"---long-removed data belonging to a prior user or proprietary design image on a cloud FPGA. 
Just as a pentimento of a painting can be exposed by infrared imaging, FPGA pentimentos can be exposed by signal timing sensors. 
The data constituting an FPGA pentimento is imprinted on the device through bias temperature instability effects on the underlying transistors. 
Measuring this degradation using a time-to-digital converter allows an attacker to (1) extract proprietary details or keys from an encrypted FPGA design image available on the AWS marketplace and (2) recover information from a previous user of a cloud-FPGA.

## Maximizing Channel Capacity in Time-to-Digital Converters
[FCCM'21][2], [FPGA'23][4], [TRETS'24][10]

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
[4]: https://dl.acm.org/doi/pdf/10.1145/3543622.3573193
[5]: https://dl.acm.org/doi/10.1145/3543622.3573172 
[6]: /papers/radit2023.pdf
[7]: https://dl.acm.org/doi/pdf/10.1145/3624990
[8]: https://dl.acm.org/doi/pdf/10.1145/3620665.3640355 
[9]: https://dl.acm.org/doi/pdf/10.1145/3665334 
[10]: https://dl.acm.org/doi/pdf/10.1145/3666092
[11]: https://dl.acm.org/doi/pdf/10.1145/3706628.3708874