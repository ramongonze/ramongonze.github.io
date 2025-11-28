---
permalink: /about/
title: "About"
---

<style>
  :root {
    --accent: #ffd447;
    --muted: #b9c0c4;
    --link: var(--link-color, #00adb5);
  }

  .accent { color: var(--accent); }
  .muted { color: var(--muted); }

  /* Section headings, similar to home */
  .section-title {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    font-size: 1.2rem;
    margin: 1.5rem 0 0.75rem 0;
  }

  .section-title span {
    color: #ffffff;
    font-weight: 600;
  }

  .section-title::after {
    content: "";
    flex: 1;
    height: 1px;
    background: rgba(255, 255, 255, 0.12);
  }

  /* Intro text, like homepage About */
  .intro {
    max-width: 60rem;
    line-height: 1.7;
    font-size: 0.98rem;
  }

  .intro a {
    color: var(--link);
  }

  /* Shared simple list style (like News/Projects/Publications pages) */
  .simple-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .simple-item {
    display: flex;
    gap: 0.6rem;
    padding: 0.35rem 0;
    font-size: 0.95rem;
  }

  .simple-date {
    min-width: 9rem;
    font-variant-numeric: tabular-nums;
    font-size: 0.82rem;
    color: var(--muted);
    flex-shrink: 0;
    margin-top: 0.15rem;
  }

  .simple-main {
    flex: 1;
  }

  .simple-main a {
    color: var(--link);
    text-decoration: none;
  }

  .simple-main a:hover {
    text-decoration: underline;
  }

  .edu-title {
    font-weight: 600;
    margin-bottom: 0.1rem;
  }

  .item-meta {
    font-size: 0.86rem;
    color: var(--muted);
    margin-bottom: 0.25rem;
  }

  .edu-body {
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .edu-body p {
    margin: 0.4rem 0;
  }
</style>

<div class="intro">
  {{ site.description }}
</div>

<h2 class="section-title"><span class="accent">Education</span></h2>

<ul class="simple-list">
  {% capture phd %}
Studying a formal model for interpreting privacy as resistance to inferences under the supervision of [Catuscia Palamidessi](https://scholar.google.com/citations?user=OOgAyqgAAAAJ&hl=en) and [Mário S. Alvim](https://scholar.google.com.br/citations?user=9r8YfCgAAAAJ&hl=en&oi=ao).
  {% endcapture %}

  {% capture msc %}
Thesis defended and approved in January 11, 2023, titled [A Quantitative Information Flow Model for Attribute-Inference Attacks and Utility in Data Releases by Sampling]({% link _publications/2023-01-01-master-thesis.md %}).

Supervised by professor [Mário Sérgio Alvim](https://homepages.dcc.ufmg.br/~msalvim).

Member of the team that executed the PRICE (Privacidade nos Censos Educacionais) project, a cooperation between the Department of Computer Science of UFMG and Inep (Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira). Studied methods to control data disclosure, focused especially on those based in differential privacy. The work [has been used by Inep](https://www.gov.br/inep/pt-br/centrais-de-conteudo/noticias/institucional/nota-de-esclarecimento-divulgacao-dos-microdados) in reviewing privacy policies in the disclosure of official educational census data.

[CAPES](https://www.gov.br/capes/pt-br) scholarship at the [Graduate Program in Computer Science](https://ppgcc.dcc.ufmg.br/en).
  {% endcapture %}

  <!-- PhD -->
  <li class="simple-item">
    <span class="simple-date">Mar 2023 – Present</span>
    <div class="simple-main">
      <div class="edu-title">PhD in Computer Science</div>
      <div class="item-meta">
        École Polytechnique, and
        <a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a>
        — Palaiseau, France · Belo Horizonte, Brazil
      </div>
      <div class="edu-body">
        {{ phd | markdownify }}
      </div>
    </div>
  </li>

  <!-- MSc -->
  <li class="simple-item">
    <span class="simple-date">Oct 2020 – Jan 2023</span>
    <div class="simple-main">
      <div class="edu-title">MSc in Computer Science</div>
      <div class="item-meta">
        <a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a>
        — Belo Horizonte, Brazil
      </div>
      <div class="edu-body">
        {{ msc | markdownify }}
      </div>
    </div>
  </li>

  <!-- BSc -->
  <li class="simple-item">
    <span class="simple-date">Jan 2016 – Jun 2020</span>
    <div class="simple-main">
      <div class="edu-title">B.Sc. in Information Systems</div>
      <div class="item-meta">
        <a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a>
        — Belo Horizonte, Brazil
      </div>
    </div>
  </li>

  <!-- Associate -->
  <li class="simple-item">
    <span class="simple-date">Jan 2012 – Dec 2015</span>
    <div class="simple-main">
      <div class="edu-title">Associate's Degree, Information Technology</div>
      <div class="item-meta">
        <a href="http://funecriacho.contagem.mg.gov.br/">Fundação de Ensino de Contagem - FUNEC</a>
        — Contagem, Brazil
      </div>
    </div>
  </li>
</ul>
