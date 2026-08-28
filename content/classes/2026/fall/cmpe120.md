---
title: "CMPE 120"
draft: false
---

## Computer Organization and Architecture

Welcome to CMPE 120!
We’re so happy to have you in this course.
Many of you have been writing programs for a couple of years now, and they have always run on computer hardware.
The cool part was that you were able to learn how to program without needing to think much about how the hardware executed your code.
But, at some point in your software engineering career, you will be confronted with the fact that some hardware is running your code---and _something_ is going wrong with the way they are interacting.
Not only does it impact your program, but also that of your colleagues!
Oh no!
This course will help demystify why this is happening and how to fix it, turning you into an even stronger software engineer.

Please read the [official course syllabus](https://sjsu.campusconcourse.com/view_syllabus?course_id=94553&public_mode=1) with all the grading information.

## Schedule

The current schedule is tentative and subject to change depending on how the class progresses.
Slides and assignments will be posted in the schedule below.
The classes listed as _(async)_ will not be held in-person.
They will instead be posted as recorded lectures on Canvas.

For the suggested reading, we will be using these textbooks:

- [Dive into Systems](https://diveintosystems.org/book/index.html) (DIS)
- [Patterson & Hennesy's Computer Organization and Design RISC-V Edition : The Hardware Software Interface](https://ebookcentral.proquest.com/lib/sjsu/detail.action?docID=7262682&pq-origsite=primo) (P&H) (Note: requires SJSU login / network access)

| Week | Date        | Lecture Topic                                                                                       | Homework         | Suggested Reading                        |
| ---- | ----------- | --------------------------------------------------------------------------------------------------- | ---------------- | ---------------------------------------- |
| 0    | Thu, Aug 20 | Introduction [[blank slides][26]; [sec01 slides][27]; [sec02 slides][28]]                           | [HW0 out][25]    |                                          |
| 1    | Tue, Aug 25 | Intro to C & binary [[blank slides][29]; [slides1][30]; [demo1][31]; [slides2][32]; [demo2][33]]    |                  | [DIS 1.1 - 1.4][0]                       |
|      | Thu, Aug 27 | More binary & overflow [[blank slides][34]; [slides1][35]; [demo1][37]; [slides2][36]; [demo2][38]] | HW0 due          | [DIS 4.1 - 4.5][1]                       |
| 2    | Tue, Sep 1  | Binary wrap-up & strings _(async)_                                                                  |                  | [DIS 1.5][2]                             |
|      | Thu, Sep 3  | Unicode & bitwise operators _(async)_                                                               | HW1 out          | [DIS 4.6][3]                             |
| 3    | Tue, Sep 8  | Intro to memory and pointers                                                                        |                  | [DIS 2.1 - 2.3][4]                       |
|      | Thu, Sep 10 | Pointers & arrays, dynamic memory allocation                                                        |                  | [DIS 2.4 - 2.5][5]                       |
| 4    | Tue, Sep 15 | Structs, dynamic data structures (linked lists)                                                     |                  | [DIS 1.6][6], [DIS 2.7][7]               |
|      | Thu, Sep 17 | Intro to ISA & assembly                                                                             | HW1 due; HW2 out | [P&H 1.1 - 1.3][8], [P & H 2.1 - 2.3][9] |
| 5    | Tue, Sep 22 | Conditional control & gdb; **HW1 quiz**                                                             |                  | [P&H 2.7][10], [DIS 3.1 - 3.2][11]       |
|      | Thu, Sep 24 | More gdb & procedures                                                                               |                  | [P&H 2.8][12]                            |
| 6    | Tue, Sep 29 | The performance equation and Amdahl's Law                                                           |                  | [P&H 1.6 - 1.7][13] [P&H 1.10][14]       |
|      | Thu, Oct 1  | The single cycle processor                                                                          | HW2 due; HW3 out | [P&H 4.1, 4.3 - 4.4][15]                 |
| 7    | Tue, Oct 6  | Pipelining & instruction level parallelism; **HW2 quiz**                                            |                  | [P&H 4.5 - 4.6][16]                      |
|      | Thu, Oct 8  | Pipelining & instruction level parallelism                                                          |                  | [P&H 4.7][17]                            |
| 8    | Tue, Oct 13 | **MIDTERM EXAM**                                                                                    |                  |                                          |
|      | Thu, Oct 15 | Speculation                                                                                         | HW3 due; HW4 out | [P&H 4.8][18]                            |
| 9    | Tue, Oct 20 | Speculation; **HW3 quiz**                                                                           |                  | [P&H 4.10][22]                           |
|      | Thu, Oct 22 | Memory hierarchy & caches                                                                           |                  | [P&H 5.1 - 5.3][19]                      |
| 10   | Tue, Oct 27 | Caches locality and design                                                                          |                  | [P&H 5.4][20]                            |
|      | Thu, Oct 29 | Caches and your programs                                                                            |                  | [P&H 5.4][20]                            |
| 11   | Tue, Nov 3  | Virtual memory & paging                                                                             |                  | [P&H 5.7][21]                            |
|      | Thu, Nov 5  | Virtual memory & paging                                                                             | HW4 due; HW5 out | [P&H 5.7][21]                            |
| 12   | Tue, Nov 10 | Memory level parallelism (loop unrolling); **HW4 quiz**                                             |                  | None                                     |
|      | Thu, Nov 12 | Memory level parallelism (data structure analysis)                                                  |                  | None                                     |
| 13   | Tue, Nov 17 | Superscalar & VLIW architectures                                                                    |                  | None                                     |
|      | Thu, Nov 19 | Multicore, SMT                                                                                      | HW5 due          | [P&H 6.2, 6.4][23]                       |
| 14   | Tue, Nov 24 | Security (cache side-channel attacks)                                                               |                  | None                                     |
|      | Thu, Nov 26 | NO CLASS - Happy Thanksgiving!                                                                      |                  |                                          |
| 15   | Tue, Dec 1  | SIMD & GPU architectures; **HW5 quiz**                                                              |                  | [P&H 6.3, 6.6][24]                       |
|      | Thu, Dec 3  | Systolic arrays & hardware-software codesign                                                        |                  | None                                     |
| 16   | Thu, Dec 10 | **FINAL EXAM - SEC 01**                                                                             |                  |                                          |
| 17   | Tue, Dec 15 | **FINAL EXAM - SEC 02**                                                                             |                  |                                          |

Many parts of this course are thanks to Leo Porter and Pat Pannuto.

[0]: https://diveintosystems.org/book/C1-C_intro/getting_started.html
[1]: https://diveintosystems.org/book/C4-Binary/bases.html
[2]: https://diveintosystems.org/book/C1-C_intro/arrays_strings.html
[3]: https://diveintosystems.org/book/C4-Binary/bitwise.html
[4]: https://diveintosystems.org/book/C2-C_depth/scope_memory.html
[5]: https://diveintosystems.org/book/C2-C_depth/dynamic_memory.html
[6]: https://diveintosystems.org/book/C1-C_intro/structs.html
[7]: https://diveintosystems.org/book/C2-C_depth/structs.html
[8]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=28&c=RVBVQg
[9]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=99&c=RVBVQg
[10]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=124&c=RVBVQg
[11]: https://diveintosystems.org/book/C3-C_debug/gdb.html
[12]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=129&c=RVBVQg
[13]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=55&c=RVBVQg
[14]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=73&c=RVBVQg
[15]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=281&c=RVBVQg
[16]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=301&c=RVBVQg
[17]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=321&c=RVBVQg
[18]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=329&c=RVBVQg
[19]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=390&c=RVBVQg
[20]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=410&c=RVBVQg
[21]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=429&c=RVBVQg
[22]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=340&c=RVBVQg
[23]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=530&c=RVBVQg
[24]: https://ebookcentral.proquest.com/lib/sjsu/reader.action?docID=7262682&ppg=534&c=RVBVQg
[25]: /assignments/2026/fall/cmpe120/hw0.pdf
[26]: /lectures/2026/fall/cmpe120/lecture1-blank.pdf
[27]: /lectures/2026/fall/cmpe120/lecture1-1030-annot.pdf
[28]: /lectures/2026/fall/cmpe120/lecture1-0130-annot.pdf
[29]: /lectures/2026/fall/cmpe120/lecture2-blank.pdf
[30]: /lectures/2026/fall/cmpe120/lecture2-1030-annot.pdf
[31]: /lectures/2026/fall/cmpe120/demo1_s1.c
[32]: /lectures/2026/fall/cmpe120/lecture2-0130-annot.pdf
[33]: /lectures/2026/fall/cmpe120/demo1_s2.c
[34]: /lectures/2026/fall/cmpe120/lecture3-blank.pdf
[35]: /lectures/2026/fall/cmpe120/lecture3-1030-annot.pdf
[36]: /lectures/2026/fall/cmpe120/lecture3-0130-annot.pdf
[37]: /lectures/2026/fall/cmpe120/demo2_s1.c
[38]: /lectures/2026/fall/cmpe120/demo2_s2.c
