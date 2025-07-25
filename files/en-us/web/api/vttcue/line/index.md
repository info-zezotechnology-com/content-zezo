---
title: "VTTCue: line property"
short-title: line
slug: Web/API/VTTCue/line
page-type: web-api-instance-property
browser-compat: api.VTTCue.line
---

{{APIRef("WebVTT")}}

The **`line`** property of the {{domxref("VTTCue")}} interface represents the cue line of this WebVTT cue.

## Value

A number, or `"auto"` representing the cue line of this WebVTT cue.

## Examples

In the following example a new {{domxref("VTTCue")}} is created, then the value of `line` is set to `1`. The value is then printed to the console.

```js
let video = document.querySelector("video");
let track = video.addTextTrack("captions", "Captions", "en");
track.mode = "showing";

let cue = new VTTCue(0, 0.9, "Hildy!");
cue.line = "1";
console.log(cue.line);

track.addCue(cue);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
