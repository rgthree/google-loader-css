#  Google/Gmail's 3D Loader

| ![Example](example.gif) | Google's 3D "Flipping-Circle" Loader as used in Gmail and other Google Products using pure CSS. |
|:---:|:---|



## How To Use

1. Download the [google-loader-current.css](src/google-loader-current.css) (or use the chart below for your tweaked version) and host it on your webserver.
2. Link the css file in the `<head>` of your webpage, and use

  ```html
<link rel="stylesheet" type="text/css" media="all" href="google-loader-current.css">
  ```

3. Add this html snippet where you would like to use your loader _(see different snippet for "bleeding" version below)_: 

  ```html
<span class="gloader"><span></span><span></span></span>
  ```

4. The `gloader` inherits from the font-size of your container using `em` units, and is of `display-inline-block` variety, so it will obey text-align. For instance, if you wanted your `gloader` to be 24px in diameter and center aligned, you could put it in a `.container` element styled as:

  ```css
.container { font-size:24px; text-align:center; }
  ```


## Versions & Browser Support

| Support  | Link                                                         | Chrome | FireFox | IE | Safari | Opera | Example |
|:---------|:-------------------------------------------------------------|:------:|:-------:|:---:|:------:|:------:|:-------:|
| Bleeding | [google-loader-bleeding.css](src/google-loader-bleeding.css) | **26**   |   16    | 10 |  **6.0**   |  12.1 | [jsFiddle](http://jsfiddle.net/gh/get/library/pure/rgthree/google-loader-css/tree/master/jsfiddle-bleeding) |
| Current  | [google-loader-current.css](src/google-loader-current.css)   |    4   |   16    | 10 |  4.0   |  12.1 | [jsFiddle](http://jsfiddle.net/gh/get/library/pure/rgthree/google-loader-css/tree/master/jsfiddle-current) |
| Old      | [google-loader-old.css](src/google-loader-old.css)           |    4   |    **5**    | 10 |  4.0   |  **12.0** | [jsFiddle](http://jsfiddle.net/gh/get/library/pure/rgthree/google-loader-css/tree/master/jsfiddle-old) |

_Compatibility derived from [caniuse.com](http://caniuse.com/#feat=css-animation). Not all mentioned browsers have been thoroughly tested._


### Bleeding Browser Version

The "bleeding" version of the google loader uses the smallest markup possible: _a single element_. It uses pseudo-elements to create the animations. Unfortunately, up until the last few Chrome and Safari releases [pseudo-elements were not supported](http://caniuse.com/#feat=css-gencontent). If you only need to support webkit browsers' Chrome 26+ and Safari 6.0+, you should [grab this version](src/google-loader-bleeding.css).

```html
<head>
  <link rel="stylesheet" type="text/css" media="all" href="google-loader-bleeding.css">
</head>
<body>
  <span class="gloader"></span>
</body>
```

### Current Browser Version
The current version supports a wider range of browsers, but requires two elements be added as children to the. This is the widest support while still saving on CSS filesize. If you want to support current versions of browsers you should [grab this version](src/google-loader-current.css).

```html
<head>
  <link rel="stylesheet" type="text/css" media="all" href="google-loader-current.css">
</head>
<body>
  <span class="gloader"><span></span><span></span></span>
</body>
```

### Old/Widest Browser Version
If you want to support Firefox 5.0-15.0 and Opera 12.0, you will need a bit more CSS, but your markup will remain the same. Note, FireFox 16 was released on October 9th, 2012 and Opera Jun 14, 2012 so if you require support for browsers older than these dates you should [grab this version](src/google-loader-old.css).

```html
<head>
  <link rel="stylesheet" type="text/css" media="all" href="google-loader-old.css">
</head>
<body>
  <span class="gloader"><span></span><span></span></span>
</body>
```

