# Adam's Website

Here is some text 2.


      {% if site.JB.blogroll != false %}
      <section>
        <h2>Blogroll</h2>
        <div class="category">
          <ul>
            {% for link in site.JB.brlist %}
              <li><a href="{{ link.url }}" target="_blank">{{ link.text }}</a></li>
            {% endfor %}
          </ul>
        </div>
      </section>
      {% endif %}
      
      
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
