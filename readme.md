# Stencil + Storybook

* Stencil component project from cli
* Add storybook/react per cli
* wire together, sharing www directory
* Force es5 build to ensure compability with IE11.
  * Note that when Stencil component is changed, you need to manually refrest Storybook

## Bug - Stencil components do not hydrate in IE11 when served in Storybook
* To test, run `npm start`.  Component storybook page works in Chrome, but not IE11 on port 6006.
* Note that Stencil start page on port 3333 works in both.

## Version testing:
- Stencil v1.1.2 - Everything works!
- Stencil v1.1.3 - The components render, but the theme with css custom properties fails to load  ...so it looks unstyled… even in Chrome.
```
ENOENT: no such file or directory, stat '/Users/12345/git/hp-web-component-library/node_modules/@storybook/core/dist/public/hp-themes/index.js'),

Refused to apply style from 'http://localhost:6006/hp-themes/lib/hp-themes-default.css' because its MIME type ('text/html') is not a supported stylesheet MIME type, and strict MIME checking is enabled.
```

- Stencil v1.1.4 - The theme bug is gone.  However, this is where the components stop rendering in ie 11.
