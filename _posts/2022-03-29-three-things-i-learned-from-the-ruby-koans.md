---
layout: post
title: Three things I learned from The Ruby Koans
---

Here are (at least) three things I learned from [The Ruby Koans](http://rubykoans.com/):

#### Some Random Stuff
- I learn to include code blocks today:

```python
class Person
  attr_accessor :first_name
  attr_accessor :last_name

  def full_name
    return self.first_name + " " + self.last_name
  end
end
```

- If the action name in route matches the view template name, then we dont need to specify the render path

- RESTFUL API creates a uniform way to name paths in your application

Based on RESTUL API, we can automatically create all golden 7 routes (create, read, update and delete) using the following syntax:
```ruby
resources(:directors)
```

- For asserts, any non-False and non-nil objects in Ruby count as TRUE 
