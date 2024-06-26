---
title: "VideoFrame: codedHeight property"
short-title: codedHeight
slug: Web/API/VideoFrame/codedHeight
page-type: web-api-instance-property
browser-compat: api.VideoFrame.codedHeight
---

{{APIRef("Web Codecs API")}}{{AvailableInWorkers("window_and_dedicated")}}

The **`codedHeight`** property of the {{domxref("VideoFrame")}} interface returns the height of the VideoFrame in pixels, potentially including non-visible padding, and prior to considering potential ratio adjustments.

## Value

An integer.

## Examples

The following example prints the `codedHeight` to the console.

```js
console.log(VideoFrame.codedHeight);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
