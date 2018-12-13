---
title: Overview
layout: doc
info: This Mirador 3 Style Guide is intended to document styles and processes related to the design and development of Mirador 3.
nav: false
---

## Style Guide Status

This style guide is currently just a prototype. It's intended for determining the potential value of a style guide for Mirador 3 design and development and how such a style guide might be structured.

Nothing in this style guide is ready for actual use.

## Pattern Status

The table below lists all UI patterns in the style guide and their current development status.

<div id="sg_roadmap">
  <input type="text" class="fluid roadmap_search fuzzy-search" placeholder="Search the patterns"/>
  <div class="table">
    <div class="sg_roadmap_header">
      <div class="tableRow">
        <div class="tableCell"><a href="javascript:void(0)" class="sort" data-sort="maturity">Status</a></div>
        <div class="tableCell"><a href="javascript:void(0)" class="sort" data-sort="header">Pattern Name</a></div>
        <div class="tableCell"><a href="javascript:void(0)" class="sort" data-sort="group">Group</a></div>
        <div class="tableCell"><a href="javascript:void(0)" class="sort" data-sort="styles">Style Location</a></div>
        <div class="tableCell"></div>
      </div>
    </div>
    <div class="list">
    {% assign patterns = site.pages | where: 'type', 'pattern' | sort: 'url' %}
    {% for pattern in patterns %}
    {% assign anchor = pattern.title | slugify | prepend: '#' %}
    {% assign group = pattern.url  | split: '/'  | slice: -2, 1 %}
    {% assign folder = pattern.url | split: '/' | slice: 3, 2 | join: '/' | prepend: '/docs/' | prepend: relative_url | append: '.html' | append: anchor %}
      <a href="{{ relative_url }}{{ folder }}" class="sg_roadmap_pattern tableRow">
        <div class="tableCell">
          <div class="sg_label maturity {{ pattern.maturity }}" data-maturity="{{ pattern.maturity }}"></div>
        </div>
        <div class="tableCell">
          <div class="header">{{ pattern.title }}</div>
        </div>
        <div class="tableCell">
          <div class="group typo_hummingbird">{{ group }}</div>
        </div>
        <div class="tableCell">
          <div class="typo_hummingbird styles">{{ pattern.styles }}</div>
        </div>
        <div class="tableCell">
          <div class="arrow"><i class="icon" data-icon="chevron_right"></i></div>
        </div>
      </a>
    {% endfor %}
    </div>
  </div>
</div>

<script src="{{ site.baseurl }}/styleguide/js/libs/list.min.js"></script>
<script>
  // Create the List
  var options = {
    valueNames: [ 'header', 'group', 'styles', { name: 'maturity', attr: 'data-maturity' } ]
  };
  var roadmap = new List('sg_roadmap', options);
  roadmap.sort("header", {
    order: "asc"
  })
</script>
