---
layout: default
title: Tags
---

{% for tag in collections.tagList %}

<span>
    <a href="/tags/{{ tag }}"><button class="bg-white hover:bg-amber-500 text-stone-800 font-semibold py-2 px-4 border border-stone-400 rounded-full shadow mr-6 mb-4">
        {{ tag }}
    </button>
    </a>
</span>
{% endfor %}