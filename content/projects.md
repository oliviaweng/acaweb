---
title: "Projects"
draft: false
---

## Compressing ResNet33 for Higher Throughput
Residual neural networks like ResNet33 are characterized by their *skip connections*, wherein layers reuse activations from previous layers, in order to circumvent the vanishing gradient problem that occurs during training. After training, these skip connections must remain in the network during inference---otherwise, its accuracy disintegrates. But skip connections introduce a bottleneck during inference because the layers whose activations are reused in future layers must wait for this reuse to occur before accepting new input and continue processing. One solution is to buffer these activations elsewhere, allowing these layers to begin processing inputs as they are received; however, this increases the memory usage of the model. 

Therefore, we propose a new inference model that is mirrors ResNet33 but has no skip connections to alleviate this bottleneck while decreasing memory usage. Using the [knowledge distillation method][2] (or the teacher-student learning method), we replace the residual layers with new layers that do not have any skip connections. These new layers are then trained as "students" that learn from their corresponding residual layers in ResNet33, who are the "teachers," so that they can achieve a comparable accuracy. Without any skip connections, our new model will be able to attain a much higher throughput at the same level of accuracy as its predecessor while maintaining a smaller memory footprint.  

## Evaluating Achievable Latency and Cost: SSD Latency Predictors
[Workshop paper][1]

Cutting tail latencies at the millisecond level in internet services to achieve good response times in data-parallel applications is possible by integrating MittOS, an OS/data center interface. Typically, MittOS analyzes white-box information of the internals of devices such as SSD's and decides if a given server can "fast reject" a service request. But commercial SSD's have a black-box design, so MittOS researchers have developed machine learning models to determine if requests to commercial SSD's can be rejected or not. When run on CPUs, however, these models cannot predict in the time it takes an SSD to fully process a request, defeating MittOS's fast-rejecting abilities. We demonstrate that ASICs such as the Efficient Inference Engine (EIE) accelerate the prediction times of these MittOS models well within the time it takes an SSD to complete a request at minimal cost, cutting SSD tail latencies. EIE achieves 2.01 us inference latency while incurring minimal area costs (20.4 mm^2) and power costs (0.29 W). We show that integrating machine learning into the critical path of operating systems becomes cost-efficient and within reason.

[1]: /accml_2020.pdf
[2]: https://arxiv.org/abs/1912.13179