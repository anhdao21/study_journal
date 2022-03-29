---
layout: post
title: Three things I learned from The Ruby Koans
---

Here are (at least) three things I learned from [The Ruby Koans](http://rubykoans.com/):

#### Some Random Stuff
- I learn to include code blocks today:

```ruby
class Person
  attr_accessor :first_name
  attr_accessor :last_name

  def full_name
    return self.first_name + " " + self.last_name
  end
end
```
