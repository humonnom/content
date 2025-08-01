---
title: "<marquee>: The Marquee element"
slug: Web/HTML/Reference/Elements/marquee
page-type: html-element
status:
  - deprecated
browser-compat: html.elements.marquee
sidebar: htmlsidebar
---

{{Deprecated_Header}}

The **`<marquee>`** [HTML](/en-US/docs/Web/HTML) element is used to insert a scrolling area of text. You can control what happens when the text reaches the edges of its content area using its attributes.

The HTML `<marquee>` element is deprecated and its use is strongly discouraged. If you must create the effect of scrolling text or continuous elements, consider using [CSS animations](/en-US/docs/Web/CSS/CSS_animations) with [CSS transforms](/en-US/docs/Web/CSS/CSS_transforms/Using_CSS_transforms) instead of `<marquee>` elements to smoothly animate content. Additionally, include the [`prefers-reduced-motion`](/en-US/docs/Web/CSS/@media/prefers-reduced-motion) CSS {{cssxref("@media")}} query to stop the animation based on user preference, thereby improving user experience and accessibility.

## Attributes

- `behavior` {{Deprecated_Inline}}
  - : Sets how the text is scrolled within the marquee. Possible values are `scroll`, `slide` and `alternate`. If no value is specified, the default value is `scroll`.
- `bgcolor` {{Deprecated_Inline}}
  - : Sets the background color through color name or hexadecimal value.
- `direction` {{Deprecated_Inline}}
  - : Sets the direction of the scrolling within the marquee. Possible values are `left`, `right`, `up` and `down`. If no value is specified, the default value is `left`.
- `height` {{Deprecated_Inline}}
  - : Sets the height in pixels or percentage value.
- `hspace` {{Deprecated_Inline}}
  - : Sets the horizontal margin
- `loop` {{Deprecated_Inline}}
  - : Sets the number of times the marquee will scroll. If no value is specified, the default value is −1, which means the marquee will scroll continuously.
- `scrollamount` {{Deprecated_Inline}}
  - : Sets the amount of scrolling at each interval in pixels. The default value is 6.
- `scrolldelay` {{Deprecated_Inline}}
  - : Sets the interval between each scroll movement in milliseconds. The default value is 85. Note that any value smaller than 60 is ignored and the value 60 is used instead unless `truespeed` is specified.
- `truespeed` {{Deprecated_Inline}}
  - : By default, `scrolldelay` values lower than 60 are ignored. If `truespeed` is present, those values are not ignored.
- `vspace` {{Deprecated_Inline}}
  - : Sets the vertical margin in pixels or percentage value.
- `width` {{Deprecated_Inline}}
  - : Sets the width in pixels or percentage value.

## Examples

```html
<marquee>This text will scroll from right to left</marquee>

<marquee direction="up">This text will scroll from bottom to top</marquee>

<marquee
  direction="down"
  width="250"
  height="200"
  behavior="alternate"
  class="outlined">
  <marquee behavior="alternate">This text will bounce</marquee>
</marquee>
```

```css
.outlined {
  border: solid;
}
```

### Result

{{EmbedLiveSample("Examples", 600, 450)}}

## Technical summary

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">DOM interface</th>
      <td>{{DOMxRef("HTMLMarqueeElement")}}</td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- CSS {{cssxref("transform")}} property
- CSS {{cssxref("translate")}} property
- [CSS transforms](/en-US/docs/Web/CSS/CSS_transforms) module
- [CSS animations](/en-US/docs/Web/CSS/CSS_animations) module
- {{DOMxRef("HTMLMarqueeElement")}}
