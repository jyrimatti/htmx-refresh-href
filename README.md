# htmx-refresh-href
Htmx extension to refresh hrefs of anchors with the actual URL used for the Ajax call

The `refresh-href` extension refreshes href attributes of anchor elements having hx-get attribute, with the actual URL used to make the Ajax call.

This enables the browser to show the actual target when hovering the link, and makes "Open link in new tab" work, assuming of course the response is a full document.

Refresh is made by default on "init" (initialization) and "mouseover" events. Events can be changed by listing them in refresh-href -attribute, separated by comma.

https://github.com/bigskysoftware/htmx/pull/1261

### Install

```html
<script src="https://unpkg.com/htmx-refresh-href/dist/refresh-href.js"></script>
```

### Usage

```html
<body hx-ext="refresh-href">
  <!-- adds href="/test?param=val" on initialization, and refreshes it onmouseover -->
  <input name="param" value="val" />
  <a hx-get="/test" hx-include="[name='param']">link</div>
</body>
```
