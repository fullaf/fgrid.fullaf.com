---
layout: docs
title: Home
permalink: /docs/
order: 10
---

## fGrid Documentation

fGrid is a responsive and customisable grid system for Sass styled websites. It's built to be flexible and small and is suitable for a wide range of projects.

This site aims to be a comprehensive resource on the features and design of the micro-framework.

### Introduction

The two main components of fGrid are the grid system and the responsive mixins. Bits we find useful when building fGrid powered sites are likely to be included as well.

fGrid can be customised by editing the `_settings.sass` file.

### Dependencies

Some of the fancy bits of fGrid need [Bourbon](http://bourbon.io/), and frankly if fGrid is being used Bourbon will be useful too.

### Usage

The easiest way to get fGrid is with [Bower](http://bower.io/), simply run `bower install fgrid` in your project directory and add `@import "bower_components/fgrid/fgrid"` to where required.

Importing Bourbon is up to you. If you've installed it using Bower putting this line above the fGrid import line will do the trick: `@import "bower_components/bourbon/dist/bourbon"`

So now your main Sass file looks like:

{% highlight sass %}
@import "bower_components/bourbon/dist/bourbon"
@import "bower_components/fgrid/fgrid"

# All your styling below here
{% endhighlight %}

### Testing

fGrid testing comprises installing dependencies and compiling the project to ensure building is successful. We use Travis for this.

To run the tests yourself do `ruby tests.rb`.

### Documentation

Examples given will be in SASS, SCSS may be useful to add later. Converting to SCSS essentially means adding curly braces to selectors and semicolons at the end of lines.
