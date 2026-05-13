---
title: "Temporal Specification Oriented Fuzzing for Trigger-Action-Programming Smart Home Integrations"
collection: publications
category: conferences
permalink: /publication/2026-04-15-temporal-specification-oriented-fuzzing
excerpt: "ICSE 2026 Research Track. Equal contribution."
date: 2026-04-15
venue: "The 48th International Conference on Software Engineering (ICSE 2026), Research Track"
venue_short: "ICSE 2026"
authors: "Jinglin Dai<sup>*</sup>, <strong>Yifan Xiong<sup>*</sup></strong>, Lezhi Ma, Shangqing Liu, and Lei Bu"
paperurl: "https://conf.researchr.org/details/icse-2026/icse-2026-research-track/26/Temporal-Specification-Oriented-Fuzzing-for-Trigger-Action-Programming-Smart-Home-Int"
citation: "Jinglin Dai*, <strong>Yifan Xiong</strong>*, Lezhi Ma, Shangqing Liu, and Lei Bu. (2026). &quot;Temporal Specification Oriented Fuzzing for Trigger-Action-Programming Smart Home Integrations.&quot; <i>Proceedings of the 48th International Conference on Software Engineering (ICSE 2026), Research Track</i>. (* equal contribution)"
---

This work studies how to efficiently find temporal specification violations in Trigger-Action Programming (TAP) smart home integrations. Existing model-checking based approaches can formally reason about smart home rules and LTL properties, but their state spaces grow quickly as the number of devices and IFTTT-style rules increases. This makes them difficult to use for large, user-customized home automation scenarios where rule chains can create unexpected or unsafe behaviors.

We propose **HAFuzz**, a fuzzing framework that combines runtime verification with formal temporal specifications. HAFuzz models TAP integrations as finite-state systems, converts LTL properties into monitor automata, and then uses finite execution traces to detect counterexamples. Its key technical idea is a dual-factor distance metric that jointly measures specification proximity and constraint satisfaction, guiding seed selection and mutation toward executions that are more likely to violate the target property.

The work also addresses the lack of diverse LTL benchmarks for smart home systems. We manually construct 180 LTL property seeds and use LLM-based mutation to expand them into a validated benchmark of 1,480 specifications. In experiments, HAFuzz detects the same 1,863 violations as MEDIC on benchmark datasets, while requiring only 0.14% of model checking execution time on average. On large-scale scenarios, it remains effective where MEDIC frequently times out, and the distance-guided strategy is substantially faster than random and LTL-Fuzzer-style seed selection.
