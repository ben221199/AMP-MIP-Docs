# AMP/MIP Documentation

Documentation for AMP (Google) and MIP (Baidu).

## Non-AMP/MIP Page Requirements

### Link to AMP/MIP page

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
<script async src="https://c.mipcdn.com/static/v2/mip.js"></script>
```

### Style

TODO

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

TODO