---
layout: page
title: "Acknowledgement"
section: sdk
permalink: /sdk/python/acknowledgement/
description: Error responses can range from access issues to processing. This table provides a listing of common errors and potential causes.
---

For every Event sent to the ENS server, an ACK message is sent back:

* Provide the max wait time(ack_wait_ms) to receive ACK from ENS server. After which,the client resends the event to the server.
* When maximum retry count (ack_retry) is reached, the client throws a       websocket exception and sends back the not acknowledged events. Ensure you are handling /resending  the  not acknowledged events.

Pleese do better!.