---
title: "<hgroup>: The Heading Group element"
slug: Web/HTML/Reference/Elements/hgroup
page-type: html-element
browser-compat: html.elements.hgroup
sidebar: htmlsidebar
---

The **`<hgroup>`** [HTML](/en-US/docs/Web/HTML) element represents a heading and related content. It groups a single [`<h1>–<h6>`](/en-US/docs/Web/HTML/Reference/Elements/Heading_Elements) element with one or more [`<p>`](/en-US/docs/Web/HTML/Reference/Elements/p).

{{InteractiveExample("HTML Demo: &lt;hgroup&gt;", "tabbed-standard")}}

```html interactive-example
<hgroup>
  <h1>Frankenstein</h1>
  <p>Or: The Modern Prometheus</p>
</hgroup>
<p>
  Victor Frankenstein, a Swiss scientist, has a great ambition: to create
  intelligent life. But when his creature first stirs, he realizes he has made a
  monster. A monster which, abandoned by his master and shunned by everyone who
  sees it, follows Dr Frankenstein to the very ends of the earth.
</p>
```

```css interactive-example
hgroup {
  text-align: right;
  padding-right: 16px;
  border-right: 10px solid #00c8d7;
}

hgroup h1 {
  margin-bottom: 0;
}

hgroup p {
  margin: 0;
  font-weight: bold;
}
```

## Attributes

This element only includes the [global attributes](/en-US/docs/Web/HTML/Reference/Global_attributes).

## Usage notes

The `<hgroup>` element allows the grouping of a heading with any secondary content, such as subheadings, an alternative title, or tagline. Each of these types of content represented as a `<p>` element within the `<hgroup>`.

The `<hgroup>` itself has no impact on the document outline of a web page. Rather, the single allowed heading within the `<hgroup>` contributes to the document outline.

## Examples

```html
<!doctype html>
<title>HTML Standard</title>
<body>
  <hgroup id="document-title">
    <h1>HTML: Living Standard</h1>
    <p>Last Updated 12 July 2022</p>
  </hgroup>
  <p>Some intro to the document.</p>
  <h2>Table of contents</h2>
  <ol id="toc">
    …
  </ol>
  <h2>First section</h2>
  <p>Some intro to the first section.</p>
</body>
```

### Result

{{EmbedLiveSample('Examples')}}

## Technical summary

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories"
          >Content categories</a
        >
      </th>
      <td>
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#flow_content"
          >Flow content</a
        >, heading content, palpable content.
      </td>
    </tr>
    <tr>
      <th scope="row">Permitted content</th>
      <td>
        Zero or more {{HTMLElement("p")}} elements, followed by one
        {{HTMLElement("Heading_Elements", "h1")}}, {{HTMLElement("Heading_Elements", "h2")}},
        {{HTMLElement("Heading_Elements", "h3")}}, {{HTMLElement("Heading_Elements", "h4")}},
        {{HTMLElement("Heading_Elements", "h5")}}, or {{HTMLElement("Heading_Elements", "h6")}} element,
        followed by zero or more {{HTMLElement("p")}} elements.
      </td>
    </tr>
    <tr>
      <th scope="row">Tag omission</th>
      <td>None, both the starting and ending tag are mandatory.</td>
    </tr>
    <tr>
      <th scope="row">Permitted parents</th>
      <td>
        Any element that accepts
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#flow_content"
          >flow content</a
        >.
      </td>
    </tr>
    <tr>
      <th scope="row">Implicit ARIA role</th>
      <td>
        <code
          ><a href="/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/group_role"
            >group</a
          ></code
        >
      </td>
    </tr>
    <tr>
      <th scope="row">Permitted ARIA roles</th>
      <td>Any</td>
    </tr>
    <tr>
      <th scope="row">DOM interface</th>
      <td>{{domxref("HTMLElement")}}</td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- Others section-related elements: {{HTMLElement("body")}}, {{HTMLElement("article")}}, {{HTMLElement("section")}}, {{HTMLElement("aside")}}, {{HTMLElement("Heading_Elements", "h1")}}, {{HTMLElement("Heading_Elements", "h2")}}, {{HTMLElement("Heading_Elements", "h3")}}, {{HTMLElement("Heading_Elements", "h4")}}, {{HTMLElement("Heading_Elements", "h5")}}, {{HTMLElement("Heading_Elements", "h6")}}, {{HTMLElement("nav")}}, {{HTMLElement("header")}}, {{HTMLElement("footer")}}, {{HTMLElement("address")}};
- [Sections and outlines of an HTML document](/en-US/docs/Web/HTML/Reference/Elements/Heading_Elements).
