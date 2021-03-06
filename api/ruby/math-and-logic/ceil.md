---
layout: api-command
language: Ruby
permalink: api/ruby/ceil/
command: ceil
related_commands:
    floor: floor/
    round: round/
---
# Command syntax #

{% apibody %}
r.ceil(number) &rarr; number
number.ceil() &rarr; number
{% endapibody %}

# Description #

Rounds the given value up, returning the smallest integer value greater than or equal to the given value (the value's ceiling).

__Example:__ Return the ceiling of 12.345.

```rb
> r.ceil(12.345).run(conn)

13.0
```

The `ceil` command can also be chained after an expression.

__Example:__ Return the ceiling of -12.345.

```rb
> r.expr(-12.345).ceil().run(conn)

-12.0
```

__Example:__ Return Iron Man's weight, rounded up with `ceil`.

```rb
r.table('superheroes').get('ironman')['weight'].ceil().run(conn)
```
