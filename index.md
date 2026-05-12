---
layout: default
title: Home
---

<div class="max-w-6xl mx-auto px-6 py-24">
    <div class="text-center mb-24">
        <span class="text-indigo-600 font-bold uppercase tracking-[0.2em] text-sm mb-4 block">Personal Operating System</span>
        <h1 class="text-6xl md:text-7xl font-extrabold text-slate-900 tracking-tighter mb-8 leading-[1.1]">How to Work <br class="hidden md:block"> with Paul</h1>
        <p class="text-xl md:text-2xl text-slate-500 max-w-3xl mx-auto leading-relaxed font-medium">
            A high-signal guide to my values, communication style, and leadership philosophy—designed for my team and stakeholders.
        </p>
    </div>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        {% assign manual_pages = site.pages | where_exp: "item", "item.path contains 'content/drafts/'" | sort: "order" %}
        {% for p in manual_pages %}
        <a href="{{ p.url | relative_url }}" class="group relative bg-white p-8 rounded-2xl border border-slate-200 shadow-sm hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
            <div class="mb-6 w-12 h-12 bg-slate-50 rounded-xl flex items-center justify-center text-slate-400 group-hover:bg-indigo-50 group-hover:text-indigo-600 transition-colors">
                <span class="text-xl font-black">{{ p.order }}</span>
            </div>
            <h3 class="text-2xl font-bold text-slate-900 group-hover:text-indigo-600 transition-colors mb-4 leading-tight">{{ p.title }}</h3>
            <div class="flex items-center text-indigo-600 font-bold text-sm uppercase tracking-wider opacity-0 group-hover:opacity-100 transition-opacity">
                <span>Read Section</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                </svg>
            </div>
        </a>
        {% endfor %}
    </div>

    <div class="mt-32 pt-20 border-t border-slate-200">
        <div class="max-w-3xl">
            <h2 class="text-4xl font-extrabold text-slate-900 tracking-tight mb-8 uppercase italic">The Core Intent</h2>
            <div class="prose prose-slate prose-xl text-slate-600">
                <p>
                    Working together is more effective when we understand each other's "API." This manual is my attempt to be transparent about my working style, what I value, and how to get the best out of our relationship.
                </p>
                <p>
                    It is rooted in my experience as a <strong>U.S. Marine</strong> and <strong>9-1-1 Dispatcher</strong>—roles that taught me the value of <em>Commander's Intent</em> and <em>Radical Accountability</em>.
                </p>
                <p class="font-bold text-slate-900">
                    This is a living document. I'm always open to feedback on how I can be a better teammate.
                </p>
            </div>
        </div>
    </div>
</div>
