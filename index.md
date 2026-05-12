---
layout: default
title: Welcome to My User Manual
---

<div class="text-center py-12">
    <h1 class="text-4xl font-extrabold text-slate-900 mb-6">How to Work with Me</h1>
    <p class="text-xl text-slate-600 mb-10 max-w-2xl mx-auto">
        A guide to my work style, preferences, and how we can collaborate effectively together.
    </p>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-left mt-12">
        {% assign manual_pages = site.pages | where_exp: "item", "item.path contains 'content/drafts/'" | sort: "order" %}
        {% for p in manual_pages %}
        <a href="{{ p.url | relative_url }}" class="block p-6 bg-white rounded-xl border border-slate-200 shadow-sm hover:border-indigo-300 hover:ring-1 hover:ring-indigo-300 transition group">
            <h3 class="text-lg font-bold text-slate-900 group-hover:text-indigo-600 transition">{{ p.title }}</h3>
            <p class="text-slate-500 text-sm mt-2">Section {{ p.order }} of the manual.</p>
        </a>
        {% endfor %}
    </div>
</div>

<div class="mt-20 border-t border-slate-200 pt-12">
    <h2 class="text-2xl font-bold text-slate-900 mb-6">Why this manual?</h2>
    <div class="prose prose-slate max-w-none">
        <p>
            Working together is easier when we understand each other's "API." This manual is my attempt to be transparent about my working style, what I value, and how to get the best out of our relationship.
        </p>
        <p>
            It's a living document, and I'm always open to feedback on how I can be a better teammate.
        </p>
    </div>
</div>
