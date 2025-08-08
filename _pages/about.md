---
permalink: /about/
title: "About"
---

<style>
  :root{
    --accent:#ffd447;
    --link:var(--link-color,#00adb5);
    --card:#2a2a2a;
    --muted:#b9c0c4;
    --divider:rgba(255,255,255,0.08);

    /* Timeline geometry (keeps line & dot aligned) */
    --tl-line-x: 14px;  /* distance from timeline's left edge to the vertical line */
    --tl-gap: 24px;     /* spacing from the vertical line to the card content */
    --tl-dot: 10px;     /* diameter of the dot */
  }

  /* Section titles */
  .about-title{
    display:flex;align-items:center;gap:.6rem;
    font-size:1.35rem;margin:0 0 .9rem 0
  }
  .about-title::after{content:"";flex:1;height:1px;background:var(--divider)}
  .b{color:var(--accent)}
  .muted{color:var(--muted)}

  /* Intro card */
  .intro-card{
    background:var(--card);border-radius:12px;padding:1.1rem 1.2rem;
    line-height:1.65;box-shadow:0 4px 12px rgba(0,0,0,.18);margin-bottom:1.6rem
  }
  .intro-card a{color:var(--link)}

  /* Education timeline (aligned like home) */
  .edu-timeline{
    position:relative;
    padding-left:calc(var(--tl-line-x) + var(--tl-gap));
    margin-top:.4rem
  }
  .edu-timeline::before{
    content:"";position:absolute;top:0;bottom:0;width:2px;background:var(--divider);
    left:var(--tl-line-x)
  }
  .edu-item{
    position:relative;background:var(--card);border-radius:12px;
    padding:1rem 1.1rem;margin:0 0 1rem 0;box-shadow:0 4px 12px rgba(0,0,0,.18);
    transition:transform .15s ease, box-shadow .15s ease
  }
  .edu-item:hover{transform:translateY(-2px);box-shadow:0 8px 18px rgba(0,0,0,.25)}
  /* Dot centered on the line */
  .edu-item::before{
    content:"";position:absolute;top:1.05rem;
    width:var(--tl-dot);height:var(--tl-dot);border-radius:50%;
    background:var(--accent);box-shadow:0 0 0 3px rgba(255,212,71,.18);
    left:calc(-0.95 * var(--tl-gap) - (var(--tl-dot) / 2))
  }

  /* Head row: title left, date badge right */
  .edu-head{
    display:flex;justify-content:space-between;align-items:center;margin:0 0 .35rem 0
  }
  .edu-head a{color:var(--link);text-decoration:none}
  .edu-head a:hover{text-decoration:underline}

  .edu-meta{font-style:italic;color:var(--muted);margin-bottom:.4rem}

  .badge{
    display:inline-block;font-weight:700;font-size:.85rem;padding:.15rem .45rem;border-radius:999px;
    background:rgba(255,212,71,.14);color:var(--accent);margin-left:.75rem;white-space:nowrap
  }

  .edu-body{margin-top:.35rem}
  .edu-body p{margin:.4rem 0}
</style>

<!-- Intro / description -->
<div class="intro-card">
  {{ site.description }}
</div>

---

# Education

<div class="edu-timeline">

  <!-- PhD -->
  <div class="edu-item">
    <div class="edu-head">
      <strong>PhD in Computer Science</strong>
      <span class="badge">Mar 2023 – Present</span>
    </div>
    <div class="edu-meta">École Polytechnique, and <a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a> — Palaiseau, France · Belo Horizonte, Brazil</div>
    {% capture phd %}
Studying a formal model for interpreting privacy as resistance to inferences under the supervision of [Catuscia Palamidessi](https://scholar.google.com/citations?user=OOgAyqgAAAAJ&hl=en) and [Mário S. Alvim](https://scholar.google.com.br/citations?user=9r8YfCgAAAAJ&hl=en&oi=ao).
    {% endcapture %}
    <div class="edu-body">
      {{ phd | markdownify }}
    </div>
  </div>

  <!-- MSc -->
  <div class="edu-item">
    <div class="edu-head">
      <strong>MSc in Computer Science</strong>
      <span class="badge">Oct 2020 – Jan 2023</span>
    </div>
    <div class="edu-meta"><a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a> — Belo Horizonte, Brazil</div>
    {% capture msc %}
Thesis defended and approved in January 11, 2023, titled [A Quantitative Information Flow Model for Attribute-Inference Attacks and Utility in Data Releases by Sampling]({% link _publications/2023-01-01-master-thesis.md %}).

Supervised by professor [Mário Sérgio Alvim](https://homepages.dcc.ufmg.br/~msalvim).

Member of the team that executed the PRICE (Privacidade nos Censos Educacionais) project, a cooperation between the Department of Computer Science of UFMG and Inep (Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira). Studied methods to control data disclosure, focused especially on those based in differential privacy. The work [has been used by Inep](https://www.gov.br/inep/pt-br/centrais-de-conteudo/noticias/institucional/nota-de-esclarecimento-divulgacao-dos-microdados) in reviewing privacy policies in the disclosure of official educational census data.

[CAPES](https://www.gov.br/capes/pt-br) scholarship at the [Graduate Program in Computer Science](https://ppgcc.dcc.ufmg.br/en).
    {% endcapture %}
    <div class="edu-body">
      {{ msc | markdownify }}
    </div>
  </div>

  <!-- BSc -->
  <div class="edu-item">
    <div class="edu-head">
      <strong>B.Sc. in Information Systems</strong>
      <span class="badge">Jan 2016 – Jun 2020</span>
    </div>
    <div class="edu-meta"><a href="https://ufmg.br/international-visitors">Universidade Federal de Minas Gerais (UFMG)</a> — Belo Horizonte, Brazil</div>
  </div>

  <!-- Associate -->
  <div class="edu-item">
    <div class="edu-head">
      <strong>Associate's Degree, Information Technology</strong>
      <span class="badge">Jan 2012 – Dec 2015</span>
    </div>
    <div class="edu-meta"><a href="http://funecriacho.contagem.mg.gov.br/">Fundação de Ensino de Contagem - FUNEC</a> — Contagem, Brazil</div>
  </div>

</div>
