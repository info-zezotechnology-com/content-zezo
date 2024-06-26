---
title: "ImageData: width property"
short-title: width
slug: Web/API/ImageData/width
page-type: web-api-instance-property
browser-compat: api.ImageData.width
---

{{APIRef("Canvas API")}}{{AvailableInWorkers}}

The readonly **`ImageData.width`** property returns the number
of pixels per row in the {{domxref("ImageData")}} object.

## Value

A number.

## Examples

This example creates an `ImageData` object that is 200 pixels wide and 100
pixels tall. Thus, the `width` property is `200`.

```js
let imageData = new ImageData(200, 100);
console.log(imageData.width); // 200
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("ImageData.height")}}
- {{domxref("ImageData")}}
