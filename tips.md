---
layout: page
title: Tips and tricks
permalink: /tips
---

### Java: atomic and thread safe updates for in memory data structure

```
import java.util.concurrent.atomic.AtomicReference

AtomicReference<List<Object>> objectsRef = new AtomicReference(new ArrayList<>);
objectsRef.getAndUpdate(objects -> {
  return ImmutableList.of(objects.get(0), 2, 3, 4);
});
```
