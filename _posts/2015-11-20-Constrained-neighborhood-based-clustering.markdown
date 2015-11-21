---
layout: post
title: Constrained neighborhood-based clustering
date: 2015-11-20 13:37 
categories: 
---

![]({{site.url}}/files/constrained-nbc.png)

Cannot-link constraints are pairs of points specified by a user before running a clustering algorithm. Cannot-link pairs of points cannot be assigned by the algorithm to the same cluster.

Must-link constraint are pairs of points that must be assigned to the same cluster.

In the above figure, must-link constraint points are connected by black solid lines, while cannot-link constraint points are "connected" by dashed red lines. There are also special, so-named, deferred points used which are marked with dark gray color if they couldn't have be assigned to any cluster.

Check out if the result is similar to what you would expect.
