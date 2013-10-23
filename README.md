# Atomic components: flexible embed

Component for responsive, intrinsic ratio embeds.

Read more about [Atomic framework](https://github.com/atomic-css/atomic).

## Installation

* [__Bower:__](http://bower.io)
  `bower install --save atomic-css-components-flex-embed`
* [__Component(1):__](http://component.io)
  `component install atomic-css/components-flex-embed`
* __Download:__
  [zip](https://github.com/atomic-css/components-flex-embed/zipball/master),
  [tar.gz](https://github.com/atomic-css/components-flex-embed/tarball/master)
* __Git:__ `git clone https://github.com/atomic-css/components-flex-embed.git`

## Available classes

* `FlexEmbed` - core responsive embed component with no dimensions
* `FlexEmbed--16by9` - modifier class for 16:9 aspect ratio embed
* `FlexEmbed--4by3` - modifier class for 4:3 aspect ratio embed
* `FlexEmbed-item` - descendant class for the media that is being embedded
  (optional for `iframe`, `embed`, and `object` elements)

## Usage

Like many Atomic components, flex embed relies on a base component class that
is extended by any number of additional modifier classes.

```html
<div class="FlexEmbed FlexEmbed--16by9">
  [iframe|object|embed]
</div>

<div class="FlexEmbed FlexEmbed--4by3">
  <img class="FlexEmbed-item" src="…" alt="">
</div>
```

The flex embed component can be extended with additional aspect ratios if
your application makes use of multi-media embeds that require them.
For example, to create a 2.35:1 aspect ratio:

```css
/**
 * Modifier: 47:20 aspect ratio
 */

.FlexEmbed--47by20 {
    padding-bottom: 42.55%;
}
```

Alternatively, aspect ratios can be calculated programmatically and the
corresponding padding-bottom value applied using an inline style.

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 8+