---
layout: page
title: Home
---

<div class="home">

  <h1 class="page-heading">{{ site.data.profile.name }}</h1>
  <p>{{ site.data.profile.tagline }}</p>
  <p>{{ site.data.profile.location }}</p>

  <hr>

  <h2>Experience</h2>
  <ul class="post-list">
    {% for job in site.data.profile.experience %}
      <li>
        <h3>{{ job.title }}</h3>
        <p class="post-meta">{{ job.company }} | {{ job.period }} | {{ job.duration }}</p>
        <p>{{ job.description }}</p>
      </li>
    {% endfor %}
  </ul>

  <hr>

  <h2>Education</h2>
  <ul class="post-list">
    {% for edu in site.data.profile.education %}
      <li>
        <h3>{{ edu.institution }}</h3>
        <p class="post-meta">{{ edu.degree }}, {{ edu.field }} | {{ edu.period }}</p>
      </li>
    {% endfor %}
  </ul>

  <hr>

  <h2>Volunteer Experience</h2>
  <ul class="post-list">
    {% for vol in site.data.profile.volunteer_experience %}
      <li>
        <h3>{{ vol.organization }}</h3>
        <p class="post-meta">{{ vol.role }} | {{ vol.period }}</p>
        <p>{{ vol.description }}</p>
      </li>
    {% endfor %}
  </ul>

</div>
