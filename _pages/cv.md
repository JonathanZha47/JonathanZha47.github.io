---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

This page summarizes my academic background and selected research experience. An updated CV will be linked here once it is ready for public sharing.

## Education

- PhD student, Vrije Universiteit Amsterdam.
- M.S. in Computer Science, Northeastern University.
- B.A. in Computer Science and Mathematics, Boston University.

## Research Interests

- Trustworthy AI and safety for agentic systems.
- Memory poisoning and defenses for agent context windows.
- Safety implications of model compression.
- AI-generated content detection and phishing detection.
- LLM evaluation, RAG systems, and agent benchmarks.

## Selected Experience

- Research on memory-poison defense for agentic systems.
- Research on model-compression safety under quantization, pruning, and related efficiency techniques.
- Work on AI-generated text detection, phishing email detection, RAG systems, and mobile-agent benchmarks.
- Earlier work on physics-guided learning for industrial systems.

## Industry Experience

### Software Engineer Intern, ByteDance, Ohayoo

Shenzhen, China · Oct 2020 - Feb 2021

**Aeolus BI Dashboard & Analytics Platform Development**

- Developed a predictive analytics framework using a Mixture-of-Experts model for game advertising ROI optimization, improving prediction accuracy by 10% through distributed PyTorch training.
- Engineered a scalable data pipeline processing 1M+ daily events with Kafka/Spark, reducing ETL latency by 50% while optimizing SQL performance through Redis caching and index optimization.

**Real-Time Game Ads Bids Adjustment Algorithm**

- Built a real-time streaming system ingesting 10,000+ CPM/CTR events with sub-500ms latency, reducing financial exposure by 40% through automated bid adjustment algorithms.
- Implemented anomaly detection with statistical monitoring and automated rollback workflows, reducing pricing errors by 80% while handling 500+ concurrent requests during peak loads.

## Publications

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
