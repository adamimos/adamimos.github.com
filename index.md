
<ul>
  {% for post in site.posts %}
    
    <h2>{{ post.title }}</h2>
    <sup>{{ post.date | date: "%b %-d, %Y" }}</sup>
      {{ post.excerpt }}
    
  {% endfor %}
</ul>


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
      
      

{% for post in site.posts %}
<li>
	<span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
	<h2 class="post-title">
		<a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
	</h2>
	{{ post.excerpt | strip_html | strip_newlines }}
</li>
{% endfor %}


      

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
