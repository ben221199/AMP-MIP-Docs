# AMP/MIP Documentation

Documentation for AMP (Google) and MIP (Baidu).

## Non-AMP/MIP Page Requirements

### Link to AMP/MIP page

This link tells search engines where to find the AMP/MIP version of the webpage.

#### AMP

```html
<link href="https://example.com/some-webpage-with-amp" rel="amphtml">
```

#### MIP

```html
<link href="https://example.com/some-webpage-with-mip" rel="miphtml">
```

## AMP/MIP Page Requirements

### Document Type

The definition of the document type, to indicate which version of HTML the page is using. It should be HTML5, because older HTML doesn't support custom attributes.

#### AMP

```html
<!DOCTYPE html>
```

#### MIP

```html
<!DOCTYPE html>
```

### HTML Tag

The first tag in the document, having a specific attribute to indicate that the page is an AMP or MIP page.

#### AMP

```html
<html amp>
```

OR

```html
<html ⚡>
```

#### MIP

```html
<html mip>
```

### Head

This element is mandiatory in both AMP and MIP.

#### AMP

```html
<head>
```

#### MIP

```html
<head>
```

### Charset

The charset metadata should be present and should be UTF-8.

#### AMP

```html
<meta charset="utf-8">
```

#### MIP

```html
<meta charset="utf-8">
```

### Canonical

There should be a canonical link. This should point to the non-AMP or non-MIP page, or in case AMP/MIP is the only page, to itself.

#### AMP

```html
<link href="https://example.com/some-webpage-without-amp" rel="canonical">
```

#### MIP

```html
<link href="https://example.com/some-webpage-without-mip" rel="canonical">
```

### Viewport

There should be a viewport set. The `width` value is mandatory and should be `device-width`. Recommended it to add `minimum-scale=1` and `initial-scale=1` too.

#### AMP

```html
<meta content="width=device-width" name="viewport">
```

#### MIP

```html
<meta content="width=device-width" name="viewport">
```

### Engine Script

The engine script should be present and should be asyncronically loaded.

#### AMP

```html
<script async src="https://cdn.ampproject.org/v0.js"></script>
```

#### MIP

```html
<script async src="https://c.mipcdn.com/static/v1/mip.js"></script>
```

OR

```html
<script async src="https://c.mipcdn.com/static/v2/mip.js"></script>
```

### Style Boilerplate

AMP/MIP pages use boilerplate code to disable some CSS rendering until the right moment.

#### AMP

```html
<style amp-boilerplate>body{-webkit-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-moz-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-ms-animation:-amp-start 8s steps(1,end) 0s 1 normal both;animation:-amp-start 8s steps(1,end) 0s 1 normal both}@-webkit-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-moz-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-ms-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-o-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}</style>
```

AND

```html
<noscript><style amp-boilerplate>body{-webkit-animation:none;-moz-animation:none;-ms-animation:none;animation:none}</style></noscript>
```

#### MIP

```html
<link href="https://c.mipcdn.com/static/v1/mip.css" rel="stylesheet" type="text/css">
```

OR

```html
<link href="https://c.mipcdn.com/static/v2/mip.css" rel="stylesheet" type="text/css">
```

### Body

This element is mandiatory in both AMP and MIP.

#### AMP

```html
<body>
```

#### MIP

```html
<body>
```

## Additionals

### Loading custom elements

For loading custom elements that aren't loaded by default.

#### AMP

```html
<script async custom-element="amp-gist" src="https://cdn.ampproject.org/v0/amp-gist-0.1.js"></script>
```

But `src` is not mandatory:

```html
<script async custom-element="amp-gist"></script>
```

#### MIP

```html
<script src="https://c.mipcdn.com/static/v2/mip-mustache/mip-accordion.js"></script>
```

### Loading custom templates

For loading custom templates that aren't loaded by default.

#### AMP

```html
<script async custom-template="amp-mustache" src="https://cdn.ampproject.org/v0/amp-mustache-0.2.js"></script>
```

But `src` is not mandatory:

```html
<script async custom-template="amp-mustache"></script>
```

#### MIP

```html
<script src="https://c.mipcdn.com/static/v2/mip-mustache/mip-mustache.js"></script>
```
