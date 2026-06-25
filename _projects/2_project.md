---
layout: page
title: More Coming Soon
description: Reach out for info on our ongoing or unpublished research

importance: 2
category: Research
 
# Research page thumbnail
# Use either thumbnail_image OR thumbnail_video.
# If both are listed, the video will be preferred by the custom project card code.
thumbnail_image: assets/img/projects/tail.jpg
# thumbnail_video: assets/video/projects/dragon-thumbnail.mp4

# Main media on the project page
# Use either main_image OR main_video.
# If both are listed, the video will be shown.
# main_image: assets/img/projects/dragon-pool-pic.jpg
# main_video: assets/video/website video.mp4

# papers:


# videos:
 

# more_info:
#  - title: GitHub
#    url: https://github.com/YOUR-GITHUB-LINK-HERE
---

<div class="project-detail-page">

  {% if page.main_video %}
    <div class="project-main-media">
      <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ page.main_video | relative_url }}" type="video/mp4">
      </video>
    </div>
  {% elsif page.main_image %}
    <div class="project-main-media">
      <img src="{{ page.main_image | relative_url }}" alt="{{ page.title }}">
    </div>
  {% endif %}

  <h2>Overview</h2>

  <p>
    Reach out for information on our ongoing or unpublished research: <p style="color: blue;"> <code> hallrf@merrimack.edu </code> /p>
  </p>

  {% if page.papers %}
    <h2>Papers</h2>

    <ul class="project-link-list">
      {% for paper in page.papers %}
        <li>
          <a href="{{ paper.url }}" target="_blank" rel="noopener noreferrer">
            {{ paper.title }}
          </a>
          {% if paper.venue %}
            <span>{{ paper.venue }}</span>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  {% endif %}

  {% if page.videos %}
    <h2>Videos</h2>

    <ul class="project-link-list">
      {% for video in page.videos %}
        <li>
          <a href="{{ video.url }}" target="_blank" rel="noopener noreferrer">
            {{ video.title }}
          </a>
        </li>
      {% endfor %}
    </ul>
  {% endif %}

  {% if page.more_info %}
    <h2>More Info</h2>

    <ul class="project-link-list">
      {% for item in page.more_info %}
        <li>
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">
            {{ item.title }}
          </a>
        </li>
      {% endfor %}
    </ul>
  {% endif %}

</div>
