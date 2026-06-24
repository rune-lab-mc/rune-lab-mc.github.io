---
layout: page
title: DRAGON
description: Flexible vectored underwater vehicle

importance: 1
category: work

# Research page thumbnail
# Use either thumbnail_image OR thumbnail_video.
# If both are listed, the video will be preferred by the custom project card code.
thumbnail_image: assets/img/projects/dragon-pool-pic.jpg
thumbnail_video: assets/video/projects/dragon-thumbnail.mp4

# Main media on the project page
# Use either main_image OR main_video.
# If both are listed, the video will be shown.
main_image: assets/img/projects/dragon-pool-pic.jpg
main_video: assets/img/projects/dragon-main.mp4

papers:
  - title: A Soft Robot for Agile and Efficient Marine Locomotion
    venue: npj Robotics
    url: https://doi.org/10.1038/s44182-026-00089-w
  - title: Untethered Underwater Soft Robot with Thrust Vectoring
    venue: ICRA 2024
    url: https://doi.org/10.1109/ICRA57147.2024.10610430

videos:
  - title: DRAGON 3D
    url: https://youtu.be/J-VXVhMY5ec
  - title: DRAGON 1
    url: https://youtu.be/S9OxFPv63ZI

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
    DRAGON is the first developed flexible fectored underwater vehicle. It is designed by 
    combining a single thruster with a flexible spine, enabling thrust vectoring for rapid and agile 3D motion.
    The project explores soft robotic design, underwater locomotion, and compact actuation for operation in aquatic environments.
  </p>

  {% if page.papers %}
    <h2>Associated Papers</h2>

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
    <h2>Associated Videos</h2>

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
