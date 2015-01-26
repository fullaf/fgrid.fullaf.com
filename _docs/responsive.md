---
layout: docs
title: Responsive Mixins
permalink: /docs/responsive/
order: 40
---

## Responsive Mixins

fGrid defines six responsive breakpoints:

- `mob-port` Mobile portrait (320px)
- `mob-land` Mobile landscape (480px)
- `tab-port` Tablet portrait (768px)
- `tab-land` Tablet landscape (1024px)
- `med-desk` Medium desktop (1200px)
- `widescreen` Widescreen desktop (1490px)

The mobile and tablet breakpoints by default have no restriction on device they will activate on small desktop as for the enviroment this will likely give the best experience.

Three mixins are available for using these breakpoints:

- `@include respond-up(<BREAKPOINT>)` Will match this size and above
- `@include respond-down(<BREAKPOINT>)` Will match this size and below
- `@include respond-to(<BREAKPOINT>)` Will match this size only

If you are following a mobile first methodology you'll probably only want to use `respond-down` when adding mobile only styling.

#### Example
The following will give a multi-line nav on mobile and single-line on tab-port and above. When mob-land only we increase the font-size.

{% highlight sass %}
header
  li
    font-size: 16px
    @include respond-to(mob-land)
      font-size: 20px
    @include respond-up(tab-port)
      display: inline-block
{% endhighlight %}

### Retina Detection

Devices that have a minimum pixel ratio of 2, i.e. mobile high res retina screens can be selected with `@include respond-to(retina)`. This selector only works with respond-to and not -up and -down.

#### Example
The following element is given a 500px wide background, when on a retina device a 1000px background is given and scaled to half size to give a high-res background.

{% highlight sass %}
element
  background: url('500px-wide.png')
  @include respond-to(retina)
    background: url('1000px-wide.png')
    background-size: 500px auto
{% endhighlight %}
