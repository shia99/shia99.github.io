---
layout: page
title: Home
---

<div class="home">

  <div class="profile">
    <div class="profile-picture">
      <img src="https://via.placeholder.com/150" alt="Profile Picture">
    </div>
    <div class="profile-info">
      <h1 class="page-heading">{{ site.data.profile.name }}</h1>
      <p class="tagline">{{ site.data.profile.tagline }}</p>
      <p class="location">{{ site.data.profile.location }}</p>
      <div class="social-links">
        <!-- Add social links here if available in _data/profile.yml -->
      </div>
    </div>
  </div>

  <hr>

  <div class="section">
    <h2>About Me</h2>
    <p>
      {{ site.data.profile.description | default: "A passionate and creative professional with experience in UX/UI design and biomedical visualization. I am always looking for new challenges and opportunities to learn and grow." }}
    </p>
  </div>

  <hr>

  <div class="section">
    <h2>Skills</h2>
    <ul class="skills-list">
      <!-- Add skills here if available in _data/profile.yml -->
      <li>UX/UI Design</li>
      <li>Biomedical Visualization</li>
      <li>3D Modeling</li>
      <li>Animation</li>
    </ul>
  </div>

  <hr>

  <div class="section">
    <h2>Projects</h2>
    <div class="projects-grid">
      <!-- Add projects here if available in _data/profile.yml -->
      <div class="project-card">
        <h3>Project 1</h3>
        <p>A short description of the project.</p>
      </div>
      <div class="project-card">
        <h3>Project 2</h3>
        <p>A short description of the project.</p>
      </div>
      <div class="project-card">
        <h3>Project 3</h3>
        <p>A short description of the project.</p>
      </div>
    </div>
  </div>

  <hr>

  <div class="section">
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
  </div>

  <hr>

  <div class="section">
    <h2>Education</h2>
    <ul class="post-list">
      {% for edu in site.data.profile.education %}
        <li>
          <h3>{{ edu.institution }}</h3>
          <p class="post-meta">{{ edu.degree }}, {{ edu.field }} | {{ edu.period }}</p>
        </li>
      {% endfor %}
    </ul>
  </div>

  <hr>

  <div class="section">
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

  <hr>

  <div class="section">
    <h2>Recommendations</h2>
    <ul class="recommendations-list">
      {% for rec in site.data.profile.recommendations %}
        <li>
          <p>"{{ rec.quote }}"</p>
          <p class="recommendation-author">- {{ rec.author }}</p>
        </li>
      {% endfor %}
    </ul>
  </div>

</div>
