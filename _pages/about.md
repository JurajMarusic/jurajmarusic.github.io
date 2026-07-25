---
permalink: /
title: "**Juraj** Marusic"
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<p class="page__lede">PhD Student in Statistics, Columbia University</p>

{% include base_path %}

<figure class="hero__photo">
  <img src="{{ site.author.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ site.author.name }}" fetchpriority="high" />
  <figcaption class="hero__caption">
    Department of Statistics<br>
    Columbia University<br>
    New York, NY, USA
  </figcaption>
</figure>

<div class="bio">
  <p>I am a third-year PhD student in the Statistics Department at Columbia University, advised by <a href="https://stat.columbia.edu/~cunningham/">John P. Cunningham</a> and <a href="https://sites.google.com/site/marcoavellamedina/home">Marco Avella Medina</a>.</p>

  <p>My work sits at the intersection of formal statistics and machine learning. In Bayesian deep learning, I study how the implicit bias of optimization can take the place of hand-crafted priors over network weights, and how choices such as the learning rate shape the function that training converges to. In robust Bayesian inference, I study how posteriors behave when the data are contaminated or the model is misspecified.</p>

  <p>Before coming to Columbia, I completed Part III of the Mathematical Tripos at the University of Cambridge, and earned my undergraduate degree in mathematics at the University of Zagreb in Croatia.</p>
</div>

{% comment %}
  Written out rather than linked: no mailto, and the address is split so it
  does not read as an address to naive scrapers. Only the domain's dots are
  spelled out, so the local part stays readable.
{% endcomment %}
{% assign email_parts = site.author.email | split: "@" %}
<p class="contact">
  You can reach me at
  <span class="contact__address">{{ email_parts[0] }} [at] {{ email_parts[1] | replace: ".", " [dot] " }}</span>
</p>

{% comment %}
  Google Scholar now sits beside the publications heading, so this row only
  appears once one of the remaining profiles is filled in.
{% endcomment %}
{% if site.author.cv or site.author.github or site.author.linkedin %}
<ul class="hero__links">
  {% if site.author.cv %}<li><a href="{% if site.author.cv contains '://' %}{{ site.author.cv }}{% else %}{{ base_path }}{{ site.author.cv }}{% endif %}"><i class="fas fa-fw fa-file-lines" aria-hidden="true"></i>CV</a></li>{% endif %}
  {% if site.author.github %}<li><a href="https://github.com/{{ site.author.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i>GitHub</a></li>{% endif %}
  {% if site.author.linkedin %}<li><a href="https://www.linkedin.com/in/{{ site.author.linkedin }}"><i class="fab fa-fw fa-linkedin" aria-hidden="true"></i>LinkedIn</a></li>{% endif %}
</ul>
{% endif %}


<section class="section" id="publications">
  <h2 class="section__title">
    Publications
    <span class="section__note">* denotes co-lead author</span>
  </h2>

  {% if site.author.googlescholar %}
    <p class="section__intro">A full list of publications can be found on my <a href="{{ site.author.googlescholar }}">Google Scholar profile</a>.</p>
  {% endif %}

  <ol class="pubs">
    <li class="pub">
      <p class="pub__title">Variational Deep Learning via Implicit Regularization</p>
      <p class="pub__authors">J. Wenger, B. Coker, <span class="me">J. Marusic</span>, and J. P. Cunningham</p>
      <div class="pub__meta">
        <p class="pub__venue">International Conference on Learning Representations (ICLR), 2026</p>
        <p class="pub__links"><a href="https://arxiv.org/abs/2505.20235">arXiv</a></p>
      </div>
    </li>

    <li class="pub">
      <p class="pub__title">Characterizing the Edge of Stability in Variational Training Without Priors</p>
      <p class="pub__authors"><span class="me">J. Marusic</span>*, J. Wenger*, B. Coker, and J. P. Cunningham</p>
      <div class="pub__meta">
        <p class="pub__venue">Preprint, 2026</p>
      </div>
    </li>

    <li class="pub">
      <p class="pub__title">A Theoretical Framework for M-posteriors: Frequentist Guarantees and Robustness Properties</p>
      <p class="pub__authors"><span class="me">J. Marusic</span>, M. Avella-Medina, and C. Rush</p>
      <div class="pub__meta">
        <p class="pub__venue">Preprint, 2025</p>
        <p class="pub__links"><a href="https://arxiv.org/abs/2510.01358">arXiv</a></p>
      </div>
    </li>

    <li class="pub">
      <p class="pub__title">Differentially Private Hyperparameter Tuning using Local Bayesian Optimization</p>
      <p class="pub__authors">G. Sopa*, <span class="me">J. Marusic</span>*, M. Avella-Medina, and J. P. Cunningham</p>
      <div class="pub__meta">
        <p class="pub__venue">Preprint, 2025</p>
        <p class="pub__links"><a href="https://arxiv.org/abs/2502.06044">arXiv</a></p>
      </div>
    </li>
  </ol>
</section>
