---
layout: page
title: ASAN vs Valgrind 
description: By comparing ASan and Valgrind, we aim to evaluate their practicality ,providing insights for developers to make informed decisions about suitable security mechanisms for their work.
img: assets/img/OS_Project.png
importance: 4
category: Operating Systems
---

- **Problem Statement**

    The problem we aim to address in this project is the **prevalent occurrence of memory bugs in operating systems** and the need for effective security mechanisms to mitigate them. These bugs can be exploited by attackers to gain unauthorized access, execute arbitrary code or cause system crashes, leading to service disruptions and potential data breaches.

    Traditional approaches to ensuring memory safety, such as static analysis and manual code reviews, have limitations in detecting and preventing memory bugs, particularly in large and complex operating system projects. By addressing memory bugs effectively, we can minimize the risks associated with software vulnerabilities and bolster the overall security posture of operating systems.

<!-- 
     ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    --- -->

- **Objective** 

    The objective of this project is to propose and implement a compelling solution that leverages existing security mechanisms to enhance memory safety in an operating system context. [AddressSanitizer (ASan)](https://github.com/google/sanitizers/wiki/AddressSanitizer) and [Valgrind](https://valgrind.org/) are two prominent security mechanisms that aim to enhance memory safety in operating systems.

    By comparing ASan and Valgrind, we aim to evaluate their practicality, benefits and limitations, providing insights for developers and system administrators to make informed decisions about the most suitable security mechanism for their projects.

- **Our specific goals include:**

    1. **Evaluate Performance**: Measure and compare the performance overhead of ASan and Valgrind when integrated into an operating system project. 

    2. **Assess Effectiveness**: Determine the effectiveness of ASan and Valgrind in detecting and mitigating memory bugs commonly found in operating systems. 

    3. **Explore Limitations**: Identify and understand the limitations and challenges associated with ASan and Valgrind in an operating system context. 

    4. **Practicality and Benefits**: Assess the practicality and benefits of integrating ASan and Valgrind into an operating system project.

* **Tools**

    1. **ASan (AddressSanitizer)** 

        ASan (AddressSanitizer) is a runtime tool developed by Google that detects **memory bugs**, such as **buffer overflows** and **use-after-free errors**, in an operating system project. It operates by instrumenting the application's code during runtime, adding checks and metadata to each memory access. During the instrumentation process, ASan replaces the memory allocation and deallocation functions, such as malloc() and free(), with its own versions.

    2. **Valgrind**

        Valgrind is a powerful open-source framework for debugging and profiling applications. It provides a suite of tools that help identify memory leaks, detect memory errors, profile performance, and analyze threading issues in programs. Valgrind operates by dynamically instrumenting the executable and running it in a virtual environment, allowing detailed analysis of memory operations and program behavior. Its ease of use and extensive capabilities make Valgrind a popular choice for developers and software testers seeking to improve the reliability and performance of their applications. 


- **Experimental Setup**

    Benchmark Selection - [Parsec](https://parsec.cs.princeton.edu/overview.htm)
    The experimental setup involved conducting benchmark tests using the Parsec benchmark suite to compare the performance and effectiveness of ASan and Valgrind. **Six out of 10 benchmarks were executed on a Linux operating system.**
    To evaluate ASan and Valgrind, they were compiled and instrumented separately. The Parsec benchmark suites were then executed and relevant metrics such as execution time and memory usage were measured.

    Following benchmarks were used in evaluation:
    * Blackscholes
    * Vips
    * Fluidanimate
    * Streamcluster
    * Raytrace
    * Canneal

- **Results**

    <div class="results">
        <img src="/assets/img/result_OS.png" width="550" height="300">
    </div>

Table summarizes the performance metrics w.r.t. Execution time for each memory sanitizer across the Parsec benchmarks.


- **Bugs**

    **These are the some of the common bugs we are trying to detech using ASan and Valgrind:**

    * Out-of-bound stack access 
    * Memory leaks  
    * Buffer overflows
    * Use-after-free errors
    * Uninitialized memory use
    * Detecting data races



- **Analysis**

    * In the case of the Vips and fluidanimate benchmarks, there is a increase of 121.3% and 208.4% in execution times when using ASan compared to the baseline. This can be attributed to several factors that contribute to the additional time taken by ASan during the memory sanitization process. Since ASan's instrumentation process adds additional instructions and checks to each memory access, an extra computational overhead is introduced. As a result, the Vips and fluidanimate, which involve a large number of memory accesses, experience increased execution time due to the added ASan instrumentation. 

    * When evaluated against Raytrace benchmark, ASan results in the highest time increase, with a staggering 940.6%. It should be noted that Raytrace involves a significant number of floating-point operations and these operations could be time-consuming. ASan's additional checks for each memory access, including those involving floating-point calculations, added to the computational overhead and further increased the execution time. 

    * The performance impact of AddressSanitizer (ASan) on the BlackScholes, Streamcluster and canneal benchmark when compared to other benchmarks is comparatively low. BlackScholes, Stream-cluster and canneal exhibit memory access patterns that align well with ASan's instrumentation and detection mechanisms, resulting in a smaller performance impact.

    * Different benchmarks may have distinct levels of optimization applied, and specific optimizations can help alleviate the performance impact of ASan. The Streamcluster benchmark is more compliant to certain optimizations that mitigate the impact of ASan compared to other benchmarks.

    * ASan and Valgrind are dynamic analysis tools for detecting memory-based errors but have subtle differences in their working. ASan is a specific tool which detects memory errors like buffer overflows, uninitialized reads, etc by adding extra instrumentation to the code. On the other hand, Valgrind is a tool used for various types of analyses including memcheck (detects memory-management related errors primarily in C and C++ programs), Cachegrind (cache profiler), Helgrind (detects data races in multithreaded programs), Massif ( heap profiler), etc. Therefore, ASan is a more specific tool while Valgrind has a variety of debugging and profiling tools. Valgrind has a significantly higher overhead than ASan because of this general purpose nature. Therefore, it slows down the execution by a factor of 5-10. ASan is relatively lighter. Valgrind emulates a virtual machine that executes the program, while ASan inserts runtime checks into the already compiled code. This makes Valgrind more efficient at detecting a range of errors which ASan cannot detect.
