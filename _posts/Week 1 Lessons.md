---
layout: page
title: Reacquaintance with Ruby
---

## Rails Base Template
1. If the action name in route matches the view template name, then we dont need to specify the render path
2. RESTFUL API creates a uniform way to name paths in your application
3. Based on RESTUL API, we can automatically create all golden 7 routes (create, read, update and delete) using the following syntax:
```ruby
resources(:directors)
```

## Ruby Koans
1. For asserts, any non-False and non-nil objects in Ruby count as TRUE
2. Shovel operator `<<` is a shorthand for `concat()` and also changes the values stored in the original object.
3. Double colon operator `::` lets you access a constant, module, or class defined inside another class or module.

```ruby
MR_COUNT = 0        # constant defined on main Object class
module Foo
  MR_COUNT = 0
  ::MR_COUNT = 1    # set global count to 1
  MR_COUNT = 2      # set local count to 2
end

puts MR_COUNT       # this is the global constant: 1
puts Foo::MR_COUNT  # this is the local constant: 2
```




