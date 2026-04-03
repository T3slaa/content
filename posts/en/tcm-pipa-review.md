---
id: "tcm-pipa-review"
title: "PIPA Review: Practical IoT Pentest Associate 2026"
author: "gorka-vila-perez"
publishedDate: 2026-04-07
updatedDate: 2026-04-07
image: ""
description: "Review of the Practical IoT Pentest Associate (PIPA) certification from TCM Security, covering the exam structure, content, and personal experience."
categories:
  - "certifications"
draft: false
featured: false
lang: "en"
---

I’ve always been interested in IoT because it basically combines electronics and networking, and this mix is exactly what makes it fun and scary from a security perspective. That’s what pushed me to go for the **Practical IoT Pentest Associate (PIPA)** certification, previously called Practical Junior IoT Tester / PJIT; the name changed, but the content stayed the same.

![PIPA badge from TCM Security](https://api.accredible.com/v1/frontend/credential_website_embed_image/certificate/161911026)

IoT pentesting feels like a “newer” niche compared to classic web/app pentesting, but it’s getting more important every year. More devices get deployed daily, and many of them transmit sensitive data over the internet, often with weak security assumptions. So if you want to get into IoT security, starting with the fundamentals is honestly a good move.

To prepare you for the exam, they provide a course called **Beginner’s Guide to IoT and Hardware Hacking**. It covers:

- Electronics fundamentals: Ohm's Law, Kirchhoff's Voltage/Current Law, Series/Parallel Circuit, Capacitors, Inductors, Diodes, Transistors, Logic Analyzers, UART
- Recon/Enumeration and OSINT: IoT architecture, embedded systems, UART shell, live enumeration
- Firmware extraction/analysis: SPI, inspecting firmware, manual firmware extraction, reverse engineering firmware

You can find most of the topics scattered across blog posts and random tutorials online, but the big advantage here is that everything is **organized in a clean learning path**. It’s easier to follow than hopping between ten different sources. The instructor, Andrew, explains concepts clearly and also gives multiple ways to contact him, which is genuinely helpful if you get stuck. You can take a look at the entire course, which has been published to YouTube, by following the link:

[Beginner's Guide to IoT and Hardware Hacking](https://www.youtube.com/watch?v=j8SqZLr64NA)

- [Electronics (my experience)](#electronics-my-experience)
- [Equipment: optional, but I'd recommend it](#equipment-optional-but-id-recommend-it)
- [The fun part: extracting and inspecting firmware](#the-fun-part-extracting-and-inspecting-firmware)
- [Exam format (important!)](#exam-format-important)
- [Difficulty/prerequisites](#difficultyprerequisites)
- [My overall take](#my-overall-take)

## Electronics (my experience)

The electronics fundamentals are aimed at people with little or no electronics background. I’m an electrical engineer, so this part was mostly revision for me, but honestly, revisiting fundamentals once in a while doesn’t hurt.

## Equipment: optional, but I'd recommend it

Buying the course equipment isn’t mandatory, but I’d still recommend it if you can. Doing things hands-on makes the learning stick way more. Plus, you’ll mess up at least once (I did), and that’s usually when you learn the most.

If you don’t get the equipment, the course can feel a bit like “watching someone else do hardware stuff,” which is still useful… but less engaging. Don’t be lazy, purchase it!

## The fun part: extracting and inspecting firmware

Once you start using the tools, you realize how “easy” it is to extract data from a device (in the course, they use a TP-Link router). Capturing boot logs over **UART** or extracting firmware via **SPI** using jumper wires feels very practical, and it’s exactly the kind of skill that can set you apart when a pentest involves hardware.

## Exam format (important!)

If you’re wondering how the exam works since hardware is involved: the exam focuses mainly on the **Reverse Engineering Firmware** part.

You get access to a VM with **logic analyzer captures** and **pre-extracted firmware**, and your goal is to identify vulnerabilities using **PulseView** and **Ghidra** (both are covered in the course). The exam also provides system context so you understand how the device fits into a bigger IoT setup and what information leaks would actually be sensitive.

You have **4 days total**:

- **First 2 days:** find vulnerabilities in the VM
- **Last 2 days:** write the report

One thing I didn’t expect: I spent **more time writing the report** than doing the actual pentest. If you find the major issues quickly, which might score enough to pass, you can absolutely move to reporting earlier, but be careful: **once you switch to the reporting phase, you can’t go back**. So take detailed notes during the first phase (commands, screenshots, evidence, everything).

To complete the report, they provided a template along with guidelines on the content they expected to see. In my case, I prepared a template just before the exam and customized it to meet their requirements. This allowed me to spend less time on formatting the report and more time writing valuable content.

Tip: I used SysReptor, which is a great tool for writing pentest reports. It has a lot of features that make the process easier, and it’s free for individual use. You can check it out here: [SysReptor](https://docs.sysreptor.com/).

## Difficulty/prerequisites

What influences most people to buy or not buy a certification, aside from the content itself, is the perceived difficulty. I’d call this an **entry-level certification** for hardware hacking / IoT security. No serious prior hardware experience is required.

That said, having basic **Linux comfort** and some **computer science fundamentals** helps a lot, especially during firmware reversing (you’ll see assembly and C code). The good news is: the course covers what you need for the exam, so you don’t have to study extra content unless you want to go deeper long-term.

## My overall take

If you want a structured, beginner-friendly path into **IoT security**, PIPA is a solid starting point. Just don't expect to learn about wireless communication protocols for IoT devices, as the course focuses more on hardware interfaces and firmware analysis. The course is well-made, and the exam is practical and relevant to real-world scenarios. If you’re interested in IoT security, this certification can be a great way to get your feet wet and build confidence in hardware hacking.
