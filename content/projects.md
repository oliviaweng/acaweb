---
title: "Projects"
draft: true
---

## Current

### Verifying in hardware implementations of cache side-channel mitigation techniques
A great deal of cache side-channel mitigation techniques and designs have been implemented, but little work has gone into verifying that the implementations of these techniques would actually be secure. My research thus focuses on creating a set of experiments that will verify if the given security properties of a protected cache design are actually met in its real-world implementation. We will also develop experiments that will simulate hardware failures to see how these secure cache designs hold up when hardware inevitably fails. 

### Cache compression to mitigate cache side-channel attacks
Cache side channel attacks, which primarily target cloud services like AWS to steal our personal information, pose a great threat to our well-being. Mitigating cache side channel attacks is a uniquely difficult problem because these attacks exploit the fundamental mechanism of what makes a cache fast: storing frequently accessed data. Another difficulty is that previous cache protection measures are expensive, either slowing down a cache's performance or increasing a cache's energy consumption. My research looks into how we can apply *cache compression*, a technique originally designed to increase cache capacity, to obfuscate the cache accesses of vulnerable data while maintaining performance. If we can compress vulnerable cache lines with non-vulnerable cache lines and tie their cache accesses together, the additional cache capacity we gain from cache compression will offset the overhead of our technique. 

## Past

### Evaluating SSD latency predictors
[Tech report][1]

**Abstract.** Cutting tail latencies at the millisecond level in internet services for good response times in data-parallel applications is possible by integrating MittOS, an OS/data center interface. Typically, MittOS analyzes white-box information of the internals of devices such as SSD's and decides if a given server can "fast reject" a service request. But
commercial SSD's have a black-box design, so MittOS researchers have developed machine learning models to determine if requests to commercial SSD’s can be rejected or not. When run on CPUs, however, these models cannot predict in the time it takes an SSD to fully process a request, defeating MittOS's fast-rejecting abilities. We demonstrate that
ASICs such as the Efficient Inference Engine (EIE) accelerate the prediction times of these MittOS models well within the time it takes an SSD to complete a request at minimal cost, cutting SSD tail latencies. EIE achieves 2.01 us inference latency while incurring minimal area costs (20.4 mm^2) and power costs (0.29 W). We show that integrating machine
learning into the critical path of operating systems becomes cost-efficient and within reason.

[1]: https://newtraell.cs.uchicago.edu/files/tr_additional/TR-2019-17.pdf