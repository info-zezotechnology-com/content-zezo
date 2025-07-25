---
title: DNT header
short-title: DNT
slug: Web/HTTP/Reference/Headers/DNT
page-type: http-header
status:
  - deprecated
  - non-standard
browser-compat: http.headers.DNT
sidebar: http
---

{{Deprecated_header}}{{non-standard_header}}

> [!NOTE]
> The DNT (Do Not Track) specification has been discontinued. See {{domxref("Navigator.doNotTrack")}} for more information.

The HTTP **`DNT`** (Do Not Track) {{Glossary("request header")}} indicates the user's tracking preference.
It lets users indicate whether they would prefer privacy rather than personalized content.

DNT is deprecated in favor of [Global Privacy Control](https://globalprivacycontrol.org/), which is communicated to servers using the {{HTTPHeader("Sec-GPC")}} header, and accessible to clients from {{domxref("navigator.globalPrivacyControl")}}.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Header type</th>
      <td>{{Glossary("Request header")}}</td>
    </tr>
    <tr>
      <th scope="row">{{Glossary("Forbidden request header")}}</th>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

## Syntax

```http
DNT: 0
DNT: 1
DNT: null
```

## Directives

- `0`
  - : The user prefers to allow tracking on the target site.
- `1`
  - : The user prefers not to be tracked on the target site.
- `null`
  - : The user has not specified a preference about tracking.

## Examples

### Reading Do Not Track status from JavaScript

The user's DNT preference can also be read from JavaScript using the
{{domxref("Navigator.doNotTrack")}} property:

```js
navigator.doNotTrack; // "0", "1" or null
```

## Specifications

Part of the discontinued [Tracking Preference Expression (DNT)](https://w3c.github.io/dnt/drafts/tracking-dnt.html#dnt-header-field) specification.

## Browser compatibility

{{Compat}}

## See also

- {{domxref("Navigator.doNotTrack")}}
- {{HTTPHeader("Tk")}} header
- [Do Not Track on Wikipedia](https://en.wikipedia.org/wiki/Do_Not_Track)
- [What Does the "Track" in "Do Not Track" Mean? – EFF](https://www.eff.org/deeplinks/2011/02/what-does-track-do-not-track-mean)
- [DNT on Electronic Frontier Foundation](https://www.eff.org/issues/do-not-track)
- DNT browser settings help:
  - [Firefox](https://support.mozilla.org/en-US/kb/how-do-i-turn-do-not-track-feature)
  - [Chrome](https://support.google.com/chrome/answer/2790761)
- [GPC - Global Privacy Control](https://globalprivacycontrol.org/)
  - [Enabling GPC in Firefox](https://support.mozilla.org/en-US/kb/global-privacy-control?as=u&utm_source=inproduct)
