# Compiler Bugs in Real-World Development: An Empirical Study

---

## Project summary

Compilers are essential in translating source files written by programmers into machine code, but compiler bugs can cause serious problems. For example,
compilers can compile valid programs to wrong code. Meanwhile, compilers can fail to identify invalid programs and generate machine code whose behaviors are undefined. As these bugs are difficult to detect, they can introduce significant risks to many software projects. As compiler bugs are critical, researchers have conducted various empirical studies to understand compiler bugs. These studies have derived interesting findings about the buggy locations, repair patterns, and causes of compiler bugs.

Compilers have issue trackers to manage bug reports and code repositories to record their revisions. All prior studies analyze compiler bugs from the issue reports. Although the two sources support the analysis from the angle of compiler developers, they are insufficient for the analysis from the angle of programmers, *e.g.*, the users of compilers. First, bug reports do not report the projects that encounter compiler bugs. From bug reports alone, it is infeasible to know whether only large projects (*e.g.*， Linux) can encounter compiler bugs. Second, the bug reports can be polluted by the reports submitted by researchers. Researchers either use random programs or mutated programs to test compilers, but compiler bugs in real development can have other distributions. Finally, bug reports rarely introduce how to bypass compiler bugs. Although the workarounds are useful for understanding the significance of compiler bugs, the prior studies never analyzed compiler bugs from this angle. Due to the above limitations, many questions are still open. For example, how to bypass compiler bugs?

To meet the timely need, we conducted an empirical study on two mainstream compilers such as `gcc` and `llvm`. Instead of bug reports and their patches, in this study, we collect 2,989 commits whose messages mention the bugs or workarounds of two mainstream compilers. We analyze the characteristics of projects that encounter compiler bugs in real development. Among them, we manually inspected 113 commits whose messages explicitly mention the urls of compiler bug reports. As our commits are collected from real development, we can analyze compiler bugs from a new angle. In this study, we explore the following research questions:

---
## Dataset
We collect 2,989 bug reports from 1,355 Github projects, and manually inspected 113 commits whose messages explicitly mention the urls of compiler bug reports. For details, see [all_bugs.txt]() for the whole set; [association.txt]() for manully inspected result of selected bugs.
