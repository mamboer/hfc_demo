# Setup

```
npm i
```

or,

```
yarn
```

## hexo-filter-cleanup configurations

```yml
# filter_cleanup
hfc_useref:
  enable: true
  concat: true

hfc_html:
  enable: true

hfc_css:
  enable: true
  exclude: 
    - '*.min.css'

hfc_js:
  enable: true
  mangle: true
  exclude: 
    - '*.min.js'

hfc_img:
  enable: true
  interlaced: false
  multipass: false
  optimizationLevel: 2
  pngquant: false
  progressive: false

hfc_favicons:
  enable: true
  src: img/my_custom_favicon.png
  target: img/
  html: true
```

### hfc_js and hfc_css

We should exclude all the minified files in case `hfc` do the minifying jobs again.

### hfc_favicons

We specified a custom favicon image `my_custom_favicon.png` to generate the favicon staffs like `favicon.ico` automatically here.

If your `favicon.ico` was already prepared manually, you should disable this feature by setting `enable` to `false`.