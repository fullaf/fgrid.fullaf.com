---
layout: docs
title: Page Wrap
permalink: /docs/page/
order: 20
---

## Grid System

By default fGrid implements a 12 column grid system. You can use the class `grid-n` where n is the number of columns. Each row is cleared and given padding by using `grid-row`, finally the grid system is sized on the page by being inside `grid-wrap`.

#### Example

{% highlight html %}
<div class="grid-wrap">
  content
</div>
{% endhighlight %}

### Default Behaviour

The left and right padding of an fGrid page and the grid gutter sizes is specified as a setting for each breakpoint. See `_settings.sass`.

### Breakpoint Transitions

When a fGrid webpage is resized and a breakpoint is reached the changes will transist. Settings `$transition-enable` and `$transition-option` allow turning off this behaviour or modification of the transition.
