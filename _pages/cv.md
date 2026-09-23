---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Research Interests
======
**Human-Centric AI Communication**: Building AI that perceives human nuance and truly communicates by integrating Multi-Modal LLMs, Multimodal Emotion Reasoning, and Visual Speech Recognition.

Education
======
* **KAIST**, Daejeon, Korea — Mar. 2023 – Present
  * Ph.D. Candidate in Electrical Engineering
  * Advisor: Prof. Yong Man Ro
  * Integrated Vision Language Lab (IVLLab)
* **Yonsei University**, Seoul, Korea — Feb. 2017 – Feb. 2023
  * B.S. in Electrical and Electronic Engineering

Publications
======
<small>(* denotes equal contribution)</small>

{% assign pubs = site.publications | where_exp: "item", "item.category != 'patents'" | sort: "date" | reverse %}
{% assign prev_year = "" %}
{% for post in pubs %}
{% assign year = post.date | date: "%Y" %}
{% if year != prev_year %}
{% if prev_year != "" %}</ul>{% endif %}
<h3>{{ year }}</h3>
<ul>
{% assign prev_year = year %}
{% endif %}
{% include archive-single-cv.html %}
{% endfor %}
</ul>

Patents
======
<ul>
{% assign pats = site.publications | where: "category", "patents" | sort: "date" | reverse %}
{% for post in pats %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>

Reviewer Activities
======
* International Journal
  * IEEE Transactions on Circuits and Systems for Video Technology (TCSVT)
  * IEEE Transactions on Image Processing (TIP)
* International Conference
  * Association for the Advancement of Artificial Intelligence (AAAI)

Skills
======
* **Programming**: Python, PyTorch
* **Languages**: Korean (Native), English

Awards & Honors
======
* **KAIST Fellowship**, 2024 – Present
* **National Government Fellowship**, 2023 – 2024
