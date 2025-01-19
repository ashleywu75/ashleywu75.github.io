---
layout: default
title: Home
---

# Welcome to My Knowledge Base

Here you'll find my notes and insights about programming, machine learning, and technology.

## Featured Article

<article class="post-preview featured">
  <h2>
    <a href="/introduction-to-monte-carlo-tree-search">Understanding Monte Carlo Tree Search (MCTS)</a>
  </h2>
  <p>An in-depth exploration of Monte Carlo Tree Search, its applications, and implementation details. Learn about this powerful decision-making algorithm used in AI systems like AlphaGo.</p>
  <span class="categories">
    Categories: Algorithms, AI, Game Theory
  </span>
</article>

## Latest Articles

{% for post in site.posts %}
  <article class="post-preview">
    <h2>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h2>
    <time datetime="{{ post.date | date_to_xmlschema }}">
      {{ post.date | date: "%B %d, %Y" }}
    </time>
    {% if post.categories %}
    <span class="categories">
      Categories: {{ post.categories | join: ", " }}
    </span>
    {% endif %}
    {% if post.description %}
    <p>{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
