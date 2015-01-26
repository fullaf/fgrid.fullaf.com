---
layout: docs
title: Box Model
permalink: /docs/box-model/
order: 100
---

## Border-Box

We use the border-box box model when we build sites, so fGrid has this set on all elements (See `core/_border_box.sass`).

The border-box model (see [this CSS Tricks article](http://css-tricks.com/box-sizing/)) changes the default behaviour of padding applied to elements.

In a nutshell in the default **context-box** model the rendered width of an element is the sum of the defined width, the width of the elements padding and the width of the elements borders. This applies in the same way to the height. This means if you want to increase the padding on an element you have to recalculate the padding and borders.

If this sounds silly, lets propose the **border-box** model. The defined width will be the rendered width. Padding and borders will compress the content inside this defined width.

Consider the following:

```sass
width: 200px
border: 1px solid
padding: 20px
```

With the context-box model the width of an element with the above styles will have a rendered width of `200 + 1*2 + 20*2 = 242px`. With border-box the width will be **200px**, the padding and border will happen inside this width. Much better!

**border-box** is [universally supported](http://caniuse.com/#search=border-box) on modern browsers.
