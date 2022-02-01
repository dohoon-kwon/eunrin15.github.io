---
title: "[React 프로젝트]"
layout: archive
permalink: categories/FastCampus
author_profile: true
sidebar_main: true
---

<!-- 공백이 포함되어 있는 카테고리 이름의 경우 site.categories.['a b c'] 이런식으로! -->

***

해당 프로젝트는 'FastCampus'의 React 강의를 공부하여 해당 내용을 기반으로 작성된 내용 및 후기입니다. 🥰

{% assign posts = site.categories.CSS %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}