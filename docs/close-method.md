---
layout: page
title: "Close Method"
section: sdk
permalink: /sdk/python/close-method/
description: Error responses can range from access issues to processing. This table provides a listing of common errors and potential causes.
---

Once the events are published/consumed, you have to close the websocket connection by calling close method.

{% highlight python %}
ens_client.close()
{% endhighlight %}

After the close is called:

* The ENS client will not accept any new events. If you try to send, it throws ConnectionClosedException. 
* The client might evict undelivered events/not acknowledged events as PublisherException or ConsumerException. Ensure to handle it.