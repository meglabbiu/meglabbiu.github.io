---
layout: splash
permalink: /
title: "MEG@BIU"
header:
  overlay_color: "#0f172a"
  overlay_filter: "0.6"
  overlay_image: /assets/images/hero-banner.jpg
  actions:
    - label: "Our Research"
      url: "/research/"
    - label: "Join the Lab"
      url: "/contact/"
excerpt: >
  **Goldstein Lab** — Gonda Brain Research Center, Bar-Ilan University.<br>
  We use electrical and magnetic recordings of brain activity to study how mental processes
  are related to neural mechanisms in typical and clinical populations.

feature_row:
  - title: "Neural Synchrony"
    excerpt: "How effective speakers synchronize brain activity across listeners. We measure alignment as inter-subject correlation of MEG signals during natural speech."
    url: "/research/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - title: "OPM-MEG & Persuasion"
    excerpt: "Investigating neural markers of persuasive speech using next-generation OPM-MEG, with β-burst suppression at event boundaries as the primary measure."
    url: "/research/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - title: "Clinical Populations"
    excerpt: "Neural mechanisms in ASD (oxytocin effects), PTSD (traumatic memory oscillations), and ADHD (high-gamma oscillations) using MEG recordings."
    url: "/research/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row %}

## Latest News
{: .text-center}

{% for post in site.posts limit:5 %}
**{{ post.date | date: "%b %Y" }}** — {{ post.title }}
{: .notice}
{% endfor %}

<div style="text-align: center; margin-top: 1em;">
  <a href="/news/" class="btn btn--primary">All News →</a>
</div>
