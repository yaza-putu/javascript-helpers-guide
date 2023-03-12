---
sidebar_position: 1
---

# Getting Started
Helpers Version V2.x

## Instalation
- Via CDN

CSS
```html
 <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yaza-putu/helpers@V2.0.4/libs/libs-core.min.css">
```
Js
```html
    <!-- remove jquery if jquery is installed -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/yaza-putu/helpers@V2.0.4/libs/libs-core.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/yaza-putu/helpers@V2.0.4/helpers.min.js"></script>
```

- Self Hosted
[Download](https://github.com/yaza-putu/helpers/archive/refs/tags/V2.0.4.zip)

# Configuration

Please paste bellow in main head (Laravel only) for auto send CSRF token
```javascript
<meta name="csrf-token" content="{{ csrf_token() }}">
```
