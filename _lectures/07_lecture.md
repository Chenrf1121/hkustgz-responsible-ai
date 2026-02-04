---
type: lecture
date: 2025-10-13T10:00:00+8:00
title: Lecture 7 - Responsible Retrieval-Augmented Generation
tldr: "This lecture introduces the RAG framework and examines methods to ensure its reliability, specifically focusing on resolving knowledge conflicts and defending against adversarial poisoning of retrieval sources."
thumbnail: /static_files/presentations/lec.jpg
links:
    - url: /static_files/presentations/lecture_7.pptx
      name: slides
---
**Topics Covered:**
- The Basic RAG Pipeline: Overview of the Indexing, Retrieval, and Generation stages.
- Improving Factuality: Advanced strategies such as Self-RAG and FLARE which use self-reflection and uncertainty-based retrieval to minimize hallucinations.
Knowledge Conflict Resolution: Frameworks like Micro-Act and ASTUTE RAG that allow LLMs to reason through contradictions between their internal memory and retrieved documents.
- Adversarial Robustness: Analyzing vulnerabilities to corpus poisoning (e.g., PoisonedRAG) and backdoor attacks (e.g., AGENTPOISON) that inject malicious text into the knowledge base to manipulate model outputs.
