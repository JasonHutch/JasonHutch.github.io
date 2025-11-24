---
layout: page
title: Projects
icon: fas fa-code-branch
order: 1
---

<div id="post-list">
  {% for post in site.posts %}
    {% if post.tags contains 'work project' or post.tags contains 'school project' %}
    <div class="card post-preview">
      <a href="{{ post.url | relative_url }}">
        <div class="card-body">
          <h1 class="card-title">
            {{ post.title }}
          </h1>

          <div class="card-text post-content">
            <p>
              {{ post.content | markdownify | strip_html | truncate: 200 | escape }}
            </p>
          </div>

          <div class="post-meta text-muted d-flex">
            <div class="mr-auto">
              <!-- posted date -->
              <i class="far fa-calendar fa-fw"></i>
              {% include datetime.html date=post.date %}

              <!-- categories -->
              {% if post.categories.size > 0 %}
                <i class="far fa-folder-open fa-fw"></i>
                <span>
                  {% for category in post.categories %}
                    {{ category }}
                    {%- unless forloop.last -%},{%- endunless -%}
                  {% endfor %}
                </span>
              {% endif %}
            </div>
          </div>
        </div>
      </a>
    </div>
    {% endif %}
  {% endfor %}
</div>
