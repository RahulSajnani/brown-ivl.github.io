---
layout: base
title: Research
permalink: /research
---

# Research

<div class="search-div">
  <input class="form-control form-control-md" type="text" id="searchInput" onkeyup="searchProjects()" placeholder="Search for a publication or report">
</div>

<div class="row research">
  {% for page in site.data.research %}
    <div class="card research-item">
      <div class="image-div">
          <a href="{{ page.projectPage }}" target="_blank">
            <img src="assets/{{ page.image }}" class="card-img-left img-fluid" alt="{{page.title}}">
          </a>
      </div>
      <div class="card-body">
          <a href="{{ page.projectPage }}" target="_blank">
            <h5 class="card-title research-title"> {{page.title}}</h5>
          </a>
          <h6 class="research-journal">{{page.journal}}</h6>
          <h6 class="card-text research-author">{{page.author}}</h6>
          <h6 class="card-text research-year">{{page.year}}</h6>
      </div>
    </div>
  {% endfor %}
</div>