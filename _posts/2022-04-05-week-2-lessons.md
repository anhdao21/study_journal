---
layout: post
title: Week 2 - Going advanced
---

Ruby automatically fix the cross-site request forgery CSRF. Include the following authentication code in each form that has a post method.

```erb
<form action="/movies" method="post">
  <input
    type="hidden"
    name="authenticity_token"
    value="<%= form_authenticity_token %>">
```
