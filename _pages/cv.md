---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[Download the PDF version]({{ base_path }}/files/StellaRubini_CV.pdf)

Work experience
======
* **Visiting Scholar** – Sky Computing Lab, UC Berkeley *(2026 – present)*
  * Research on the evaluation of LLM-based and multi-agent systems

* **Data Scientist** – Intesa Sanpaolo *(Sep 2024 – present)*
  * AI Delivery Factory, Generative AI solutions for Human Resources processes
  * Designed evaluation pipelines combining standard and custom metrics to monitor LLM performance and integrate real user feedback
  * Co-developed an LLM-based RAG chatbot for employee support
  * Led experimentation with LLM fine-tuning and multi-agent architectures
  * Built document classification and entity extraction pipelines with OCR and LLMs

* **Advanced Analytics Consultant** – Avvale *(Sep 2021 – Aug 2024)*
  * Data Scientist and Project Lead on AI projects in insurance, energy, and manufacturing
  * Built a multi-agent LLM system for motor insurance document processing
  * Developed a RAG and Knowledge Graph chatbot supporting geologists in drafting technical reports
  * Built computer vision pipelines for georeferenced map generation and real-time paint defect detection

Education
======
* **MSc in Applied Mathematics**, Sapienza University of Rome, 2021
  * 110/110 cum laude, Honors Program
  * Thesis: *Support Vector Machines: Mathematical Methods and Experimental Results*
* **BSc in Mathematics**, Sapienza University of Rome, 2019

Skills
======
* **AI & Data Science:** LLMs, RAG, multi-agent systems, LLM evaluation, NLP, Machine Learning, Deep Learning, Computer Vision
* **Programming:** Python (Transformers, LangChain, AutoGen/AG2, Ragas, Unsloth, Pandas, NumPy, OpenCV), SQL, MATLAB, C
* **Cloud & MLOps:** Microsoft Azure, Docker, Kubernetes, Git

Certifications
======
* Microsoft Certified: Azure AI Engineer Associate, 2023

Languages
======
* Italian (native), English (working proficiency)

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
