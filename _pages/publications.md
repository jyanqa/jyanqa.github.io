---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

## Publications

* **[Improving Cross-Domain Named Entity Recognition with Multi-Task Learning and Domain Adaptation](https://aclanthology.org/2022.case-1.11.pdf)**  
  *EMNLP Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE) 2022*

* **[Multilingual Named Entity Recognition for Socio-political Event Data](https://ceur-ws.org/Vol-3180/paper-86.pdf)**  
  *CLEF 2022*

* **[Cross-lingual Transfer Learning for Named Entity Recognition in Historical Texts](https://aclanthology.org/2022.vardial-1.10.pdf)**  
  *COLING Workshop on Computational Approaches to Historical Language Change 2022*

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
