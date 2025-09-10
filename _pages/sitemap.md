---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A curated list of pages and content on this site.  
For crawlers, see the [XML version]({{ base_path }}/sitemap.xml).

<h2>Pages</h2>
{%- assign pages_curated = site.pages
  | where_exp: "p", "p.sitemap != false"
  | where_exp: "p", "p.title"
  | reject: "permalink", "/404.html"
  | reject: "url", "/404.html"
  | reject: "title", "Archive Layout with Content"
  | reject: "title", "Posts by Category"
  | reject: "title", "Posts by Collection"
  | reject: "title", "Page Archive"
  | reject: "title", "Posts by Tags"
  | sort: "title" -%}

{%- for post in pages_curated -%}
  {%- include archive-single.html -%}
{%- endfor -%}

{%- comment -%}
  如果你完全沒有寫部落格，可以註解掉「Posts」這段。
{%- endcomment -%}
{%- if site.posts and site.posts.size > 0 -%}
<h2>Posts</h2>
{%- for post in site.posts -%}
  {%- if post.sitemap != false -%}
    {%- include archive-single.html -%}
  {%- endif -%}
{%- endfor -%}
{%- endif -%}

{%- comment -%}
  只列出想要的 collections：publications, talks, teaching, portfolio
{%- endcomment -%}
{%- assign allowed = "publications|talks|teaching|portfolio" -%}
{%- for c in site.collections -%}
  {%- assign label = c.label | downcase -%}
  {%- if allowed contains label and c.output != false -%}
    <h2>{{ c.label }}</h2>
    {%- for doc in c.docs -%}
      {%- if doc.sitemap != false -%}
        {%- include archive-single.html -%}
      {%- endif -%}
    {%- endfor -%}
  {%- endif -%}
{%- endfor -%}
