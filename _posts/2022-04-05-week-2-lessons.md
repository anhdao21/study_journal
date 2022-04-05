---
layout: post
title: Week 2 - Going advanced
---

1. Ruby automatically fix the cross-site request forgery CSRF. Include the following authentication code in each form that has a post method.

```erb
<form action="/movies" method="post">
  <input
    type="hidden"
    name="authenticity_token"
    value="<%= form_authenticity_token %>">
```

2. Cleaner way to filter and select the first record that matches:

```erb
matching_movies = Movie.where({ :id => the_id })
@the_movie = matching_movies.at(0)
```

is shortened to
```erb
@the_movie = Movie.find_by({ :id => the_id })
```

Note that `where` returns a relation, whereas `find_by` return a record or `nil`. However, the exception here is confusing and not helpful.

The best solution is using `find` (only looks in ID column, and ID is unique so only a single record is returned), which automatically raises 404 and a more helpful "There's no Movie with ID=<##>" error message.

```erb
@the_movie = Movie.find(params.fetch(:id))
```

Note: instead of using [0] the params will throw an exception right away so you don't have to deal with `nil` later

3. To adhere to RESTFUL naming convention, then we need to use verbs that match CRUD that HTML doesn't support. Here instead of using GET, Ruby creates fake methods PATCH and DELETE (from HTTP guideline) to direct HTML to update and delete records.

4. Next week, we'll learn a more concise way of writing links and forms will use the helper methods `link_to` and `form_with`
