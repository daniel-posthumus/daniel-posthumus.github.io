---
permalink: /
title: "Daniel Posthumus"
author_profile: true
classes: wide
redirect_from:
  - /about/
  - /about.html
  - /research/
---

I am currently a pre-doctoral research fellow with Professor Neale Mahoney at the Stanford Institute for Economic Policy Research (SIEPR). I am currently working on projects related to the political economy, housing, and industrial organization (in particular productivity and retail gasoline markets). My CV can be found [here](https://drive.google.com/file/d/1rNDbdbki0cW_wVZ3nc4b5J_w3y-X7vo6/view?usp=sharing).

On a personal note, I love playing tennis, reading, history, watching movies, obsessing over politics, exploring the texture of urban life, and (in true California fashion) cycling.

Feel free to contact me at [danpost@stanford.edu](mailto:danpost@stanford.edu).

{% include base_path %}

{% if author.googlescholar %}
<p>You can also find my work on <a href="{{ author.googlescholar }}" target="_blank" rel="noopener"><u>my Google Scholar profile</u></a>.</p>
{% endif %}

<style>
  .pub-item { margin: 0 0 1.25rem 0; }
  .pub-title { font-weight: 600; }
  .pub-meta { display: block; }
  details.pub-abstract { margin-top: .35rem; }
  details.pub-abstract > summary { cursor: pointer; }
  .pub-abstract-body { margin-top: .35rem; }
</style>

{% assign me = site.author.name | default: "Daniel Posthumus" %}

{% assign peer = site.research | where: "pub_type", "peer_reviewed" | sort: "order" %}
{% if peer and peer.size > 0 %}
## Peer-Reviewed Publications

{% for pub in peer %}{% include pub-entry-publication.html pub=pub %}{% endfor %}
{% endif %}

{% assign wp = site.research | where: "pub_type", "working_paper" | sort: "order" %}
{% if wp and wp.size > 0 %}
## Working Papers and Works-in-Progress

{% for pub in wp %}{% include pub-entry-working.html pub=pub me=me %}{% endfor %}
{% endif %}

{% assign other = site.research | where: "pub_type", "other_work" | sort: "order" %}
{% if other and other.size > 0 %}
## Other Work

{% for pub in other %}{% include pub-entry-publication.html pub=pub %}{% endfor %}
{% endif %}
