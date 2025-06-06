---
title: xChannelSelector
slug: Web/SVG/Reference/Attribute/xChannelSelector
page-type: svg-attribute
browser-compat: svg.elements.feDisplacementMap.xChannelSelector
sidebar: svgref
---

The **`xChannelSelector`** attribute indicates which color channel from {{SVGAttr("in2")}} to use to displace the pixels in {{SVGAttr("in")}} along the x-axis.

## Elements

You can use this attribute with the {{SVGElement("feDisplacementMap")}} SVG element.

## Usage notes

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Value</th>
      <td><code>R</code> | <code>G</code> | <code>B</code> | <code>A</code></td>
    </tr>
    <tr>
      <th scope="row">Default value</th>
      <td><code>A</code></td>
    </tr>
    <tr>
      <th scope="row">Animatable</th>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

- `R`
  - : This keyword specifies that the red color channel of the input image defined in {{SVGAttr("in2")}} will be used to displace the pixels of the input image defined in {{SVGAttr("in")}} along the x-axis.
- `G`
  - : This keyword specifies that the green color channel of the input image defined in {{SVGAttr("in2")}} will be used to displace the pixels of the input image defined in {{SVGAttr("in")}} along the x-axis.
- `B`
  - : This keyword specifies that the blue color channel of the input image defined in {{SVGAttr("in2")}} will be used to displace the pixels of the input image defined in {{SVGAttr("in")}} along the x-axis.
- `A`
  - : This keyword specifies that the alpha channel of the input image defined in {{SVGAttr("in2")}} will be used to displace the pixels of the input image defined in {{SVGAttr("in")}} along the x-axis.

## Examples

```css hidden
html,
body,
svg {
  height: 100%;
}
```

```html
<svg viewBox="0 0 440 160" xmlns="http://www.w3.org/2000/svg">
  <filter id="displacementFilter">
    <feImage
      href="mdn.svg"
      x="0"
      y="0"
      width="100%"
      height="100%"
      result="abc" />
    <feDisplacementMap
      in2="abc"
      in="SourceGraphic"
      scale="30"
      xChannelSelector="R" />
  </filter>
  <filter id="displacementFilter2">
    <feImage
      href="mdn.svg"
      x="0"
      y="0"
      width="100%"
      height="100%"
      result="abc" />
    <feDisplacementMap
      in2="abc"
      in="SourceGraphic"
      scale="30"
      xChannelSelector="B" />
  </filter>

  <text x="10" y="60" font-size="50" filter="url(#displacementFilter)">
    Some displaced text
  </text>
  <text x="10" y="120" font-size="50" filter="url(#displacementFilter2)">
    Some displaced text
  </text>
</svg>
```

{{EmbedLiveSample("Examples", "480", "200")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
