---
layout: post
title:  "Add primary key to existing table in PostgreSQL"
date:   2015-04-15 13:19:06
categories: 
---

{% highlight SQL%}
ALTER TABLE table_name ADD COLUMN id SERIAL PRIMARY KEY;
{% endhighlight %}
