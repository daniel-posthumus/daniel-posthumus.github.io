---
layout: single
title: "Writing"
permalink: /writing/
author_profile: true
classes: wide
redirect_from:
  - /public_writing/
---

{% include base_path %}

{% if author.googlescholar %}
<p>You can also find my articles on <u><a href="{{ author.googlescholar }}" target="_blank" rel="noopener">my Google Scholar profile</a></u>.</p>
{% endif %}

<style>
  .pub-item { margin: 0 0 1.25rem 0; }
  .pub-title { font-weight: 600; }
  .pub-meta { display: block; }
</style>

{% assign me = site.author.name | default: "Daniel Posthumus" %}

{% assign policy = site.short_writing | where: "pub_type", "policy" | sort: "order" %}
{% if policy and policy.size > 0 %}
## Policy Briefs

{% for pub in policy %}{% include pub-entry-publication.html pub=pub me=me %}{% endfor %}
{% endif %}

{% assign public = site.short_writing | where: "pub_type", "public" | sort: "order" %}
{% if public and public.size > 0 %}
## Op-Eds

{% for pub in public %}{% include pub-entry-publication.html pub=pub me=me %}{% endfor %}
{% endif %}
