---
layout: home
---

<div class="index-content blog">
    	<div class="section">
	{% if site.alert %}
		<div class="notificationgeneric rednotification">
			<p><i class="fa fa-exclamation-circle" aria-hidden="true"></i>{{ site.alert }}</p>
		</div>
	{% endif %}
	{% if site.alright %}
		<div class="notificationgeneric greennotification">
			<p><i class="fa fa-check-circle" aria-hidden="true"></i>{{ site.alright }}</p>
		</div>
	{% endif %}
	{% if site.warning %}
		<div class="notificationgeneric yellownotification">
			<p><i class="fa fa-exclamation-triangle" aria-hidden="true"></i>{{ site.warning }}</p>
		</div>
	{% endif %}
	{% if site.notification %}
		<div class="notificationgeneric bluenotification">
			<p><i class="fa fa-info-circle" aria-hidden="true"></i>{{ site.notification }}</p>
		</div>
	{% endif %}
        <ul class="artical-cate">
            <li class="on"><a href="/"><span>Blog</span></a></li>
            <li style="text-align:center"><a href="/pages"><span>Pages</span></a></li>
            <li style="text-align:right"><a href="/bulletin"><span>Bulletin</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
          {% for post in site.categories.blog %}
            <li>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <div class="title-desc">{{ post.description }}</div>
            </li>
          {% endfor %}
        </ul>
    </div>
    <div class="aside">
    </div>
</div>
