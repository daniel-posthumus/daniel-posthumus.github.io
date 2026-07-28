---
permalink: /
title: "Daniel Posthumus"
hide_title: true
author_profile: true
classes: wide
redirect_from:
  - /about/
  - /about.html
  - /research/
---

I am a PhD student in Business Economics at Boston University's Questrom School of Business. Before BU, I was a predoctoral research fellow at the Stanford Institute for Economic Policy Research (SIEPR).

My research applies empirical industrial organization methods to questions in urban and environmental economics. I am currently working on projects related to data center siting and fragmentation in local land-use regulation.

Feel free to reach out to me at [danpost@bu.edu](mailto:danpost@bu.edu)!

{% include base_path %}

<style>
  .pub-item { margin: 0 0 1.25rem 0; }
  .pub-title { font-weight: 600; }
  .pub-meta { display: block; }
  details.pub-abstract { margin-top: .35rem; }
  details.pub-abstract > summary { cursor: pointer; }
  .pub-abstract-body { margin-top: .35rem; }
</style>

## Research

{% if author.googlescholar %}
<p>You can also find my work on <a href="{{ author.googlescholar }}" target="_blank" rel="noopener"><u>my Google Scholar profile</u></a>.</p>
{% endif %}

{% assign me = site.author.name | default: "Daniel Posthumus" %}

{% assign peer = site.research | where: "pub_type", "peer_reviewed" | sort: "date" | reverse %}
{% if peer and peer.size > 0 %}
### Peer-Reviewed Publications

{% for pub in peer %}{% include pub-entry-publication.html pub=pub %}{% endfor %}
{% endif %}

{% assign wp = site.research | where: "pub_type", "working_paper" | sort: "date" | reverse %}
{% if wp and wp.size > 0 %}
### Working Papers

{% for pub in wp %}{% include pub-entry-working.html pub=pub me=me %}{% endfor %}
{% endif %}

{% assign other = site.research | where: "pub_type", "other_work" | sort: "date" | reverse %}
{% if other and other.size > 0 %}
### Other Work

{% for pub in other %}{% include pub-entry-publication.html pub=pub %}{% endfor %}
{% endif %}
