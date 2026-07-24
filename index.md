---
layout: about
image: /assets/img/groundhog-carleton.jpeg
description: >
  Personal website of Luis M. B. Varona.
hide_description: true
title: Luis M. B. Varona
cover: true
---

<!--author-->

My three favourite courses at MtA thus far have been Political & Cultural Change, Cryptography, and Real Analysis II (although that may change as I head into my final year!). After finishing my undergraduate degree, I plan to pursue graduate studies in computer science and continue researching social networks, graph algorithms, or graph structures more broadly in some form. I hope to eventually end up in a line of work or research related—at least tangentially so—to public policy and/or democratic governance.

My other school-adjacent hobbies/activities include competitive programming and open-source software. Additionally, I have worked on (non-academic) accessibility policy research with the Government of New Brunswick's Accessibility Office, particularly in the education sector. Outside of research and academics, I love cats, reading, travelling, and searching for bears in the woods.

<p style="text-align: center;">
    <img src="{{ '/assets/img/ash-and-yuki.jpeg' | relative_url }}" alt="Ash and Yuki" style="width: 80%;">
    <br>
    <em style="font-size: 1.05em;">Two of my family's cats, Ash (top) and Yuki, both sleeping.</em>
</p>

## Important Milestones

{%- for m in site.data.milestones %}
    {%- assign color_mod = forloop.rindex | modulo: 3 -%}
    {%- if color_mod == 1 -%}
        {%- assign color = "#F32F88" -%}
    {%- elsif color_mod == 2 -%}
        {%- assign color = "mediumorchid" -%}
    {%- else -%}
        {%- assign color = "#5A7AF5" -%}
    {%- endif -%}
    {%- assign rendered = m.text -%}
    {%- if m.links -%}
        {%- for link in m.links -%}
            {%- assign resolved = link.path | relative_url -%}
            {%- assign rendered = rendered | replace: link.placeholder, resolved -%}
        {%- endfor -%}
    {%- endif -%}
    {%- assign rendered = rendered | markdownify | remove: '<p>' | remove: '</p>' -%}
    {%- if m.math -%}
        {%- for expr in m.math -%}
            {%- assign rendered = rendered | replace: expr.placeholder, expr.tex -%}
        {%- endfor -%}
    {%- endif %}
* <span style="color: {{ color }}; font-weight: bold;">({{ m.date }})</span> {{ rendered }}
{%- endfor %}
