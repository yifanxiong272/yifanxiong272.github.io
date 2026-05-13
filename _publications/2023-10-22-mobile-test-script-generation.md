---
title: "Mobile Test Script Generation from Natural Language Descriptions"
collection: publications
category: conferences
permalink: /publication/2023-10-22-mobile-test-script-generation
excerpt: "QRS 2023."
date: 2023-10-22
venue: "2023 IEEE 23rd International Conference on Software Quality, Reliability, and Security (QRS)"
venue_short: "QRS 2023"
authors: "Chun Li, <strong>Yifan Xiong</strong>, Zhong Li, Wenhua Yang, and Minxue Pan"
paperurl: "https://doi.org/10.1109/QRS60937.2023.00042"
citation: "Chun Li, <strong>Yifan Xiong</strong>, Zhong Li, Wenhua Yang, and Minxue Pan. (2023). &quot;Mobile Test Script Generation from Natural Language Descriptions.&quot; <i>2023 IEEE 23rd International Conference on Software Quality, Reliability, and Security (QRS)</i>, 348-359."
---

This work explores a more robust way to write mobile GUI tests. Traditional Android test scripts often hard-code widget attributes or screen positions, making them expensive to author and fragile under UI changes. Instead, this paper lets testers describe each intended action in natural language, such as a short test intent, and then automatically translates those intents into executable test events.

We propose **GenDroid**, a test script generation approach that matches natural-language test intents to UI widgets. GenDroid combines SentenceBERT-based semantic similarity with positional features through a random forest classifier, then uses a UI transfer graph built by Droidbot to plan omitted navigation steps between consecutive intents. This path planning module reduces the burden on testers and prevents one failed intent from cascading into failures for later intents.

The evaluation uses PixelHelp and 11 additional open-source Android applications from F-Droid. GenDroid achieves 88.1% intent coverage on the PixelHelp tasks, improving over seq2act by 20.68%. Across 636 intents from all evaluated applications, it reaches 84.4% coverage, and the widget matching module independently achieves 93.7% accuracy. The ablation study shows that path planning is important, improving total intent coverage from 70.3% to 84.4%.
