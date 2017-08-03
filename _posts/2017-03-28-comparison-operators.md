---
published: true
title: Comparison Operators
layout: post
tags: [mongodb, operator]
categories: [mongodb]
---

* **$eq**	Matches values that are equal to a specified value.
* **$gt**	Matches values that are greater than a specified value.
* **$gte**	Matches values that are greater than or equal to a specified value.
* **$lt** Matches values that are less than a specified value.
* **$lte**	Matches values that are less than or equal to a specified value.
* **$ne** Matches all values that are not equal to a specified value.
* **$in**	Matches any of the values specified in an array.
* **$nin**	Matches none of the values specified in an array.

**Examples**
{% highlight bash %}
db.collectionName.find({ runtime: { $gt: 90 } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ runtime: { $gt: 90, $lt: 120 } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ "tomato.meter": { $gte: 95 }, runtime: { $gt: 180 } })
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ rated: { $ne: "UNRATED" } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ rated: { $in: ["G", "PG"] } }).pretty()
{% endhighlight %}