---
layout: docs
title: Grid
permalink: /docs/grid/
order: 30
---

## Grid System

By default fGrid implements a 12 column grid system. You can use the class `grid-n` where n is the number of columns. Each row is cleared and given padding by using `grid-row`, finally the grid system is sized on the page by being inside `grid-wrap`.

#### Example

{% highlight html %}
<div class="grid-wrap">
  <div class="grid-row demo-grid">
    <div class="grid-3">
      <div class="demo-inner">
        .grid-3
      </div>
    </div>
    <div class="grid-3">
      <div class="demo-inner">
        .grid-3
      </div>
    </div>
    <div class="grid-6">
      <div class="demo-inner">
        .grid-6
      </div>
    </div>
  </div>
</div>
{% endhighlight %}

### Grid Mixins

While using the built-in classes will work, it's not semantic as it dirties your code with meaningless classes. Instead it is recommended to use the grid mixins.

{% highlight sass %}
sass
header, div.wrapper, footer
    @include grid-wrap

div.row
    @include grid-row

article
    # Emulate .grid-8
    @include grid-x-col(8)

aside
    # Emulate .grid-4
    @include grid-x-col(4)

div.weird-grid
    # We also can do a grid element using an arbritary percentage
    @include grid-x-percent(43.7%)
{% endhighlight %}
