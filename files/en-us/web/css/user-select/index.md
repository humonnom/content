---
title: user-select
slug: Web/CSS/user-select
page-type: css-property
browser-compat: css.properties.user-select
sidebar: cssref
---

The **`user-select`** [CSS](/en-US/docs/Web/CSS) property controls whether the user can select text. This doesn't have any effect on content loaded as part of a browser's user interface (its {{Glossary("Chrome", "chrome")}}), except in textboxes.

{{InteractiveExample("CSS Demo: user-select")}}

```css interactive-example-choice
user-select: none;
```

```css interactive-example-choice
user-select: text;
```

```css interactive-example-choice
user-select: all;
```

```html interactive-example
<section id="default-example">
  <p id="example-element">Try to select this text</p>
</section>
```

```css interactive-example
#example-element {
  font-size: 1.5rem;
}
```

## Syntax

```css
/* Keyword values */
user-select: none;
user-select: auto;
user-select: text;
user-select: all;

/* Global values */
user-select: inherit;
user-select: initial;
user-select: revert;
user-select: revert-layer;
user-select: unset;
```

> [!NOTE]
> `user-select` is not an inherited property, though the initial `auto` value makes it behave like it is inherited most of the time. WebKit/Chromium-based browsers _do_ implement the property as inherited, which violates the behavior described in the spec, and this will bring some issues. Until now, Chromium has chosen to [fix the issues](https://chromium.googlesource.com/chromium/src/+/b01af0b296ecb855aac95c4ed335d188e6eac2de) to make the final behavior meet the specifications.

### Values

- `none`
  - : The text of the element and its sub-elements is not selectable. Note that the {{domxref("Selection")}} object can contain these elements.
- `auto`
  - : The used value of `auto` is determined as follows:
    - On the `::before` and `::after` pseudo elements, the used value is `none`
    - If the used value of `user-select` on the parent of this element is `none`, the used value is `none`
    - Otherwise, if the used value of `user-select` on the parent of this element is `all`, the used value is `all`
    - Otherwise, the used value is `text`

- `text`
  - : The text can be selected by the user.
- `all`
  - : The content of the element shall be selected atomically: If a selection would contain part of the element, then the selection must contain the entire element including all its descendants. If a double-click or context-click occurred in sub-elements, the highest ancestor with this value will be selected.

> [!NOTE]
> The [CSS basic user interface](/en-US/docs/Web/CSS/CSS_basic_user_interface) module defines a `contain` value for the `user-select` property to enable selection to start within the element to be contained by the bounds of that element, however, this is not supported in any browsers.

## Formal definition

{{CSSInfo}}

## Formal syntax

{{csssyntax}}

## Examples

### HTML

```html
<p>You should be able to select this text.</p>
<p class="unselectable">Hey, you can't select this text!</p>
<p class="all">Clicking once will select all of this text.</p>
```

### CSS

```css
.unselectable {
  -webkit-user-select: none; /* Safari */
  user-select: none;
}

.all {
  -webkit-user-select: all;
  user-select: all;
}
```

### Result

{{EmbedLiveSample("Examples")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{Cssxref("::selection")}} pseudo-element
- The JavaScript {{domxref("Selection")}} object
