---
title: "CMPE 120"
# date: 2026-08-13T08:50:01-07:00
draft: true
---

## Computer Organization and Architecture

Welcome to CMPE 120!
We’re so happy to have you in this course.
Many of you have been writing programs for a couple of years now, and they have always run on computer hardware.
The cool part was that you were able to learn how to program without needing to think much about how the hardware executed your code.
But, at some point in your software engineering career, you will be confronted with the fact that some hardware is running your code—and something is going wrong with the way they are interacting.
Not only does it impact your program, but also that of your colleagues!
Oh no!
This course will help demystify why this is happening and how to fix it, turning you into an even stronger software engineer.

<!-- CMPE 120 brings together many of the concepts you learned in CS 46B and CS 146 about theoretical runtime analysis and (for those of you who have already taken it) what you learned in CMPE 102 about assembly language, tying them to how code runs on real systems (where constants matter!).
Similar to how becoming a top Formula 1 driver requires solid knowledge of how a race car works, becoming a top software engineer requires solid knowledge of how a computer works.
Writing high performance code requires understanding the hardware (you have or need) to achieve its goals. -->

Please read the [official course syllabus](https://sjsu.campusconcourse.com/view_syllabus?course_id=94553&public_mode=1) with all the grading information.

## Schedule

The current schedule is tentative and subject to change depending on how the class progresses.
Slides and assignments will be posted in the schedule below.

| Week | Date        | Lecture Topic                                      | Homework         | Suggested Reading |
| ---- | ----------- | -------------------------------------------------- | ---------------- | ----------------- |
| 0    | Thu, Aug 20 | Introduction                                       |                  |                   |
| 1    | Tue, Aug 25 | Intro to C & binary representation                 |                  |                   |
|      | Thu, Aug 27 | More binary representation & overflow              |                  |                   |
| 2    | Tue, Sep 1  | Binary wrap-up & strings                           |                  |                   |
|      | Thu, Sep 3  | Unicode & bitwise operators                        | HW1 out          |                   |
| 3    | Tue, Sep 8  | Intro to memory and pointers                       |                  |                   |
|      | Thu, Sep 10 | Pointers & arrays, dynamic memory allocation       |                  |                   |
| 4    | Tue, Sep 15 | Structs, dynamic data structures (linked lists)    |                  |                   |
|      | Thu, Sep 17 | Intro to ISA & assembly                            | HW1 due; HW2 out |                   |
| 5    | Tue, Sep 22 | Conditional control & gdb                          |                  |                   |
|      | Thu, Sep 24 | Functions in assembly                              |                  |                   |
| 6    | Tue, Sep 29 | The performance equation and Amdahl's Law          |                  |                   |
|      | Thu, Oct 1  | The single cycle processor                         | HW2 due; HW3 out |                   |
| 7    | Tue, Oct 6  | Pipelining & instruction level parallelism         |                  |                   |
|      | Thu, Oct 8  | Pipelining & instruction level parallelism         |                  |                   |
| 8    | Tue, Oct 13 | **MIDTERM EXAM**                                   |                  |                   |
|      | Thu, Oct 15 | Speculation                                        | HW3 due; HW4 out |                   |
| 9    | Tue, Oct 20 | Speculation                                        |                  |                   |
|      | Thu, Oct 22 | Memory hierarchy & caches                          |                  |                   |
| 10   | Tue, Oct 27 | Caches locality and design                         |                  |                   |
|      | Thu, Oct 29 | Caches and your programs                           |                  |                   |
| 11   | Tue, Nov 3  | Virtual memory & paging                            |                  |                   |
|      | Thu, Nov 5  | Virtual memory & paging                            | HW4 due; HW5 out |                   |
| 12   | Tue, Nov 10 | Memory level parallelism (loop unrolling)          |                  |                   |
|      | Thu, Nov 12 | Memory level parallelism (data structure analysis) |                  |                   |
| 13   | Tue, Nov 17 | Multicore, SMT                                     |                  |                   |
|      | Thu, Nov 19 | Superscalar & VLIW architectures                   | HW5 due          |                   |
| 14   | Tue, Nov 24 | SIMD & GPU architectures                           |                  |                   |
|      | Thu, Nov 26 | NO CLASS - Happy Thanksgiving!                     |                  |                   |
| 15   | Tue, Dec 1  | Security (cache side-channel attacks)              |                  |                   |
|      | Thu, Dec 3  | Systolic arrays & hardware-software codesign       |                  |                   |
| 16   | Thu, Dec 10 | **FINAL EXAM - SEC 01**                            |                  |                   |
| 17   | Tue, Dec 15 | **FINAL EXAM - SEC 02**                            |                  |                   |

Many parts of this syllabus are thanks to Leo Porter and Pat Pannuto.

<!-- | Week | Date        | Lecture Topic                                           |
| ---- | ----------- | ------------------------------------------------------- |
|    0 | Thu, Aug 20 | Introduction                                            |
|    1 | Tue, Aug 25 | Intro to C & binary representation                      |
|      | Thu, Aug 27 | More binary representation & overflow                   |
|    2 | Tue, Sep 1  | Binary wrap-up & strings                                |
|      | Thu, Sep 3  | Unicode & bitwise operators                             |
|    3 | Tue, Sep 8  | Intro to memory and pointers                            |
|      | Thu, Sep 10 | Pointers & arrays, dynamic memory allocation            |
|    4 | Tue, Sep 15 | Structs, dynamic data structures (linked lists)         |
|      | Thu, Sep 17 | Intro to ISA & assembly                                 |
|    5 | Tue, Sep 22 | Conditional control & gdb                               |
|      | Thu, Sep 24 | Functions in assembly                                   |
|    6 | Tue, Sep 29 | Memory hierarchy & caches                               |
|      | Thu, Oct 1  | Cache locality                                          |
|    7 | Tue, Oct 6  | Cache memories (associativity)                          |
|      | Thu, Oct 8  | Caches and your programs, measuring performance         |
|    8 | Tue, Oct 13 | **MIDTERM EXAM**                                        |
|      | Thu, Oct 15 | Pipelining & instruction level parallelism              |
|    9 | Tue, Oct 20 | Instruction level parallelism & speculation             |
|      | Thu, Oct 22 | More speculation (branch prediction)                    |
|   10 | Tue, Oct 27 | More speculation (prefetching)                          |
|      | Thu, Oct 29 | Virtual memory & paging                                 |
|   11 | Tue, Nov 3  | Virtual memory & paging                                 |
|      | Thu, Nov 5  | Memory level parallelism (loop unrolling)               |
|   12 | Tue, Nov 10 | More memory level parallelism (data structure analysis) |
|      | Thu, Nov 12 | Multicore, Amdahl's law                                 |
|   13 | Tue, Nov 17 | SMT                                                     |
|      | Thu, Nov 19 | Superscalar & VLIW architectures                        |
|   14 | Tue, Nov 24 | SIMD & GPU architectures                                |
|      | Thu, Nov 26 | NO CLASS - Happy Thanksgiving!                          |
|   15 | Tue, Dec 1  | Security (cache side-channel attacks)                   |
|      | Thu, Dec 3  | Systolic arrays & hardware-software codesign            |
|   16 | Thu, Dec 10 | **FINAL EXAM - SEC 01**                                 |
|   17 | Tue, Dec 15 | **FINAL EXAM - SEC 02**                                 | -->
