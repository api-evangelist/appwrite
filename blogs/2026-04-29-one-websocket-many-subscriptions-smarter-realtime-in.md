---
title: "One WebSocket, many subscriptions: smarter Realtime in Appwrite"
url: "https://appwrite.io/blog/post/announcing-message-based-realtime-sdk"
date: "Wed, 29 Apr 2026 00:00:00 GMT"
author: ""
feed_url: "https://appwrite.io/blog/rss.xml"
---
Appwrite Realtime now keeps one persistent WebSocket and drives subscriptions with messages instead of cramming state into the connection URL. Client SDKs expose unsubscribe(), update(), and disconnect() for clearer lifecycle control.
