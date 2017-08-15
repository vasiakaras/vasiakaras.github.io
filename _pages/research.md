---
layout: single
title: "Research Projects"
permalink: /research/
author_profile: true
---

- **[Lift](http://www.lift-project.org)** is a project aiming to achieve _performance portability_ across modern parallel architectures. The _Lift compiler_ transforms a program expressed in the high-level  _Lift programming language_ into optimised low-level OpenCL code. In this transformation optimisations are automatically explored using a set of rewrite rules.
  Lift is open source software available on [GitHub](https://github.com/lift-project/lift).
  Lift has been described in multiple research [publications](/publications-lift/).
  Lift is actively developed by a [research team](http://www.lift-project.org/index.html#team) including currently six PhD students based in Scotland and Germany.

- **[PACXX](http://pacxx.github.io/page/)** allows programming of accelerators with modern C++.
  PACXX is developed by [Michael Haidl](http://www.uni-muenster.de/PVS/en/mitarbeiter/haidl.shtml) at the University of Münster.
  In a series of collaborative [publications](publications#pacxx) we explore [challenges of heterogeneous compiler implementations](/publications/2016/GPGPU-2/) and the [design of modern C++ range-based libraries](/publications/2017/PMAM/) for parallel programming.

- **[GPU Compilation for Interpreted Languages](publications#vee2017)** is the one of the first solutions for compiling a dynamic interpreted programming language -- namely R -- to GPU code.
  The generation of GPU code happens at runtime after crucial information of the program, such as data types, have been observed by profiling.
  [Juan Fumero](http://homepages.inf.ed.ac.uk/s1369892/) has been developed our implementation which is described in our recent [paper](/publications/2017/VEE/).

- **[Marawacc](publications#marawacc)** is a solution for GPU programming from Java.
  Marawacc combines a library interface similar to the stream API from Java 8 and a compiler which generates OpenCL code from Java byte code at runtime.
  Data management optimisations eliminate the overhead of data marshalling.
  Marawacc is described in multiple [publications](publications#marawacc) and has been developed by [Juan Fumero](http://homepages.inf.ed.ac.uk/s1369892/).

- **[SkelCL](https://skelcl.github.io)** is a library providing high-level abstractions to alleviate programming of modern parallel heterogeneous systems comprising of multi-core CPUs and GPUs.
  SkelCL is open source software available on [GitHub](https://github.com/skelcl/skelcl).
  SkelCL has been described in multiple research [publications](publications#skelcl).
  SkelCL is no longer under active development.
