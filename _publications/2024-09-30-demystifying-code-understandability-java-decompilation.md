---
title: "Demystifying and Assessing Code Understandability in Java Decompilation"
collection: publications
category: manuscripts
permalink: /publication/2024-09-30-demystifying-code-understandability-java-decompilation
excerpt: "arXiv preprint arXiv:2409.20343. Equal contribution."
date: 2024-09-30
venue: "arXiv preprint arXiv:2409.20343"
venue_short: "Preprint"
authors: "Ruixin Qin<sup>*</sup>, <strong>Yifan Xiong<sup>*</sup></strong>, Yifei Lu, and Minxue Pan"
paperurl: "https://arxiv.org/abs/2409.20343"
citation: "Ruixin Qin*, <strong>Yifan Xiong</strong>*, Yifei Lu, and Minxue Pan. (2024). &quot;Demystifying and Assessing Code Understandability in Java Decompilation.&quot; <i>arXiv preprint arXiv:2409.20343</i>. (* equal contribution)"
---

This work investigates a question that is often overlooked in decompilation research: beyond semantic correctness, how understandable is the code produced by Java decompilers? Since decompilation is mainly used to help developers understand code when source code is unavailable, unreadable output can directly undermine the practical value of a decompiler even when the recovered program is correct.

We conduct the first empirical study on Java decompiled-code understandability. The study combines a stakeholder survey with experiments over 429 Java files from 14 projects and outputs from three Java decompilers. The results show that practitioners value understandability as highly as correctness, and that understandability issues are encountered more frequently than actual decompilation failures. Manual analysis further reveals recurring decompilation patterns that hurt readability, including deeply nested structures, omitted parentheses, excessively long lines, omitted braces, inlined assignments, and numerical literals in expressions.

Based on these findings, we design **Cognitive ComplexityD**, a metric extending Cognitive Complexity with decompilation-specific rules. Compared with existing rule-based and language-model-based metrics, Cognitive ComplexityD better captures relative understandability between original source code and decompiled code. It achieves a macro F1-score of 0.88 on the original annotated dataset and 0.86 on an updated test set, providing a practical basis for automatically identifying understandability problems in decompiler output.
