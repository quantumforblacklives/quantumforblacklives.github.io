---
layout: page
title: Plans
permalink: /plans/
---
Here is the full list of action plans submitted by folks to this site.
Use these as inspiration to write your own plan and hold each other accountable.
By signing this you also agree to our community <a href="/code-of-conduct/">code of conduct</a>.
> _For more resources and to continue the discussion, <a href="https://join.slack.com/t/quantumforblacklives/shared_invite/zt-ewh0c6s3-2FQvyRi7xjliW6DR5Odgww">join our slack</a>_

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{% if post.title and post.title != "" %}{{post.title}}{% else %}{{post.excerpt |strip_html}}{%endif%}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>

## Submit an action plan

It’s one thing to sign a letter stating your support of a position. It’s another thing to commit to joining campaigns and writing codes of conduct. We can support each other in this. If you think it will be helpful to you in your work, send us a summary of your plan for action, in whatever capacity you are working. We’ll organize a slack channel where we can talk about how things are going and send out email reminders of your commitments in a few months.

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdRL-cd4dja4p_D9_mhDoJM54LGN9kOPLClmpOzi2DaJ2mAXQ/viewform?embedded=true" width="640" height="1700" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
  
----  
### Here are some plans submitted by others:
<div class="posts">
  {% for post in paginator.posts %}
    <article class="post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <h1>{{ post.title }}</h1>

        <div>
          <p class="post_date">{{ post.date | date: "%B %e, %Y" }}</p>
        </div>
      </a>
      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
