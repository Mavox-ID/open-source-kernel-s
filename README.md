# Open Source Kernel's (OSK)

> A family of open kernels for OS and various systems, mainly ARM and ARMv7 for calculators, is always with you: OSK - Open Source Kernel's!

Welcome to the central hub of the **OSK Ecosystem**. OSK is an open-source umbrella project and design family dedicated to low-level systems engineering, custom microkernels, monolithic operating system kernels, and bare-metal environments. 

Our primary engineering focus is highly optimized, lightweight architectures—specifically targeting **ARM** and **ARMv7-A/R/M** platforms, embedded hardware, and specific restricted platforms like system-driven engineering calculators.

---

## Ecosystem Architecture & Philosophy

OSK is not just a collection of random codebases; it is a **family unified by standard engineering practices**. Every kernel under the OSK flag follows strict design principles:

1. **Extreme Resource Efficiency:** Optimized for environments with limited RAM (down to kilobytes) and strict storage limits.
2. **Predictable Bare-Metal Execution:** Minimalistic, transparent boot pipelines, custom bootloaders, and structured linker scripts.
3. **Hardware Independence (HAL abstraction):** Decoupling core kernel logic (schedulers, memory managers) from target boards via a strict Hardware Abstraction Layer.
4. **No-Magic Codebase:** Written purely in low-level dialects (Standard C, Assembly) without bloated runtime dependencies.

---

## Target Hardware Focus: ARM & ARMv7 Calculator Systems

Why focus on calculators and deeply embedded ARM platforms? Because restriction breeds pure engineering art. Developing kernels for these platforms poses unique, exciting challenges:

* **MMU & Memory Layouts:** Writing custom memory maps for physical layouts without relying on standard PC BIOS/UEFI.
* **Interfacing:** Writing naked, register-level drivers for custom keyboards, LCD display matrices, and internal bus protocols.
* **Bootloaders:** Bypassing stock vendor restrictions using tailored payload loaders, custom links, and explicit positioning in memory.

Whether you are targeting an single-board microcontroller or an engineering calculator ecosystem, OSK provides the architectural foundation.

---

## The OSK Compliance Standard

To be classified as an official OSK project, a kernel must implement the following unified structure:

```tree
kernel-repo/
├── docs/
│   └── DESIGN.md        <-- Detailed explanation of memory map & scheduling
├── src/
│   ├── arch/            <-- Architecture-dependent assembly (ARM, x86)
│   ├── core/            <-- Pure OS logic (allocators, tasks)
│   └── drivers/         <-- Raw hardware interfaces
├── tools/               <-- Cross-compilation scripts & deployment toolchains
└── build.sh             <-- Standard, clean build pipeline

```

---

## Join the Family (Contribute to the Project)

We're always looking for systems programmers, assembly language enthusiasts, and aspiring programmers who want to create their own kernels.

* **Want to propose your own kernel?** Open an issue with the prefix `[Proposal]`, detailing the architecture, code license, and current upload status. (And include a link to your kernel, which we'll add to our family.)

* **Want to help improve existing kernels?** Check out the individual repositories listed in this repository (Links), find open tasks, and send your suggestions or PRs to the owner!

---

## License & Intellectual Property

All architectural specifications and registry logs in this repository are open source. Individual kernels listed in the registry retain their respective open source licenses (e.g., MIT, GPLv3, or BSD-3-Clause), as explicitly stated in their respective repositories.

The GNU GPL v2 license is also mandatory for inclusion in the project.
