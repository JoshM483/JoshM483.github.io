---
title: "Projects"
permalink: /projects/
layout: splash
---

# Projects

A brief description

## 
A grid of project 'cards' [3 x n]
Cards include:
- Project title
- Icon / url for: working feature and/or git repo
- Brief description/ purpose of project
- Tech used [icon]


<div class="projects-grid">
{% for project in site.projects %}
    <div class="project-card">
        <h3>{{ project.title }}</h3>
        <p>{{ project.content | strip_html | truncate: 150 }}</p>
        <div class="project-tech">
            {% for tech in project.tech %}
                {% if tech == "React" %}
                    <i class="fab fa-react" style="color: #61DAFB;"></i> React
                {% elsif tech == "MongoDB" %}
                    <i class="fas fa-database" style="color: #4DB33D;"></i> MongoDB
                {% elsif tech == "Node.js" %}
                    <i class="fab fa-node-js" style="color: #43853D;"></i> Node.js
                {% elsif tech == "Python" %}
                    <i class="fab fa-python" style="color: #306998;"></i> Python
                {% elsif tech == "HTML" %}
                    <i class="fab fa-html5" style="color: #E34F26;"></i> HTML
                {% elsif tech == "CSS" %}
                    <i class="fab fa-css3-alt" style="color: #1572B6;"></i> CSS
                {% elsif tech == "Docker" %}
                    <i class="fab fa-docker" style="color: #2496ED;"></i> Docker
                {% elsif tech == "GitHub" %}
                    <i class="fab fa-github" style="color: #181717;"></i> GitHub
                {% elsif tech == "SQL" %}
                    <i class="fas fa-database" style="color: #4479A1;"></i> SQL
                {% elsif tech == "Visual Studio" %}
                    <i class="fas fa-code" style="color: #5C2D91;"></i> Visual Studio
                {% elsif tech == "Firebase Hosting" %}
                    <i class="fas fa-fire" style="color: #FFCA28;"></i> Firebase Hosting
                {% elsif tech == "GCP Cloud Functions" %}
                    <i class="fas fa-cloud" style="color: #4285F4;"></i> GCP Cloud Functions
                {% elsif tech == "OpenAI" %}
                    <i class="fas fa-robot" style="color: #A0AABF;"></i> OpenAI
                {% else %}
                    <!-- For unknown techs, assume an image will be sourced -->
                    <img src="/assets/images/icon/test.png" alt="{{ tech }}" style="width:24px; height:24px;"/> {{ tech }}
                {% endif %}
            {% endfor %}
        </div>
        <div class="project-card-links">
            <a href=" {{ project.link }}" target="_blank">Live</a> 
            <span>|</span>
            <a href=" {{ project.repo }}" target="_blank">Github</a>
        </div>
    </div>
{% endfor %}
</div>