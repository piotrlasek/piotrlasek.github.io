---
layout: page
title: Blog
permalink: /blog/
---

<ul >
    {% for post in site.posts limit 4 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
        {{ post.content | truncatewords:75}}<br>
            <a href="{{ post.url }}">Read more...</a><br><br>
    {% endfor %}
</ul>


{% for post in paginator.posts %}

	<article class="post">

		{% if post.external-url %}
			<h1>
				<a href="{{ post.external-url }}">{{ post.title }}</a>
				<a class="anchor" href="{{ post.url }}"><i class="icon-anchor"></i></a>
			</h1>
		{% else %}
			<h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
		{% endif %}

		<div class="post-content">{{ post.content }}</div>

	</article>

{% endfor %}


{% if paginator.total_pages > 1 %}
	<div class="postnavigation">

		{% if paginator.previous_page %}
			{% if paginator.page == 2 %}
				<a class="prev left" href="/">&larr; Newer</a>
			{% else %}
				<a class="prev left" href="/page{{paginator.previous_page}}/">&larr; Newer</a>
			{% endif %}
		{% else %}
			<span class="nope left">&larr; Newer</span>
		{% endif %}

		<span class="pages">Page {{ paginator.page }} of {{ paginator.total_pages }}</span>

		{% if paginator.next_page %}
			<a class="next right" href="/page{{paginator.next_page}}/">Older &rarr;</a>
		{% else %}
			<span class="nope right">Older &rarr;</span>
		{% endif %}

	</div>
{% endif %}
