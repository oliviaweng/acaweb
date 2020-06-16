---
title: "Projects"
draft: false
---

## Evaluating Achievable Latency and Cost: SSD Latency Predictors
[Workshop paper][1]

**Abstract.** Cutting tail latencies at the millisecond level in internet services for good response times in data-parallel applications is possible by integrating MittOS, an OS/data center interface. Typically, MittOS analyzes white-box information of the internals of devices such as SSD's and decides if a given server can "fast reject" a service request. But
commercial SSD's have a black-box design, so MittOS researchers have developed machine learning models to determine if requests to commercial SSD’s can be rejected or not. When run on CPUs, however, these models cannot predict in the time it takes an SSD to fully process a request, defeating MittOS's fast-rejecting abilities. We demonstrate that
ASICs such as the Efficient Inference Engine (EIE) accelerate the prediction times of these MittOS models well within the time it takes an SSD to complete a request at minimal cost, cutting SSD tail latencies. EIE achieves 2.01 us inference latency while incurring minimal area costs (20.4 mm^2) and power costs (0.29 W). We show that integrating machine
learning into the critical path of operating systems becomes cost-efficient and within reason.

[1]: /accml_2020.pdf