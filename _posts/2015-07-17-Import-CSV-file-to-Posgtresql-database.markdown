---
layout: post
title: Import CSV file to Posgtresql database
date: 2015-07-17 13:02 
categories: 
---

{% highlight bash %}
\copy <table_name> from '</full/path/to/csv/file>' DELIMITER '<delimiter>' CSV;
{% endhighlight %}
